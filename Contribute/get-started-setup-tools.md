---
title: 安裝內容撰寫工具
description: 本文可協助您下載與安裝使用 Git 與編輯 Markdown 檔案所需的用戶端工具。
author: jasonwhowell
ms.author: jasonh
manager: kfile
ms.date: 04/30/2018
ms.openlocfilehash: 9f22a416810711c076645a9483f022112a3a7642
ms.sourcegitcommit: 886ca76086a302d1d6124967df12a5bcfe4fd4b5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/10/2018
ms.locfileid: "40251444"
---
# <a name="install-content-authoring-tools"></a>安裝內容撰寫工具

本文說明以互動方式安裝 Git 用戶端工具和 Visual Studio Code 的步驟。
> [!div class="checklist"]
> * 安裝 [Git](https://git-scm.com/)
> * 安裝 [Visual Studio Code](https://code.visualstudio.com/)
> * 安裝 [Docs 編寫套件](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) \(英文\)

>[!IMPORTANT]
> 若只是要對文章進行很少量的變更，*不*需要完成此文章中的步驟，而可繼續直接進入[快速變更工作流程](index.md#quick-edits-to-existing-documents)。
>
> 我們建議主要參與者完成這些步驟，因為這可讓您使用[主要/長期變更工作流程](how-to-write-workflows-major.md)。 即使您在主要存放庫中具有寫入權限，仍然*強烈建議您 (且此指南假設您會) 對存放庫進行派生和複製*，這樣您會具有在分支中儲存所建議變更的讀取/寫入權限。

## <a name="install-git-client-tools"></a>安裝 Git 用戶端工具 

 安裝適用於您平台的 [Software Freedom Conservancy 的 Git 用戶端工具](https://git-scm.com/download/)最新版本。 

* [適用於 Windows 的 Git](https://git-scm.com/download/win)。 安裝包含了 Git 版本控制系統和 Git Bash，您可以使用此命令列應用程式來與本機 Git 存放庫互動。
* 適用於 Mac 的 Git 是隨著 Xcode 命令列工具提供。 只要從命令列執行 `git`。 系統將會提示您視需要安裝該命令列工具。 您也可以從 Software Freedom Conservancy 下載[適用於 Mac 的 Git](https://git-scm.com/download/mac)。
* [適用於 Linux 與 Unix 的 Git](https://git-scm.com/download/linux)

如果您較偏好圖形化使用者介面 (GUI) 而非命令列介面 (CLI)，請參閱 [Software Freedom Conservancy 的可用 GUI 用戶端頁面](https://git-scm.com/downloads/guis) \(英文\)、[GitHub 的 GitHub 電腦版](https://desktop.github.com/)+ \(英文\)，或 [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) \(英文\) 以取得一些較受歡迎的選項。

請遵循您所選擇用戶端的指示，以進行安裝與設定。

在下一篇文章中，您將[設定本機 Git 存放庫](get-started-setup-local.md)。

   其他的 Git 資源可在此處取得：[Git 術語](https://help.github.com/articles/github-glossary) | [Git 基本概念](https://git-scm.com/book/en/v2/Getting-Started-Git-Basics) | [學習 Git 與 GitHub](https://help.github.com/articles/good-resources-for-learning-git-and-github/)

## <a name="understand-markdown-editors"></a>了解 Markdown 編輯器

Markdown 是一種容易閱讀及學習的輕量型標記語言。 因此，它快速地成為業界標準。 若要以 Markdown 撰寫文章，建議您先下載並安裝 Markdown 編輯器。  [Visual Studio Code](https://code.visualstudio.com/) 是 Microsoft 用來編輯 Markdown 的偏好工具。 [Atom](https://atom.io) 是另一個用來編輯 Markdown 的熱門工具。

Markdown 文字會儲存到副檔名為 .md 的檔案中。

關於如何使用 Markdown 撰寫的其他詳細資料，包括 Markdown 基本概念及 OPS 自訂 Markdown 擴充功能所支援的功能，都會在稍後的[如何使用 Markdown](how-to-write-use-markdown.md) 文章中涵蓋。

## <a name="visual-studio-code"></a>Visual Studio Code

[Visual Studio Code](https://code.visualstudio.com/) 也稱為 VS Code，是一種輕量型編輯器，適用於 Windows、Linux 和 Mac。 它包含 Git 整合，並支援擴充功能。

下載並安裝 [VS Code](https://code.visualstudio.com/)。 VS Code 首頁應該會正確地偵測到您的作業系統。

- [Windows](https://code.visualstudio.com/docs/setup/windows)
- [Mac](https://code.visualstudio.com/docs/setup/mac)
- [Linux](https://code.visualstudio.com/docs/setup/linux)

> [!TIP]
> 若要啟動 VS Code 並開啟目前的資料夾，請在命令列或 bash 殼層中執行 `code .` 命令。 如果目前的資料夾為本機 Git 存放庫的一部分，則 Github 整合會自動在 Visual Studio Code 中顯示。

## <a name="docs-authoring-pack"></a>Docs 編寫套件
安裝適用於 Visual Studio Code 的 Docs 編寫套件。 此延伸模組集包括撰寫 Markdown 時的基本編寫協助，以及可讓您能以 docs.microsoft.com 網站的樣式查看 Markdown 外觀的預覽功能。

   請造訪此[市集頁面](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) \(英文\) 並選取 [Install] \(安裝\)，或在 VS Code 視窗的延伸模組清單中搜尋 `docsmsft.docs-authoring-pack`。 

   Docs 編寫套件可透過在 VS Code 內按 Alt+M 來存取。 工具列預設會隱藏，但可以顯示它。 編輯 VS Code 設定 (Control+逗號) 並新增使用者設定 `"markdown.showToolbar": true` 以顯示工具列。

   如需詳細資訊，請參閱 [Docs 編寫套件](how-to-write-docs-auth-pack.md)頁面。


## <a name="next-steps"></a>後續步驟

現在您已準備好[設定本機 Git 存放庫](get-started-setup-local.md)。
