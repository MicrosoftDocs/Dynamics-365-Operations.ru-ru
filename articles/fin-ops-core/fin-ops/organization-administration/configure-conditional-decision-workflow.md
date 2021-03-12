---
title: Настройка условных решений в workflow-процессе
description: Используйте следующую процедуру для настройки свойств условного решения.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a880d4be461ea9b2caa61b7d038f9b24486a919
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798888"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="14aed-103">Настройка условных решений в workflow-процессе</span><span class="sxs-lookup"><span data-stu-id="14aed-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14aed-104">Используйте следующую процедуру для настройки свойств условного решения.</span><span class="sxs-lookup"><span data-stu-id="14aed-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="14aed-105">Условное решение - Точка, в которой workflow-процесс делится на две ветви.</span><span class="sxs-lookup"><span data-stu-id="14aed-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="14aed-106">Чтобы настроить условное решение, в редакторе workflow-процесс, щелкните правой кнопкой мыши условное решение, а затем щелкните **Свойства**, чтобы открыть форму **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="14aed-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="14aed-107">Задание имени решения</span><span class="sxs-lookup"><span data-stu-id="14aed-107">Name a decision</span></span>

<span data-ttu-id="14aed-108">Чтобы ввести имя условного решения, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14aed-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="14aed-109">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="14aed-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="14aed-110">В поле **Имя** введите уникальное имя для условного решения.</span><span class="sxs-lookup"><span data-stu-id="14aed-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="14aed-111">Установка условий</span><span class="sxs-lookup"><span data-stu-id="14aed-111">Set conditions</span></span>

<span data-ttu-id="14aed-112">Система определяет, какая ветвь будет использоваться, оценивая документ отправленный, чтобы определить, отвечает ли документ указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="14aed-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="14aed-113">В левой области нажмите **Основные настройки**.</span><span class="sxs-lookup"><span data-stu-id="14aed-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="14aed-114">Щелкните **Добавить условие**.</span><span class="sxs-lookup"><span data-stu-id="14aed-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="14aed-115">Введите условие.</span><span class="sxs-lookup"><span data-stu-id="14aed-115">Enter a condition.</span></span>
4. <span data-ttu-id="14aed-116">При необходимости введите дополнительные условия.</span><span class="sxs-lookup"><span data-stu-id="14aed-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="14aed-117">Чтобы убедиться, что введенные условия настроены верно, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="14aed-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="14aed-118">Щелкните **Проверка** для открытия формы **Условия тестового workflow-процесса**.</span><span class="sxs-lookup"><span data-stu-id="14aed-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="14aed-119">Выберите запись в области **Проверка условия** формы.</span><span class="sxs-lookup"><span data-stu-id="14aed-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="14aed-120">Щелкните **Тест**.</span><span class="sxs-lookup"><span data-stu-id="14aed-120">Click **Test**.</span></span> <span data-ttu-id="14aed-121">Система оценит запись и определит, соответствует ли она определенным вами условиям.</span><span class="sxs-lookup"><span data-stu-id="14aed-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="14aed-122">Щелкните **OK** или **Отмена** для возврата к форме **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="14aed-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>
