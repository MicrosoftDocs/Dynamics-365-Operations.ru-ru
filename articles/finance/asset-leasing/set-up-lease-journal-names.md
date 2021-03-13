---
title: Настройка наименований журналов аренды
description: В этом разделе объясняется, как определить наименования журналов аренды. Названия журналов аренды определяют журналы, в которые разносятся записи, созданные в модуле аренды активов.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990925"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="8352a-104">Настройка наименований журналов аренды</span><span class="sxs-lookup"><span data-stu-id="8352a-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8352a-105">Названия журналов аренды определяют журналы, в которые разносятся проводки аренды активов.</span><span class="sxs-lookup"><span data-stu-id="8352a-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="8352a-106">Только имена журналов, назначенных для типа журнала **Аренда активов**, отображаются в полях **Первоначальное признание** и **Имя ежемесячного журнала** на странице **Параметры аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="8352a-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="8352a-107">Только тип журнала **запись накладных поставщика** может быть назначен в поле **Наименование журнала накладных**.</span><span class="sxs-lookup"><span data-stu-id="8352a-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="8352a-108">Для настройки наименований журналов аренды выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8352a-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="8352a-109">Перейдите в раздел **Аренда активов \> Настройка \> Параметры аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="8352a-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="8352a-110">На вкладке **Общие** в поле **Имя журнала первоначального признания** выберите журнал.</span><span class="sxs-lookup"><span data-stu-id="8352a-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="8352a-111">Все записи журнала первоначального признания будут разнесены по этому имени журнала.</span><span class="sxs-lookup"><span data-stu-id="8352a-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="8352a-112">В поле **Имя журнала накладных** выберите журнал.</span><span class="sxs-lookup"><span data-stu-id="8352a-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="8352a-113">Если для параметра **Оплата поставщику** установлено значение **Да** для книги аренды, накладные по арендной плате и по расходам будут разнесены по этому имени журнала.</span><span class="sxs-lookup"><span data-stu-id="8352a-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="8352a-114">В поле **Имя журнала аренды** выберите журнал.</span><span class="sxs-lookup"><span data-stu-id="8352a-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="8352a-115">Все амортизации, проценты и записи изменения классификации краткосрочной аренды будут разнесены по этому имени журнала.</span><span class="sxs-lookup"><span data-stu-id="8352a-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="8352a-116">Если для параметра **Оплата поставщику** установлено значение **Нет** для книги аренды, записи арендных платежей и платежей по расходам также будут разнесены по этому имени журнала.</span><span class="sxs-lookup"><span data-stu-id="8352a-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>