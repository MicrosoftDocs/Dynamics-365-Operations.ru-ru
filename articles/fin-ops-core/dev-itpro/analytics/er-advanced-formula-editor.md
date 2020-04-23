---
title: Расширенный редактор формул электронной отчетности
description: В этом разделе описывается, как можно использовать расширенный редактор формул для настройки выражений в сопоставлении моделей электронной отчетности и компонентов формата.
author: NickSelin
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: d9911c858d6832aa70378d37e0fd5cf7d7831b1b
ms.sourcegitcommit: dce8c5d3b2fc4a752d676cf9ba91e0dea2fa80d8
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/10/2020
ms.locfileid: "3257069"
---
# <a name="electronic-reporting-advanced-formula-editor"></a><span data-ttu-id="1e898-103">Расширенный редактор формул электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="1e898-103">Electronic reporting advanced formula editor</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e898-104">Кроме [редактора формул](general-electronic-reporting.md) [электронной отчетности](general-electronic-reporting-formula-designer.md) можно использовать расширенный редактор формул электронной отчетности для улучшения процесса настройки выражений электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="1e898-104">In addition to the [Electronic reporting](general-electronic-reporting.md) [formula editor](general-electronic-reporting-formula-designer.md), you can use the advanced Electronic reporting formula editor to improve the experience of configuring Electronic reporting (ER) expressions.</span></span> <span data-ttu-id="1e898-105">Расширенный редактор базируется на веб-браузерах и работает с помощью [редактора Monaco](https://microsoft.github.io/monaco-editor).</span><span class="sxs-lookup"><span data-stu-id="1e898-105">The advanced editor is browser-based and powered by the [Monaco editor](https://microsoft.github.io/monaco-editor).</span></span> <span data-ttu-id="1e898-106">В данном разделе описываются наиболее часто используемые возможности расширенного редактора:</span><span class="sxs-lookup"><span data-stu-id="1e898-106">The most commonly used advanced editor features are described in this topic:</span></span>

