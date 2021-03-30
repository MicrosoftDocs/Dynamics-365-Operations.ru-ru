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
ms.openlocfilehash: 9686efb228e123671ba93a37480d2daac8d038a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252974"
---
# <a name="maintenance-schedule-cost"></a><span data-ttu-id="92ae6-103">Стоимость для графика обслуживания</span><span class="sxs-lookup"><span data-stu-id="92ae6-103">Maintenance schedule cost</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="92ae6-104">В модуле "Управление активами" можно рассчитать бюджетные затраты по строкам графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="92ae6-104">In Asset Management, you can calculate budget costs on maintenance schedule lines.</span></span> <span data-ttu-id="92ae6-105">Это полезно, если требуется получить обзор ожидаемых затрат, например, затраты, связанные с запланированными заданиями профилактического обслуживания для следующего года.</span><span class="sxs-lookup"><span data-stu-id="92ae6-105">This is useful if you want to get an overview of expected costs, for example, costs relating to planned preventive maintenance jobs for the next year.</span></span> <span data-ttu-id="92ae6-106">Расчеты основаны на существующих строках графика обслуживания с типами "Планы обслуживания", "Циклы обслуживания" и "Запросы на обслуживание".</span><span class="sxs-lookup"><span data-stu-id="92ae6-106">The calculations are based on existing maintenance schedule lines of type "Maintenance plans" and "Maintenance rounds" and "Maintenance requests".</span></span>

1. <span data-ttu-id="92ae6-107">Щелкните **Управление активами** > **Запросы** > **Активы** > **Затраты для графика обслуживания**.</span><span class="sxs-lookup"><span data-stu-id="92ae6-107">Click **Asset management** > **Inquiries** > **Assets** > **Maintenance schedule cost**.</span></span>

2. <span data-ttu-id="92ae6-108">В диалоговом окне **Затраты для графика обслуживания** можно выбрать **Набор финансовых аналитик**, если требуется просмотреть затраты, сгруппированные в финансовые аналитики.</span><span class="sxs-lookup"><span data-stu-id="92ae6-108">In the **Maintenance schedule cost** dialog, you can select a **Financial dimension set** if you want to see costs grouped in financial dimensions.</span></span>

>[!NOTE]
><span data-ttu-id="92ae6-109">Наборы финансовых аналитик настраиваются в разделе **Главная книга** > **План счетов** > **Аналитики** > **Наборы финансовых аналитик**.</span><span class="sxs-lookup"><span data-stu-id="92ae6-109">Financial dimension sets are set up in **General ledger** > **Chart of accounts** > **Dimensions** > **Financial dimension sets**.</span></span>

3. <span data-ttu-id="92ae6-110">Можно использовать поле **Уровень**, чтобы указать, насколько подробными должны быть строки графика обслуживания относительно функциональных местоположений.</span><span class="sxs-lookup"><span data-stu-id="92ae6-110">You can use the **Level** field to indicate how detailed you want the maintenance schedule lines to be regarding functional locations.</span></span> <span data-ttu-id="92ae6-111">Например, если вставить число "1" в это поле, и имеется структура функциональных местоположений с несколькими уровнями, все строки графика обслуживания для функционального местоположения будут показаны на верхнем уровне, и поэтому часы по строке могут быть добавлены из функциональных местоположений, расположенных на более низком уровне.</span><span class="sxs-lookup"><span data-stu-id="92ae6-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance schedule lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="92ae6-112">Если вставить число "0" в поле **Уровень**, будет выведен подробный результат, отображающий все строки графика обслуживания на всех уровнях функциональных местоположений, к которым они относятся.</span><span class="sxs-lookup"><span data-stu-id="92ae6-112">If you insert the number "0" in the **Level** field, you will see a detailed result showing all maintenance schedule lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="92ae6-113">Если требуется выполнить расчет для отдельных активов, щелкните **Фильтр** на экспресс-вкладке **Записи для добавления** и выберите соответствующие активы.</span><span class="sxs-lookup"><span data-stu-id="92ae6-113">If you want to make a calculation for specific assets, click **Filter** on the **Records to include** FastTab, and select the relevant assets.</span></span> <span data-ttu-id="92ae6-114">Если необходимо, можно также указать значение **Ожидаемая дата начала** для расчета затрат или выбрать другое **Состояние** для расчета затрат.</span><span class="sxs-lookup"><span data-stu-id="92ae6-114">If required, you can also specify an **Expected start** date for the cost calculation or select a different **Status** for the cost calculation</span></span>

5. <span data-ttu-id="92ae6-115">Нажмите **ОК**, чтобы начать расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="92ae6-115">Click **OK** to start the cost calculation.</span></span>

6. <span data-ttu-id="92ae6-116">На вкладке **Затраты для графика обслуживания** в группах панели операций **Группировать по...** щелкните соответствующие кнопки, чтобы отобразить необходимый уровень детализации для расчета.</span><span class="sxs-lookup"><span data-stu-id="92ae6-116">On the **Maintenance schedule cost** tab > in the **Group by...** Action Pane groups, click the relevant buttons to show the required detail level of the cost calculation.</span></span> <span data-ttu-id="92ae6-117">Выбранные кнопки группы панели операций выделяются.</span><span class="sxs-lookup"><span data-stu-id="92ae6-117">The selected Action Pane group buttons are highlighted.</span></span> <span data-ttu-id="92ae6-118">Нажимайте кнопку, чтобы активировать или деактивировать ее.</span><span class="sxs-lookup"><span data-stu-id="92ae6-118">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="92ae6-119">Нажмите кнопку **Рассчитать затраты**, если необходимо сделать новый расчет затрат.</span><span class="sxs-lookup"><span data-stu-id="92ae6-119">Click the **Calculate cost** button if you want to make a new cost calculation.</span></span>

<span data-ttu-id="92ae6-120">На приведенном ниже рисунке показаны результаты расчета стоимости для графика обслуживания.</span><span class="sxs-lookup"><span data-stu-id="92ae6-120">The illustration below shows the results of a maintenance schedule cost calculation.</span></span>

![Рисунок 1](media/17-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]