---
title: Mapper le code prétraité au code source
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: b48c67584b3f3253ada99e32c5dabfdccb2fa4de
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581795"
---
<!-- Copyright Meggin Kearney and Paul Bakaus

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="dc72e-103">Mapper le code prétraité au code source</span><span class="sxs-lookup"><span data-stu-id="dc72e-103">Map Preprocessed Code to Source Code</span></span>   




<span data-ttu-id="dc72e-104">Gardez votre code côté client lisible et déboguable même après l’avoir combiné, minify défini ou compilé.</span><span class="sxs-lookup"><span data-stu-id="dc72e-104">Keep your client-side code readable and debuggable even after you combine, minify, or compile it.</span></span>  <span data-ttu-id="dc72e-105">Utilisez les mappages sources pour mapper votre code source à votre code compilé.</span><span class="sxs-lookup"><span data-stu-id="dc72e-105">Use source maps to map your source code to your compiled code.</span></span>  

### <span data-ttu-id="dc72e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="dc72e-106">Summary</span></span>  

*   <span data-ttu-id="dc72e-107">Utilisez les mappages sources pour mapper le code minified au code source.</span><span class="sxs-lookup"><span data-stu-id="dc72e-107">Use Source Maps to map minified code to source code.</span></span> <span data-ttu-id="dc72e-108">Vous pouvez ensuite lire et déboguer du code compilé dans la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="dc72e-108">You are then able to read and debug compiled code in the original source.</span></span>  
*   <span data-ttu-id="dc72e-109">Utilisez uniquement le préprocesseur capable de générer des cartes sources.</span><span class="sxs-lookup"><span data-stu-id="dc72e-109">Only use preprocessors capable of producing Source Maps.</span></span>  
*   <span data-ttu-id="dc72e-110">Vérifiez que votre serveur Web peut servir de cartes sources.</span><span class="sxs-lookup"><span data-stu-id="dc72e-110">Verify that your web server is able to serve Source Maps.</span></span>  

<!--todo: add link to preprocessors capable of producing Source Maps when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

## <span data-ttu-id="dc72e-111">Premiers pas avec les préprocesseurs</span><span class="sxs-lookup"><span data-stu-id="dc72e-111">Get started with preprocessors</span></span>  

<span data-ttu-id="dc72e-112">Cet article explique comment interagir avec des cartes sources JavaScript dans le volet sources de DevTools.</span><span class="sxs-lookup"><span data-stu-id="dc72e-112">This article explains how to interact with JavaScript Source Maps in the DevTools Sources Panel.</span></span>  <!--For a first overview of what preprocessors are, how each may help, and how Source Maps work; see Set Up CSS & JS Preprocessors.  -->  

<!--todo: add link to Set Up CSS & JS Preprocessors when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors#debugging-and-editing-preprocessed-content ""  -->  

## <span data-ttu-id="dc72e-113">Utiliser un préprocesseur pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc72e-113">Use a supported preprocessor</span></span>  

<span data-ttu-id="dc72e-114">Vous devez utiliser un Minifier capable de créer des mappages sources.</span><span class="sxs-lookup"><span data-stu-id="dc72e-114">You need to use a minifier that is capable of creating source maps.</span></span>  <!--For the most popular options, see the preprocessor support section.  -->  <span data-ttu-id="dc72e-115">Pour un affichage étendu, voir la page [mappages de sources: langues, outils et autres informations][GitHubWikiSourceMapsLanguagesTools] wiki.</span><span class="sxs-lookup"><span data-stu-id="dc72e-115">For an extended view, see the [Source maps: languages, tools and other info][GitHubWikiSourceMapsLanguagesTools] wiki page.</span></span>  

<!--todo: add link to see the preprocessor support section when section is available -->  
<!--[]: /web/tools/setup/setup-preprocessors?#supported_preprocessors ""  -->  

<span data-ttu-id="dc72e-116">Les types de préprocesseurs suivants sont couramment utilisés en association avec des cartes sources:</span><span class="sxs-lookup"><span data-stu-id="dc72e-116">The following types of preprocessors are commonly used in combination with Source Maps:</span></span>  

