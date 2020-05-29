---
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans EdgeHTML 15.
title: Nouveautés de EdgeHTML 15
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.custom: seodec18
ms.openlocfilehash: e750a9272bb8bcdb51662839a31cc303c4064ef9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564718"
---
# <span data-ttu-id="ca60d-104">Nouveautés de EdgeHTML 15</span><span class="sxs-lookup"><span data-stu-id="ca60d-104">What's new in EdgeHTML 15</span></span>
<span data-ttu-id="ca60d-105">Voici les modifications apportées à la version actuelle de la plate-forme Microsoft Edge, à partir de [Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (04/2017, Build 15063).</span><span class="sxs-lookup"><span data-stu-id="ca60d-105">Here are the changes shipped with the current release of the Microsoft Edge platform, as of the [Windows 10 Creators Update](https://blogs.windows.com/buildingapps/2017/04/05/windows-10-creators-update-creators-update-sdk-released/#MMhK2OdcrR12Vi6u.97) (04/2017, Build 15063).</span></span> <span data-ttu-id="ca60d-106">Pour obtenir une vue d’ensemble des modifications apportées au navigateur Microsoft Edge global, voir [Nouveautés de Microsoft Edge dans Windows 10 Creators Update](https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/#DrVEvmPU6TPq3tMK.97)</span><span class="sxs-lookup"><span data-stu-id="ca60d-106">For an overview of changes to the overall Microsoft Edge browser, see [What's new in Microsoft Edge in the Windows 10 Creators Update](https://blogs.windows.com/msedgedev/2017/04/11/introducing-edgehtml-15/#DrVEvmPU6TPq3tMK.97)</span></span>

<span data-ttu-id="ca60d-107">Pour plus d’informations sur les modifications apportées aux versions préliminaires de Windows Insider Preview, voir [Nouveautés de EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="ca60d-107">For changes in subsequent Windows Insider Preview builds, see [What's New in EdgeHTML](../whats-new.md).</span></span>

<span data-ttu-id="ca60d-108">Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante: **[https://aka.ms/devguide_edgehtml_15](https://aka.ms/devguide_edgehtml_15)** .</span><span class="sxs-lookup"><span data-stu-id="ca60d-108">Here's the permalink for the following list of changes: **[https://aka.ms/devguide_edgehtml_15](https://aka.ms/devguide_edgehtml_15)**.</span></span>

## <span data-ttu-id="ca60d-109">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="ca60d-109">New features</span></span>

### <span data-ttu-id="ca60d-110">Propriétés personnalisées CSS</span><span class="sxs-lookup"><span data-stu-id="ca60d-110">CSS Custom Properties</span></span>
<span data-ttu-id="ca60d-111">Microsoft Edge prend désormais en charge les [propriétés personnalisées CSS](https://drafts.csswg.org/css-variables/), une variable. k. une variable CSS.</span><span class="sxs-lookup"><span data-stu-id="ca60d-111">Microsoft Edge now supports [CSS Custom Properties](https://drafts.csswg.org/css-variables/), a.k.a CSS Variables.</span></span> <span data-ttu-id="ca60d-112">Les variables CSS vous permettent de créer des propriétés CSS personnalisées qui peuvent être réutilisées dans toutes les feuilles de style afin de réduire la quantité de données dupliquées, par exemple les couleurs répétées.</span><span class="sxs-lookup"><span data-stu-id="ca60d-112">CSS Variables allow you to create custom CSS properties that can be reused throughout stylesheets to help reduce the amount of duplicate data, like repeated colors.</span></span> <span data-ttu-id="ca60d-113">L’utilisation de variables CSS est simple:</span><span class="sxs-lookup"><span data-stu-id="ca60d-113">Using CSS Variables is simple:</span></span>

```css
/* define a custom property by using two dashes and assign it a value */
body {   
   --default-color: #3390b1
}

/* reference it in your stylesheet with the "var()" function */
h1 {
   color: var(--default-color);
}
```  

### <span data-ttu-id="ca60d-114">Observateur d’intersection</span><span class="sxs-lookup"><span data-stu-id="ca60d-114">Intersection Observer</span></span>
<span data-ttu-id="ca60d-115">EdgeHTML 15 présente la spécification de l' [API d’observation d’intersection](https://w3c.github.io/IntersectionObserver/) .</span><span class="sxs-lookup"><span data-stu-id="ca60d-115">EdgeHTML 15 introduces the [Intersection Observer API](https://w3c.github.io/IntersectionObserver/) specification.</span></span> <span data-ttu-id="ca60d-116">L’API d’observation d’intersection vous permet d’interroger de manière asynchrone la position et la visibilité des éléments DOM par rapport à d’autres éléments ou à la fenêtre d’affichage globale.</span><span class="sxs-lookup"><span data-stu-id="ca60d-116">The Intersection Observer API allows you to asynchronously query the position and visibility of DOM elements relative to other elements or the global viewport.</span></span> <span data-ttu-id="ca60d-117">Cette API élimine le besoin d’utiliser du code coûteux personnalisé en créant une méthode pour avertir efficacement les éléments lorsqu’ils sont en vue.</span><span class="sxs-lookup"><span data-stu-id="ca60d-117">This API eliminates the need for custom expensive code by creating a method to efficiently notify elements when they are in view.</span></span>

### <span data-ttu-id="ca60d-118">JavaScript</span><span class="sxs-lookup"><span data-stu-id="ca60d-118">JavaScript</span></span>

<span data-ttu-id="ca60d-119">Les optimisations de performance prennent du temps central avec la rév. EdgeHTML 15 du moteur JavaScript Chakra.</span><span class="sxs-lookup"><span data-stu-id="ca60d-119">Performance optimizations take center stage with the EdgeHTML 15 rev of the Chakra JavaScript engine.</span></span> <span data-ttu-id="ca60d-120">À l’aide de Windows 10 Creators Update, chakra enregistre de la mémoire en redifférant les fonctions et en optimisant les arguments du tas et améliore les performances du code minified.</span><span class="sxs-lookup"><span data-stu-id="ca60d-120">With the Windows 10 Creators Update, Chakra saves memory by re-deferring functions and optimizing away heap arguments and improves performance for minified code.</span></span>

<span data-ttu-id="ca60d-121">De plus, le EdgeHTML 15 présente les aperçus des fonctionnalités suivants:</span><span class="sxs-lookup"><span data-stu-id="ca60d-121">Additionally, EdgeHTML 15 introduces the following feature previews:</span></span>

#### <span data-ttu-id="ca60d-122">Fonctionnalités JavaScript expérimentales (activées avec *à propos de: indicateurs*)</span><span class="sxs-lookup"><span data-stu-id="ca60d-122">Experimental JavaScript features (enabled with *about:flags*)</span></span>

* <span data-ttu-id="ca60d-123">[Webassemblage](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([démo](https://webassembly.org/demo/))</span><span class="sxs-lookup"><span data-stu-id="ca60d-123">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) ([demo](https://webassembly.org/demo/))</span></span>
* [<span data-ttu-id="ca60d-124">Mémoire partagée et Atomic.</span><span class="sxs-lookup"><span data-stu-id="ca60d-124">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)

<span data-ttu-id="ca60d-125">Pour plus d’informations [*, voir amélioration des performances JavaScript, de l’assemblage webassemblage et de la mémoire partagée dans Microsoft Edge*](https://blogs.windows.com/msedgedev/2017/04/20/improved-javascript-performance-webassembly-shared-memory/#t4gwUKjjtdmstMbs.97) .</span><span class="sxs-lookup"><span data-stu-id="ca60d-125">See [*Improved JavaScript performance, WebAssembly, and Shared Memory in Microsoft Edge*](https://blogs.windows.com/msedgedev/2017/04/20/improved-javascript-performance-webassembly-shared-memory/#t4gwUKjjtdmstMbs.97) for further details.</span></span>

### <span data-ttu-id="ca60d-126">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="ca60d-126">Payment Request API</span></span>
<span data-ttu-id="ca60d-127">L' [API de demande de paiement](https://w3.org/TR/payment-request/) est désormais prise en charge, ce qui permet d’extraire et de payer plus facilement sur le Web sur des PC et téléphones Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ca60d-127">The [Payment Request API](https://w3.org/TR/payment-request/) is now supported, enabling simpler checkout and payments on the web on Windows 10 PCs and Phones.</span></span> <span data-ttu-id="ca60d-128">Cette API permet à Microsoft Edge d’agir en tant qu’intermédiaire entre commerçants, consommateurs et modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="ca60d-128">This API enables Microsoft Edge to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> <span data-ttu-id="ca60d-129">Pour plus d’informations sur l’API de demande de paiement, consultez l’article utilisation de l’API de [demande](https://blogs.windows.com/msedgedev/2016/12/15/payment-request-api-edge/) de paiement et Guide du développeur de l’API de [demande de paiement](/microsoft-edge/dev-guide/device/payment-request-api) .</span><span class="sxs-lookup"><span data-stu-id="ca60d-129">For more information on the Payment Request API, check out [Simpler web payments: Introducing the Payment Request API](https://blogs.windows.com/msedgedev/2016/12/15/payment-request-api-edge/) and the [Payment Request API](/microsoft-edge/dev-guide/device/payment-request-api) developer guide.</span></span>

### <span data-ttu-id="ca60d-130">TCP Fast Open (TFO)</span><span class="sxs-lookup"><span data-stu-id="ca60d-130">TCP Fast Open (TFO)</span></span>
<span data-ttu-id="ca60d-131">TCP Fast Open est une fonctionnalité qui réduit le nombre de boucles nécessaires pour ouvrir une connexion TCP et améliorer les performances réseau du navigateur.</span><span class="sxs-lookup"><span data-stu-id="ca60d-131">TCP Fast Open is a feature that reduces the number of round trips required to open a TCP connection, improving browser networking performance.</span></span> <span data-ttu-id="ca60d-132">Pour plus d’informations, consultez [création d’un site Web plus rapide et plus sécurisé avec TCP Fast Open](https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/#eQMauReErmIRXYqh.97).</span><span class="sxs-lookup"><span data-stu-id="ca60d-132">For more details, see [Building a faster and more secure web with TCP Fast Open](https://blogs.windows.com/msedgedev/2016/06/15/building-a-faster-and-more-secure-web-with-tcp-fast-open-tls-false-start-and-tls-1-3/#eQMauReErmIRXYqh.97).</span></span> <span data-ttu-id="ca60d-133">En raison de différences d’interopérabilité de diverses topologies réseau, cette fonctionnalité n’est pas activée par défaut dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ca60d-133">Due to interoperability differences in various network topologies, this features is not enabled by default in Microsoft Edge.</span></span> <span data-ttu-id="ca60d-134">Pour l’activer, tapez `about:flags` votre barre d’adresses, puis activez la case à cocher **activer le protocole TCP Fast Open** dans la section *réseau* .</span><span class="sxs-lookup"><span data-stu-id="ca60d-134">To enable it, type `about:flags` in your address bar, and select the checkbox for **Enable TCP Fast Open** under the *Networking* section.</span></span> 

### <span data-ttu-id="ca60d-135">Prise en charge du codec vidéo WebRTC et interopérable RTC</span><span class="sxs-lookup"><span data-stu-id="ca60d-135">WebRTC and interoperable RTC video codec support</span></span>

<span data-ttu-id="ca60d-136">EdgeHTML 15 prend en charge un sous-ensemble de l’API 1,0 d’WebRTC pour l’interopérabilité avec des applications créées avec des versions antérieures de l’API WebRTC-PC sur 2015.</span><span class="sxs-lookup"><span data-stu-id="ca60d-136">EdgeHTML 15 supports a subset of the WebRTC 1.0 API for interoperability with applications built with earlier versions of the W3C WebRTC-PC API circa 2015.</span></span> <span data-ttu-id="ca60d-137">Pour plus d’informations, voir la référence de l' [API WebRTC](https://msdn.microsoft.com/library/mt806139(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ca60d-137">See the [WebRTC API reference](https://msdn.microsoft.com/library/mt806139(v=vs.85).aspx) for details.</span></span>

<span data-ttu-id="ca60d-138">Pour tirer parti des fonctionnalités plus avancées de la communication audio et vidéo d’égal à égal, nous vous recommandons d’utiliser l' [API Object Real-Time communications)](../realtime-communication/object-rtc-api.md).</span><span class="sxs-lookup"><span data-stu-id="ca60d-138">To take advantage of our most advanced features in peer-to-peer audio and video communication, we recommend using the [Object Real-Time Communication) API](../realtime-communication/object-rtc-api.md).</span></span> <span data-ttu-id="ca60d-139">L’API ORTC est mieux adaptée aux situations dans lesquelles vous souhaitez configurer les appels audio et vidéo de groupe, ou contrôler directement les objets de transport, d’expéditeur et de destinataire.</span><span class="sxs-lookup"><span data-stu-id="ca60d-139">The ORTC API is better suited for situations where you want to set up group audio and video calls, or directly control individual transport, sender, and receiver objects.</span></span>

<span data-ttu-id="ca60d-140">Le Microsoft Edge prend en charge les fonctions H. 264/AVC et VP8 avec la fonction ORTC et WebRTC [1,0, et](https://tools.ietf.org/html/rfc4588)fournit les fonctionnalités suivantes pour la prise en charge des deux types de codec: [ABS-Send-Time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time/) [,](https://tools.ietf.org/html/rfc4585)utilisation de la [fonction](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03)d’affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="ca60d-140">The Microsoft Edge supports both H.264/AVC and VP8 video with ORTC and WebRTC 1.0, and provides the following features in support of both codec types: [abs-send-time](https://webrtc.org/experiments/rtp-hdrext/abs-send-time/), [goog-remb](https://tools.ietf.org/html/draft-alvestrand-rmcat-remb-03), [Picture Loss Indication and Generic NACK feedback](https://tools.ietf.org/html/rfc4585), [RTP Retransmission](https://tools.ietf.org/html/rfc4588).</span></span>

<span data-ttu-id="ca60d-141">Pour plus d’informations, reportez-vous à [Présentation de WebRTC 1,0 et interopérabilité en temps réel dans Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31/introducing-webrtc-microsoft-edge/#k8XMeWKyZDQDPYR4.97).</span><span class="sxs-lookup"><span data-stu-id="ca60d-141">For more info, see [Introducing WebRTC 1.0 and interoperable real-time communications in Microsoft Edge](https://blogs.windows.com/msedgedev/2017/01/31/introducing-webrtc-microsoft-edge/#k8XMeWKyZDQDPYR4.97).</span></span>

### <span data-ttu-id="ca60d-142">WebVR</span><span class="sxs-lookup"><span data-stu-id="ca60d-142">WebVR</span></span>

<span data-ttu-id="ca60d-143">Microsoft Edge est désormais pris en charge par [WebVR](https://immersive-web.github.io/webxr/), une API expérimentale qui connecte les affichages de la tête de la fenêtre mixte Windows mixte et Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ca60d-143">Microsoft Edge now has support for [WebVR](https://immersive-web.github.io/webxr/), an experimental API that connects Windows Mixed Reality head mounted displays and Microsoft Edge.</span></span> <span data-ttu-id="ca60d-144">Cette connexion permet d’avoir accès au contenu VR au sein d’un site Web, ce qui signifie que les expériences de VR ne sont plus limitées aux applications de bureau.</span><span class="sxs-lookup"><span data-stu-id="ca60d-144">This connection enables VR content to be experienced within a website, meaning immersive VR experiences are no longer limited to desktop applications.</span></span>  

<span data-ttu-id="ca60d-145">La réalité virtuelle dans Microsoft Edge est optimisée par WebGL, une API JavaScript pour le rendu des graphismes 3D et 2D.</span><span class="sxs-lookup"><span data-stu-id="ca60d-145">Virtual reality in Microsoft Edge is powered by WebGL, a JavaScript API for rendering 3D and 2D graphics.</span></span> <span data-ttu-id="ca60d-146">Les applications WebGL et applications créées avec des bibliothèques WebGL telles que BabylonJS sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ca60d-146">WebGL applications and applications built with WebGL libraries like BabylonJS are supported.</span></span> <span data-ttu-id="ca60d-147">Une fois connecté, WebVR envoie des visuels correspondant à la position et aux informations de capteur du casque.</span><span class="sxs-lookup"><span data-stu-id="ca60d-147">Once connected, WebVR sends visuals corresponding to the position and sensor information around the headset.</span></span> <span data-ttu-id="ca60d-148">L’API WebVR prend également en charge les contrôleurs spatiaux grâce à une extension de l' [API de boîtier](../dom/gamepad-api.md)de commandes.</span><span class="sxs-lookup"><span data-stu-id="ca60d-148">The WebVR API also supports spatial controllers thanks to an extension to the [Gamepad API](../dom/gamepad-api.md).</span></span> <span data-ttu-id="ca60d-149">Cette API est activée par défaut, il n’est donc pas nécessaire de basculer sur un indicateur.</span><span class="sxs-lookup"><span data-stu-id="ca60d-149">This API is on by default, so no need to toggle a flag.</span></span>

<span data-ttu-id="ca60d-150">Pour plus d’informations, voir les informations de référence sur les API [WebVR](https://msdn.microsoft.com/library/mt806281(v=vs.85).aspx) et le [boîtier](https://msdn.microsoft.com/library/dn743630(v=vs.85).aspx) de connexion.</span><span class="sxs-lookup"><span data-stu-id="ca60d-150">See the [WebVR API reference](https://msdn.microsoft.com/library/mt806281(v=vs.85).aspx) and [Gamepad API reference](https://msdn.microsoft.com/library/dn743630(v=vs.85).aspx) for details.</span></span>

 > [!NOTE] 
 > <span data-ttu-id="ca60d-151">Dans la mesure où la spécification WebVR est toujours en développement, la mise en œuvre de Microsoft Edge peut changer plus tard.</span><span class="sxs-lookup"><span data-stu-id="ca60d-151">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>



## <span data-ttu-id="ca60d-152">Fonctionnalités mises à jour</span><span class="sxs-lookup"><span data-stu-id="ca60d-152">Updated features</span></span>

### <span data-ttu-id="ca60d-153">Stratégie de sécurité du contenu (niveau 2)</span><span class="sxs-lookup"><span data-stu-id="ca60d-153">Content Security Policy (Level 2)</span></span>
<span data-ttu-id="ca60d-154">Les sites utilisant déjà un fournisseur de services cryptographiques 1 doivent continuer à utiliser la prise en charge de Microsoft Edge pour FSC 2, mais il est préférable de basculer entre les directives permettant de `frame-src` charger les scripts de travail dans la nouvelle `child-src` directive afin de vérifier l’évolution de votre site.</span><span class="sxs-lookup"><span data-stu-id="ca60d-154">Sites already using CSP 1 should continue to work with Microsoft Edge support for CSP 2, however it's best to switch any `frame-src` directives that load worker scripts to the new `child-src` directive to future-proof your site.</span></span> <span data-ttu-id="ca60d-155">(Dans FSC 3, `frame-src` ne s’appliquera plus aux travailleurs.) Le FSC 2 ajoute également ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="ca60d-155">(In CSP 3, `frame-src` will no longer apply to workers.) CSP 2 also adds the following:</span></span>

1. <span data-ttu-id="ca60d-156">Nouvelles directives: `base-uri` , `child-src` , `form-action` , `frame-ancestors` et `plugin-types` .</span><span class="sxs-lookup"><span data-stu-id="ca60d-156">New directives: `base-uri`, `child-src`, `form-action`, `frame-ancestors` and `plugin-types`.</span></span> <span data-ttu-id="ca60d-157">Pour plus d’informations, voir [directives CSP prises en charge par Microsoft Edge](../security/content-security-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="ca60d-157">See [Microsoft Edge supported CSP directives](../security/content-security-policy.md) for more.</span></span>

2. <span data-ttu-id="ca60d-158">Support pour les travailleurs: les scripts de travail en arrière-plan sont régis par leur propre stratégie, indépendamment de la stratégie de chargement du document.</span><span class="sxs-lookup"><span data-stu-id="ca60d-158">Workers support: Background worker scripts are governed by their own policy, separate from the policy of the document loading them.</span></span> <span data-ttu-id="ca60d-159">Comme pour les documents hôtes, vous pouvez définir le CSP d’un travailleur dans l’en-tête de réponse.</span><span class="sxs-lookup"><span data-stu-id="ca60d-159">As with host documents, you can set the CSP for a worker in the response header.</span></span> <span data-ttu-id="ca60d-160">Par ailleurs, le nouveau fournisseur de services cryptographiques 2 a pour `allow-scripts` `allow-same-origin` `sandbox` effet d’affecter la création de threads de travail.</span><span class="sxs-lookup"><span data-stu-id="ca60d-160">Also new in CSP 2 is that  `allow-scripts` and `allow-same-origin` flags of the `sandbox` directive now affect worker thread creation.</span></span>

3. <span data-ttu-id="ca60d-161">Scripts et styles inline: le fournisseur de services cryptographiques 2 autorise l’exécution de scripts et de blocs de style inline en fournissant des nonces et des hacheurs comme un mécanisme de création de listes de blocage.</span><span class="sxs-lookup"><span data-stu-id="ca60d-161">Inline scripts and styles: CSP 2 allows for the execution of inline scripts and style blocks by providing nonces and hashes as a whitelisting mechanism.</span></span> <span data-ttu-id="ca60d-162">Les nonces sont des valeurs de base 64 aléatoires générées lors de chaque chargement de page qui s’affiche dans la stratégie de FSC et dans les balises de script de la page.</span><span class="sxs-lookup"><span data-stu-id="ca60d-162">Nonces are random base-64 values generated on each page load that appears in both the CSP policy and in the script tags in the page.</span></span> <span data-ttu-id="ca60d-163">Lorsque la page est générée dynamiquement au chargement, le serveur génère une valeur nonce, l’insère dans le NonceToken de la page et la déclare dans l’en-tête HTTP de la stratégie de sécurité du contenu.</span><span class="sxs-lookup"><span data-stu-id="ca60d-163">When the page is dynamically generated on load, the server generates a nonce value, inserts it into the NonceToken in the page and also declares it in the Content Security Policy HTTP header.</span></span> <span data-ttu-id="ca60d-164">Les hachages sont des valeurs statiques générées (par le biais d’algorithmes *SHA256*, *SHA384* ou *SHA512* ) à partir du contenu d’un `<script>` `<style>` élément ou qui est ensuite spécifié (via `script-src` ou `style-src` directives) dans la stratégie de FSC.</span><span class="sxs-lookup"><span data-stu-id="ca60d-164">Hashes are static values generated (via *sha256*, *sha384* or *sha512* algorithms) from the content of a `<script>` or `<style>` element that are then specified (via `script-src` or `style-src` directives) in the CSP policy.</span></span>

4. <span data-ttu-id="ca60d-165">Rapport de violation des CSP: un nouvel événement, SecurityPolicyViolationEvent est désormais déclenché lors des violations du fournisseur de services cryptographiques.</span><span class="sxs-lookup"><span data-stu-id="ca60d-165">CSP violation reporting: A new event, SecurityPolicyViolationEvent is now fired upon CSP violations.</span></span> <span data-ttu-id="ca60d-166">Le mécanisme antérieur pour la création de rapports de FSC, `report-uri` continue d’être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ca60d-166">The earlier mechanism for CSP reporting, `report-uri`, continues to be supported.</span></span> <span data-ttu-id="ca60d-167">Plusieurs nouveaux champs ont été ajoutés aux rapports de violation communs aux deux, y compris `effectiveDirective` (la stratégie qui a été violée), `statusCode` (le code de réponse http) ( `sourceFile` URL de la ressource contrevenante), `lineNumber` et `columnNumber` .</span><span class="sxs-lookup"><span data-stu-id="ca60d-167">Several new fields have been added to the violation reports common to both, including `effectiveDirective` (the policy that was violated), `statusCode` (the HTTP response code), `sourceFile` (the URL of the offending resource), `lineNumber`, and `columnNumber`.</span></span>

### <span data-ttu-id="ca60d-168">Authentification Web</span><span class="sxs-lookup"><span data-stu-id="ca60d-168">Web Authentication</span></span>
<span data-ttu-id="ca60d-169">La prise en charge de Microsoft Edge pour l' [API d’authentification Web](../device/web-authentication.md) émergeant à l’aide de [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biométrique a été mise à jour avec les modifications suivantes:</span><span class="sxs-lookup"><span data-stu-id="ca60d-169">Microsoft Edge support for the emerging [Web Authentication API](../device/web-authentication.md) using [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics has been updated with the following changes:</span></span>
- <span data-ttu-id="ca60d-170">[Dans le cadre de la](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#TVSCzKDkG4jCI5mt.97) mise à jour anniversaire de Windows 10, la build 10240, 7/2016) est exposée par le biais d’API MS-préfixé (l’interface [MSCredentials](https://msdn.microsoft.com/library/mt697639) ).</span><span class="sxs-lookup"><span data-stu-id="ca60d-170">The initial implementation of the experimental Web Authentication API introduced in [EdgeHTML 14](https://blogs.windows.com/msedgedev/2016/08/04/introducing-edgehtml-14/#TVSCzKDkG4jCI5mt.97) (Windows 10 Anniversary Update, build 10240, 7/2016) was exposed through MS- prefixed APIs (the [MSCredentials](https://msdn.microsoft.com/library/mt697639) interface).</span></span> <span data-ttu-id="ca60d-171">Même si ces API sont toujours disponibles dans EdgeHTML 15, elles sont désormais déconseillées en faveur des API et des comportements non prédéfinis et prédéfinis définis dans un [instantané plus récent](https://w3.org/TR/2016/WD-webauthn-20160928) de la spécification, et sont susceptibles de continuer à changer à mesure que les spécifications arrivent à l’évolution de la normalisation.</span><span class="sxs-lookup"><span data-stu-id="ca60d-171">While these APIs are still available in EdgeHTML 15, they are now deprecated in favor of the non-prefixed, standards-based APIs and behaviors defined in a more [recent snapshot](https://w3.org/TR/2016/WD-webauthn-20160928) of the specification, and are likely to continue changing as the spec matures toward standardization.</span></span>

- <span data-ttu-id="ca60d-172">La dernière mise en œuvre de Microsoft Edge est désactivée par défaut et est fournie derrière un indicateur (tapez `about:flags` dans la barre d’adresse pour activer la fonctionnalité).</span><span class="sxs-lookup"><span data-stu-id="ca60d-172">The latest Microsoft Edge implementation is turned off by default and ships behind a flag (type `about:flags` in your address bar to turn on the feature).</span></span>

- <span data-ttu-id="ca60d-173">Microsoft Edge ne prend pas encore en charge les informations d’identification externes telles que les clés USB ou les appareils Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="ca60d-173">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="ca60d-174">L’API actuelle est limitée aux informations d’identification incorporées stockées dans le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ca60d-174">The current API is limited to embedded credentials stored in the TPM.</span></span> <span data-ttu-id="ca60d-175">Un remplacement logiciel est utilisé si la plateforme sécurisée n’est pas disponible sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ca60d-175">A software fallback is used if TPM is not available on the device.</span></span>

- <span data-ttu-id="ca60d-176">Le compte d’utilisateur Windows actuellement connecté doit être configuré de manière à prendre en charge au moins un code confidentiel, et de préférence au visage ou à l’empreinte digitale biométriques.</span><span class="sxs-lookup"><span data-stu-id="ca60d-176">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="ca60d-177">Cela permet de s’assurer que Windows peut authentifier l’accès au module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="ca60d-177">This is to ensure that Windows can authenticate the access to the TPM.</span></span>

- <span data-ttu-id="ca60d-178">Parmi les [Extensions prédéfinies](https://w3.org/TR/webauthn/#extension-predef) décrites dans la spécification, Microsoft Edge ne prend en charge que l' [AppID](https://w3.org/TR/webauthn/#extension-appid) d’une ( `webauthn_txAuthSimple` ).</span><span class="sxs-lookup"><span data-stu-id="ca60d-178">Of the [predefined extensions](https://w3.org/TR/webauthn/#extension-predef) described in the spec, Microsoft Edge only supports the [FIDO AppId](https://w3.org/TR/webauthn/#extension-appid) (`webauthn_txAuthSimple`) at this time.</span></span>

- <span data-ttu-id="ca60d-179">L' `timeoutSeconds` option n’est pas évaluée actuellement</span><span class="sxs-lookup"><span data-stu-id="ca60d-179">The `timeoutSeconds` option is not currently evaluated</span></span>

### <span data-ttu-id="ca60d-180">WebDriver</span><span class="sxs-lookup"><span data-stu-id="ca60d-180">WebDriver</span></span>

<span data-ttu-id="ca60d-181">EdgeHTML 15 apporte quelques mises à jour du service clientèle, notamment la prise en charge de l’indicateur de ligne de commande Silent et de nouveaux points de terminaison de commande:</span><span class="sxs-lookup"><span data-stu-id="ca60d-181">EdgeHTML 15 brings a handful of WebDriver updates including support for the silent command line flag and new command endpoints:</span></span>

<span data-ttu-id="ca60d-182">Méthode</span><span class="sxs-lookup"><span data-stu-id="ca60d-182">Method</span></span> | <span data-ttu-id="ca60d-183">Modèle d’URI</span><span class="sxs-lookup"><span data-stu-id="ca60d-183">URI Template</span></span> | <span data-ttu-id="ca60d-184">Commande</span><span class="sxs-lookup"><span data-stu-id="ca60d-184">Command</span></span>
:----- | :----------  | :--------
<span data-ttu-id="ca60d-185">POST</span><span class="sxs-lookup"><span data-stu-id="ca60d-185">POST</span></span> | <span data-ttu-id="ca60d-186">ID/session/{session/Alert/Accept</span><span class="sxs-lookup"><span data-stu-id="ca60d-186">/session/{session id}/alert/accept</span></span> | [<span data-ttu-id="ca60d-187">Accepter l’alerte</span><span class="sxs-lookup"><span data-stu-id="ca60d-187">Accept Alert</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-accept-alert)
<span data-ttu-id="ca60d-188">POST</span><span class="sxs-lookup"><span data-stu-id="ca60d-188">POST</span></span> | <span data-ttu-id="ca60d-189">ID/session/{session/Alert/dismiss</span><span class="sxs-lookup"><span data-stu-id="ca60d-189">/session/{session id}/alert/dismiss</span></span> | [<span data-ttu-id="ca60d-190">Ignorer l’alerte</span><span class="sxs-lookup"><span data-stu-id="ca60d-190">Dismiss Alert</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-dismiss-alert)
<span data-ttu-id="ca60d-191">GET</span><span class="sxs-lookup"><span data-stu-id="ca60d-191">GET</span></span> | <span data-ttu-id="ca60d-192">ID/session/{session/Alert/Text</span><span class="sxs-lookup"><span data-stu-id="ca60d-192">/session/{session id}/alert/text</span></span> | [<span data-ttu-id="ca60d-193">Obtenir le texte d’une alerte</span><span class="sxs-lookup"><span data-stu-id="ca60d-193">Get Alert Text</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-alert-text)
<span data-ttu-id="ca60d-194">POST</span><span class="sxs-lookup"><span data-stu-id="ca60d-194">POST</span></span> | <span data-ttu-id="ca60d-195">ID/session/{session/Alert/Text</span><span class="sxs-lookup"><span data-stu-id="ca60d-195">/session/{session id}/alert/text</span></span> | [<span data-ttu-id="ca60d-196">Envoyer un message d’alerte</span><span class="sxs-lookup"><span data-stu-id="ca60d-196">Send Alert Text</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-send-alert-text)
<span data-ttu-id="ca60d-197">POST</span><span class="sxs-lookup"><span data-stu-id="ca60d-197">POST</span></span> | <span data-ttu-id="ca60d-198">ID/session/{session/Execute/Async</span><span class="sxs-lookup"><span data-stu-id="ca60d-198">/session/{session id}/execute/async</span></span> | [<span data-ttu-id="ca60d-199">Exécuter le script Async</span><span class="sxs-lookup"><span data-stu-id="ca60d-199">Execute Async Script</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-async-script)
<span data-ttu-id="ca60d-200">POST</span><span class="sxs-lookup"><span data-stu-id="ca60d-200">POST</span></span> | <span data-ttu-id="ca60d-201">ID/session/{session/Execute/Sync</span><span class="sxs-lookup"><span data-stu-id="ca60d-201">/session/{session id}/execute/sync</span></span> | [<span data-ttu-id="ca60d-202">Exécuter le script</span><span class="sxs-lookup"><span data-stu-id="ca60d-202">Execute Script</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-execute-script)
<span data-ttu-id="ca60d-203">GET</span><span class="sxs-lookup"><span data-stu-id="ca60d-203">GET</span></span> | <span data-ttu-id="ca60d-204">ID/session/{session/Window</span><span class="sxs-lookup"><span data-stu-id="ca60d-204">/session/{session id}/window</span></span> | [<span data-ttu-id="ca60d-205">Handle de fenêtre Get</span><span class="sxs-lookup"><span data-stu-id="ca60d-205">Get Window Handle</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#get-window-handle)
<span data-ttu-id="ca60d-206">GET</span><span class="sxs-lookup"><span data-stu-id="ca60d-206">GET</span></span> | <span data-ttu-id="ca60d-207">ID/session/{session/Window/Handles</span><span class="sxs-lookup"><span data-stu-id="ca60d-207">/session/{session id}/window/handles</span></span> | [<span data-ttu-id="ca60d-208">Obtenir des poignées de fenêtre</span><span class="sxs-lookup"><span data-stu-id="ca60d-208">Get Window Handles</span></span>](https://w3c.github.io/webdriver/webdriver-spec.html#dfn-get-window-handles)

<span data-ttu-id="ca60d-209">Pour plus d’informations et l’état des autres fonctionnalités du WebDriver, voir [WebDriver](../../webdriver.md).</span><span class="sxs-lookup"><span data-stu-id="ca60d-209">For more info and the status of other WebDriver features, check out [WebDriver](../../webdriver.md).</span></span>

## <span data-ttu-id="ca60d-210">Nouvelles API dans EdgeHTML 15</span><span class="sxs-lookup"><span data-stu-id="ca60d-210">New APIs in EdgeHTML 15</span></span>

<span data-ttu-id="ca60d-211">Voici la liste complète des nouvelles API dans EdgeHTML 15.</span><span class="sxs-lookup"><span data-stu-id="ca60d-211">Here's the full list of new APIs in EdgeHTML 15.</span></span> <span data-ttu-id="ca60d-212">Ils sont répertoriés au format **[nom de l’interface]. [ nom de l’API]**.</span><span class="sxs-lookup"><span data-stu-id="ca60d-212">They are listed in the format of **[interface name].[api name]**.</span></span>

<iframe height='582' scrolling='no' title='<span data-ttu-id="ca60d-213">Nouvelles API EdgeHTML15</span><span class="sxs-lookup"><span data-stu-id="ca60d-213">New EdgeHTML15 APIs</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/evRjjZ/?height=582&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="ca60d-214">Voir le stylo <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'> nouvelles API EdgeHTML15 </a> par Microsoft Edge Docs ( <a href='http://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) sur <a href='http://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="ca60d-214">See the Pen <a href='http://codepen.io/MicrosoftEdgeDocumentation/pen/evRjjZ/'>New EdgeHTML15 APIs</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  

## <span data-ttu-id="ca60d-215">Versions précédentes de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="ca60d-215">Previous EdgeHTML releases</span></span>
[<span data-ttu-id="ca60d-216">EdgeHTML 12/Windows Build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="ca60d-216">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](https://aka.ms/devguide_edgehtml_12)

[<span data-ttu-id="ca60d-217">EdgeHTML 13/Windows Build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="ca60d-217">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](https://aka.ms/devguide_edgehtml_13)

[<span data-ttu-id="ca60d-218">EdgeHTML 14/Windows Build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="ca60d-218">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](https://aka.ms/devguide_edgehtml_14)