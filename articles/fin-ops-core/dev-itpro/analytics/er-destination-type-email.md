---
title: Тип места назначения ER электронной почты
description: В этой теме приводятся сведения о настройке места назначения электронной почты для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.
author: NickSelin
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 086114d6a8d425ca01521d9607e4a70ec5aa766b
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019966"
---
# <span data-ttu-id="a9cf1-103"><a name="EmailDestinationType">Место назначения электронной почты</a></span><span class="sxs-lookup"><span data-stu-id="a9cf1-103"><a name="EmailDestinationType">Email destination</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a9cf1-104">Можно настроить место назначения электронной почты для каждого компонента ПАПКА или ФАЙЛ формата электронной отчетности (ER), настроенного для создания исходящих документов.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-104">You can configure an email destination for each FOLDER or FILE component of an Electronic reporting (ER) format that is configured to generate outbound documents.</span></span> <span data-ttu-id="a9cf1-105">На основании настройки места назначения созданный документ передается в виде вложения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-105">Based on the destination setting, a generated document is delivered as an attachment of an electronic mail.</span></span>

<span data-ttu-id="a9cf1-106">Задайте для параметра **Включено** значение **Да**, чтобы отправить выходной файл по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-106">Set **Enabled** to **Yes** to send an output file by email.</span></span> <span data-ttu-id="a9cf1-107">После включения этого параметра вы можете указать получателей сообщения электронной почты, и также изменить тему и текст сообщения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-107">After this option is enabled, you can specify the email recipients and edit the subject and body of the email message.</span></span> <span data-ttu-id="a9cf1-108">Можно настроить постоянные тексты для темы и текста сообщения электронной почты или можно использовать [формулы](er-formula-language.md) электронной отчетности для динамического создания текстов сообщений электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-108">You can set up constant texts for the email subject and body, or you can use ER [formulas](er-formula-language.md) to dynamically create email texts.</span></span> 

<span data-ttu-id="a9cf1-109">Адреса электронной почты для электронной отчетности можно настроить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-109">You can configure email addresses for ER in two ways.</span></span> <span data-ttu-id="a9cf1-110">Настройка может быть выполнена так же, как она выполняется средством управления печатью, или можно разрешить адрес электронной почты, используя прямую ссылку на конфигурацию ER через формулу.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-110">The configuration can be completed in the same way that the Print management feature completes it, or you can resolve an email address by using a direct reference to the ER configuration through a formula.</span></span>

