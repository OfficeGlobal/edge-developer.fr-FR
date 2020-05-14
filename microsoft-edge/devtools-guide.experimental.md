---
description: Découvrir les outils de développement Microsoft Edge
title: Outils de développement Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft Edge, développement Web, outils F12, devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 47b7a3f4f523170f4dfb6f3ef674cecfdc0e157c
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645328"
---
# <span data-ttu-id="ac548-104">Outils de développement Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="ac548-104">Microsoft Edge Developer Tools</span></span>  

> [!NOTE]
> <span data-ttu-id="ac548-105">Les développeurs Microsoft Edge DevTools permettent aux développeurs de créer et de tester des sites Web.</span><span class="sxs-lookup"><span data-stu-id="ac548-105">The Microsoft Edge DevTools help web developers build and test websites.</span></span>  <span data-ttu-id="ac548-106">Si vous avez accidentellement ouvert le DevTools, il vous suffit d’appuyer sur `F12` pour le fermer.</span><span class="sxs-lookup"><span data-stu-id="ac548-106">If you accidentally opened the DevTools, just press `F12` to close.</span></span>  

<span data-ttu-id="ac548-107">Les applications Microsoft Edge DevTools sont créées [à l’aide de la](https://www.typescriptlang.org/)fonction de création de code, optimisée par une [source ouverte](https://github.com/Microsoft/ChakraCore), optimisée pour les flux de travail frontal modernes et désormais disponibles sous la forme d’une [application Windows 10 autonome](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) sur le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="ac548-107">The Microsoft Edge DevTools are built with [TypeScript](https://www.typescriptlang.org/), powered by [open source](https://github.com/Microsoft/ChakraCore), optimized for modern front-end workflows, and now available as a [standalone Windows 10 app](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) in the Microsoft Store!</span></span>

<span data-ttu-id="ac548-108">Pour plus d’informations sur les dernières fonctionnalités, consultez [*devtools la dernière mise à jour de Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="ac548-108">For more on the latest features, check out [*DevTools in the latest update of Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).</span></span>

## <span data-ttu-id="ac548-109">Outils principaux</span><span class="sxs-lookup"><span data-stu-id="ac548-109">Core tools</span></span>

![Outils Microsoft Edge Dev](./devtools-guide/media/devtools.png)

<span data-ttu-id="ac548-111">Les DevTools de Microsoft Edge sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="ac548-111">The Microsoft Edge DevTools include:</span></span>

 - <span data-ttu-id="ac548-112">Panneau d' [**éléments**](./devtools-guide/elements.md) permettant de modifier les propriétés d’accessibilité, d’afficher les détecteurs d’événements et de définir des points d’arrêt de mutation DOM</span><span class="sxs-lookup"><span data-stu-id="ac548-112">An [**Elements**](./devtools-guide/elements.md) panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>
 - <span data-ttu-id="ac548-113">Une [**console**](./devtools-guide/console.md) pour afficher et filtrer des messages de journaux, inspecter des objets JavaScript et des nœuds DOM et exécuter JavaScript dans le contexte de la fenêtre ou du cadre sélectionné.</span><span class="sxs-lookup"><span data-stu-id="ac548-113">A [**Console**](./devtools-guide/console.md) to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>
 - <span data-ttu-id="ac548-114">Le [**débogueur**](./devtools-guide/debugger.md) pour parcourir le code, définir des espions et des points d’arrêt, modifier votre code et inspecter les caches de stockage et de cookies Web</span><span class="sxs-lookup"><span data-stu-id="ac548-114">A [**Debugger**](./devtools-guide/debugger.md) to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>
 - <span data-ttu-id="ac548-115">Panneau [**réseau**](./devtools-guide/network.md) permettant de surveiller et d’inspecter les demandes et les réponses du réseau et du cache du navigateur</span><span class="sxs-lookup"><span data-stu-id="ac548-115">A [**Network**](./devtools-guide/network.md) panel to monitor and inspect requests and responses from the network and browser cache</span></span> 
 - <span data-ttu-id="ac548-116">Panneau [**performance**](./devtools-guide/performance.md) pour le profil du temps et des ressources système requis par votre site</span><span class="sxs-lookup"><span data-stu-id="ac548-116">A [**Performance**](./devtools-guide/performance.md) panel to profile the time and system resources required by your site</span></span>
 - <span data-ttu-id="ac548-117">Panneau [**mémoire**](./devtools-guide/memory.md) permettant de mesurer votre utilisation des ressources de mémoire et de comparer les instantanés de tas dans différents États de l’exécution du code</span><span class="sxs-lookup"><span data-stu-id="ac548-117">A [**Memory**](./devtools-guide/memory.md) panel to measure your use of memory resources and compare heap snapshots at different states of code execution</span></span>
 - <span data-ttu-id="ac548-118">Panneau d' [**émulation**](./devtools-guide/emulation.md) pour tester votre site avec différents profils de navigateur, résolutions d’écran et coordonnées d’emplacement GPS</span><span class="sxs-lookup"><span data-stu-id="ac548-118">An [**Emulation**](./devtools-guide/emulation.md) panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>

<span data-ttu-id="ac548-119">Continuez à envoyer vos [commentaires et demandes de fonctionnalité](#feedback).</span><span class="sxs-lookup"><span data-stu-id="ac548-119">Please keep sending your [feedback and feature requests](#feedback)!</span></span>

> [!TIP]
> <span data-ttu-id="ac548-120">**[Testez gratuitement Microsoft Edge à partir de n’importe quel navigateur](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: nous nous sommes associés à [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) pour proposer des tests gratuits en temps réel et automatisés sur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ac548-120">**[Test on Microsoft Edge free from any browser](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: We partnered with [BrowserStack](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) to provide free live and automated testing on Microsoft Edge.</span></span>

## <span data-ttu-id="ac548-121">Application du MicrosoftStore</span><span class="sxs-lookup"><span data-stu-id="ac548-121">Microsoft Store app</span></span>

<span data-ttu-id="ac548-122">Les **devtools Microsoft Edge** sont [désormais disponibles pour l’aperçu](./devtools-guide/whats-new.md) en tant qu' [application Windows 10 autonome à partir du Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), en plus de l’outil de navigation intégré dans le navigateur `F12` .</span><span class="sxs-lookup"><span data-stu-id="ac548-122">The **Microsoft Edge DevTools** are [now available for preview](./devtools-guide/whats-new.md) as a standalone [Windows 10 app from the Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), in addition to the in-browser (`F12`) tooling experience.</span></span> <span data-ttu-id="ac548-123">La version du Windows Store est une fenêtre de *sélection* qui permet de joindre des cibles de page locales et distantes ouvertes et une disposition avec onglets pour faciliter le basculement entre les instances devtools.</span><span class="sxs-lookup"><span data-stu-id="ac548-123">With the store version comes a *chooser* panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>

### <span data-ttu-id="ac548-124">Débogage local</span><span class="sxs-lookup"><span data-stu-id="ac548-124">Local debugging</span></span>

<span data-ttu-id="ac548-125">Pour déboguer une page en local, lancez simplement l’application *Microsoft Edge devtools* .</span><span class="sxs-lookup"><span data-stu-id="ac548-125">To debug a page locally, simply launch the *Microsoft Edge DevTools* app.</span></span> <span data-ttu-id="ac548-126">Le panneau **local** du sélecteur affiche tous les processus du contenu EdgeHTML actif, y compris les onglets du navigateur Open Edge, exécutant [PWAS](./progressive-web-apps-edgehtml/index.md) (processus*WWAHost. exe* ) et contrôles [WebView](./webview.md) .</span><span class="sxs-lookup"><span data-stu-id="ac548-126">The **Local** panel of the chooser will display all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* processes), and [webview](./webview.md) controls.</span></span> <span data-ttu-id="ac548-127">Cliquez sur la cible souhaitée pour joindre et ouvrir une nouvelle instance de l’onglet du DevTools.</span><span class="sxs-lookup"><span data-stu-id="ac548-127">Click on your desired target to attach and open a new tab instance of the DevTools.</span></span>

![Panneau local de l’application DevTools](./devtools-guide/media/chooser_local.png)

### <span data-ttu-id="ac548-129">Débogage à distance</span><span class="sxs-lookup"><span data-stu-id="ac548-129">Remote debugging</span></span>

<span data-ttu-id="ac548-130">L’application *Microsoft Edge devtools* présente une prise en charge de base pour le débogage de pages sur un ordinateur distant par le biais de notre [**protocole devtools**](./devtools-protocol/index.md)nouvellement publiée.</span><span class="sxs-lookup"><span data-stu-id="ac548-130">The *Microsoft Edge DevTools* app introduces basic support for debugging pages on a remote machine via our newly released [**DevTools Protocol**](./devtools-protocol/index.md).</span></span> <span data-ttu-id="ac548-131">Avec cette version, l’accès distant aux funtionality principaux dans le volet [**débogueur**](./devtools-guide/debugger.md) est l’inspection du cache moins (pour le stockage Web, le travailleur de service, l’API de cache et IndexedDB).</span><span class="sxs-lookup"><span data-stu-id="ac548-131">With this release comes remote access to core funtionality in the [**Debugger**](./devtools-guide/debugger.md) panel, minus cache inspection (for Web storage, Service worker, Cache API, and IndexedDB).</span></span> <span data-ttu-id="ac548-132">Le débogage à distance est limité à *Microsoft Edge* exécutant des hôtes de *Bureau* , avec la prise en charge d’autres hôtes EdgeHTML et des appareils Windows 10 qui arrivent dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ac548-132">Remote debugging is limited to *Microsoft Edge* running *desktop* hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="ac548-133">Pour commencer, consultez la section [*Microsoft Edge devtools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) des documents du [protocole devtools](./devtools-protocol/index.md) .</span><span class="sxs-lookup"><span data-stu-id="ac548-133">To get started, check out the [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) section of the [DevTools Protocol](./devtools-protocol/index.md) docs.</span></span>

![Panneau distant de l’application DevTools](./devtools-guide/media/chooser_remote.png)

## <span data-ttu-id="ac548-135">Commentaires</span><span class="sxs-lookup"><span data-stu-id="ac548-135">Feedback</span></span>

<span data-ttu-id="ac548-136">Envoyez-nous vos commentaires pour que nous puissions continuer à améliorer Microsoft Edge DevTools pour vous.</span><span class="sxs-lookup"><span data-stu-id="ac548-136">Please send us your feedback so we can continue improving the Microsoft Edge DevTools for you!</span></span> <span data-ttu-id="ac548-137">Il suffit d’ouvrir le menu Outils ( `F12` ) et de cliquer sur le bouton [**Envoyer des commentaires**](#microsoft-edge-developer-tools) .</span><span class="sxs-lookup"><span data-stu-id="ac548-137">Simply open the tools (`F12`) and click the [**Send feedback**](#microsoft-edge-developer-tools) button.</span></span>

<span data-ttu-id="ac548-138">Vous pouvez également ajouter des demandes d’instrumentation aux fonctions d’instrumentation et les voter dans le [Forum UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) et participer au programme [Windows Insider](https://insider.windows.com/) pour prévisualiser les [dernières fonctionnalités disponibles dans le devtools](./devtools-guide/whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="ac548-138">You can also add and upvote tooling requests to our [UserVoice forum](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) and become a [Windows Insider](https://insider.windows.com/) to preview the [latest features coming to the DevTools](./devtools-guide/whats-new.md).</span></span> <span data-ttu-id="ac548-139">Utilisez l’application **Hub de commentaires** Windows pour publier, voter, suivre et obtenir de l’aide sur les suggestions et problèmes généraux concernant Windows.</span><span class="sxs-lookup"><span data-stu-id="ac548-139">Use the Windows **Feedback Hub** app to post, upvote, track and get support for general Windows suggestions and problems.</span></span>

## <span data-ttu-id="ac548-140">Raccourcis clavier généraux</span><span class="sxs-lookup"><span data-stu-id="ac548-140">General Shortcuts</span></span>

<span data-ttu-id="ac548-141">Ces raccourcis contrôlent la fenêtre principale de DevTools et/ou travaillent sur tous les outils.</span><span class="sxs-lookup"><span data-stu-id="ac548-141">These shortcuts control the main DevTools window and/or work across all tools.</span></span>

<span data-ttu-id="ac548-142">Action</span><span class="sxs-lookup"><span data-stu-id="ac548-142">Action</span></span> | <span data-ttu-id="ac548-143">Raccourci</span><span class="sxs-lookup"><span data-stu-id="ac548-143">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="ac548-144">Afficher/masquer DevTools (s’ouvre au panneau dernier affichage)</span><span class="sxs-lookup"><span data-stu-id="ac548-144">Show/Hide DevTools (opens to last viewed panel)</span></span> | <span data-ttu-id="ac548-145">F12, Ctrl + Maj + I</span><span class="sxs-lookup"><span data-stu-id="ac548-145">F12, Ctrl+Shift+I</span></span>
<span data-ttu-id="ac548-146">Basculer l’ancrage (détacher/bas/droite)</span><span class="sxs-lookup"><span data-stu-id="ac548-146">Toggle docking (Undock/Bottom/Right)</span></span> | <span data-ttu-id="ac548-147">Ctrl + Maj + D</span><span class="sxs-lookup"><span data-stu-id="ac548-147">Ctrl+Shift+D</span></span> 
<span data-ttu-id="ac548-148">Afficher le code source HTML non modifiable dans le débogueur</span><span class="sxs-lookup"><span data-stu-id="ac548-148">Show non-editable HTML source code in Debugger</span></span> | <span data-ttu-id="ac548-149">Ctrl + U</span><span class="sxs-lookup"><span data-stu-id="ac548-149">Ctrl+U</span></span>
<span data-ttu-id="ac548-150">Afficher/masquer la console en bas de n’importe quel autre outil</span><span class="sxs-lookup"><span data-stu-id="ac548-150">Show/hide Console at the bottom of any other tool</span></span>  | <span data-ttu-id="ac548-151">Ctrl +**\`**</span><span class="sxs-lookup"><span data-stu-id="ac548-151">Ctrl+**\`**</span></span>
<span data-ttu-id="ac548-152">Basculer vers des éléments (Explorateur DOM)</span><span class="sxs-lookup"><span data-stu-id="ac548-152">Switch to Elements (DOM Explorer)</span></span> | <span data-ttu-id="ac548-153">CTRL + 1</span><span class="sxs-lookup"><span data-stu-id="ac548-153">Ctrl+1</span></span>
<span data-ttu-id="ac548-154">Basculer vers la console</span><span class="sxs-lookup"><span data-stu-id="ac548-154">Switch to Console</span></span> |  <span data-ttu-id="ac548-155">CTRL + 2</span><span class="sxs-lookup"><span data-stu-id="ac548-155">Ctrl+2</span></span>
<span data-ttu-id="ac548-156">Basculer vers le débogueur</span><span class="sxs-lookup"><span data-stu-id="ac548-156">Switch to Debugger</span></span> | <span data-ttu-id="ac548-157">Ctrl + 3</span><span class="sxs-lookup"><span data-stu-id="ac548-157">Ctrl+3</span></span>
<span data-ttu-id="ac548-158">Basculer en réseau</span><span class="sxs-lookup"><span data-stu-id="ac548-158">Switch to Network</span></span> | <span data-ttu-id="ac548-159">CTRL + 4</span><span class="sxs-lookup"><span data-stu-id="ac548-159">Ctrl+4</span></span>
<span data-ttu-id="ac548-160">Basculer vers performance</span><span class="sxs-lookup"><span data-stu-id="ac548-160">Switch to Performance</span></span> | <span data-ttu-id="ac548-161">Ctrl + 5</span><span class="sxs-lookup"><span data-stu-id="ac548-161">Ctrl+5</span></span>
<span data-ttu-id="ac548-162">Basculer en mémoire</span><span class="sxs-lookup"><span data-stu-id="ac548-162">Switch to Memory</span></span> | <span data-ttu-id="ac548-163">Ctrl + 6</span><span class="sxs-lookup"><span data-stu-id="ac548-163">Ctrl+6</span></span>
<span data-ttu-id="ac548-164">Basculer vers l’émulation</span><span class="sxs-lookup"><span data-stu-id="ac548-164">Switch to Emulation</span></span> | <span data-ttu-id="ac548-165">CTRL + 7</span><span class="sxs-lookup"><span data-stu-id="ac548-165">Ctrl+7</span></span>
<span data-ttu-id="ac548-166">Document d’aide</span><span class="sxs-lookup"><span data-stu-id="ac548-166">Help Document</span></span> | <span data-ttu-id="ac548-167">F1</span><span class="sxs-lookup"><span data-stu-id="ac548-167">F1</span></span>
<span data-ttu-id="ac548-168">Outil suivant</span><span class="sxs-lookup"><span data-stu-id="ac548-168">Next tool</span></span> | <span data-ttu-id="ac548-169">Ctrl + F6</span><span class="sxs-lookup"><span data-stu-id="ac548-169">Ctrl+F6</span></span>
<span data-ttu-id="ac548-170">Outil précédent</span><span class="sxs-lookup"><span data-stu-id="ac548-170">Previous tool</span></span> | <span data-ttu-id="ac548-171">CTRL + MAJ + F6</span><span class="sxs-lookup"><span data-stu-id="ac548-171">Ctrl+Shift+F6</span></span>
<span data-ttu-id="ac548-172">Outil précédent (de l’historique)</span><span class="sxs-lookup"><span data-stu-id="ac548-172">Previous tool (from history)</span></span> | <span data-ttu-id="ac548-173">Ctrl + Maj + [</span><span class="sxs-lookup"><span data-stu-id="ac548-173">Ctrl+Shift+[</span></span>
<span data-ttu-id="ac548-174">Outil suivant (de l’historique)</span><span class="sxs-lookup"><span data-stu-id="ac548-174">Next tool (from history)</span></span> | <span data-ttu-id="ac548-175">Ctrl + Maj +]</span><span class="sxs-lookup"><span data-stu-id="ac548-175">Ctrl+Shift+]</span></span>
<span data-ttu-id="ac548-176">Sous-image suivante</span><span class="sxs-lookup"><span data-stu-id="ac548-176">Next Subframe</span></span>    | <span data-ttu-id="ac548-177">F6</span><span class="sxs-lookup"><span data-stu-id="ac548-177">F6</span></span>
<span data-ttu-id="ac548-178">Sous-cadre précédent</span><span class="sxs-lookup"><span data-stu-id="ac548-178">Previous Subframe</span></span> | <span data-ttu-id="ac548-179">MAJ + F6</span><span class="sxs-lookup"><span data-stu-id="ac548-179">Shift+F6</span></span>
<span data-ttu-id="ac548-180">Résultat suivant dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="ac548-180">Next match in Search box</span></span> | <span data-ttu-id="ac548-181">F3</span><span class="sxs-lookup"><span data-stu-id="ac548-181">F3</span></span>
<span data-ttu-id="ac548-182">Résultat précédent dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="ac548-182">Previous match in Search box</span></span> | <span data-ttu-id="ac548-183">Maj + F3</span><span class="sxs-lookup"><span data-stu-id="ac548-183">Shift+F3</span></span>
<span data-ttu-id="ac548-184">Rechercher dans la zone de recherche</span><span class="sxs-lookup"><span data-stu-id="ac548-184">Find in search box</span></span> | <span data-ttu-id="ac548-185">Ctrl+F</span><span class="sxs-lookup"><span data-stu-id="ac548-185">Ctrl+F</span></span>
<span data-ttu-id="ac548-186">Mettre le focus sur la console en bas</span><span class="sxs-lookup"><span data-stu-id="ac548-186">Give focus to console at the bottom</span></span> | <span data-ttu-id="ac548-187">Alt + Maj + I</span><span class="sxs-lookup"><span data-stu-id="ac548-187">Alt+Shift+I</span></span>
<span data-ttu-id="ac548-188">Outils d’ancrage/de déconnexion (basculer vers l’ancrage)</span><span class="sxs-lookup"><span data-stu-id="ac548-188">Dock/undock tools (toggle docking)</span></span> | <span data-ttu-id="ac548-189">Ctrl+P</span><span class="sxs-lookup"><span data-stu-id="ac548-189">Ctrl+P</span></span>  
<span data-ttu-id="ac548-190">Lancer DevTools vers la console</span><span class="sxs-lookup"><span data-stu-id="ac548-190">Launch DevTools to Console</span></span> | <span data-ttu-id="ac548-191">Ctrl + Maj + J</span><span class="sxs-lookup"><span data-stu-id="ac548-191">Ctrl+Shift+J</span></span>
<span data-ttu-id="ac548-192">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="ac548-192">Refresh the page.</span></span> <span data-ttu-id="ac548-193">**Remarque:** si vous déboguez un point d’arrêt et que vous êtes en pause, l’exécution reprend en premier.</span><span class="sxs-lookup"><span data-stu-id="ac548-193">**Note:** if you're debugging and paused at a breakpoint, this resumes execution first.</span></span> | <span data-ttu-id="ac548-194">Ctrl + Maj + F5 ou Ctrl + R</span><span class="sxs-lookup"><span data-stu-id="ac548-194">Ctrl+Shift+F5 or Ctrl+R</span></span>