- [<span data-ttu-id="1e898-107">Автоформатирование кода</span><span class="sxs-lookup"><span data-stu-id="1e898-107">Code autoformatting</span></span>](#Autoformatting)
- [<span data-ttu-id="1e898-108">IntelliSense</span><span class="sxs-lookup"><span data-stu-id="1e898-108">IntelliSense</span></span>](#IntelliSense)
- [<span data-ttu-id="1e898-109">Завершение кода</span><span class="sxs-lookup"><span data-stu-id="1e898-109">Code completion</span></span>](#CodeCompletion)
- [<span data-ttu-id="1e898-110">Навигация по коду</span><span class="sxs-lookup"><span data-stu-id="1e898-110">Code navigation</span></span>](#CodeNavigation)
- [<span data-ttu-id="1e898-111">Структурирование кода</span><span class="sxs-lookup"><span data-stu-id="1e898-111">Code structuring</span></span>](#CodeStructuring)
- [<span data-ttu-id="1e898-112">Найти и заменить</span><span class="sxs-lookup"><span data-stu-id="1e898-112">Find and replace</span></span>](#FindAndReplace)
- [<span data-ttu-id="1e898-113">Вставка данных</span><span class="sxs-lookup"><span data-stu-id="1e898-113">Data pasting</span></span>](#DataPasting)
- [<span data-ttu-id="1e898-114">Цветовое выделение синтаксиса</span><span class="sxs-lookup"><span data-stu-id="1e898-114">Syntax colorization</span></span>](#SyntaxColorization)

## <a name=""></a><span data-ttu-id="1e898-115"><a name="ActivateAdvEditor">Активация расширенного редактора формул</a></span><span class="sxs-lookup"><span data-stu-id="1e898-115"><a name="ActivateAdvEditor">Activate the advanced formula editor</a></span></span>

<span data-ttu-id="1e898-116">Выполните следующие действия, чтобы начать работу с расширенным редактором формул в своем экземпляре Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="1e898-116">Complete the following steps to start using the advanced formula editor in your instance of Microsoft Dynamics 365 Finance.</span></span>

1.  <span data-ttu-id="1e898-117">Перейдите в раздел  **Управление организацией** \> **Электронная отчетность** \> **Конфигурации**.</span><span class="sxs-lookup"><span data-stu-id="1e898-117">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2.  <span data-ttu-id="1e898-118">На странице **Конфигурации** в области действий на вкладке **Конфигурации** в группе **Дополнительные параметры** выберите **Параметры пользователя**.</span><span class="sxs-lookup"><span data-stu-id="1e898-118">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3.  <span data-ttu-id="1e898-119">В диалоговом окне **Параметры пользователя** в разделе **Трассировка выполнения** установите для параметра **Включить расширенный редактор формул** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="1e898-119">In the **User parameters** dialog box, in the **Execution tracing** section, set the **Enable advanced formula editor** parameter to **Yes**.</span></span>

<span data-ttu-id="1e898-120">[![Страница конфигураций электронной отчетности](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span><span class="sxs-lookup"><span data-stu-id="1e898-120">[![ER configurations page](./media/ER-AdvEditor-Activate.png)](./media/ER-AdvEditor-Activate.png)</span></span>

> [!NOTE]
> <span data-ttu-id="1e898-121">Имейте в виду, что этот параметр используется отдельно для пользователя и для компании.</span><span class="sxs-lookup"><span data-stu-id="1e898-121">Be aware that this parameter is user specific and company specific.</span></span>

## <a name=""></a><span data-ttu-id="1e898-122"><a name="Autoformatting">Автоформатирование кода</a></span><span class="sxs-lookup"><span data-stu-id="1e898-122"><a name="Autoformatting">Code autoformatting</a></span></span>

<span data-ttu-id="1e898-123">При написании сложного выражения, которое состоит из нескольких строк кода, отступ новой введенной строки будет автоматически изменяться на основе отступов предыдущей строки.</span><span class="sxs-lookup"><span data-stu-id="1e898-123">When you write a complex expression that consists of multiple rows of code, the indentation of a new entered line will be automatic based on the indentation of the previous row.</span></span> <span data-ttu-id="1e898-124">Можно выбрать строки и изменить их отступы, нажав **Tab** или **Shift+Tab**.</span><span class="sxs-lookup"><span data-stu-id="1e898-124">You can select lines and change their indentation by typing **Tab** or **Shift+Tab**.</span></span>

<span data-ttu-id="1e898-125">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-125">[![ER formula editor](./media/ER-AdvEditor-Indentation.gif)](./media/ER-AdvEditor-Indentation.gif)</span></span>

<span data-ttu-id="1e898-126">Автоформатирование позволяет полностью отформатировать выражение, чтобы облегчить дальнейшее обслуживание и упростить понимание настроенной логики.</span><span class="sxs-lookup"><span data-stu-id="1e898-126">Autoformatting allows you to keep the entire expression well formatted to make further maintenance easier and to simplify understanding of the configured logic.</span></span>

## <a name=""></a><span data-ttu-id="1e898-127"><a name="IntelliSense">IntelliSense</a></span><span class="sxs-lookup"><span data-stu-id="1e898-127"><a name="IntelliSense">IntelliSense</a></span></span>

<span data-ttu-id="1e898-128">Редактор предоставляет завершение слов, помогающее ускорить написание выражений и избежать опечаток.</span><span class="sxs-lookup"><span data-stu-id="1e898-128">The editor provides word completion to help you write expression faster and avoid typos.</span></span> <span data-ttu-id="1e898-129">При добавлении нового текста редактор автоматически предлагает список функций, поддерживаемых функциями электронной отчетности, которые содержат введенные символы.</span><span class="sxs-lookup"><span data-stu-id="1e898-129">When you start adding new text, the editor automatically offers a list of functions supported in ER functions that contain the characters you have entered.</span></span> <span data-ttu-id="1e898-130">Можно также активировать IntelliSense в любом месте настроенного выражения, нажав **Ctrl+Space**.</span><span class="sxs-lookup"><span data-stu-id="1e898-130">You can also trigger IntelliSense in any place of a configured expression by typing **Ctrl+Space**.</span></span>

<span data-ttu-id="1e898-131">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-131">[![ER formula editor](./media/ER-AdvEditor-Intelisense.gif)](./media/ER-AdvEditor-Intelisense.gif)</span></span>

## <a name=""></a><span data-ttu-id="1e898-132"><a name="CodeCompletion">Завершение кода</a></span><span class="sxs-lookup"><span data-stu-id="1e898-132"><a name="CodeCompletion">Code completion</a></span></span>

<span data-ttu-id="1e898-133">Редактор автоматически обеспечивает завершение кода следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1e898-133">The editor automatically provides code completion by:</span></span>

- <span data-ttu-id="1e898-134">Вставка закрывающей скобки при вводе открывающей скобки, сохраняя курсор внутри квадратных скобок.</span><span class="sxs-lookup"><span data-stu-id="1e898-134">Inserting a closing bracket when an opening  bracket is entered, keeping the cursor inside the brackets.</span></span>
- <span data-ttu-id="1e898-135">Вставка второго символа кавычки при вводе первого, сохраняя курсор внутри кавычек.</span><span class="sxs-lookup"><span data-stu-id="1e898-135">Inserting the second quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>
- <span data-ttu-id="1e898-136">Вставка второго символа двойной кавычки при вводе первого, сохраняя курсор внутри кавычек.</span><span class="sxs-lookup"><span data-stu-id="1e898-136">Inserting the second double quotation symbol when the first one is entered, keeping the cursor inside the quotations.</span></span>

<span data-ttu-id="1e898-137">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-137">[![ER formula editor](./media/ER-AdvEditor-CodeCompletion.gif)](./media/ER-AdvEditor-CodeCompletion.gif)</span></span>

<span data-ttu-id="1e898-138">При наведении указателя на введенную скобку автоматически выделяется вторая скобка этой пары скобок для отображения поддерживаемой конструкции.</span><span class="sxs-lookup"><span data-stu-id="1e898-138">When you point to the typed bracket, the second bracket of this pair is automatically highlighted to show the construct that they support.</span></span>

## <a name=""></a><span data-ttu-id="1e898-139"><a name="CodeNavigation">Навигация по коду</a></span><span class="sxs-lookup"><span data-stu-id="1e898-139"><a name="CodeNavigation">Code navigation</a></span></span>

<span data-ttu-id="1e898-140">Чтобы найти необходимые символы или строки выражения, введите команду **Перейти** с помощью палитры команд или контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="1e898-140">You can locate required symbols or lines in your expression by typing the **Go to** command using the command palette or the context menu.</span></span>

<span data-ttu-id="1e898-141">Например, чтобы перейти к строке **8**, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-141">For example, to jump to line **8**, do the following:</span></span>

- <span data-ttu-id="1e898-142">Нажмите сочетание клавиш **CTRL+G**, введите значение **8**, а затем нажмите клавишу **ВВОД**.</span><span class="sxs-lookup"><span data-stu-id="1e898-142">Press **Ctrl+G**, enter the value **8**, and then press **Enter**.</span></span>

  <span data-ttu-id="1e898-143">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-143">-or-</span></span>

- <span data-ttu-id="1e898-144">Нажмите клавишу **F1**,введите **G**, выберите **Перейти к строке**, введите значение **8**, а затем нажмите клавишу **ВВОД**.</span><span class="sxs-lookup"><span data-stu-id="1e898-144">Press **F1**, type **G**, select **Go to line**, enter the value **8**, and the press **Enter**.</span></span>

<span data-ttu-id="1e898-145">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-145">[![ER formula editor](./media/ER-AdvEditor-Goto.gif)](./media/ER-AdvEditor-Goto.gif)</span></span>

## <a name=""></a><span data-ttu-id="1e898-146"><a name="CodeStructuring">Структурирование кода</a></span><span class="sxs-lookup"><span data-stu-id="1e898-146"><a name="CodeStructuring">Code structuring</a></span></span>

<span data-ttu-id="1e898-147">Код для некоторых функций, таких как [IF](er-functions-logical-if.md) или [CASE](er-functions-logical-case.md), автоматически структурирован.</span><span class="sxs-lookup"><span data-stu-id="1e898-147">The code for some functions, such as [IF](er-functions-logical-if.md) or [CASE](er-functions-logical-case.md), is automatically structured.</span></span> <span data-ttu-id="1e898-148">Можно развернуть или свернуть все области свертывания этого кода, чтобы уменьшить редактируемую часть выражения, чтобы сосредоточиться только на части кода, требующей вашего внимания.</span><span class="sxs-lookup"><span data-stu-id="1e898-148">You can expand and collapse any or all of the folding regions of this code to reduce the editable part of an expression in order to focus on only  thepiece of code that requires your attention.</span></span> <span data-ttu-id="1e898-149">Для этого можно использовать команды "свернуть" и "развернуть".</span><span class="sxs-lookup"><span data-stu-id="1e898-149">The toggle fold/unfold commands can be used for that.</span></span>

<span data-ttu-id="1e898-150">Например, чтобы свернуть все регионы, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-150">For example, to fold all regions, do the following:</span></span>

- <span data-ttu-id="1e898-151">Нажмите сочетание клавиш **CTRL+K**</span><span class="sxs-lookup"><span data-stu-id="1e898-151">Press **Ctrl+K**</span></span>

  <span data-ttu-id="1e898-152">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-152">-or-</span></span>

- <span data-ttu-id="1e898-153">Нажмите клавишу **F1**, нажмите **FO**, выберите команду **Свернуть все**, а затем нажмите клавишу **ВВОД**</span><span class="sxs-lookup"><span data-stu-id="1e898-153">Press **F1**, press **FO**, select **Fold all**, and then press **Enter**</span></span>

<span data-ttu-id="1e898-154">Чтобы развернуть все регионы, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-154">To unfold all regions, do the following:</span></span>

- <span data-ttu-id="1e898-155">Нажмите сочетание клавиш **CTRL+J**</span><span class="sxs-lookup"><span data-stu-id="1e898-155">Press **Ctrl+J**</span></span>

  <span data-ttu-id="1e898-156">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-156">-or-</span></span>
  
- <span data-ttu-id="1e898-157">Нажмите клавишу **F1**, введите **UN**, выберите команду **Развернуть все**, а затем нажмите клавишу **ВВОД**</span><span class="sxs-lookup"><span data-stu-id="1e898-157">Press **F1**, type **UN**, select **Unfold all**, and then press **Enter**</span></span>

<span data-ttu-id="1e898-158">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-158">[![ER formula editor](./media/ER-AdvEditor-ToggleFold.gif)](./media/ER-AdvEditor-ToggleFold.gif)</span></span>

## <a name=""></a><span data-ttu-id="1e898-159"><a name="FindAndReplace">Найти и заменить</a></span><span class="sxs-lookup"><span data-stu-id="1e898-159"><a name="FindAndReplace">Find and replace</a></span></span>

<span data-ttu-id="1e898-160">Чтобы найти вхождения определенного текста, выберите текст в выражении и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-160">To find occurrences of certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1e898-161">Нажмите сочетание клавиш **CTRL+F**, а затем нажмите клавишу **F3**, чтобы найти следующее вхождение выбранного текста, или нажмите сочетание клавиш **SHIFT+F3**, чтобы найти предыдущее вхождение.</span><span class="sxs-lookup"><span data-stu-id="1e898-161">Press **Ctrl+F** and then press **F3** to find the next occurrence of the selected text, or press **Shift+F3** to find the previous occurrence.</span></span>

  <span data-ttu-id="1e898-162">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-162">-or-</span></span>
  
- <span data-ttu-id="1e898-163">Нажмите клавишу **F1**, введите **F**, а затем выберите нужный вариант, чтобы найти выбранный текст.</span><span class="sxs-lookup"><span data-stu-id="1e898-163">Press **F1**, type **F**, and then select the required option to find the selected text.</span></span>

<span data-ttu-id="1e898-164">Чтобы заменить вхождения определенного текста, выберите текст в выражении и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-164">To replace occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1e898-165">Нажмите сочетание клавиш **CTRL+H**.</span><span class="sxs-lookup"><span data-stu-id="1e898-165">Press **Ctrl+H**.</span></span> <span data-ttu-id="1e898-166">Введите замещающий текст и выберите параметр замены для замены выбранного текста или всех вхождений данного текста в текущем выражении.</span><span class="sxs-lookup"><span data-stu-id="1e898-166">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

  <span data-ttu-id="1e898-167">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-167">-or-</span></span>
  
- <span data-ttu-id="1e898-168">Нажмите клавишу **F1**, введите **R**, а затем выберите нужный вариант, чтобы заменить выбранный текст.</span><span class="sxs-lookup"><span data-stu-id="1e898-168">Press **F1**, type **R**, and then select the required option to replace the selected text.</span></span> <span data-ttu-id="1e898-169">Введите замещающий текст и выберите параметр замены для замены выбранного текста или всех вхождений данного текста в текущем выражении.</span><span class="sxs-lookup"><span data-stu-id="1e898-169">Enter the alternative text and select the replacement option to replace either the selected text or all occurrences of this text in the current expression.</span></span>

<span data-ttu-id="1e898-170">Чтобы изменить все вхождения определенного текста, выберите текст в выражении и выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="1e898-170">To change all occurrences of a certain text, select the text in your expression, and do the following:</span></span>

- <span data-ttu-id="1e898-171">Нажмите сочетание клавиш **CTRL+F2**, а затем введите замещающий текст.</span><span class="sxs-lookup"><span data-stu-id="1e898-171">Press **Ctrl+F2** and then enter the alternative text.</span></span>

  <span data-ttu-id="1e898-172">–или–</span><span class="sxs-lookup"><span data-stu-id="1e898-172">-or-</span></span>
  
- <span data-ttu-id="1e898-173">Нажмите клавишу **F1**, введите **C**, а затем выберите нужный вариант, чтобы изменить выбранный текст.</span><span class="sxs-lookup"><span data-stu-id="1e898-173">Press **F1**, type **C**, and then select the required option to change the selected text.</span></span> <span data-ttu-id="1e898-174">Введите замещающий текст.</span><span class="sxs-lookup"><span data-stu-id="1e898-174">Enter the alternative text.</span></span>

<span data-ttu-id="1e898-175">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-175">[![ER formula editor](./media/ER-AdvEditor-Find.gif)](./media/ER-AdvEditor-Find.gif)</span></span>

## <a name=""></a><span data-ttu-id="1e898-176"><a name="DataPasting">Вставка источников данных и функций</a></span><span class="sxs-lookup"><span data-stu-id="1e898-176"><a name="DataPasting">Data sources and functions pasting</a></span></span>

<span data-ttu-id="1e898-177">Можно выбрать **Добавить источник данных**, который вставит в текущее выражение источник данных, выбранный в левой панели **Источник данных**.</span><span class="sxs-lookup"><span data-stu-id="1e898-177">You can select **Add data source**, which pastes to the current expression a data source that is currently selected on the **Data source** left panel.</span></span> <span data-ttu-id="1e898-178">Аналогичным образом можно выбрать **Добавить функцию**, который вставит в текущее выражение функцию, выбранную в правой панели **Функции**.</span><span class="sxs-lookup"><span data-stu-id="1e898-178">Simlilarly, you can select **Add function**, which pastes to the current expression a function that is currently selected on the **Functions** right panel.</span></span> <span data-ttu-id="1e898-179">При использовании редактора формул электронной отчетности выбранная функция или выбранный источник данных всегда будет вставлен в конец настроенного выражения.</span><span class="sxs-lookup"><span data-stu-id="1e898-179">If you use the ER formula editor, a selected function or a selected data source will always be pasted to the end of the configured expression.</span></span> <span data-ttu-id="1e898-180">При использовании расширенного редактора формул электронной отчетности выбранная функция или выбранный источник данных могут быть вставлен в любую часть настроенного выражения.</span><span class="sxs-lookup"><span data-stu-id="1e898-180">When you use the advanced ER formula editor, a selected function or a selected data source can be pasted to any part of the configured expression.</span></span> <span data-ttu-id="1e898-181">Необходимо использовать курсор, чтобы указать, куда необходимо вставить данные.</span><span class="sxs-lookup"><span data-stu-id="1e898-181">You will need to use the cursor to specify where you want to paste the data.</span></span>

<span data-ttu-id="1e898-182">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span><span class="sxs-lookup"><span data-stu-id="1e898-182">[![ER formula editor](./media/ER-AdvEditor-PasteValue.gif)](./media/ER-AdvEditor-PasteValue.gif)</span></span>

## <a name=""></a><span data-ttu-id="1e898-183"><a name="SyntaxColorization">Цветовое выделение синтаксиса</a></span><span class="sxs-lookup"><span data-stu-id="1e898-183"><a name="SyntaxColorization">Syntax colorization</a></span></span>

<span data-ttu-id="1e898-184">В настоящее время для выделения следующих частей выражений используются разные цвета:</span><span class="sxs-lookup"><span data-stu-id="1e898-184">Currently, different colors are used to highlight the following parts of expressions:</span></span>

- <span data-ttu-id="1e898-185">Текст в двойных скобках, который может представлять код метки текстовой константы.</span><span class="sxs-lookup"><span data-stu-id="1e898-185">The text in double brackets that can represent a label ID of a text constant.</span></span>

<span data-ttu-id="1e898-186">[![Редактор формул электронной отчетности](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span><span class="sxs-lookup"><span data-stu-id="1e898-186">[![ER formula editor](./media/ER-AdvEditor-SyntaxColorization.png)](./media/ER-AdvEditor-SyntaxColorization.png)</span></span>

## <a name="limitations"></a><span data-ttu-id="1e898-187">Ограничения</span><span class="sxs-lookup"><span data-stu-id="1e898-187">Limitations</span></span>

<span data-ttu-id="1e898-188">В настоящее время редактор поддерживается в следующих веб-браузерах:</span><span class="sxs-lookup"><span data-stu-id="1e898-188">The editor is currently supported in the following web browsers:</span></span>

- <span data-ttu-id="1e898-189">Chrome</span><span class="sxs-lookup"><span data-stu-id="1e898-189">Chrome</span></span>
- <span data-ttu-id="1e898-190">Edge</span><span class="sxs-lookup"><span data-stu-id="1e898-190">Edge</span></span>
- <span data-ttu-id="1e898-191">Firefox</span><span class="sxs-lookup"><span data-stu-id="1e898-191">Firefox</span></span>
- <span data-ttu-id="1e898-192">Opera</span><span class="sxs-lookup"><span data-stu-id="1e898-192">Opera</span></span>
- <span data-ttu-id="1e898-193">Safari</span><span class="sxs-lookup"><span data-stu-id="1e898-193">Safari</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1e898-194">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="1e898-194">Additional resources</span></span>

- [<span data-ttu-id="1e898-195">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="1e898-195">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="1e898-196">Конструктор формул в электронной отчетности</span><span class="sxs-lookup"><span data-stu-id="1e898-196">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="1e898-197">Редактор Monaco</span><span class="sxs-lookup"><span data-stu-id="1e898-197">Monaco editor</span></span>](https://microsoft.github.io/monaco-editor)
