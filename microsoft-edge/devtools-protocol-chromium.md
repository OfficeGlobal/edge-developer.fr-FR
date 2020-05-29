---
description: Mise à jour du protocole Microsoft Edge DevTools
title: Mise à jour du protocole Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565500"
---
# <span data-ttu-id="e1a10-103">Protocole DevTools Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="e1a10-103">Microsoft Edge (Chromium) DevTools Protocol</span></span>

<span data-ttu-id="e1a10-104">Avec le Shift dans la plate-forme Web sous-jacente de Microsoft Edge à chrome, le [protocole devtools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ne recevra pas de nouvelles mises à jour.</span><span class="sxs-lookup"><span data-stu-id="e1a10-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) will not be receiving any further updates.</span></span> <span data-ttu-id="e1a10-105">Le protocole DevTools de Microsoft Edge (chrome) correspondra aux API du protocole chrome DevTools.</span><span class="sxs-lookup"><span data-stu-id="e1a10-105">The Microsoft Edge (Chromium) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span> 

<span data-ttu-id="e1a10-106">Vous trouverez des informations sur ces domaines et méthodes en vous référant à la [visionneuse du protocole chrome devtools](https://chromedevtools.github.io/devtools-protocol/tot/).</span><span class="sxs-lookup"><span data-stu-id="e1a10-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>

> [!NOTE]
> <span data-ttu-id="e1a10-107">Toutes les méthodes qui ont été préfixées `ms` dans le [protocole devtools de Microsoft Edge (EdgeHTML)](./devtools-protocol/index.md) ne sont plus prises en charge dans le protocole devtools Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="e1a10-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) are no longer supported in the Microsoft Edge (Chromium) DevTools Protocol.</span></span>

## <span data-ttu-id="e1a10-108">Utiliser le protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="e1a10-108">Using the DevTools Protocol</span></span>

<span data-ttu-id="e1a10-109">Voici comment joindre un client d’outillage personnalisé au serveur DevTools dans Microsoft Edge (chrome).</span><span class="sxs-lookup"><span data-stu-id="e1a10-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge (Chromium).</span></span>

1. <span data-ttu-id="e1a10-110">Assurez-vous que toutes les instances de Microsoft Edge (chrome) sont fermées.</span><span class="sxs-lookup"><span data-stu-id="e1a10-110">Ensure all instances of Microsoft Edge (Chromium) are closed.</span></span>

2. <span data-ttu-id="e1a10-111">Lancez Microsoft Edge (chrome) avec le port de débogage à distance:</span><span class="sxs-lookup"><span data-stu-id="e1a10-111">Launch Microsoft Edge (Chromium) with the remote debugging port:</span></span>

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. <span data-ttu-id="e1a10-112">Si vous le souhaitez, vous pouvez démarrer une instance séparée d’Edge à l’aide d’un profil utilisateur distinct, si vous le souhaitez:</span><span class="sxs-lookup"><span data-stu-id="e1a10-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired:</span></span>

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. <span data-ttu-id="e1a10-113">Ensuite, utilisez le `list` point de terminaison HTTP pour obtenir une liste des cibles de page pouvant être attachées:</span><span class="sxs-lookup"><span data-stu-id="e1a10-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets:</span></span>

    ```
    http://localhost:9222/json/list
    ```

5. <span data-ttu-id="e1a10-114">Enfin, connectez-vous à la `webSocketDebuggerUrl` cible souhaitée et émettez des commandes/souscrivez à des messages d’événements via le serveur de socket Web devtools.</span><span class="sxs-lookup"><span data-stu-id="e1a10-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>

## <span data-ttu-id="e1a10-115">Points de terminaison HTTPs du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="e1a10-115">DevTools Protocol HTTP Endpoints</span></span>

<span data-ttu-id="e1a10-116">Le protocole DevTools Microsoft Edge (chrome) prend en charge les points de terminaison HTTP suivants.</span><span class="sxs-lookup"><span data-stu-id="e1a10-116">The Microsoft Edge (Chromium) DevTools Protocol supports the following HTTP endpoints.</span></span>

## <span data-ttu-id="e1a10-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="e1a10-117">/json/version</span></span>
<span data-ttu-id="e1a10-118">Fournit des informations sur le navigateur de l’ordinateur hôte et la version du protocole DevTools qu’il prend en charge.</span><span class="sxs-lookup"><span data-stu-id="e1a10-118">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="e1a10-119">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-119">Parameters</span></span>**

*<span data-ttu-id="e1a10-120">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-120">None</span></span>*

**<span data-ttu-id="e1a10-121">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-121">Return object</span></span>**

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
}
```

## <span data-ttu-id="e1a10-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="e1a10-122">/json/protocol</span></span>

<span data-ttu-id="e1a10-123">Fournit la totalité de la surface de l’API de protocole sérialisée en JSON.</span><span class="sxs-lookup"><span data-stu-id="e1a10-123">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="e1a10-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-124">Parameters</span></span>**

*<span data-ttu-id="e1a10-125">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-125">None</span></span>*

**<span data-ttu-id="e1a10-126">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-126">Return object</span></span>**

<span data-ttu-id="e1a10-127">Objet JSON qui représente la surface d’API disponible pour la version actuelle du protocole.</span><span class="sxs-lookup"><span data-stu-id="e1a10-127">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="e1a10-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="e1a10-128">/json/list</span></span>

<span data-ttu-id="e1a10-129">Fournit une liste de cibles de pages pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="e1a10-129">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="e1a10-130">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-130">Parameters</span></span>**

*<span data-ttu-id="e1a10-131">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-131">None</span></span>*

**<span data-ttu-id="e1a10-132">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-132">Return object</span></span>**

```json
[{
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## <span data-ttu-id="e1a10-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="e1a10-133">/json/close</span></span>

<span data-ttu-id="e1a10-134">Ferme le processus cible (par exemple, dans Microsoft Edge (chrome), ferme l’onglet de page.)</span><span class="sxs-lookup"><span data-stu-id="e1a10-134">Closes down the target process (e.g., in Microsoft Edge (Chromium), closes the page tab.)</span></span>

**<span data-ttu-id="e1a10-135">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-135">Parameters</span></span>**

<span data-ttu-id="e1a10-136">ID cible</span><span class="sxs-lookup"><span data-stu-id="e1a10-136">Target ID</span></span> 

**<span data-ttu-id="e1a10-137">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-137">Return object</span></span>**

```
String(“Target is closing”)
```

## <span data-ttu-id="e1a10-138">Outils de contrôle à distance pour Microsoft Edge (bêta)</span><span class="sxs-lookup"><span data-stu-id="e1a10-138">Remote Tools for Microsoft Edge (Beta)</span></span>

<span data-ttu-id="e1a10-139">Vous pouvez maintenant installer les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) à partir du [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="e1a10-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span> <span data-ttu-id="e1a10-140">Cette application vous permet de déboguer à distance Microsoft Edge (chrome) exécuté sur un appareil Windows 10 à partir de votre ordinateur de développement.</span><span class="sxs-lookup"><span data-stu-id="e1a10-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>

<span data-ttu-id="e1a10-141">Pour découvrir comment configurer votre appareil Windows 10 et y accéder à partir de votre ordinateur de développement, consultez [ce didacticiel](./devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="e1a10-141">To learn how to set up your Windows 10 device and connect to it from your development machine, check out [this tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span></span>

<span data-ttu-id="e1a10-142">Les [outils de contrôle à distance de Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) utilisent le même protocole devtools Microsoft Edge (chrome) que le [devtools](./devtools-guide-chromium.md) pour communiquer avec Microsoft Edge exécuté sur l’appareil Windows 10 que vous voulez déboguer.</span><span class="sxs-lookup"><span data-stu-id="e1a10-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](./devtools-guide-chromium.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span> <span data-ttu-id="e1a10-143">Cette application vient tout juste `/msedge/` d’être un ID de processus ( `pid` ) avant chaque appel au protocole.</span><span class="sxs-lookup"><span data-stu-id="e1a10-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span> <span data-ttu-id="e1a10-144">Il prend en charge les points de terminaison HTTP suivants.</span><span class="sxs-lookup"><span data-stu-id="e1a10-144">It supports the following HTTP endpoints.</span></span>

### <span data-ttu-id="e1a10-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="e1a10-145">/msedge/json/list</span></span>

<span data-ttu-id="e1a10-146">Fournit une liste de tous les `msedge.exe` processus (y compris les onglets [PWAS](./progressive-web-apps-chromium/index.md) et All dans toutes les instances de Microsoft Edge) sur l’appareil Windows 10 pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="e1a10-146">Provides a candidate list of all `msedge.exe` processes (including [PWAs](./progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge) on the Windows 10 device for debugging.</span></span>

**<span data-ttu-id="e1a10-147">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-147">Parameters</span></span>**

*<span data-ttu-id="e1a10-148">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-148">None</span></span>*

**<span data-ttu-id="e1a10-149">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-149">Return object</span></span>**

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, … ]
```

### <span data-ttu-id="e1a10-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="e1a10-150">/msedge/</span></span>

<span data-ttu-id="e1a10-151">Équivalent de la fonction [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="e1a10-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span> 

### <span data-ttu-id="e1a10-152">/msedge/[PID]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="e1a10-152">/msedge/[pid]/json/list</span></span>

<span data-ttu-id="e1a10-153">Fournit une liste de cibles de pages pour l’instance Microsoft Edge qui correspond à la fournie `[pid]` pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="e1a10-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>

**<span data-ttu-id="e1a10-154">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-154">Parameters</span></span>**

*<span data-ttu-id="e1a10-155">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-155">None</span></span>*

**<span data-ttu-id="e1a10-156">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-156">Return object</span></span>**

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, … ]
```

### <span data-ttu-id="e1a10-157">/msedge/[PID]/JSON/version</span><span class="sxs-lookup"><span data-stu-id="e1a10-157">/msedge/[pid]/json/version</span></span>

<span data-ttu-id="e1a10-158">Fournit des informations sur l’instance Microsoft Edge qui correspond à la `[pid]` version fournie et la version du protocole devtools prise en charge.</span><span class="sxs-lookup"><span data-stu-id="e1a10-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="e1a10-159">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-159">Parameters</span></span>**

*<span data-ttu-id="e1a10-160">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-160">None</span></span>*

**<span data-ttu-id="e1a10-161">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-161">Return object</span></span>**

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```

### <span data-ttu-id="e1a10-162">/msedge/[PID]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="e1a10-162">/msedge/[pid]/json/protocol/</span></span>

<span data-ttu-id="e1a10-163">Fournit la totalité de la surface de l’API de protocole sérialisée en JSON pour l’instance Microsoft Edge correspondant au fourni `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="e1a10-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>

**<span data-ttu-id="e1a10-164">Parameters</span><span class="sxs-lookup"><span data-stu-id="e1a10-164">Parameters</span></span>**

*<span data-ttu-id="e1a10-165">None</span><span class="sxs-lookup"><span data-stu-id="e1a10-165">None</span></span>*

**<span data-ttu-id="e1a10-166">Objet renvoyé</span><span class="sxs-lookup"><span data-stu-id="e1a10-166">Return object</span></span>**

<span data-ttu-id="e1a10-167">Objet JSON qui représente la surface d’API disponible pour la version du protocole utilisée par l’instance Microsoft Edge correspondant à la fournie `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="e1a10-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>