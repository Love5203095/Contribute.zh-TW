---
title: 適用於 Visual Studio Code 的 Docs 編寫套件
description: 本文說明 Visual Studio Code 延伸模組套件，以協助針對 docs.microsoft.com 編寫 Markdown。
ms.topic: contributor-guide
ms.prod: non-product-specific
ms.custom: external-contributor-guide
author: meganbradley
ms.author: mbradley
ms.date: 03/05/2020
ms.openlocfilehash: 5bbf51af52069d5636715ffb2bd3f59bf459d5b9
ms.sourcegitcommit: cfba5ad25b898bfed76046126ce8ff4871910701
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2020
ms.locfileid: "78336412"
---
# <a name="docs-authoring-pack-for-vs-code"></a><span data-ttu-id="52a3e-103">適用於 VS Code 的 Docs 編寫套件</span><span class="sxs-lookup"><span data-stu-id="52a3e-103">Docs Authoring Pack for VS Code</span></span>

<span data-ttu-id="52a3e-104">Docs 編寫套件是 VS Code 延伸模組的集合，有助於 docs.microsoft.com 的 Markdown 編寫。</span><span class="sxs-lookup"><span data-stu-id="52a3e-104">The Docs Authoring Pack is a collection of VS Code extensions to aid with Markdown authoring for docs.microsoft.com.</span></span> <span data-ttu-id="52a3e-105">此套件[可在 VS Code Marketplace 中取得](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack)，且包含下列延伸模組：</span><span class="sxs-lookup"><span data-stu-id="52a3e-105">The pack is [available in the VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-authoring-pack) and contains the following extensions:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="52a3e-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)：為 docs.microsoft.com (Docs) 內容提供 Markdown 撰寫協助，包括基本 Markdown 支援以及對 Docs 中自訂 Markdown 語法的支援，例如：警示、程式碼片段、不可當地語系化的文字。</span><span class="sxs-lookup"><span data-stu-id="52a3e-106">[Docs Markdown](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown): Provides Markdown authoring assistance for docs.microsoft.com (Docs) content, including basic Markdown support and support for custom Markdown syntax in Docs, such as alerts, code snippets, and non-localizable text.</span></span> <span data-ttu-id="52a3e-107">現在也包含一些基本的 YAML 編寫協助，例如插入目錄項目。</span><span class="sxs-lookup"><span data-stu-id="52a3e-107">Now also includes some basic YAML authoring assistance, such as inserting TOC entries.</span></span>
> * <span data-ttu-id="52a3e-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)：David Anson 提供的熱門 Markdown Linter，可協助確保您的 Markdown 有效。</span><span class="sxs-lookup"><span data-stu-id="52a3e-108">[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): A popular Markdown linter by David Anson to help make sure your Markdown is valid.</span></span>
> * <span data-ttu-id="52a3e-109">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) (拼字檢查工具)：由 Street Side Software 開發的完整離線拼字檢查工具。</span><span class="sxs-lookup"><span data-stu-id="52a3e-109">[Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker): A fully offline spell checker by Street Side Software.</span></span>
> * <span data-ttu-id="52a3e-110">[Docs 預覽](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview)：使用 docs.microsoft.com CSS 來取得更精確的 Markdown 預覽，包括自訂 Markdown。</span><span class="sxs-lookup"><span data-stu-id="52a3e-110">[Docs Preview](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-preview): Uses the docs.microsoft.com CSS for more accurate Markdown preview, including custom Markdown.</span></span>
> * <span data-ttu-id="52a3e-111">[Docs 文章範本](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates)：可讓使用者建構學習模組，套用 Markdown 骨架內容到新檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-111">[Docs Article Templates](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-article-templates): Allows users to scaffold Learn modules and apply Markdown skeleton content to new files.</span></span>
> * <span data-ttu-id="52a3e-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml)：提供 Docs YAML 架構驗證和自動完成。</span><span class="sxs-lookup"><span data-stu-id="52a3e-112">[Docs YAML](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-yaml): Provides Docs YAML schema validation and auto-complete.</span></span>
> * <span data-ttu-id="52a3e-113">[Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images)：提供資料夾和個別檔案的影像壓縮和調整大小，以協助 docs.microsoft.com 的作者。</span><span class="sxs-lookup"><span data-stu-id="52a3e-113">[Docs Images](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-images): Provides image compression and resizing for folders and individual files to help authors of docs.microsoft.com.</span></span>