*   <span data-ttu-id="dc72e-117">Transpileurs \ ([Babel][BabelJS], [traceur][GitHubWikiGoogleTraceurCompiler]\)</span><span class="sxs-lookup"><span data-stu-id="dc72e-117">Transpilers \([Babel][BabelJS], [Traceur][GitHubWikiGoogleTraceurCompiler]\)</span></span>  
*   <span data-ttu-id="dc72e-118">Compileurs \ ([compilateur de fermeture][GitHubGoogleClosureCompiler], [dactylographié][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [DART][DartMain]\)</span><span class="sxs-lookup"><span data-stu-id="dc72e-118">Compilers \([Closure Compiler][GitHubGoogleClosureCompiler], [TypeScript][|::ref1::|Main], [CoffeeScript][|::ref2::|Main], [Dart][DartMain]\)</span></span>  
*   <span data-ttu-id="dc72e-119">Minifiers \ ([UglifyJS][GitHubMishooUglifyJS]\)</span><span class="sxs-lookup"><span data-stu-id="dc72e-119">Minifiers \([UglifyJS][GitHubMishooUglifyJS]\)</span></span>  

## <span data-ttu-id="dc72e-120">Cartes sources dans le panneau sources de DevTools</span><span class="sxs-lookup"><span data-stu-id="dc72e-120">Source Maps in DevTools Sources panel</span></span>  

<span data-ttu-id="dc72e-121">Les cartes sources des préprocesseurs entraînent le chargement de vos fichiers d’origine en plus de vos fichiers minified par DevTools.</span><span class="sxs-lookup"><span data-stu-id="dc72e-121">Source Maps from preprocessors cause DevTools to load your original files in addition to your minified ones.</span></span>  <span data-ttu-id="dc72e-122">Vous utilisez ensuite les originaux pour définir des points d’arrêt et parcourir le code.</span><span class="sxs-lookup"><span data-stu-id="dc72e-122">You then use the originals to set breakpoints and step through code.</span></span>  <span data-ttu-id="dc72e-123">Entre-temps, Microsoft Edge exécute actuellement votre code minified.</span><span class="sxs-lookup"><span data-stu-id="dc72e-123">Meanwhile, Microsoft Edge is actually running your minified code.</span></span> <span data-ttu-id="dc72e-124">Cela vous donne l’illusion d’exécuter un site de développement en production.</span><span class="sxs-lookup"><span data-stu-id="dc72e-124">This gives you the illusion of running a development site in production.</span></span>  

<span data-ttu-id="dc72e-125">Lorsque vous exécutez des mappages source dans DevTools, vous remarquerez que le JavaScript n’est pas compilé et que vous pouvez voir tous les fichiers JavaScript qu’il référence.</span><span class="sxs-lookup"><span data-stu-id="dc72e-125">When running Source Maps in DevTools, you should notice that the JavaScript is not compiled and you are able to see all the individual JavaScript files it references.</span></span>  <span data-ttu-id="dc72e-126">Cela utilise le mappage source, mais en coulisses, les scènes exécutent réellement le code compilé.</span><span class="sxs-lookup"><span data-stu-id="dc72e-126">This is using source mapping, but behind the scenes actually runs the compiled code.</span></span>  <span data-ttu-id="dc72e-127">Les erreurs, journaux et points d’arrêt mappent au code de développement pour le débogage Isard.</span><span class="sxs-lookup"><span data-stu-id="dc72e-127">Any errors, logs, and breakpoints map to the dev code for awesome debugging!</span></span>  <span data-ttu-id="dc72e-128">En effet, il vous donne l’illusion que vous exécutez un site de développement en production.</span><span class="sxs-lookup"><span data-stu-id="dc72e-128">So in effect it gives you the illusion that you are running a dev site in production.</span></span>  

### <span data-ttu-id="dc72e-129">Activer les cartes sources dans les paramètres</span><span class="sxs-lookup"><span data-stu-id="dc72e-129">Enable Source Maps in settings</span></span>  

<span data-ttu-id="dc72e-130">Les cartes sources sont activées par défaut</span><span class="sxs-lookup"><span data-stu-id="dc72e-130">Source Maps are enabled by default</span></span> <!--\(as of Microsoft Edge 39\)--><span data-ttu-id="dc72e-131">, mais si vous voulez vérifier ou activer un contrôle; Commencez par ouvrir DevTools, cliquez sur le bouton **personnaliser et contrôler devtools** `...` , puis sélectionnez **paramètres**.</span><span class="sxs-lookup"><span data-stu-id="dc72e-131">, but if you want to double-check or enable them; first open DevTools, click the **Customize and control DevTools** `...` button, and select **Settings**.</span></span>  <span data-ttu-id="dc72e-132">Dans le volet **Préférences** , sous **sources**, activez la case à cocher **activer les mappages de sources JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="dc72e-132">On the **Preferences** pane, under **Sources**, check **Enable JavaScript Source Maps**.</span></span>  <span data-ttu-id="dc72e-133">Vous pouvez également activer la case à cocher **activer les mappages de sources CSS**.</span><span class="sxs-lookup"><span data-stu-id="dc72e-133">You may also check **Enable CSS Source Maps**.</span></span>  

> ##### <span data-ttu-id="dc72e-134">Figure1</span><span class="sxs-lookup"><span data-stu-id="dc72e-134">Figure 1</span></span>  
> <span data-ttu-id="dc72e-135">Activer les mappages sources</span><span class="sxs-lookup"><span data-stu-id="dc72e-135">Enable Source Maps</span></span>  
> ![Activer les mappages sources][ImageSourceMaps]  

### <span data-ttu-id="dc72e-137">Débogage avec des mappages sources</span><span class="sxs-lookup"><span data-stu-id="dc72e-137">Debugging with Source Maps</span></span>  

<span data-ttu-id="dc72e-138">Lors du débogage de votre code et des mappages de sources activés, les cartes sources apparaissent à deux emplacements:</span><span class="sxs-lookup"><span data-stu-id="dc72e-138">When debugging your code and Source Maps enabled, Source Maps show in two places:</span></span>  

1.  <span data-ttu-id="dc72e-139">Dans la console \ (le lien vers la source doit être le fichier d’origine, et non le fichier généré \)</span><span class="sxs-lookup"><span data-stu-id="dc72e-139">In the console \(the link to source should be the original file, not the generated one\)</span></span>  
1.  <span data-ttu-id="dc72e-140">Lorsque vous parcourez le code \ (les liens dans la pile d’appels doivent ouvrir le fichier source d’origine \)</span><span class="sxs-lookup"><span data-stu-id="dc72e-140">When stepping through code \(the links in the call stack should open the original source file\)</span></span>  

<!--todo: add link to debugging your code when section is available -->  
<!--[DebugBreakpointsStepCode]: https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium/debug/breakpoints/step-code ""  -->  

## <span data-ttu-id="dc72e-141">@sourceURL et displayName</span><span class="sxs-lookup"><span data-stu-id="dc72e-141">@sourceURL and displayName</span></span>  

<span data-ttu-id="dc72e-142">Si ce n’est pas le `@sourceURL` cas, vous pouvez simplifier le développement lors de l’utilisation d’eval.</span><span class="sxs-lookup"><span data-stu-id="dc72e-142">While not part of the Source Map spec, the `@sourceURL` allows you to make development much easier when working with evals.</span></span>  <span data-ttu-id="dc72e-143">Ce programme d’assistance se présente de manière très similaire à la `//# sourceMappingURL` propriété et est en fait mentionné dans les spécifications du mappage source v3.</span><span class="sxs-lookup"><span data-stu-id="dc72e-143">This helper looks very similar to the `//# sourceMappingURL` property and is actually mentioned in the Source Map V3 specifications.</span></span>  

<span data-ttu-id="dc72e-144">En incluant le commentaire spécial suivant dans votre code, qui est considéré comme étant Eval, vous pouvez nommer les évaluations et les scripts intralignes et les styles de sorte qu’ils apparaissent sous la forme de noms plus logiques dans votre DevTools.</span><span class="sxs-lookup"><span data-stu-id="dc72e-144">By including the following special comment in your code, which is be evaled, you are able to name evals and inline scripts and styles so each appears as more logical names in your DevTools.</span></span>  

```javascript
//# sourceURL=source.coffee
```  

<span data-ttu-id="dc72e-145">Accédez à la page suivante.</span><span class="sxs-lookup"><span data-stu-id="dc72e-145">Navigate to the following page.</span></span>  

*   [<span data-ttu-id="dc72e-146">démonstration</span><span class="sxs-lookup"><span data-stu-id="dc72e-146">demo</span></span>][CssNinjaDemoSourceMapping]

<span data-ttu-id="dc72e-147">Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="dc72e-147">Follow these steps.</span></span>  

1.  <span data-ttu-id="dc72e-148">Ouvrez le DevTools et accédez au panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="dc72e-148">Open the DevTools and go to the **Sources** panel.</span></span>  
1.  <span data-ttu-id="dc72e-149">Entrez un nom de fichier dans le champ **_nom de votre code:_** champ de saisie.</span><span class="sxs-lookup"><span data-stu-id="dc72e-149">Enter in a filename into the **_Name your code:_** input field.</span></span>  
1.  <span data-ttu-id="dc72e-150">Cliquez sur le bouton **compiler** .</span><span class="sxs-lookup"><span data-stu-id="dc72e-150">Click on the **compile** button.</span></span>  
1.  <span data-ttu-id="dc72e-151">Une alerte apparaît avec la somme évaluée à partir de la source de CoffeeScript.</span><span class="sxs-lookup"><span data-stu-id="dc72e-151">An alert appears with the evaluated sum from the CoffeeScript source.</span></span>  

<span data-ttu-id="dc72e-152">Si vous développez le sous-panneau **_sources_** , vous voyez maintenant un nouveau fichier avec le nom de fichier personnalisé que vous avez entré précédemment.</span><span class="sxs-lookup"><span data-stu-id="dc72e-152">If you expand the **_Sources_** sub-panel you now see a new file with the custom filename you entered earlier.</span></span>  <span data-ttu-id="dc72e-153">Si vous double-cliquez sur le fichier pour l’afficher, il contient le code JavaScript compilé pour la source d’origine.</span><span class="sxs-lookup"><span data-stu-id="dc72e-153">If you double-click to view this file it contains the compiled JavaScript for the original source.</span></span>  <span data-ttu-id="dc72e-154">En revanche, la dernière ligne est un `// @sourceURL` Commentaire indiquant le fichier source d’origine.</span><span class="sxs-lookup"><span data-stu-id="dc72e-154">On the last line, however, is a `// @sourceURL` comment indicating the original source file.</span></span>  <span data-ttu-id="dc72e-155">Cela risque de vous aider à procéder au débogage lorsque vous travaillez avec des résumés de langue.</span><span class="sxs-lookup"><span data-stu-id="dc72e-155">This may help you with debugging while working with language abstractions.</span></span>  

> ##### <span data-ttu-id="dc72e-156">Figure 2</span><span class="sxs-lookup"><span data-stu-id="dc72e-156">Figure 2</span></span>
> <span data-ttu-id="dc72e-157">Utilisation de sourceURL</span><span class="sxs-lookup"><span data-stu-id="dc72e-157">Working with sourceURL</span></span>  
> ![Utilisation de sourceURL][ImageCoffeeScript]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageSourceMaps]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-preferences-sources-enable-javascript-source-maps.msft.png "Figure 1: activer les mappages sources"  
[ImageCoffeeScript]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-coffeeeeeeee.msft.png "Figure 2: utilisation de sourceURL"  

