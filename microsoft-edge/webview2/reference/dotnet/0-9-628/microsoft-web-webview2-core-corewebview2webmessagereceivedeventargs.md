---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: ab273337307eeef6e8842d337296756877939aff
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011852"
---
# <span data-ttu-id="cc270-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cc270-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="cc270-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cc270-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cc270-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="cc270-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cc270-107">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="cc270-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="cc270-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="cc270-108">Summary</span></span>

 <span data-ttu-id="cc270-109">Ses</span><span class="sxs-lookup"><span data-stu-id="cc270-109">Members</span></span>                        | <span data-ttu-id="cc270-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cc270-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cc270-111">Source</span><span class="sxs-lookup"><span data-stu-id="cc270-111">Source</span></span>](#source) | <span data-ttu-id="cc270-112">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="cc270-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="cc270-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="cc270-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="cc270-114">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="cc270-114">The message posted from the WebView content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="cc270-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="cc270-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="cc270-116">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="cc270-116">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="cc270-117">Ses</span><span class="sxs-lookup"><span data-stu-id="cc270-117">Members</span></span>

#### <span data-ttu-id="cc270-118">Source</span><span class="sxs-lookup"><span data-stu-id="cc270-118">Source</span></span> 

<span data-ttu-id="cc270-119">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="cc270-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="cc270-120">[source](#source) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="cc270-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="cc270-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="cc270-121">WebMessageAsJson</span></span> 

<span data-ttu-id="cc270-122">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="cc270-122">The message posted from the WebView content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="cc270-123">[WebMessageAsJson](#webmessageasjson) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="cc270-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="cc270-124">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cc270-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="cc270-125">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="cc270-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="cc270-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="cc270-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="cc270-127">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="cc270-127">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="cc270-128">chaîne publique [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="cc270-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="cc270-129">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="cc270-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="cc270-130">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="cc270-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="cc270-131">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="cc270-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```
