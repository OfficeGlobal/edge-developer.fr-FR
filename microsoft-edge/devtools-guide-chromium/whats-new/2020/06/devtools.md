---
title: Nouveautés de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7b0193d25fb1d081e5746ec1271ca7b9f4e60c23
ms.sourcegitcommit: ad5eb43172280974b8c063867c2097f7c5c0e77d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/27/2020
ms.locfileid: "10898263"
---
# <span data-ttu-id="01c08-103">Nouveautés de DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="01c08-103">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <span data-ttu-id="01c08-104">Annonces de l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="01c08-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="01c08-105">Les sections suivantes répertorient les annonces que vous pouvez avoir manquées dans l’équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="01c08-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="01c08-106">Consultez les annonces pour essayer de nouvelles fonctionnalités dans les extensions de code DevTools, VS, etc.</span><span class="sxs-lookup"><span data-stu-id="01c08-106">See the announcements to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="01c08-107">Pour rester à jour sur les fonctionnalités les plus récentes de vos outils de développement, téléchargez les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] et [suivez l’équipe Microsoft Edge devtools sur Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="01c08-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="01c08-108">Fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="01c08-108">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="01c08-110">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="01c08-110">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-111">L’équipe Microsoft Edge DevTools collabore avec les membres de l’équipe chrome DevTools et de la communauté de chrome pour ajouter de nouvelles fonctionnalités de débogage de grille CSS à DevTools.</span><span class="sxs-lookup"><span data-stu-id="01c08-111">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="01c08-112">Vous pouvez désormais afficher les numéros des lignes de la grille, les espaces de la grille et les quadrillages étendus en tant que superposition sur la page.</span><span class="sxs-lookup"><span data-stu-id="01c08-112">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="01c08-113">De plus, d’autres améliorations apportées aux outils de grille seront bientôt possibles.</span><span class="sxs-lookup"><span data-stu-id="01c08-113">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Fonctionnalités de débogage de grille CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="01c08-115">Fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="01c08-115">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="01c08-116">Pour activer l’expérience, voir [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer de nouvelles fonctionnalités de débogage de grille CSS**.</span><span class="sxs-lookup"><span data-stu-id="01c08-116">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="01c08-117">Pour tester l’expérience à l’aide d’un exemple, voir [exemple de planificateur de grille CSS][CodepenRachelweilYzwBzKM].</span><span class="sxs-lookup"><span data-stu-id="01c08-117">To try out the experiment with a sample, see [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="01c08-118">[#1047356][CR1047356] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-118">Chromium issue [#1047356][CR1047356]</span></span>  

### <span data-ttu-id="01c08-119">Modification et lecture de requêtes avec la console réseau</span><span class="sxs-lookup"><span data-stu-id="01c08-119">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="01c08-121">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="01c08-121">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-122">Vous pouvez désormais utiliser les requêtes **modification et lecture** dans le [Journal du réseau][DevtoolsNetworkIndexLogActivity] à l’aide de la **console réseau**.</span><span class="sxs-lookup"><span data-stu-id="01c08-122">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Modification et lecture d’une demande dans le NetworkLog avec la console réseau" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="01c08-124">Modification et lecture d’une demande dans le [NetworkLog][DevtoolsNetworkIndexLogActivity] avec la **console réseau**</span><span class="sxs-lookup"><span data-stu-id="01c08-124">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-125">Un nouveau panneau, la **console réseau** s’ouvre dans le [tiroir devtools][DevtoolsCustomizeIndexDrawer] et remplit automatiquement les informations pour la requête http.</span><span class="sxs-lookup"><span data-stu-id="01c08-125">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="01c08-126">Pour afficher la réponse renvoyée par le serveur, modifiez-la si nécessaire, puis sélectionnez **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="01c08-126">To see the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="01c08-127">Vous pouvez également utiliser la **console réseau** pour créer et envoyer des demandes http directement à partir du devtools.</span><span class="sxs-lookup"><span data-stu-id="01c08-127">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panneau de la console réseau" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="01c08-129">Panneau de la **console réseau**</span><span class="sxs-lookup"><span data-stu-id="01c08-129">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="01c08-130">Pour afficher la **console réseau** dans le volet principal \ (en haut de la fenêtre) au lieu du [tiroir devtools][DevtoolsCustomizeIndexDrawer], voir [déplacement d’outils entre les panneaux](#move-tools-between-panels).</span><span class="sxs-lookup"><span data-stu-id="01c08-130">To see **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], see [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="01c08-131">Pour activer l’expérience, voir [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer la console réseau**.</span><span class="sxs-lookup"><span data-stu-id="01c08-131">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="01c08-132">Ouvrez le [Journal du réseau][DevtoolsNetworkIndexLogActivity], ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier puis relire**.</span><span class="sxs-lookup"><span data-stu-id="01c08-132">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and select **Edit and Replay**.</span></span>  