<!-- links -->  

[BabelJS]: https://babeljs.io "Babel est un compilateur JavaScript"  
[CoffeeScriptMain]: https://coffeescript.org "CoffeeScript"  
[CssNinjaDemoSourceMapping]: https://www.thecssninja.com/demo/source_mapping/compile.html "Voici un exemple simple d’utilisation de l’appellation eval"  
[DartMain]: https://www.dartlang.org "Langage de programmation DART"  
[GitHubGoogleClosureCompiler]: https://github.com/google/closure-compiler "Google/Closure-compilateur | GitHub"  
[GitHubMishooUglifyJS]: https://github.com/mishoo/UglifyJS "mishoo/UglifyJS | GitHub"  
[GitHubWikiSourceMapsLanguagesTools]: https://github.com/ryanseddon/source-map/wiki/Source-maps:-languages,-tools-and-other-info "Cartes sources: langues, outils et autres informations | Wiki GitHub"  
[GitHubWikiGoogleTraceurCompiler]: https://github.com/google/traceur-compiler/wiki/Getting-Started "Mise en route-Google/traceur-compilateur | Wiki GitHub"  
[TypeScriptMain]: https://www.typescriptlang.org "Dactylographié"  

> [!NOTE]
> <span data-ttu-id="dc72e-170">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc72e-170">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dc72e-171">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \) et [Paul Bakaus][PaulBakaus] \ (Open Web Developer défenseur, Google: Tools, performance, animation et expérience utilisateur).</span><span class="sxs-lookup"><span data-stu-id="dc72e-171">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/source-maps) and is authored by [Meggin Kearney][MegginKearney] \(Tech Writer\) and [Paul Bakaus][PaulBakaus] \(Open Web Developer Advocate, Google: Tools, Performance, Animation, and UX\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="dc72e-173">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dc72e-173">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
[PaulBakaus]: https://developers.google.com/web/resources/contributors/pbakaus  