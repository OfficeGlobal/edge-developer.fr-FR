---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653304"
---
# interface ICoreWebView2WebResourceResponse 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

Réponse HTTP utilisée avec l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Contenu de réponse HTTP en tant que flux.
[get_Headers](#get_headers) | En-têtes de réponse HTTP ignorés.
[get_ReasonPhrase](#get_reasonphrase) | Expression de raison de réponse HTTP.
[get_StatusCode](#get_statuscode) | Code d’état de réponse HTTP.
[put_Content](#put_content) | Définissez la propriété Content.
[put_ReasonPhrase](#put_reasonphrase) | Définissez la propriété ReasonPhrase.
[put_StatusCode](#put_statuscode) | Définissez la propriété StatusCode.

## Ses

#### get_Content 

Contenu de réponse HTTP en tant que flux.

> accès public HRESULT [get_Content](#get_content)(IStream * * content)

Le flux doit avoir toutes les données de contenu disponibles lors du report de l’événement WebResourceRequested de la réponse. Le flux doit être agile ou être créé à partir d’un thread d’arrière-plan pour empêcher l’impact sur les performances du thread d’interface utilisateur. Null signifie qu’il n’y a pas de données de contenu. La sémantique IStream s’applique (retour S_OK pour lire les appels jusqu’à ce que toutes les données soient épuisées)

#### get_Headers 

En-têtes de réponse HTTP ignorés.

> [get_Headersles](#get_headers)HRESULT publiques[(en](icorewebview2httpresponseheaders.md) -têtes * *)

#### get_ReasonPhrase 

Expression de raison de réponse HTTP.

> valeur publique HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### get_StatusCode 

Code d’état de réponse HTTP.

> valeur publique HRESULT [get_StatusCode](#get_statuscode)

#### put_Content 

Définissez la propriété Content.

> [put_Content](#put_content)par le biais du contenu public HRESULT

#### put_ReasonPhrase 

Définissez la propriété ReasonPhrase.

> [put_ReasonPhrase](#put_reasonphrase)par le biais du public HRESULT (LPCWSTR ReasonPhrase)

#### put_StatusCode 

Définissez la propriété StatusCode.

> [put_StatusCodes](#put_statuscode)par valeur HRESULT publiques (StatusCode de type ent)
