---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653530"
---
# interface ICoreWebView2Deferral 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Cette interface est utilisée pour effectuer des reports sur des arguments d’événement qui prennent en charge l’affichage des reports via leur méthode GetDeferral.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Complete](#complete) | Termine l’événement différé associé.

## Ses

#### Complete 

Termine l’événement différé associé.

> valeur publique HRESULT [achevée](#complete)()

Complète doit être appelé une seule fois pour chaque Report.
