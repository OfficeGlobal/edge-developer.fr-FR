---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 11e58cbc9c2d9cba7f470344358e6f9a16dfaa97
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653545"
---
# Globales 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails) | Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée de Edge, un répertoire de données utilisateur et/ou des commutateurs de navigateur supplémentaires.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Crée un environnement WebView2 persistant à l’aide de la version latérale installée.
[GetCoreWebView2BrowserVersionInfo](#getcorewebview2browserversioninfo) | Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.
[CompareBrowserVersions](#comparebrowserversions) | Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.

## Ses

#### CreateCoreWebView2EnvironmentWithDetails 

> public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR AdditionalBrowserArguments,[ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md) * environment_created_handler)

Exportation de fichier DLL pour créer un environnement WebView2 avec une version personnalisée de Edge, un répertoire de données utilisateur et/ou des commutateurs de navigateur supplémentaires.

browserExecutableFolder est le chemin d’accès relatif au dossier qui contient le bord incorporé. Le bord intégré peut être obtenu en copiant la version nommée dossier d’une bordure installée, telle que 73.0.52.0 sous-dossier d’un bord 73.0.52.0 installé. Le dossier doit comporter msedge. exe, msedge. dll, etc. Utilisez la valeur null ou une chaîne vide pour browserExecutableFolder pour créer un WebView à l’aide de Edge installé sur l’ordinateur, auquel cas l’API tente de rechercher une version compatible de Edge installée sur l’ordinateur en fonction de la préférence de canal qui tente de rechercher la première installation par utilisateur, puis par installation par machine.

L’ordre de recherche de canal par défaut est stable, bêta, dev et Canaries. S’il existe une substitution WEBVIEW2_RELEASE_CHANNEL_PREFERENCE variable d’environnement ou une valeur de Registre releaseChannelPreference applicable ayant la valeur 1, l’ordre de recherche de canal est inversé.

userDataFolder peut être spécifié pour changer l’emplacement du dossier des données utilisateur par défaut pour WebView2. Il peut s’agir d’un chemin d’accès absolu ou d’un chemin de fichier relatif qui est interprété comme relatif au fichier exécutable du processus actuel. Dans le cas contraire, pour les applications UWP, le dossier de données utilisateur par défaut sera le dossier Data App pour le package. dans le cas des applications non UWP, le dossier de données utilisateur par défaut `{Executable File Name}.WebView2` sera créé dans le même répertoire en regard du fichier exécutable de l’application. La création de WebView2 peut échouer si le fichier exécutable s’exécute dans un répertoire dans lequel le processus n’est pas autorisé à créer un nouveau dossier. Lorsque l’application est exécutée, l’application est chargée de nettoyer son dossier de données utilisateur.

additionalBrowserArguments peut être spécifié pour modifier le comportement du WebView. Celles-ci sont transmises au processus de navigateur dans le cadre de la ligne de commande. Pour plus d’informations sur les commutateurs de ligne de commande pour les navigateurs, voir [exécuter du chrome avec des indicateurs](https://aka.ms/RunChromiumWithFlags) . Si l’application est lancée à l’aide d’un commutateur de ligne `--edge-webview-switches=xxx` de commande, la valeur de ce commutateur (xxx dans l’exemple ci-dessus) est également ajoutée à la ligne de commande du processus du navigateur. Certains commutateurs comme `--user-data-dir` les éléments internes et importants sont importants pour le WebView. Ces commutateurs seront ignorés même en cas de spécification. Si les mêmes commutateurs sont spécifiés plusieurs fois, le dernier gagne. Notez que cela s’applique également aux commutateurs comme `--enable-features` . Il n’est pas nécessaire de fusionner les différentes valeurs du même commutateur. La valeur de la ligne de commande du processus d’application est `--edge-webview-switches` traitée après le traitement du paramètre additionalBrowserArguments. Notez également que dans le cas d’un processus de navigateur, il est possible que les commutateurs s’appliquent à l’exception du premier WebView qui démarre le processus de navigateur. Si l’analyse a échoué pour les commutateurs spécifiés, elle est ignorée. `nullptr` exécute le processus de navigateur sans indicateurs.

environment_created_handler est le résultat du gestionnaire à l’opération asynchrone qui contient le WebView2Environment qui a été créé.

Les valeurs de browserExecutableFolder, userDataFolder et additionalBrowserArguments du environmentParams pourront être remplacées par les valeurs spécifiées dans les variables d’environnement ou dans le registre.

Lors de la création d’un WebView2Environment, les variables d’environnement suivantes sont activées:

```cpp
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

S’il existe une variable d’environnement de substitution, nous utilisons les valeurs browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithDetails.

Bien qu’il ne soit pas nécessaire de remplacer strictement, il existe d’autres variables d’environnement qui peuvent être définies:

```cpp
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Dans le cas d’une valeur non vide, cela indique que le WebView est démarré sous un débogueur de script. Dans ce cas, le WebView lancera une `Page.waitForDebugger` commande CDP qui entraînera l’exécution du script à l’intérieur du WebView sur le lancement, jusqu’à ce qu’un débogueur publie une `Runtime.runIfWaitingForDebugger` commande CDP correspondante pour reprendre l’exécution. Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.

```cpp
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Dans le cas d’une valeur non vide, cela signifie que l’application WebView est lancée sous un débogueur de script qui prend également en charge les applications hébergées sur plusieurs vues Web. La valeur est utilisée comme identificateur pour un canal nommé qui sera ouvert et écrit lors de la création d’un nouveau WebView par l’application hôte. La charge utile correspond à celle de la cible JSON du débogage à distance et peut être utilisée par le débogueur externe pour être attachée à une instance WebView spécifique. Le format du canal créé par le débogueur doit être `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` le suivant:

* `{app_name}` est le nom de fichier exe de l’application hôte (par exemple, WebView2Example. exe)

* `{pipe_name}` est la valeur définie pour WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Pour activer le débogage des cibles identifiées par le JSON, vous devez également définir la variable d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS à envoyer `--remote-debugging-port={port_num}` :

* `{port_num}` correspond au port sur lequel est lié le serveur CDP.

N’ayez pas à faire en sorte que la définition des variables d’environnement WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS et WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER entraîne l’affichage des webvues hébergées dans votre application et de leur contenu aux applications tierces, telles que les débogueurs.

Remarque: il n’y a pas d’équivalent de clé de registre de cette variable d’environnement.

S’il n’existe aucune de ces variables d’environnement, le Registre est examiné suivant. Les clés de Registre suivantes sont activées:

```cpp
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

Dans le cas improbable où certaines instances de WebView sont ouvertes lors d’une mise à jour de navigateur, nous pouvons dès lors bloquer la suppression de anciens navigateurs de bord. Pour éviter de manquer d’espace disque, une nouvelle création d’affichage WebView échoue avec l’erreur suivante s’il détecte qu’il existe de nombreuses versions antérieures.

```cpp
ERROR_DISK_FULL
```

Le nombre maximal de versions Edge autorisées par défaut est 20.

Il est possible d’écraser le nombre maximal de versions latérales antérieures autorisées avec la valeur de la variable d’environnement suivante.

```cpp
WEBVIEW2_MAX_INSTANCES
```

Si WebView dépend d’une périphérie installée et qu’elle est désinstallée, tout création ultérieure échoue avec l’erreur suivante

```cpp
ERROR_PRODUCT_UNINSTALLED
```

Tout d’abord, nous allons vérifier avec root, puis HKCU. AppId est d’abord défini sur l’ID de modèle utilisateur de l’application du processus de l’appelant, s’il n’y a pas de clé de Registre correspondante, l’AppId est défini sur le nom exécutable du processus de l’appelant, ou si ce n’est pas une clé de Registre, ' * '. S’il existe une clé de registre de remplacement, nous utilisons les valeurs de Registre browserExecutableFolder, userDataFolder et additionalBrowserArguments en tant que remplacement des valeurs correspondantes dans les paramètres CreateCoreWebView2EnvironmentWithDetails. Si l’une de ces valeurs de Registre n’est pas présente, le paramètre transmis à CreateCoreWebView2Environment est utilisé.

#### CreateCoreWebView2Environment 

> public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md) * environment_created_handler)

