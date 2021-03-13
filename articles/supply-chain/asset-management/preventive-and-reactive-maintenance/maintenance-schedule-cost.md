---
title: Стоимость для графика обслуживания
description: В этом разделе описываются затраты для графика обслуживания в модуле "Управление активами".
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9befa52d27a1a12e7a2d9f2615c2ce8e5f1ebe53
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018004"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="e9f30-103">Стоимость для графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="e9f30-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="e9f30-104">В модуле "Управление активами" можно рассчитать бюджетные затраты по строкам графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e9f30-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="e9f30-105">Это полезно, если требуется получить обзор ожидаемых затрат, например, затраты, связанные с запланированными заданиями профилактического обслуживания для следующего года.</span><span class="sxs-lookup"><span data-stu-id="e9f30-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="e9f30-106">Расчеты основаны на существующих строках графика обслуживания с типами "Планы обслуживания", "Циклы обслуживания" и "Запросы на обслуживание".</span><span class="sxs-lookup"><span data-stu-id="e9f30-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="e9f30-107">Щелкните **Управление активами** > **Запросы** > **Активы** > **Затраты для графика обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="e9f30-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="e9f30-108">В диалоговом окне **Затраты для графика обслуживания** можно выбрать **Набор финансовых аналитик**, если требуется просмотреть затраты, сгруппированные в финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="e9f30-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="e9f30-109">Наборы финансовых аналитик настраиваются в разделе **Главная книга** > **План счетов** > **Аналитики** > **Наборы финансовых аналитик**.</span><span class="sxs-lookup"><span data-stu-id="e9f30-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="e9f30-110">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки графика обслуживания относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="e9f30-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="e9f30-111">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки графика обслуживания для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="e9f30-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="e9f30-112">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки графика обслуживания на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="e9f30-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="e9f30-113">Если требуется выполнить расчет для отдельных активов, щелкните **Фильтр** на экспресс-вкладке **Записи для добавления** и выберите соответствующие активы.</span><span class="sxs-lookup"><span data-stu-id="e9f30-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="e9f30-114">Если необходимо, можно также указать значение **Ожидаемая дата начала** для расчета затрат или выбрать другое **Состояние** для расчета затрат.</span><span class="sxs-lookup"><span data-stu-id="e9f30-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="e9f30-115">Нажмите **ОК**, чтобы начать расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="e9f30-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="e9f30-116">На вкладке **Затраты для графика обслуживания** в группах панели операций **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="e9f30-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="e9f30-117">Выбранные кнопки группы панели операций выделяются.</span><span class="sxs-lookup"><span data-stu-id="e9f30-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="e9f30-118">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="e9f30-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="e9f30-119">Нажмите кнопку **Рассчитать затраты**, если необходимо сделать новый расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="e9f30-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="e9f30-120">На приведенном ниже рисунке показаны результаты расчета стоимости для графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="e9f30-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Рисунок 1](media/17-preventive-maintenance.png)