<span data-ttu-id="a9cf1-111">[![Включить место назначения электронной почты](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-111">[![Enable email destination](./media/ER_Destinations-EnableSingleDestination.png)](./media/ER_Destinations-EnableSingleDestination.png)</span></span>

## <a name="email-address-types"></a><span data-ttu-id="a9cf1-112">Типы адреса электронной почты</span><span class="sxs-lookup"><span data-stu-id="a9cf1-112">Email address types</span></span>

<span data-ttu-id="a9cf1-113">При выборе **Изменить** для поля **Кому** или **Cc** открывается диалоговое окно **Кому**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-113">When you select **Edit** in the **To** or **Cc** fields, the **Email to** dialog box appears.</span></span> <span data-ttu-id="a9cf1-114">Затем можно выбрать тип адреса электронной почты для использования.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-114">You can then select the type of email address to use.</span></span> <span data-ttu-id="a9cf1-115">Типы электронной почты **Конфигурационное сообщение эл. почты** и **Управление печатью** в настоящее время поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-115">The **Configuration email** and **Print Management** email types are currently supported.</span></span>

<span data-ttu-id="a9cf1-116">[![Выбор типа электронной почты](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-116">[![Select email type](./media/ER_Destinations-EmailSelectAddressType.png)](./media/ER_Destinations-EmailSelectAddressType.png)</span></span>

### <a name="print-management"></a><span data-ttu-id="a9cf1-117">Управление печатью</span><span class="sxs-lookup"><span data-stu-id="a9cf1-117">Print management</span></span>

<span data-ttu-id="a9cf1-118">При выборе типа электронной почты **Управление печатью** можно ввести фиксированные адреса электронной почты в поле **Кому**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-118">If you select the **Print Management** email type, you can enter fixed email addresses in the **To** field.</span></span> 

<span data-ttu-id="a9cf1-119">[![Настройка фиксированных адресов электронной почты](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-119">[![Configure fixed email addresses](./media/ER_Destinations-EmailFixedAddress.png)](./media/ER_Destinations-EmailFixedAddress.png)</span></span>

<span data-ttu-id="a9cf1-120">Чтобы использовать нефиксированные адреса электронной почты, необходимо выбрать тип источника электронной почты для места назначения файла.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-120">To use email addresses that aren't fixed, you must select the email source type for a file destination.</span></span> <span data-ttu-id="a9cf1-121">Поддерживаются следующие значения: **Клиент**, **Поставщик**, **Перспективный клиент**, **Контакт**, **Конкурент**, **Работник**, **Кандидат**, **Потенциальный поставщик** и **Неодобренный поставщик**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-121">The following values are supported: **Customer**, **Vendor**, **Prospect**, **Contact**, **Competitor**, **Worker**, **Applicant**, **Prospective vendor**, and **Disallowed vendor**.</span></span> <span data-ttu-id="a9cf1-122">После выбора типа источника электронной почты нажмите кнопку рядом с полем **Исходная учетная запись эл. почты**, чтобы открыть форму **Конструктор формул**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-122">After you select an email source type, use the button next to the **Email source account** field to open the **Formula designer** form.</span></span> <span data-ttu-id="a9cf1-123">Можно использовать эту форму, чтобы приложить формулу, возвращающую во время выполнения **счет субъекта** выбранного типа источника из обработанного документа в место назначения электронной почты.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-123">You can use this form to attach a formula that returns at runtime, the **party account** of the selected source type from the processed document to the email destination.</span></span>

<span data-ttu-id="a9cf1-124">[![Настройка учетной записи источника электронной почты](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-124">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSource.png)](./media/ER_Destinations-EmailDefineAddressSource.png)</span></span>

<span data-ttu-id="a9cf1-125">Формулы зависят от конфигурации электронной отчетности.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-125">Formulas are specific to the ER configuration.</span></span> <span data-ttu-id="a9cf1-126">В поле **Формула** введите характерную для конкретного документа ссылку на тип субъекта клиента или поставщика.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-126">In the **Formula** field, enter a document-specific reference to a customer or vendor party type.</span></span> <span data-ttu-id="a9cf1-127">Вместо печати можно найти узел источника данных, который представляет счет клиента или поставщика, и выбрать **Добавить источник данных**, чтобы обновить формулу.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-127">Instead of typing, you can find the data source node that represents the customer or vendor account, and then select **Add data source** to update the formula.</span></span> <span data-ttu-id="a9cf1-128">Пример, при использовании конфигурации **перемещения кредита ISO 20022** узел, представляющий счет поставщика, — `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-128">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents a vendor account is `'\$PaymentsForCoveringLetter'.Creditor.Identification.SourceID`.</span></span>

<span data-ttu-id="a9cf1-129">Если ввести строковое значение, например `"DE-001"`, и сохранить формулу, контактному лицу поставщика будет направлено сообщение электронной почты, **DE-001**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-129">If you enter a string value, such as `"DE-001"`, and save a formula, an email will be sent to the contact person of the vendor, **DE-001**.</span></span>


<span data-ttu-id="a9cf1-130">[![Страница конструктора формул ER](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-130">[![ER formula designer page](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)](./media/ER_Destinations-EmailDefineAddressSourceFormula.png)</span></span>

<span data-ttu-id="a9cf1-131">[![Настройка учетной записи источника электронной почты](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-131">[![Configure email source account](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)](./media/ER_Destinations-EmailDefineAddressSourceAttributes.png)</span></span>



### <a name="configuration-email"></a><span data-ttu-id="a9cf1-132">Конфигурационное сообщение эл. почты</span><span class="sxs-lookup"><span data-stu-id="a9cf1-132">Configuration email</span></span>

<span data-ttu-id="a9cf1-133">Используйте этот тип электронной почты, если конфигурация, которую вы используете, имеет узел в источниках данных, который возвращает **адрес электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-133">Use this email type if the configuration that you use has a node in the data sources that returns an **email address**.</span></span> <span data-ttu-id="a9cf1-134">Можно использовать источники данных и функции в конструкторе формул, чтобы получить адрес электронной почты в правильном формате.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-134">You can use data sources and functions in the formula designer to get a correctly formatted email address.</span></span> <span data-ttu-id="a9cf1-135">Пример, при использовании конфигурации **перемещения кредита ISO 20022** узел, представляющий адрес электронной почты контактного лица поставщика, — `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span><span class="sxs-lookup"><span data-stu-id="a9cf1-135">For example, if you use the **ISO 20022 Credit Transfer** configuration, the node that represents an email address of a vendor's contact person is `'$PaymentsForCoveringLetter'.Creditor.ContactDetails.Email`.</span></span>

<span data-ttu-id="a9cf1-136">[![Настройка источника адреса электронной почты](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-136">[![Configure email address source](./media/ER_Destinations-EmailDefineAddressSource2.png)](./media/ER_Destinations-EmailDefineAddressSource2.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9cf1-137">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a9cf1-137">Additional resources</span></span>

- [<span data-ttu-id="a9cf1-138">Обзор электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-138">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="a9cf1-139">Места назначения электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-139">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="a9cf1-140">Конструктор формул в электронной отчетности (ER)</span><span class="sxs-lookup"><span data-stu-id="a9cf1-140">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
