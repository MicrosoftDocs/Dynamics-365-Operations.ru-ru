---
title: Настройка регистрационных номеров TDS для юридических лиц
description: В этой теме объясняется, как настроить регистрационные номера для юридических лиц для налогов, которые удерживаются в источнике (TDS).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 3550b2b7b305702ffc337ba0a9bb79f60a9de120
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023535"
---
# <a name="set-up-tds-registration-numbers-for-legal-entities"></a><span data-ttu-id="85b6c-103">Настройка регистрационных номеров TDS для юридических лиц</span><span class="sxs-lookup"><span data-stu-id="85b6c-103">Set up TDS registration numbers for legal entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85b6c-104">В этой теме объясняется, как настроить регистрационные номера для юридических лиц для налогов, которые удерживаются в источнике (TDS).</span><span class="sxs-lookup"><span data-stu-id="85b6c-104">This topic explains how to set up Tax Deducted at Source (TDS) registration numbers for legal entities.</span></span>

1. <span data-ttu-id="85b6c-105">Перейдите в раздел **Управление организацией \> Организации \> Юридические лица**.</span><span class="sxs-lookup"><span data-stu-id="85b6c-105">Go to **Organization administration \> Organizations \> Legal entities**.</span></span>

    <span data-ttu-id="85b6c-106">[![Страница "Юридические лица"](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span><span class="sxs-lookup"><span data-stu-id="85b6c-106">[![Legal entities page](./media/apac-ind-TDS-4.png)](./media/apac-ind-TDS-4.png)</span></span>

2. <span data-ttu-id="85b6c-107">На экспресс-вкладке **Сведения о налоге** в поле **Постоянный номер счета** введите постоянный номер счета (PAN) юридического лица.</span><span class="sxs-lookup"><span data-stu-id="85b6c-107">On the **Tax information** FastTab, in the **Permanent account number** field, enter the permanent account number (PAN) of the legal entity.</span></span>
3. <span data-ttu-id="85b6c-108">В поле **Номер круга** введите номер круга органа TDS.</span><span class="sxs-lookup"><span data-stu-id="85b6c-108">In the **Circle number** field, enter the circle number of the TDS authority.</span></span>
4. <span data-ttu-id="85b6c-109">В поле **Номер района** введите номер района органа TDS.</span><span class="sxs-lookup"><span data-stu-id="85b6c-109">In the **Ward number** field, enter the ward number of the TDS authority.</span></span>
5. <span data-ttu-id="85b6c-110">В поле **Номер налогового оценщика** введите сведения о налоговом оценщике для органа TDS.</span><span class="sxs-lookup"><span data-stu-id="85b6c-110">In the **Assessing officer** field, enter the details of the assessing officer for the TDS authority.</span></span>
6. <span data-ttu-id="85b6c-111">В поле **Тип удержания** выберите категорию типа удержания для юридического лица.</span><span class="sxs-lookup"><span data-stu-id="85b6c-111">In the **Type of deductor** field, select the deductor type category for the legal entity.</span></span>
7. <span data-ttu-id="85b6c-112">В области действий выберите **Регистрационные номера**, чтобы открыть страницу **Управление адресами**.</span><span class="sxs-lookup"><span data-stu-id="85b6c-112">On the Action Pane, select **Registration IDs** to open the **Manage addresses** page.</span></span>
8. <span data-ttu-id="85b6c-113">На экспресс-вкладке **Сведения о налоге** выберите **Добавить** или **Изменить**, чтобы открыть страницу **Управление сведениями о налогах**, где можно вести запись регистрации налога.</span><span class="sxs-lookup"><span data-stu-id="85b6c-113">On the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>

    <span data-ttu-id="85b6c-114">[![Страница "Управление адресами"](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span><span class="sxs-lookup"><span data-stu-id="85b6c-114">[![Manage addresses page](./media/apac-ind-TDS-5.png)](./media/apac-ind-TDS-5.png)</span></span>

9. <span data-ttu-id="85b6c-115">На экспресс-вкладке **Подоходный налог** в поле **Номер налогового счета (TAN)** введите регистрационный номер.</span><span class="sxs-lookup"><span data-stu-id="85b6c-115">On the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the registration number.</span></span> <span data-ttu-id="85b6c-116">Этот номер должен состоять из четырех букв, затем пяти цифр, а затем одной буквы.</span><span class="sxs-lookup"><span data-stu-id="85b6c-116">This number must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="85b6c-117">Пример: **AXDF87645F**.</span><span class="sxs-lookup"><span data-stu-id="85b6c-117">Here is an example: **AXDF87645F**.</span></span>
10. <span data-ttu-id="85b6c-118">В поле **Имя или описание** введите описание регистрационного номера подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="85b6c-118">In the **Name or description** field, enter a description of the withholding tax registration number.</span></span>

    <span data-ttu-id="85b6c-119">[![Страница "Управление сведениями о налогах"](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span><span class="sxs-lookup"><span data-stu-id="85b6c-119">[![Manage tax information page](./media/apac-ind-TDS-5-1.png)](./media/apac-ind-TDS-5-1.png)</span></span>

11. <span data-ttu-id="85b6c-120">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="85b6c-120">Close the page.</span></span>
