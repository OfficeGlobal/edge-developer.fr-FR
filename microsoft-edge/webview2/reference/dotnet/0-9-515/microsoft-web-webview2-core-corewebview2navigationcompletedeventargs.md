---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2a18fe9f8f79a109047d029affab8d84a6ef845c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653272"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Arguments d’événement pour l’événement NavigationCompleted.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Propriétés IsSuccess](#issuccess) | True lorsque la navigation est réussie.
[NavigationId](#navigationid) | ID de la navigation.
[WebErrorStatus](#weberrorstatus) | Code d’erreur en cas d’échec de la navigation.

## Ses

#### Propriétés IsSuccess 

True lorsque la navigation est réussie.

> public bool [Propriétés IsSuccess](#issuccess)

Il s’agit de la valeur false pour une navigation qui s’est produite dans une page d’erreur (échecs en raison d’un réseau, échec de recherche DNS, serveur HTTP répond avec 4xx), mais peut également avoir la valeur false pour des éléments supplémentaires tels que Window. Stop () appelé sur la page de navigation.

#### NavigationId 

ID de la navigation.

> public ulong [NavigationId](#navigationid)

#### WebErrorStatus 

Code d’erreur en cas d’échec de la navigation.

> public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)
