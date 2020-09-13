---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Experimental
ms.openlocfilehash: 44795ab425e814054dd3d58cba585f1badfbf431
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011928"
---
# <span data-ttu-id="70cb9-104">interface ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="70cb9-104">interface ICoreWebView2Experimental</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## <span data-ttu-id="70cb9-105">Résumé</span><span class="sxs-lookup"><span data-stu-id="70cb9-105">Summary</span></span>

 <span data-ttu-id="70cb9-106">Ses</span><span class="sxs-lookup"><span data-stu-id="70cb9-106">Members</span></span>                        | <span data-ttu-id="70cb9-107">Descriptions</span><span class="sxs-lookup"><span data-stu-id="70cb9-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70cb9-108">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="70cb9-108">add_WebResourceResponseReceived</span></span>](#add_webresourceresponsereceived) | <span data-ttu-id="70cb9-109">Ajoutez un gestionnaire d’événements pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="70cb9-109">Add an event handler for the WebResourceResponseReceived event.</span></span>
[<span data-ttu-id="70cb9-110">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="70cb9-110">remove_WebResourceResponseReceived</span></span>](#remove_webresourceresponsereceived) | <span data-ttu-id="70cb9-111">Supprime le gestionnaire d’événements WebResourceResponseReceived précédemment ajouté avec add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="70cb9-111">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

## <span data-ttu-id="70cb9-112">Ses</span><span class="sxs-lookup"><span data-stu-id="70cb9-112">Members</span></span>

#### <span data-ttu-id="70cb9-113">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="70cb9-113">add_WebResourceResponseReceived</span></span> 

<span data-ttu-id="70cb9-114">Ajoutez un gestionnaire d’événements pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="70cb9-114">Add an event handler for the WebResourceResponseReceived event.</span></span>

> <span data-ttu-id="70cb9-115">[add_WebResourceResponseReceived](#add_webresourceresponsereceived)par le biais du[mot de passe](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md)</span><span class="sxs-lookup"><span data-stu-id="70cb9-115">public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="70cb9-116">L’événement WebResourceResponseReceived se déclenche après que le WebView a reçu et traité la réponse à une demande de ressource Resource.</span><span class="sxs-lookup"><span data-stu-id="70cb9-116">WebResourceResponseReceived event fires after the WebView has received and processed the response for a WebResource request.</span></span> <span data-ttu-id="70cb9-117">Les arguments d’événement incluent le WebResourceRequest envoyé par le filaire et WebResourceResponse reçu, y compris les en-têtes supplémentaires ajoutés par la pile réseau qui n’ont pas été inclus dans le cadre de l’événement WebResourceRequested associé, tels que les en-têtes d’authentification.</span><span class="sxs-lookup"><span data-stu-id="70cb9-117">The event args include the WebResourceRequest as sent by the wire and WebResourceResponse received, including any additional headers added by the network stack that were not be included as part of the associated WebResourceRequested event, such as Authentication headers.</span></span> 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### <span data-ttu-id="70cb9-118">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="70cb9-118">remove_WebResourceResponseReceived</span></span> 

<span data-ttu-id="70cb9-119">Supprime le gestionnaire d’événements WebResourceResponseReceived précédemment ajouté avec add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="70cb9-119">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

> <span data-ttu-id="70cb9-120">[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="70cb9-120">public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken token)</span></span>
