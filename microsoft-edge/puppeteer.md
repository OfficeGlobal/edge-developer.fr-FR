---
description: Utiliser Puppeteer pour automatiser et effectuer des tests dans Microsoft Edge
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft Edge, développement Web, développeur, outils, Automation, test
ms.openlocfilehash: a78bdc0eb96db018818ef122c772bc9023adac46
ms.sourcegitcommit: 4187d4c3fbf4ef99a3b8a63db8a182355c84c1f9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601936"
---
# Puppeteer  

[Puppeteer][|::ref1::|Main] est une bibliothèque de [nœuds][NodejsMain] qui fournit une API de haut niveau pour contrôler Microsoft Edge \ (chrome \) sur le [protocole devtools][GithubChromedevtoolsProtocol].  Puppeteer exécute [headless][WikiHeadlessBrowser] par défaut, ce qui signifie que vous ne voyez pas d’interface utilisateur et que vous devez utiliser la ligne de commande.  Vous pouvez également configurer Puppeteer pour qu’il exécute le complet \ (non-headless \) Microsoft Edge ou chrome.  

Par défaut, lorsque vous installez Puppeteer, le programme d’installation télécharge une version récente de [chrome][ChromiumHome], le navigateur open source [sur lequel Microsoft Edge est également intégré][MicrosoftBlogsWindowsExperience20181206].  S’il est installé sur votre ordinateur, vous pouvez utiliser [Puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` est une version légère d’Puppeteer qui lance une installation de navigateur existante, telle que Microsoft Edge \ (chrome \).  Pour télécharger Microsoft Edge \ (chrome \), voir [Télécharger les canaux Microsoft Edge Insider][MicrosoftedgeinsiderDownload].

## Installation de Puppeteer-Core  

Vous pouvez `puppeteer-core` l’ajouter à votre site Web ou à votre application en utilisant l’une des commandes suivantes.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Lancer Microsoft Edge avec Puppeteer-Core  

> [!NOTE]
> `puppeteer-core` repose sur le nœud v 8.9.0 ou une version ultérieure.  L’exemple ci-dessous utilise `async` / `await` qui est uniquement pris en charge dans le nœud v 7.6.0 ou version ultérieure.  Exécuté `node -v` à partir de la ligne de commande pour vérifier que vous disposez d’une version compatible de node. js.  

`puppeteer-core` Familiarisez-vous aux utilisateurs d’autres infrastructures de test de navigateur comme le contrôleurs de [disque][WebDriverEdgehtmlMain]Web.  Vous pouvez créer une instance du navigateur, ouvrir une page, puis la manipuler avec l’API Puppeteer.  Dans l’exemple de code suivant, `puppeteer-core` lance Microsoft Edge \ (chrome \), accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran sous `example.png` .  

Copiez l’exemple de code ci-dessous et enregistrez-le sous la forme `example.js` .  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

Changez `executablePath` de point pour qu’il pointe vers votre installation de Microsoft Edge \ (chrome \).  Par exemple, sur macOS, le `executablePath` Canaries pour Microsoft Edge doit être défini sur `/Applications/Microsoft\ Edge\ Canary.app/` .  Pour rechercher le `executablePath` , accédez à `edge://version` .  Cliquez sur Enregistrer pour enregistrer vos modifications.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) ne fonctionne pas `puppeteer-core` .  Pour continuer à suivre cet exemple, vous devez installer les [canaux Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] .  

Exécuté `example.js` à partir de la ligne de commande.  

```shell
node example.js
```  

`puppeteer-core` lance Microsoft Edge, accède à `https://www.microsoftedgeinsider.com` et enregistre une capture d’écran 800px x 600px de la page.  Vous pouvez personnaliser la taille de la page avec [page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Exemple de fichier. png produit par example. js":::
   Figure 1: `example.png` fichier obtenu par `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Voici un exemple simple de scénarios d’Automation et de test activés par Puppeteer et `puppeteer-core` .  Pour plus d’informations sur le fonctionnement de Puppeteer et son fonctionnement, voir [Puppeteer][|::ref2::|Main].  

## Envoyer des commentaires  

L’équipe de développement Edge est impatient d’entendre vos commentaires concernant l’utilisation de Puppeteer, `puppeteer-core` et Microsoft Edge.  Utilisez l’icône d' **envoi de commentaires** dans le Microsoft Edge devtools ou Tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] pour faire savoir à l’équipe Microsoft Edge ce que vous en pensez.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Icône de commentaires dans le Microsoft Edge DevTools":::
   Figure 2: icône de **Commentaires** dans le Microsoft Edge devtools  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "Web Driver (chrome)"  
[WebdriverEdgehtmlMain]: ./webdriver.md "WebDriver (EdgeHTML)"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Visionneuse de protocole chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: améliorer davantage le Web grâce à une collaboration plus ouverte sur le Web Blog sur l’interface Microsoft"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[ChromiumHome]: https://www.chromium.org/Home "Chrome | Projets de chrome"  

[NodejsMain]: https://nodejs.org "Node. js"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "Puppeteer et Puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "page. setViewport (fenêtre d’affichage) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-publiez un tweet | Twitter"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Navigateur headless | Wikipédia"  