## <a name="prerequisites-and-assumptions"></a><span data-ttu-id="52a3e-114">必要條件與假設</span><span class="sxs-lookup"><span data-stu-id="52a3e-114">Prerequisites and assumptions</span></span>

<span data-ttu-id="52a3e-115">若要使用 Docs Markdown 延伸模組插入相關連結、影像與其他內嵌內容，您必須將 VS Code 工作區的範圍設為已複製之開放式發佈系統 (OPS) 存放庫的根目錄。</span><span class="sxs-lookup"><span data-stu-id="52a3e-115">To insert relative links, images, and other embedded content with the Docs Markdown extension, you must have your VS Code workspace scoped to the root of your cloned Open Publishing System (OPS) repo.</span></span> <span data-ttu-id="52a3e-116">例如，如果您已將 Docs 存放庫複製到 `C:\git\SomeDocsRepo\`，請在 VS Code 中開啟該資料夾或子資料夾：[檔案]  >  [開啟資料夾] 功能表，或從命令列輸入 `code C:\git\SomeDocsRepo\`。</span><span class="sxs-lookup"><span data-stu-id="52a3e-116">For example, if you have cloned the docs repository to `C:\git\SomeDocsRepo\`, then open that folder or a subfolder in VS Code: **File** > **Open Folder** menu,  or `code C:\git\SomeDocsRepo\` from the command line.</span></span>

<span data-ttu-id="52a3e-117">延伸模組支援的某些語法 (例如警示和程式碼片段) 是 OPS 的自訂 Markdown。</span><span class="sxs-lookup"><span data-stu-id="52a3e-117">Some syntax supported by the extension, such as alerts and snippets, are custom Markdown for OPS.</span></span> <span data-ttu-id="52a3e-118">除非透過 OPS 發佈，否則無法正確轉譯自訂 Markdown。</span><span class="sxs-lookup"><span data-stu-id="52a3e-118">Custom Markdown will not render correctly unless published via OPS.</span></span>

## <a name="how-to-use-the-docs-markdown-extension"></a><span data-ttu-id="52a3e-119">如何使用 Docs Markdown 延伸模組</span><span class="sxs-lookup"><span data-stu-id="52a3e-119">How to use the Docs Markdown extension</span></span>

<span data-ttu-id="52a3e-120">若要存取 [Docs Markdown] 功能表，輸入 <kbd>ALT+M</kbd>。</span><span class="sxs-lookup"><span data-stu-id="52a3e-120">To access the **Docs Markdown** menu, type <kbd>ALT+M</kbd>.</span></span> <span data-ttu-id="52a3e-121">您可以按一下或使用向上鍵/向下鍵來選取您想要的命令。</span><span class="sxs-lookup"><span data-stu-id="52a3e-121">You can click or use the up and down arrows to select the command you want.</span></span> <span data-ttu-id="52a3e-122">或者，您可以輸入篩選條件開始進行篩選，然後當所需函式在功能表中反白顯示時，點擊 <kbd>ENTER</kbd>。</span><span class="sxs-lookup"><span data-stu-id="52a3e-122">Or you can type to start filtering, then hit <kbd>ENTER</kbd> when the function you want is highlighted in the menu.</span></span>

<span data-ttu-id="52a3e-123">如需最新命令的清單，請參閱 [Docs Markdown 讀我檔案](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown)。</span><span class="sxs-lookup"><span data-stu-id="52a3e-123">See the [Docs Markdown readme](https://marketplace.visualstudio.com/items?itemName=docsmsft.docs-markdown) for an up-to-date list of commands.</span></span>

## <a name="how-to-generate-a-master-redirect-file"></a><span data-ttu-id="52a3e-124">如何產生主要重新導向檔案</span><span class="sxs-lookup"><span data-stu-id="52a3e-124">How to generate a master redirect file</span></span>

<span data-ttu-id="52a3e-125">Docs Markdown 延伸模組包含一個指令碼，可根據個別檔案中的 `redirect_url` 中繼資料，產生或更新存放庫的主要重新導向檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-125">The Docs Markdown extension includes a script to generate or update a master redirection file for a repo, based on the `redirect_url` metadata in individual files.</span></span> <span data-ttu-id="52a3e-126">此指令碼會檢查存放庫內每個 Markdown 檔案中的 `redirect_url`，將重新導向中繼資料新增至存放庫的主要重新導向檔案 (.openpublishing.redirection.json)，並將重新導向後的檔案移至存放庫外的資料夾。</span><span class="sxs-lookup"><span data-stu-id="52a3e-126">This script checks every Markdown file in the repo for `redirect_url`, adds the redirection metadata to the master redirection file (*.openpublishing.redirection.json*) for the repo, and moves the redirected files to a folder outside the repo.</span></span> <span data-ttu-id="52a3e-127">執行指令碼：</span><span class="sxs-lookup"><span data-stu-id="52a3e-127">To run the script:</span></span>

1. <span data-ttu-id="52a3e-128">選取 <kbd>F1</kbd> 以開啟 VS Code 命令選擇區。</span><span class="sxs-lookup"><span data-stu-id="52a3e-128">Select <kbd>F1</kbd> to open the VS Code command palette.</span></span>
2. <span data-ttu-id="52a3e-129">開始輸入 "Docs:Generate..."</span><span class="sxs-lookup"><span data-stu-id="52a3e-129">Start typing "Docs: Generate..."</span></span>
3. <span data-ttu-id="52a3e-130">選取 `Docs: Generate master redirection file` 命令。</span><span class="sxs-lookup"><span data-stu-id="52a3e-130">Select the command `Docs: Generate master redirection file`.</span></span>
4. <span data-ttu-id="52a3e-131">當指令碼完成執行時，重新導向結果會顯示在 VS Code 的輸出窗格中，而被移除的 Markdown 檔案將會新增至預設路徑底下的 Docs Authoring\redirects 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="52a3e-131">When the script finishes running, the redirection results will show in the VS Code output pane, and the removed Markdown files will be added to the Docs Authoring\redirects folder under your default path.</span></span>
5. <span data-ttu-id="52a3e-132">檢閱結果。</span><span class="sxs-lookup"><span data-stu-id="52a3e-132">Review the results.</span></span> <span data-ttu-id="52a3e-133">如果結果如預期，請提交提取要求以更新存放庫。</span><span class="sxs-lookup"><span data-stu-id="52a3e-133">If they are as expected, submit a pull request to update the repo.</span></span>

## <a name="how-to-assign-keyboard-shortcuts"></a><span data-ttu-id="52a3e-134">如何指派鍵盤快速鍵</span><span class="sxs-lookup"><span data-stu-id="52a3e-134">How to assign keyboard shortcuts</span></span>

1. <span data-ttu-id="52a3e-135">按 <kbd>CTRL+K</kbd> 然後按 <kbd>Ctrl+S</kbd> 開啟 [鍵盤快速鍵] 清單。</span><span class="sxs-lookup"><span data-stu-id="52a3e-135">Type <kbd>CTRL+K</kbd> then <kbd>Ctrl+S</kbd> to open the **Keyboard Shortcuts** list.</span></span>
1. <span data-ttu-id="52a3e-136">搜尋您要建立自訂按鍵繫結關係的命令，例如 `formatBold`。</span><span class="sxs-lookup"><span data-stu-id="52a3e-136">Search for the command, such as `formatBold`, for which you want to create a custom key binding.</span></span>
1. <span data-ttu-id="52a3e-137">按一下當您將滑鼠移至該行上時，顯示在命令名稱附近的加號。</span><span class="sxs-lookup"><span data-stu-id="52a3e-137">Click the plus that appears near the command name when you mouse over the line.</span></span>
1. <span data-ttu-id="52a3e-138">看到新的輸入方塊之後，請鍵入您要連結至該特定命令的鍵盤快速鍵。</span><span class="sxs-lookup"><span data-stu-id="52a3e-138">After a new input box is visible, type the keyboard shortcut you want to bind to that particular command.</span></span> <span data-ttu-id="52a3e-139">例如，若要使用粗體的常用快速鍵，請按 <kbd>Ctrl+B</kbd>。</span><span class="sxs-lookup"><span data-stu-id="52a3e-139">For example, to use the common shortcut for bold, type <kbd>Ctrl+B</kbd>.</span></span>
1. <span data-ttu-id="52a3e-140">最好是將 `when` 子句插入按鍵繫結關係中，使其無法用於 Markdown 之外的檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-140">It's a good idea to insert a `when` clause into your key binding, so it won't be available in files other than Markdown.</span></span> <span data-ttu-id="52a3e-141">若要執行此作業，請開啟 *keybindings.json*，並在命令名稱下面插入下行 (務必在各行之間新增逗號)：</span><span class="sxs-lookup"><span data-stu-id="52a3e-141">To do this, open *keybindings.json* and insert the following line below the command name (be sure to add a comma between lines):</span></span>

    `"when": "editorTextFocus && editorLangId == 'markdown'"`

    <span data-ttu-id="52a3e-142">您在 keybindings.json 中完成的自訂按鍵繫結關係應如下所示：</span><span class="sxs-lookup"><span data-stu-id="52a3e-142">Your completed custom key binding should look like this in *keybindings.json*:</span></span>

    ```json
    [
        {
            "key": "ctrl+b",
            "command": "formatBold",
            "when": "editorTextFocus && editorLangId == 'markdown'"
        }
    ]
    ```

    > [!TIP]
    > <span data-ttu-id="52a3e-143">將您的按鍵繫結關係放在此檔案中以覆寫預設值</span><span class="sxs-lookup"><span data-stu-id="52a3e-143">Place your key bindings in this file to overwrite the defaults</span></span>

1. <span data-ttu-id="52a3e-144">儲存 keybindings.json。</span><span class="sxs-lookup"><span data-stu-id="52a3e-144">Save *keybindings.json*.</span></span>

<span data-ttu-id="52a3e-145">如需按鍵繫結關係的詳細資訊，請參閱 [VS Code 文件](https://code.visualstudio.com/docs/getstarted/keybindings)。</span><span class="sxs-lookup"><span data-stu-id="52a3e-145">For more information on key bindings, see the [VS Code docs](https://code.visualstudio.com/docs/getstarted/keybindings).</span></span>

## <a name="how-to-show-the-legacy-gauntlet-toolbar"></a><span data-ttu-id="52a3e-146">如何顯示舊版 "Gauntlet" 工具列</span><span class="sxs-lookup"><span data-stu-id="52a3e-146">How to show the legacy "Gauntlet" toolbar</span></span>

<span data-ttu-id="52a3e-147">"Gauntlet" 延伸模組程式碼的先前使用者將會注意到，安裝 Docs Markdown 延伸模組後，編寫工具列不再顯示於 VS Code 視窗的底端。</span><span class="sxs-lookup"><span data-stu-id="52a3e-147">Former users of the extension code-named "Gauntlet" will notice that the authoring toolbar no longer appears at the bottom of the VS Code window when the Docs Markdown Extension is installed.</span></span> <span data-ttu-id="52a3e-148">這是因為該工具列在 VS Code 狀態列上佔用了大量空間，且未遵循延伸模組 UX 的最佳做法，所以在新的延伸模組中已淘汰使用。</span><span class="sxs-lookup"><span data-stu-id="52a3e-148">This is because the toolbar took up a large space on the VS Code status bar and did not follow best practices for extension UX, so it is deprecated in the new extension.</span></span> <span data-ttu-id="52a3e-149">不過，您可以更新 VS Code 的 settings.json 檔案，以便選擇性地顯示工具列，如下所示：</span><span class="sxs-lookup"><span data-stu-id="52a3e-149">However, you can optionally show the toolbar by updating your VS Code settings.json file as follows:</span></span>

1. <span data-ttu-id="52a3e-150">在 VS Code 中，移至 [檔案]  >  [喜好設定]  >  [設定]，或選取<kbd>Ctrl+,</kbd>。</span><span class="sxs-lookup"><span data-stu-id="52a3e-150">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="52a3e-151">選取 [使用者設定] 以變更所有 VS Code 工作區的設定，或選取 [工作區設定] 只變更目前工作區的設定。</span><span class="sxs-lookup"><span data-stu-id="52a3e-151">Select **User Settings** to change the settings for all VS Code workspaces or **Workspace Settings** to change them for just the current workspace.</span></span>
1. <span data-ttu-id="52a3e-152">選取 [延伸模組]  >  [Docs Markdown 延伸模組設定]，然後選取 [在底部狀態列中顯示舊版工具列]。</span><span class="sxs-lookup"><span data-stu-id="52a3e-152">Select **Extensions** > **Docs Markdown Extension Configuration**, and then select **Show the legacy toolbar in the bottom status bar**.</span></span>

   ![VS Code 中顯示舊版工具列設定](docs-authoring/media/show-gauntlet-bar.png)

<span data-ttu-id="52a3e-154">完成選取之後，VS Code 會更新 settings.json 檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-154">Once you've made your selection, VS Code updates the *settings.json* file.</span></span> <span data-ttu-id="52a3e-155">系統會提示您重新載入視窗，讓變更生效。</span><span class="sxs-lookup"><span data-stu-id="52a3e-155">You will then be prompted to reload the window for the changes to take effect.</span></span>

<span data-ttu-id="52a3e-156">延伸模組新增加的較新命令將無法從工具列取得。</span><span class="sxs-lookup"><span data-stu-id="52a3e-156">Newer commands added to the extension will not be available from the toolbar.</span></span>

## <a name="how-to-use-docs-templates"></a><span data-ttu-id="52a3e-157">如何使用文件範本</span><span class="sxs-lookup"><span data-stu-id="52a3e-157">How to use Docs templates</span></span>

<span data-ttu-id="52a3e-158">Docs Article Templates (文件文章範本) 延伸模組可讓 VS Code 中的作者從中央存放庫提取 Markdown 範本並將它套用到檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-158">The Docs Article Templates extension lets writers in VS Code pull a Markdown template from a centralized store and apply it to a file.</span></span> <span data-ttu-id="52a3e-159">範本可以協助確保文章中包含必要中繼資料，以及遵循內容標準等等。</span><span class="sxs-lookup"><span data-stu-id="52a3e-159">Templates can help ensure that required metadata is included in articles, that content standards are followed, and so on.</span></span> <span data-ttu-id="52a3e-160">範本是在 GitHub 存放庫中以 Markdown 檔案方式管理。</span><span class="sxs-lookup"><span data-stu-id="52a3e-160">Templates are managed as Markdown files in a public GitHub repository.</span></span>

### <a name="to-apply-a-template-in-vs-code"></a><span data-ttu-id="52a3e-161">在 VS Code 中套用範本</span><span class="sxs-lookup"><span data-stu-id="52a3e-161">To apply a template in VS Code</span></span>

1. <span data-ttu-id="52a3e-162">請確定已安裝並啟用 Docs 文章範本延伸模組。</span><span class="sxs-lookup"><span data-stu-id="52a3e-162">Ensure the Docs Article Templates extension is installed and enabled.</span></span>
1. <span data-ttu-id="52a3e-163">若您沒有安裝 Docs Markdown 延伸模組，按 <kbd>F1</kbd> 開啟命令選擇區，開始輸入 "template" 以進行篩選，然後按一下 `Docs: Template`。</span><span class="sxs-lookup"><span data-stu-id="52a3e-163">If you don't have the Docs Markdown extension installed, click <kbd>F1</kbd> to open the command palette, start typing "template" to filter, then click `Docs: Template`.</span></span> <span data-ttu-id="52a3e-164">若您已安裝 Docs Markdown，您可以使用命令選擇區或按 <kbd>Alt+M</kbd> 以帶出 Docs Markdown QuickPick 功能表，然後從清單中選取 `Template`。</span><span class="sxs-lookup"><span data-stu-id="52a3e-164">If you do have Docs Markdown installed, you can use either the command palette or click <kbd>Alt+M</kbd> to bring up the Docs Markdown QuickPick menu, then select `Template` from the list.</span></span>
1. <span data-ttu-id="52a3e-165">從出現的清單中選取想要的範本。</span><span class="sxs-lookup"><span data-stu-id="52a3e-165">Select the desired template from the list that appears.</span></span>

### <a name="to-add-your-github-id-andor-microsoft-alias-to-your-vs-code-settings"></a><span data-ttu-id="52a3e-166">將您的 GitHub ID 和/或 Microsoft 別名新增到您的 VS Code 設定</span><span class="sxs-lookup"><span data-stu-id="52a3e-166">To add your GitHub ID and/or Microsoft alias to your VS Code settings</span></span>

<span data-ttu-id="52a3e-167">Templates (範本) 延伸模組支援三種動態中繼資料欄位：作者、ms.author 與 ms.date。</span><span class="sxs-lookup"><span data-stu-id="52a3e-167">The Templates extension supports three dynamic metadata fields: author, ms.author, and ms.date.</span></span> <span data-ttu-id="52a3e-168">這表示若範本建立者在 Markdown 範本的中繼資料標頭中使用這些欄位，當您套用此範本時，系統將會在您的檔案中自動填入，如下所示：</span><span class="sxs-lookup"><span data-stu-id="52a3e-168">That means that if a template creator uses these fields in the metadata header of a Markdown template, they will be auto-populated in your file when you apply the template, as follows:</span></span>

| <span data-ttu-id="52a3e-169">中繼資料欄位</span><span class="sxs-lookup"><span data-stu-id="52a3e-169">Metadata field</span></span> | <span data-ttu-id="52a3e-170">值</span><span class="sxs-lookup"><span data-stu-id="52a3e-170">Value</span></span> |
|--|--|
| `author` | <span data-ttu-id="52a3e-171">您的 GitHub 別名 (若已在您的 VS Code 設定檔中指定)。</span><span class="sxs-lookup"><span data-stu-id="52a3e-171">Your GitHub alias, if specified in your VS Code settings file.</span></span> |
| `ms.author` | <span data-ttu-id="52a3e-172">您的 GitHub 識別碼 (若已在您的 VS Code 設定檔中指定)。</span><span class="sxs-lookup"><span data-stu-id="52a3e-172">Your Microsoft alias, if specified in your VS Code settings file.</span></span> <span data-ttu-id="52a3e-173">若您不是 Microsoft 員工，請不要指定。</span><span class="sxs-lookup"><span data-stu-id="52a3e-173">If you are not a Microsoft employee, leave unspecified.</span></span> |
| `ms.date` | <span data-ttu-id="52a3e-174">目前日期，為Docs 支援的格式 `MM/DD/YYYY`。</span><span class="sxs-lookup"><span data-stu-id="52a3e-174">The current date in the Docs-supported format, `MM/DD/YYYY`.</span></span> <span data-ttu-id="52a3e-175">如果您之後更新檔案，日期不會自動更新，您必須手動更新。</span><span class="sxs-lookup"><span data-stu-id="52a3e-175">The date is not automatically updated if you subsequently update the file - you must update it manually.</span></span> <span data-ttu-id="52a3e-176">這個欄位是用來表達「文章的時效性」。</span><span class="sxs-lookup"><span data-stu-id="52a3e-176">This field is used to indicate the "article freshness".</span></span> |

### <a name="to-set-author-andor-msauthor"></a><span data-ttu-id="52a3e-177">設定作者和/或 ms.author</span><span class="sxs-lookup"><span data-stu-id="52a3e-177">To set author and/or ms.author</span></span>

1. <span data-ttu-id="52a3e-178">在 VS Code 中，移至 [檔案]  >  [喜好設定]  >  [設定]，或選取<kbd>Ctrl+,</kbd>。</span><span class="sxs-lookup"><span data-stu-id="52a3e-178">In VS Code, go to **File** > **Preferences** > **Settings** or select <kbd>Ctrl+,</kbd>.</span></span>
1. <span data-ttu-id="52a3e-179">選取 [使用者] 設定以變更所有 VS Code 工作區的設定，或選取 [工作區] 設定只變更目前工作區的設定。</span><span class="sxs-lookup"><span data-stu-id="52a3e-179">Select **User** settings to change the settings for all VS Code workspaces, or **Workspace** settings to change them for just the current workspace.</span></span>
1. <span data-ttu-id="52a3e-180">在左邊的 [預設設定] 窗格中，尋找 [Docs 文章範本延伸模組設定]，按一下所需設定旁的鉛筆圖示，然後按一下 [在設定中取代]。</span><span class="sxs-lookup"><span data-stu-id="52a3e-180">In the Default Settings pane on the left, find **Docs Article Templates Extension Configuration**, click the pencil icon next to the desired setting, then click Replace in Settings.</span></span>
1. <span data-ttu-id="52a3e-181">[使用者] 設定將會並排開啟，而且底部會顯示新項目。</span><span class="sxs-lookup"><span data-stu-id="52a3e-181">The **User** settings pane will open side by side, with a new entry at the bottom.</span></span>
1. <span data-ttu-id="52a3e-182">視需要新增您的 GitHub 識別碼或 Microsoft 電子郵件別名，然後儲存檔案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-182">Add your GitHub ID or Microsoft email alias, as appropriate, and save the file.</span></span>
1. <span data-ttu-id="52a3e-183">您可能需要關閉並重新啟動 VS Code，變更才會生效。</span><span class="sxs-lookup"><span data-stu-id="52a3e-183">You might need to close and restart VS Code for the changes to take effect.</span></span>
1. <span data-ttu-id="52a3e-184">現在，當您套用使用動態欄位的範本時，您的 GitHub 識別碼和/或 Microsoft 別名將會在中繼資料標頭中自動填入。</span><span class="sxs-lookup"><span data-stu-id="52a3e-184">Now, when you apply a template that uses dynamic fields, your GitHub ID and/or Microsoft alias will be auto-populated in the metadata header.</span></span>

### <a name="to-make-a-new-template-available-in-vs-code"></a><span data-ttu-id="52a3e-185">在 VS Code 中提供新的範本</span><span class="sxs-lookup"><span data-stu-id="52a3e-185">To make a new template available in VS Code</span></span>

1. <span data-ttu-id="52a3e-186">以 Markdown 檔案的形式草擬您的範本。</span><span class="sxs-lookup"><span data-stu-id="52a3e-186">Draft your template as a Markdown file.</span></span>
1. <span data-ttu-id="52a3e-187">提交提取要求至 [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) 存放庫的範本資料夾。</span><span class="sxs-lookup"><span data-stu-id="52a3e-187">Submit a pull request to the templates folder of the [MicrosoftDocs/content-templates](https://github.com/MicrosoftDocs/content-templates) repo.</span></span>

<span data-ttu-id="52a3e-188">docs.microsoft.com 小組會審查您的範本，若其符合 docs.microsoft.com 樣式指導方針便會合併 PR。</span><span class="sxs-lookup"><span data-stu-id="52a3e-188">The docs.microsoft.com team will review your template and merge the PR if it meets docs.microsoft.com style guidelines.</span></span> <span data-ttu-id="52a3e-189">合併之後，此範本就可供 Docs 文章範本延伸模組的所有使用者使用。</span><span class="sxs-lookup"><span data-stu-id="52a3e-189">Once merged, the template will be available to all users of the Docs Article Templates extension.</span></span>

## <a name="demo-several-features"></a><span data-ttu-id="52a3e-190">示範數個功能</span><span class="sxs-lookup"><span data-stu-id="52a3e-190">Demo several features</span></span>

<span data-ttu-id="52a3e-191">以下的簡短影片示範 Docs 編寫套件的下列功能：</span><span class="sxs-lookup"><span data-stu-id="52a3e-191">Here's a short video that demonstrates the following features of the Docs Authoring Pack:</span></span>

* <span data-ttu-id="52a3e-192">**YAML 檔案**</span><span class="sxs-lookup"><span data-stu-id="52a3e-192">**YAML files**</span></span>
  * <span data-ttu-id="52a3e-193">支援 Docs:連結到存放庫中的檔案</span><span class="sxs-lookup"><span data-stu-id="52a3e-193">Support for "Docs: Link to file in repo"</span></span>
* <span data-ttu-id="52a3e-194">**Markdown 檔案**</span><span class="sxs-lookup"><span data-stu-id="52a3e-194">**Markdown files**</span></span>
  * <span data-ttu-id="52a3e-195">[更新 ms. date 中繼資料值] 操作功能表選項</span><span class="sxs-lookup"><span data-stu-id="52a3e-195">Update "ms.date" Metadata Value context menu option</span></span>
  * <span data-ttu-id="52a3e-196">用於程式碼隔離語言識別碼的程式碼自動完成</span><span class="sxs-lookup"><span data-stu-id="52a3e-196">Code auto-completion support for code-fence language identifiers</span></span>
  * <span data-ttu-id="52a3e-197">無法辨識的程式碼隔離語言識別碼警告/自動校正支援</span><span class="sxs-lookup"><span data-stu-id="52a3e-197">Unrecognized code-fence language identifier warnings / auto correction support</span></span>
  * <span data-ttu-id="52a3e-198">遞增排序選取項目 (A 到 Z)</span><span class="sxs-lookup"><span data-stu-id="52a3e-198">Sort selection ascending (A to Z)</span></span>
  * <span data-ttu-id="52a3e-199">遞減排序選取項目 (Z 到 A)</span><span class="sxs-lookup"><span data-stu-id="52a3e-199">Sort selection descending (Z to A)</span></span>

> [!VIDEO https://www.youtube.com/embed/6zfbBRdjlw8]

## <a name="contribution-expectations"></a><span data-ttu-id="52a3e-200">參與貢獻的期望</span><span class="sxs-lookup"><span data-stu-id="52a3e-200">Contribution expectations</span></span>

<span data-ttu-id="52a3e-201">Docs 編寫套件延伸模組為開放原始碼，能讓任何有 GitHub 帳戶的人參與貢獻。</span><span class="sxs-lookup"><span data-stu-id="52a3e-201">The Docs Authoring Pack extension is open source and available for contributions to anyone with a GitHub account.</span></span> <span data-ttu-id="52a3e-202">Microsoft 內部有專門的小組正全心投入這個專案。</span><span class="sxs-lookup"><span data-stu-id="52a3e-202">There is a dedicated internal Microsoft team that actively works on this project.</span></span> <span data-ttu-id="52a3e-203">這個小組會監視問題和提取要求。</span><span class="sxs-lookup"><span data-stu-id="52a3e-203">This team monitors issues and pull requests.</span></span> <span data-ttu-id="52a3e-204">服務等級協定 (SLA) 和預期取得提取要求的審查時間目前為一周。</span><span class="sxs-lookup"><span data-stu-id="52a3e-204">The service level agreement (SLA) and expectation of getting a pull request reviewed is currently one week.</span></span> <span data-ttu-id="52a3e-205">小組正在進行自動化工作，以改善此回應時間。</span><span class="sxs-lookup"><span data-stu-id="52a3e-205">The team is undergoing automation efforts to improve this turn around time.</span></span>

## <a name="next-steps"></a><span data-ttu-id="52a3e-206">下一步</span><span class="sxs-lookup"><span data-stu-id="52a3e-206">Next steps</span></span>

<span data-ttu-id="52a3e-207">探索 Docs 編寫套件 (Visual Studio Code 延伸模組) 的各種功能。</span><span class="sxs-lookup"><span data-stu-id="52a3e-207">Explore the various features available in the Docs Authoring Pack, Visual Studio Code extension.</span></span>

* [<span data-ttu-id="52a3e-208">開發語言完成</span><span class="sxs-lookup"><span data-stu-id="52a3e-208">Dev lang completion</span></span>](docs-authoring/dev-lang-completion.md)
* [<span data-ttu-id="52a3e-209">影像壓縮</span><span class="sxs-lookup"><span data-stu-id="52a3e-209">Image compression</span></span>](docs-authoring/image-compression.md)
* [<span data-ttu-id="52a3e-210">中繼資料更新</span><span class="sxs-lookup"><span data-stu-id="52a3e-210">Metadata updates</span></span>](docs-authoring/metadata-updates.md)
* [<span data-ttu-id="52a3e-211">重新格式化資料表</span><span class="sxs-lookup"><span data-stu-id="52a3e-211">Reformat table</span></span>](docs-authoring/reformat-table.md)
* [<span data-ttu-id="52a3e-212">智慧引號取代</span><span class="sxs-lookup"><span data-stu-id="52a3e-212">Smart quote replacement</span></span>](docs-authoring/smart-quote-replacement.md)
* [<span data-ttu-id="52a3e-213">排序重新導向</span><span class="sxs-lookup"><span data-stu-id="52a3e-213">Sort redirects</span></span>](docs-authoring/sort-redirects.md)
* [<span data-ttu-id="52a3e-214">排序選取項目</span><span class="sxs-lookup"><span data-stu-id="52a3e-214">Sort selection</span></span>](docs-authoring/sort-selection.md)
