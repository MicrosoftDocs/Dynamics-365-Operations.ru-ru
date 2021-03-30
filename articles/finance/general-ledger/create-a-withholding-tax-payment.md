---
title: Создание платежа подоходного налога
description: Процедура задания платежа подоходного налога сопоставит сальдо подоходного налога из модуля расчетов с поставщиками в налоговых счетах и корреспондирует их со счетом сопоставления подоходного налога за определенный период. В этом разделе перечислены шаги для настройки платежа по подоходному налогу.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
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
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212285"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="a5943-104">Создание платежа подоходного налога</span><span class="sxs-lookup"><span data-stu-id="a5943-104">Create a withholding tax payment</span></span>

<span data-ttu-id="a5943-105">Процедура задания платежа подоходного налога сопоставит сальдо подоходного налога из модуля расчетов с поставщиками в налоговых счетах и корреспондирует их со счетом сопоставления подоходного налога за определенный период.</span><span class="sxs-lookup"><span data-stu-id="a5943-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="a5943-106">В этом разделе перечислены шаги для настройки платежа по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="a5943-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="a5943-107">Корреспондирование подоходного налога (из расчетов с клиентами) не учитывается при расчете платежа по подоходному налогу.</span><span class="sxs-lookup"><span data-stu-id="a5943-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="a5943-108">Перейдите в раздел **Область перехода> Модули > Налог > Декларации > Подоходный налог > Платеж подоходного налога**.</span><span class="sxs-lookup"><span data-stu-id="a5943-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="a5943-109">В поле **Период сопоставления** нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="a5943-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a5943-110">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="a5943-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a5943-111">В поле **Дата начала** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a5943-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="a5943-112">В поле **Дата проводки** введите дату.</span><span class="sxs-lookup"><span data-stu-id="a5943-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="a5943-113">Выберите **Обновить** для разноски операции по платежу подоходного налога на счет сопоставления подоходного налога.</span><span class="sxs-lookup"><span data-stu-id="a5943-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="a5943-114">Щелкните **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5943-114">Click **OK**.</span></span>

![Параметры для платежа по подоходному налогу](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]