<span data-ttu-id="01c08-133">[#1093687][CR1093687] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-133">Chromium issue [#1093687][CR1093687]</span></span>  

### <span data-ttu-id="01c08-134">Événements de respondWith du travailleur de service sous l’onglet Minutage</span><span class="sxs-lookup"><span data-stu-id="01c08-134">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="01c08-135">L’onglet **minutage** du panneau **réseau** comporte désormais des `respondWith` événements de travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="01c08-135">The **Timing** tab of the **Network** panel now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="01c08-136">L' `respondWith` événement de travailleur de service affiche la durée du temps immédiatement avant que le `fetch` Gestionnaire d’événements du travailleur de service démarre, au moment où la `respondWith` promesse du `fetch` gestionnaire est finalisée.</span><span class="sxs-lookup"><span data-stu-id="01c08-136">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Événement du travailleur de service respondWith dans l’onglet Minutage du panneau réseau" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="01c08-138">`respondWith`Événement du travailleur de service sous l’onglet **minutage** du panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="01c08-138">The `respondWith` service worker event in the **Timing** tab of the **Network** panel</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-139">Développez **Response received** pour afficher d’autres informations de la `fetch` réponse comme `CacheStorageCacheName` , `serviceWorkerResponseSource` et `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="01c08-139">Expand **Response received** to see additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Développer la réponse reçue pour afficher des informations supplémentaires dans la réponse de récupération" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="01c08-141">Développer la **réponse reçue** pour afficher des informations supplémentaires dans la `fetch` réponse</span><span class="sxs-lookup"><span data-stu-id="01c08-141">Expand **Response received** to see additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-142">[#1066579][CR1066579] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-142">Chromium issue [#1066579][CR1066579]</span></span>  

### <span data-ttu-id="01c08-143">Commentaires de webhint dans le volet problèmes</span><span class="sxs-lookup"><span data-stu-id="01c08-143">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="01c08-145">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="01c08-145">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-146">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l’accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, PWAS, ainsi que d’autres problèmes courants liés au développement Web sur les sites Web.</span><span class="sxs-lookup"><span data-stu-id="01c08-146">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="01c08-147">Vous pouvez à présent afficher des commentaires sur le webhint dans le volet [problèmes][DevtoolsIssues] .</span><span class="sxs-lookup"><span data-stu-id="01c08-147">You are now able to see webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="01c08-149">Commentaires de webhint dans le volet problèmes</span><span class="sxs-lookup"><span data-stu-id="01c08-149">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="01c08-150">Pour activer l’expérience, voir [activation des fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis activez la case à cocher en regard de **activer webhint**.</span><span class="sxs-lookup"><span data-stu-id="01c08-150">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="01c08-151">Ouvrez le volet [problèmes][DevtoolsIssues] pour afficher les commentaires du webhint.</span><span class="sxs-lookup"><span data-stu-id="01c08-151">Open the [Issues][DevtoolsIssues] panel to see feedback from webhint.</span></span>  

<span data-ttu-id="01c08-152">[#1070378][CR1070378] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-152">Chromium issue [#1070378][CR1070378]</span></span>  

### <span data-ttu-id="01c08-153">Déplacer des outils entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="01c08-153">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalités expérimentales":::
   <span data-ttu-id="01c08-155">Fonctionnalités expérimentales</span><span class="sxs-lookup"><span data-stu-id="01c08-155">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-156">En règle générale, il est possible d’ouvrir des outils tels que des **éléments** et un **réseau** uniquement dans le panneau principal \ (Top \) de devtools.</span><span class="sxs-lookup"><span data-stu-id="01c08-156">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="01c08-157">De même, il est possible d’ouvrir des outils tels que la vue et les **problèmes** en **3D** uniquement dans le panneau tiroir \ (en bas) de devtools.</span><span class="sxs-lookup"><span data-stu-id="01c08-157">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="01c08-158">Vous pouvez désormais personnaliser votre disposition DevTools en déplaçant des outils entre les volets supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="01c08-158">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="01c08-160">Déplacement d’un onglet entre les panneaux</span><span class="sxs-lookup"><span data-stu-id="01c08-160">Moving tabs between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="01c08-161">Pour activer l’expérience, voir [activer les fonctionnalités expérimentales][DevtoolsExperimentalFeaturesTurnOn] , puis cochez la case **en regard de permettre la prise en charge du déplacement des onglets entre les volets**.</span><span class="sxs-lookup"><span data-stu-id="01c08-161">To enable the experiment, see [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="01c08-162">[#897944][CR897944] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-162">Chromium issue [#897944][CR897944]</span></span>  

### <span data-ttu-id="01c08-163">Info-bulle améliorée de l’initiateur dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="01c08-163">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="01c08-164">Dans Microsoft Edge 83 et 84, les info-bulles de la colonne Initiator, qui indique la cause de la demande de ressource, dans le [Journal de réseau][DevtoolsNetworkIndexLogActivity] affiché avec une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="01c08-164">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="01c08-165">Vous pouvez uniquement afficher la pile d’appels à l’origine de la demande en effectuant un défilement horizontal dans l’info-bulle.</span><span class="sxs-lookup"><span data-stu-id="01c08-165">You were only able to see the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="Info-bulle de l’initiateur dans Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="01c08-167">Info-bulle de l’initiateur dans Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="01c08-167">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-168">À partir de Microsoft Edge 85, vous pouvez maintenant voir la pile d’appels d’initiateur dans l’info-bulle sans faire défiler l’affichage horizontalement.</span><span class="sxs-lookup"><span data-stu-id="01c08-168">Starting with Microsoft Edge 85, you are now able to see the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="Info-bulle de l’initiateur dans Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="01c08-170">Info-bulle de l’initiateur dans Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="01c08-170">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="01c08-171">[#1069404][CR1069404] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-171">Chromium issue [#1069404][CR1069404]</span></span>  

## <span data-ttu-id="01c08-172">Annonces du projet de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-172">Announcements from the Chromium project</span></span>  

<span data-ttu-id="01c08-173">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 85 qui ont été fournies au projet de chrome Open source.</span><span class="sxs-lookup"><span data-stu-id="01c08-173">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="01c08-174">Modification de styles pour les infrastructures CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="01c08-174">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="01c08-175">Le volet **styles** dispose désormais d’une meilleure prise en charge de l’édition des styles qui ont été créés avec les API [CSSOM (CSS Object Model)][CsswgDraftsCssom] .</span><span class="sxs-lookup"><span data-stu-id="01c08-175">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="01c08-176">De nombreux infrastructures et bibliothèques CSS-in-JS utilisent les API CSSOM du capot pour créer des styles.</span><span class="sxs-lookup"><span data-stu-id="01c08-176">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="01c08-177">Vous pouvez à présent modifier les styles ajoutés en JavaScript à l’aide de [feuilles de style de construction][WicgConstructStylesheet].</span><span class="sxs-lookup"><span data-stu-id="01c08-177">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="01c08-178">Les feuilles de style construites constituent un nouveau moyen de créer et de répartir des styles réutilisables lors de l’utilisation de l' [ombre DOM][MdnShadowDom].</span><span class="sxs-lookup"><span data-stu-id="01c08-178">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="01c08-179">Par exemple, les `h1` styles ajoutés avec `CSSStyleSheet` \ (API CSSOM \) ne sont pas modifiables auparavant.</span><span class="sxs-lookup"><span data-stu-id="01c08-179">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="01c08-180">Les styles sont désormais modifiables dans le volet **styles** .</span><span class="sxs-lookup"><span data-stu-id="01c08-180">The styles are editable now in the **Styles** pane.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Modification de la propriété Background des styles H1 ajoutés avec CSSStyleSheet de rose à LightBlue égale" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="01c08-182">Modification `background` de la propriété des `h1` styles ajoutés à `CSSStyleSheet` partir de `pink` à `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="01c08-182">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="01c08-183">Pour ce faire, utilisez un [exemple qui utilise CSS-in-js][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="01c08-183">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="01c08-184">[#946975][CR946975] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-184">Chromium issue [#946975][CR946975]</span></span>  

### <span data-ttu-id="01c08-185">Panneau de signalisation 6</span><span class="sxs-lookup"><span data-stu-id="01c08-185">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="01c08-186">Le panneau de **signalisation** est désormais exécuté sur le phare 6.</span><span class="sxs-lookup"><span data-stu-id="01c08-186">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="01c08-187">Pour obtenir la liste complète des modifications, voir [notes de publication pour v 6.0.0][GithubGoogleChromeLighthouse600].</span><span class="sxs-lookup"><span data-stu-id="01c08-187">For a full list of all changes, see [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="01c08-188">Le phare 6,0 introduit trois nouvelles mesures pour le rapport: le plus grand nombre de contenus (LCP \), le décalage de la disposition cumulé \ (CLS \) et le temps de blocage total \ (TBT \).</span><span class="sxs-lookup"><span data-stu-id="01c08-188">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="01c08-189">La formule d’indice de performance a également été pondérée pour mieux refléter l’expérience de chargement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="01c08-189">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="01c08-190">[#772558][CR772558] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-190">Chromium issue [#772558][CR772558]</span></span>  

#### <span data-ttu-id="01c08-191">Première dépréciation significative de Paint</span><span class="sxs-lookup"><span data-stu-id="01c08-191">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="01c08-192">Tout d’abord, Paint (FMP \) est déconseillé dans la couleur de la 6,0.</span><span class="sxs-lookup"><span data-stu-id="01c08-192">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="01c08-193">Le FMP a également été supprimé du panneau **performances** .</span><span class="sxs-lookup"><span data-stu-id="01c08-193">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="01c08-194">Le **plus grand** nombre de peintures est le remplacement recommandé pour le logiciel FMP.</span><span class="sxs-lookup"><span data-stu-id="01c08-194">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--See [First Meaningful Paint][WebDevFirstMeaningfulPaint] for an explanation of why it was deprecated.  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="01c08-195">[#1096008][CR1096008] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-195">Chromium issue [#1096008][CR1096008]</span></span>  

### <span data-ttu-id="01c08-196">Prise en charge des nouvelles fonctionnalités JavaScript</span><span class="sxs-lookup"><span data-stu-id="01c08-196">Support for new JavaScript features</span></span>  

<span data-ttu-id="01c08-197">DevTools possède désormais une meilleure prise en charge de certaines des fonctionnalités de langage JavaScript les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="01c08-197">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="01c08-198">Saisie semi-automatique de syntaxe de [chaînage facultative][V8DevOptionalChaining]</span><span class="sxs-lookup"><span data-stu-id="01c08-198">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="01c08-199">La saisie semi-automatique de propriété dans la **console** prend désormais en charge la syntaxe de chaînage facultative, par exemple, `name?.` fonctionne désormais en plus de `name.` et `name[` .</span><span class="sxs-lookup"><span data-stu-id="01c08-199">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="01c08-200">Mise en surbrillance de syntaxe pour les [champs privés][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="01c08-200">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="01c08-201">la syntaxe des champs de classe privée est désormais correcte, mise en évidence et à l’impression dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="01c08-201">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="01c08-202">Mise en surbrillance de syntaxe pour l' [opérateur de fusion Null][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="01c08-202">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="01c08-203">DevTools est désormais correctement à l’impression de l’opérateur de fusion Null dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="01c08-203">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="01c08-204">Problèmes de chrome [#1073903][CR1073903], [#1083214][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="01c08-204">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <span data-ttu-id="01c08-205">Avertissements relatifs aux nouveaux raccourcis d’application dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="01c08-205">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="01c08-206">Les **raccourcis d’application** permettent aux utilisateurs de démarrer rapidement des tâches courantes ou recommandées au sein d’une application Web.</span><span class="sxs-lookup"><span data-stu-id="01c08-206">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="01c08-207">Le volet **manifeste** affiche désormais des avertissements pour les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="01c08-207">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="01c08-208">Les icônes de raccourci de l’application sont inférieures à 96 x 96 pixels</span><span class="sxs-lookup"><span data-stu-id="01c08-208">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="01c08-209">Les icônes de raccourci de l’application et les icônes du manifeste ne sont pas carrées \ (dans la mesure où les icônes sont ignorées \)</span><span class="sxs-lookup"><span data-stu-id="01c08-209">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avertissements relatifs aux raccourcis d’application" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="01c08-211">Avertissements relatifs aux raccourcis d’application</span><span class="sxs-lookup"><span data-stu-id="01c08-211">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-212">[#955497][CR955497] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-212">Chromium issue [#955497][CR955497]</span></span>  

### <span data-ttu-id="01c08-213">Affichage cohérent du volet calculé</span><span class="sxs-lookup"><span data-stu-id="01c08-213">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="01c08-214">Le volet **calculé** dans le panneau des **éléments** s’affiche désormais comme un volet dans toutes les tailles de fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="01c08-214">The **Computed** pane in the **Elements** panel now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="01c08-215">Auparavant, le volet **calculé** fusionné à l’intérieur du volet **styles** lorsque la largeur de la fenêtre d’affichage de devtools était étroite.</span><span class="sxs-lookup"><span data-stu-id="01c08-215">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Le volet calculé s’affiche de façon cohérente sous forme de volet distinct même lorsque le DevTools est étroit." lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="01c08-217">Le volet **calculé** s’affiche de façon cohérente sous forme de volet distinct même lorsque le devtools est étroit.</span><span class="sxs-lookup"><span data-stu-id="01c08-217">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="01c08-218">[#1073899][CR1073899] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-218">Chromium issue [#1073899][CR1073899]</span></span>  

### <span data-ttu-id="01c08-219">Décalages du bytecode pour les fichiers webassembly</span><span class="sxs-lookup"><span data-stu-id="01c08-219">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="01c08-220">DevTools utilise désormais les décalages du bytecode pour afficher les numéros de ligne de l’WASM de démontage.</span><span class="sxs-lookup"><span data-stu-id="01c08-220">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="01c08-221">Les numéros de ligne permettent de clarifier le fait que vous examinez les données binaires et qu’ils se conservent de manière plus cohérente sur la manière dont WASM Runtime référence les emplacements.</span><span class="sxs-lookup"><span data-stu-id="01c08-221">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="01c08-222">[#1071432][CR1071432] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-222">Chromium issue [#1071432][CR1071432]</span></span>  

### <span data-ttu-id="01c08-223">Copies par ligne et couper dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="01c08-223">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="01c08-224">Lorsque vous effectuez une opération de copie ou de coupe sans sélection dans l' [éditeur du panneau sources][DevtoolsSourcesEditCssJavascript], devtools copie ou coupe la ligne de contenu actuelle.</span><span class="sxs-lookup"><span data-stu-id="01c08-224">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Lorsque le curseur se trouve à la fin de la ligne 5, en copiant l’ensemble de la ligne à partir de pen.js dans le DevTools et en la collant dans le code VS" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="01c08-226">Le curseur étant placé à la fin de la ligne 5, copiez l’ensemble de la ligne à partir de **pen.js** dans le devtools et collez-la dans le [code vs][VSCode].</span><span class="sxs-lookup"><span data-stu-id="01c08-226">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [VS Code][VSCode].</span></span>
:::image-end:::  

<span data-ttu-id="01c08-227">[#800028][CR800028] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-227">Chromium issue [#800028][CR800028]</span></span>

### <span data-ttu-id="01c08-228">Mises à jour des paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="01c08-228">Console Settings updates</span></span>  

#### <span data-ttu-id="01c08-229">Dissocier les mêmes messages de console</span><span class="sxs-lookup"><span data-stu-id="01c08-229">Ungroup same console messages</span></span>  

<span data-ttu-id="01c08-230">Le bouton bascule **similaire** dans les paramètres de la console s’applique désormais aux messages en double.</span><span class="sxs-lookup"><span data-stu-id="01c08-230">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="01c08-231">Auparavant, il vient d’être appliqué à des messages similaires.</span><span class="sxs-lookup"><span data-stu-id="01c08-231">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="01c08-232">Par exemple, auparavant, DevTools n’a pas dissocier les `hello` messages même si le **groupe similaire** n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="01c08-232">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="01c08-233">Les `hello` messages sont désormais dissociés.</span><span class="sxs-lookup"><span data-stu-id="01c08-233">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Lorsque le groupe similaire n’est pas activé, les messages Hello ne sont pas regroupés" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="01c08-235">Lorsque le **groupe similaire** est désactivé, les `hello` messages ne sont pas regroupés.</span><span class="sxs-lookup"><span data-stu-id="01c08-235">When **Group similar** is unchecked, the `hello` messages are ungrouped.</span></span>
:::image-end:::  

<span data-ttu-id="01c08-236">[Pour ce faire, utilisez un exemple qui envoie des messages en double à la console][CodepenZoherghadyaliZyrjgdJ].</span><span class="sxs-lookup"><span data-stu-id="01c08-236">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="01c08-237">[#1082963][CR1082963] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-237">Chromium issue [#1082963][CR1082963]</span></span>  

### <span data-ttu-id="01c08-238">Conservation des paramètres de contexte sélectionnés uniquement</span><span class="sxs-lookup"><span data-stu-id="01c08-238">Persisting Selected context only settings</span></span>  

<span data-ttu-id="01c08-239">Les paramètres de **contexte sélectionnés uniquement** dans les paramètres de la console sont désormais conservés.</span><span class="sxs-lookup"><span data-stu-id="01c08-239">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="01c08-240">Auparavant, les paramètres étaient réinitialisés chaque fois que vous avez fermé et rouvert DevTools.</span><span class="sxs-lookup"><span data-stu-id="01c08-240">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="01c08-241">La modification fait en sorte que le comportement de la configuration soit cohérent avec d’autres options de paramètres de la console.</span><span class="sxs-lookup"><span data-stu-id="01c08-241">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Paramètre de contexte sélectionné uniquement" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="01c08-243">Paramètre de **contexte sélectionné uniquement**</span><span class="sxs-lookup"><span data-stu-id="01c08-243">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-244">[#1055875][CR1055875] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-244">Chromium issue [#1055875][CR1055875]</span></span>  

### <span data-ttu-id="01c08-245">Mises à jour du panneau de performance</span><span class="sxs-lookup"><span data-stu-id="01c08-245">Performance panel updates</span></span>  

#### <span data-ttu-id="01c08-246">Informations du cache de compilation JavaScript dans le panneau performances</span><span class="sxs-lookup"><span data-stu-id="01c08-246">JavaScript compilation cache information in Performance panel</span></span>  

<span data-ttu-id="01c08-247">Les [informations du cache de compilation JavaScript][V8DevCodeCaching] sont désormais toujours affichées sous l’onglet Résumé du panneau performance.</span><span class="sxs-lookup"><span data-stu-id="01c08-247">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the Summary tab of the Performance panel.</span></span>  <span data-ttu-id="01c08-248">Auparavant, DevTools n’affichait aucune information liée à la mise en cache du code si la mise en cache du code ne s’est pas produit.</span><span class="sxs-lookup"><span data-stu-id="01c08-248">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informations du cache de compilation JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="01c08-250">Informations du cache de compilation JavaScript</span><span class="sxs-lookup"><span data-stu-id="01c08-250">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-251">[#912581][CR912581] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-251">Chromium issue [#912581][CR912581]</span></span>  

#### <span data-ttu-id="01c08-252">Alignement du minutage de la navigation dans le panneau performance</span><span class="sxs-lookup"><span data-stu-id="01c08-252">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="01c08-253">Panneau **performance** permettant de montrer les heures dans les règles en fonction de la date de début de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="01c08-253">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="01c08-254">Le minutage est désormais modifié pour les enregistrements dans lesquels l’utilisateur navigue, où DevTools affiche désormais les heures de règle relatives à la navigation à la place.</span><span class="sxs-lookup"><span data-stu-id="01c08-254">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Aligner le minutage de la navigation dans le panneau performances" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="01c08-256">Aligner le minutage de la navigation dans le panneau **performances**</span><span class="sxs-lookup"><span data-stu-id="01c08-256">Align navigation timing in **Performance** panel</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-257">Les heures pour `DOMContentLoaded` , première peinture, première image de dessin, et les événements de peinture volumineux le plus volumineux sont mis à jour de manière à être par rapport au début de la navigation, ce qui signifie que le minutage correspond au minutage indiqué par `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="01c08-257">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="01c08-258">[#974550][CR974550] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-258">Chromium issue [#974550][CR974550]</span></span>  

### <span data-ttu-id="01c08-259">Nouvelles icônes pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints</span><span class="sxs-lookup"><span data-stu-id="01c08-259">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="01c08-260">Le panneau **sources** comporte de nouvelles conceptions pour les points d’arrêt, les points d’arrêt conditionnel et la logpoints.</span><span class="sxs-lookup"><span data-stu-id="01c08-260">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="01c08-261">Les points d’arrêt sont représentés par un cercle rouge, comme le [code vs][VSCode] et [Visual Studio][VS].</span><span class="sxs-lookup"><span data-stu-id="01c08-261">Breakpoints are represented by a red circle, just like [VS Code][VSCode] and [Visual Studio][VS].</span></span>  <span data-ttu-id="01c08-262">Des icônes sont ajoutées pour différencier les points d’arrêt conditionnels et logpoints.</span><span class="sxs-lookup"><span data-stu-id="01c08-262">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Points d’arrêt" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="01c08-264">Points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="01c08-264">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="01c08-265">[#1041830][CR1041830] problème de chrome</span><span class="sxs-lookup"><span data-stu-id="01c08-265">Chromium issue [#1041830][CR1041830]</span></span>  

## <span data-ttu-id="01c08-266">Télécharger les canaux Microsoft Edge preview</span><span class="sxs-lookup"><span data-stu-id="01c08-266">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="01c08-267">Si vous utilisez Windows ou macOS, envisagez d’utiliser les [canaux Microsoft Edge Preview][MicrosoftEdgePreviewChannels] comme navigateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="01c08-267">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="01c08-268">Les canaux d’aperçu vous permettent d’accéder aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="01c08-268">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="01c08-269">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="01c08-269">Getting in touch with Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="01c08-270">Utilisez les options suivantes pour discuter des nouvelles fonctionnalités et modifications du billet, ou tout autre sujet lié à DevTools.</span><span class="sxs-lookup"><span data-stu-id="01c08-270">Use the following options to discuss the new features and changes in the post, or anything else related to DevTools.</span></span>  

* <span data-ttu-id="01c08-271">Envoyez vos commentaires à l’aide de l’icône de **Commentaires** dans le devtools</span><span class="sxs-lookup"><span data-stu-id="01c08-271">Send your feedback using the **Feedback** icon in the DevTools</span></span>  
* <span data-ttu-id="01c08-272">Tweeter sur [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="01c08-272">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
* <span data-ttu-id="01c08-273">Envoyez une suggestion au [site Web de votre choix][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="01c08-273">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
* <span data-ttu-id="01c08-274">Classer les bogues sur cette page dans le référentiel [Edge-développeurs][GitHubMicrosoftDocsEdgeDeveloperNewIssue]</span><span class="sxs-lookup"><span data-stu-id="01c08-274">File bugs on this page in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

:::image type="complex" source="../../media/2020/05/feedback-icon.msft.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools" lightbox="../../media/2020/05/feedback-icon.msft.png":::
  <span data-ttu-id="01c08-276">Icône de **Commentaires** dans le Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="01c08-276">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Tiroir-personnaliser Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctionnalités expérimentales-fonctionnalités expérimentales | Documents Microsoft"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Présentation de la modification du panneau CSS et JavaScript-sources | Documents Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journalisation de l’activité du réseau-Inspectez l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Modification de styles pour les infrastructures CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Envoyer des messages en double à la console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemple de planificateur de grille CSS | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bugs du chrome"  

[CR772558]: https://crbug.com/772558 "DevTools: mise à jour vers la dernière version de phare | Bugs du chrome"  
[CR800028]: https://crbug.com/800028 "Le raccourci de ligne dupliqué dans l’éditeur des outils de développeur ne fonctionne pas après la mise à jour de chrome | Bugs du chrome"  
[CR912581]: https://crbug.com/912581 "Exposez les scripts dont le code a été mis en cache par V8 dans DevTools/à propos de. Bugs du chrome"  
[CR946975]: https://crbug.com/946975 "L’encadré styles DevTools ne fonctionne pas avec les feuilles de style construites | Bugs du chrome"  
[CR955497]: https://crbug.com/955497 "Menu contextuel de l’icône d’application pour PWAs | Bugs du chrome"  
[CR974550]: https://crbug.com/974550 "Incompatibilité métrique entre le panneau perf et performanceObserver | Bugs du chrome"  
[CR1041830]: https://crbug.com/1041830 "Amélioration des couleurs pour les points d’arrêt | Bugs du chrome"  
[CR1055875]: https://crbug.com/1055875 "La valeur du paramètre de console de contexte sélectionné ne persiste pas après la fermeture et la réouverture des outils de développement | Bugs du chrome"  
[CR1066579]: https://crbug.com/1066579 "DevTools: afficher ServiceWorkers de récupération de la chronologie par requête dans le panneau réseau | Bugs du chrome"  
[CR1071432]: https://crbug.com/1071432 "WASM Basic Basic Developer Bugs du chrome"  
[CR1073899]: https://crbug.com/1073899 "L’onglet style calculé disparaît en mode réactif | Bugs du chrome"  
[CR1073903]: https://crbug.com/1073903 "DevTools: la surbrillance de syntaxe ne fonctionne pas avec les champs privés | Bugs du chrome"  
[CR1082963]: https://crbug.com/1082963 "Impossible de désactiver le comportement des messages similaires du groupe de la console | Bugs du chrome"  
[CR1083214]: https://crbug.com/1083214 "Acorn ne prend pas en charge le chaînage facultatif. Bugs du chrome"  
[CR1083797]: https://crbug.com/1083797 "Impression incorrecte pour une fusion nulle Bugs du chrome"  
[CR1096008]: https://crbug.com/1096008 "Supprimer le FMP | Bugs du chrome"  
[CR1047356]: https://crbug.com/1047356 "Outils CSS Grid/Flexbox/tableau | Bugs du chrome"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil permettant de créer et de relire des demandes de réseau synthétique Bugs du chrome"  
[CR1070378]: https://crbug.com/1070378 "Intégration de webhint dans DevTools | Bugs du chrome"  
[CR1069404]: https://crbug.com/1069404 "[Outils de développement] les fenêtres contextuelles de widgets sont trop étroites | Bugs du chrome"  
[CR897944]: https://crbug.com/897944 "Panneaux devtool déplaçables | Bugs du chrome"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v 6.0.0-GoogleChrome/phare | GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème-MicrosoftDocs/Edge-développeur"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Utilisation de l’ombre DOM | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canaux Microsoft Edge preview"  

[VS]: https://visualstudio.microsoft.com/ "Visual Studio"
[VSCode]: https://code.visualstudio.com/ "Code Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modèle d’objet CSS (CSSOM) | Brouillons de l’éditeur de groupe de travail CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publiez un tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privée-champs de classe publique et privée | V8. Développeur"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Mise en cache de code pour les développeurs JavaScript | V8. Développeur"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "Fusion par zéro | V8. Développeur"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Chaînage facultatif | V8. Développeur"  

[WebhintMain]: https://webhint.io "Astuce"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objets StyleSheet de construction | CG"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Le site Web de votre choix"  

> [!NOTE]
> <span data-ttu-id="01c08-325">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="01c08-325">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="01c08-326">La page d’origine est disponible [ici](https://developers.google.com/web/updates/2020/06/devtools/index) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).</span><span class="sxs-lookup"><span data-stu-id="01c08-326">The original page is found [here](https://developers.google.com/web/updates/2020/06/devtools/index) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="01c08-328">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="01c08-328">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  