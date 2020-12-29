---
title: Использование внешних данных в прогнозах движения денежных средств (предварительная версия)
description: В этой теме описываются шаги настройки, которые необходимо выполнить, чтобы внешние данные могли быть введены или импортированы в прогнозы движения денежных средств.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 801327dc54f6d4cfef7a9f062395e29846783e8f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/25/2020
ms.locfileid: "4644953"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="3d6c7-103">Использование внешних данных в прогнозах движения денежных средств (предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3d6c7-104">Внешние данные можно вводить или импортировать в прогнозы движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="3d6c7-105">В этой теме описываются шаги настройки, которые относятся к использованию внешних данных и позволяют включить внешние данные для включения в прогноз движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="3d6c7-106">Настройка внешних данных</span><span class="sxs-lookup"><span data-stu-id="3d6c7-106">External data setup</span></span>

<span data-ttu-id="3d6c7-107">Используйте вкладку **Внешний источник** на странице **Настройка прогноза движения денежных средств** (**Управление банком и кассовыми операциями \> Прогнозирование движения денежных средств**) для ввода настроек, которые поддерживают использование внешних данных в прогнозах движения денежных средств.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="3d6c7-108">Дополнительные сведения о настройке см. в разделе [Прогнозирование движения денежных средств](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="3d6c7-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="3d6c7-109">Чтобы ввести внешние данные для прогнозов движения денежных средств, можно использовать интерфейс открытия в Excel для ввода и изменения внешних данных.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="3d6c7-110">Выберите кнопку **Внешние данные**, а затем выберите либо **Добавить внешние данные**, либо **Изменить существующие внешние данные**.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="3d6c7-111">Когда открыт файл Microsoft Excel, можно ввести информацию в следующие поля:</span><span class="sxs-lookup"><span data-stu-id="3d6c7-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="3d6c7-112">**Код записи**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-112">**Entry ID**</span></span>
- <span data-ttu-id="3d6c7-113">**Описание** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-113">**Description** (optional)</span></span>
- <span data-ttu-id="3d6c7-114">**Имя внешнего источника** — выберите одно из значений в списке, которое было определено при настройке финансового анализа.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="3d6c7-115">**Информация о компании**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-115">**Legal Entity**</span></span>
- <span data-ttu-id="3d6c7-116">**Дата**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-116">**Date**</span></span>
- <span data-ttu-id="3d6c7-117">**Сумма в валюте проводки**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="3d6c7-118">**Код валюты**</span><span class="sxs-lookup"><span data-stu-id="3d6c7-118">**Currency Code**</span></span>
- <span data-ttu-id="3d6c7-119">**Аналитика по умолчанию** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="3d6c7-120">**Номер документа** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-120">**Document number** (optional)</span></span>
- <span data-ttu-id="3d6c7-121">**Номер счета** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-121">**Account number** (optional)</span></span>
- <span data-ttu-id="3d6c7-122">**Имя счета** (необязательно)</span><span class="sxs-lookup"><span data-stu-id="3d6c7-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="3d6c7-123">Импорт внешних данных с помощью платформы управления данными</span><span class="sxs-lookup"><span data-stu-id="3d6c7-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="3d6c7-124">Можно импортировать внешние данные для прогнозов движения денежных средств с помощью рабочей области **Управление данными** и сущности, которая называется **Ввод внешнего источника прогноза движения денежных средств**.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="3d6c7-125">Кроме того, если необходимо переместить данные настройки из одной среды в другую, можно использовать следующие сущности для таблиц настройки, которые являются обязательными:</span><span class="sxs-lookup"><span data-stu-id="3d6c7-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="3d6c7-126">Настройка внешнего источника прогноза движения денежных средств</span><span class="sxs-lookup"><span data-stu-id="3d6c7-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="3d6c7-127">Настройка юридического лица внешнего источника прогноза движения денежных средств</span><span class="sxs-lookup"><span data-stu-id="3d6c7-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="3d6c7-128">Уведомление о конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="3d6c7-128">Privacy notice</span></span>
<span data-ttu-id="3d6c7-129">Предварительные версии (1) могут использовать меньшую степень конфиденциальности и безопасности, чем сервис Dynamics 365 Finance and Operations, (2) не включаются в соглашение об уровне обслуживания (SLA) для этого сервиса, (3), не должны использоваться для обработки личных данных или других данных, являющихся объектом соответствия юридическим или нормативным требованиям и (4) имеет ограниченную поддержку.</span><span class="sxs-lookup"><span data-stu-id="3d6c7-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