Crée un environnement WebView2 persistant à l’aide de la version latérale installée.

Cela équivaut à appeler CreateCoreWebView2EnvironmentWithDetails avec nullptr pour browserExecutableFolder, userDataFolder, additionalBrowserArguments. Pour plus d’informations, consultez CreateCoreWebView2EnvironmentWithDetails.

#### GetCoreWebView2BrowserVersionInfo 

> public STDAPI [GetCoreWebView2BrowserVersionInfo](#getcorewebview2browserversioninfo)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWStr * VERSIONINFO)

Obtenez les informations de la version du navigateur, y compris le nom du canal, s’il ne s’agit pas du canal stable ou du bord intégré.

Les noms de canaux sont Beta, dev et Canaries. S’il existe un remplacement pour le browserExecutableFolder ou l’option de canal, la substitution est utilisée. S’il n’y a pas de remplacement, le paramètre transmis à GetCoreWebView2BrowserVersionInfo est utilisé.

#### CompareBrowserVersions 

> public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int * result)

Cette méthode consiste à ce qu’il ne s’agit pas de comparer la version pour déterminer la version la plus récente, la plus ancienne ou la plus récente.

Il peut être utilisé pour déterminer s’il est possible d’utiliser webview2 ou certaines fonctionnalités de la version. Définit la valeur de result sur-1, 0 ou 1 si la valeur version1 est inférieure ou égale ou supérieure à la valeur version2 respectivement. Renvoie E_INVALIDARG s’il n’y a pas d’analyse des chaînes de version ou si aucun paramètre d’entrée n’a la valeur null. Les données d’entrée peuvent utiliser directement le versionInfo obtenu à partir de GetCoreWebView2BrowserVersionInfo, les informations de canal seront ignorées.
