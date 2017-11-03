---
title: "Электронная отчетность для образцов чеков поставщика"
description: "Этот раздел содержит общие сведения об использовании электронной отчетности для образцов чеков поставщика."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c9abea228cdaae84ca2b9aada9f36bbe79c1dc6b
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="d53ab-103">Электронная отчетность для форматов образцов чеков поставщика</span><span class="sxs-lookup"><span data-stu-id="d53ab-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="d53ab-104">Электронную отчетность (ER) можно использовать для форматирования чеков поставщика.</span><span class="sxs-lookup"><span data-stu-id="d53ab-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="d53ab-105">На рынке есть множество форматов чеков в зависимости от банков и поставщиков.</span><span class="sxs-lookup"><span data-stu-id="d53ab-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="d53ab-106">Форматы образцов чеков флажок были включены в модель чека платежа в репозитории средства электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="d53ab-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="d53ab-107">Эти образцы чеков помечаются как **Чек в середине (США)** и **Чек на верхней позиции ниже (США)**.</span><span class="sxs-lookup"><span data-stu-id="d53ab-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="d53ab-108">Какие форматы чеков в настоящее время поддерживаются?</span><span class="sxs-lookup"><span data-stu-id="d53ab-108">What check formats are currently supported?</span></span>

<span data-ttu-id="d53ab-109">Следует обязательно перейти в библиотеку общих средств в службах Microsoft Dynamics Lifecycle Services (LCS) и просмотреть новейший список доступных файлов, которые имеют тип ресурса **Конфигурация GER**.</span><span class="sxs-lookup"><span data-stu-id="d53ab-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="d53ab-110">В следующем разделе "Что нужно настроить?" приведена ссылка на раздел, в котором объясняется, как создать репозиторий LCS для просмотра доступных конфигураций и импорта выбранных конфигураций.</span><span class="sxs-lookup"><span data-stu-id="d53ab-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="d53ab-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition включает формат образца, где чек находится сверху, а после него идут два раздела предъявления к оплате.</span><span class="sxs-lookup"><span data-stu-id="d53ab-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="d53ab-112">Он также включает формат образца, где чека находится посередине, между двумя разделами предъявления к оплате.</span><span class="sxs-lookup"><span data-stu-id="d53ab-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="d53ab-113">Эти форматы образцов соответствуют форматам бизнес чеков Deluxe.</span><span class="sxs-lookup"><span data-stu-id="d53ab-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="d53ab-114">Что следует настроить?</span><span class="sxs-lookup"><span data-stu-id="d53ab-114">What do I have to set up?</span></span>

- <span data-ttu-id="d53ab-115">Прежде чем печатать чеки с помощью электронной отчетности, по крайней мере одна активная конфигурация чека должна быть импортирована в ваши конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="d53ab-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="d53ab-116">Инструкции см. в разделе [Загрузка конфигураций электронной отчетности из Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="d53ab-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
- <span data-ttu-id="d53ab-117">Если настраиваются чеки управления банком и кассовыми операциями для банковского счета, установите флажок **Универсальный электронный формат экспорта** и выберите соответствующий формат чека как конфигурацию формата экспорта.</span><span class="sxs-lookup"><span data-stu-id="d53ab-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="d53ab-118">Необходимо также указать число строк накладных, которые будут печататься при предъявлении к оплате.</span><span class="sxs-lookup"><span data-stu-id="d53ab-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="d53ab-119">Не забудьте включить строки заголовка при расчете этот номера.</span><span class="sxs-lookup"><span data-stu-id="d53ab-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="d53ab-120">Для двух форматов образцов чеков рекомендуемое число строк накладных — 17.</span><span class="sxs-lookup"><span data-stu-id="d53ab-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="d53ab-121">Тем не менее, это число будет зависеть от запаса чека и драйверов принтера.</span><span class="sxs-lookup"><span data-stu-id="d53ab-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="d53ab-122">Мы рекомендуем распечатать тестовый чек для проверки макета чека.</span><span class="sxs-lookup"><span data-stu-id="d53ab-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="d53ab-123">Для печати тестового чека выберите параметр **Тест печати**.</span><span class="sxs-lookup"><span data-stu-id="d53ab-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="d53ab-124">Форматы образцов чеков работают лучше, когда **Поля** заданы как **Нет** в расширенных свойствах принтера в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d53ab-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="d53ab-125">После создания тестового чека разрешите редактирование выходных данных Excel и настройте макет страницы, чтобы все поля были равны **0** (ноль).</span><span class="sxs-lookup"><span data-stu-id="d53ab-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="d53ab-126">Сравните тестовые копии чеков с запасом чеков и измените настройки, пока не будет достигнуто подходящее выравнивание.</span><span class="sxs-lookup"><span data-stu-id="d53ab-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="d53ab-127">При создании платежей для настроенного банковского счета в журнале платежей, чеки будут напечатаны в указанном формате.</span><span class="sxs-lookup"><span data-stu-id="d53ab-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="d53ab-128">Дополнительные сведения см. в разделе [Изменение формата электронной отчетности](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span><span class="sxs-lookup"><span data-stu-id="d53ab-128">For more information, see [Modify an Electronic reporting format](../../dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).</span></span>

