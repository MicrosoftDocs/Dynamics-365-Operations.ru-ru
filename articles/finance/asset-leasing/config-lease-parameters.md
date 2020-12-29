---
title: Настройка параметров аренды (предварительная версия)
description: В этой теме описываются параметры конфигурации для аренды активов, такие как сведения о безопасности и параметры учета.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/28/2020
ms.locfileid: "4447403"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="06094-103">Настройка параметров аренды</span><span class="sxs-lookup"><span data-stu-id="06094-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="06094-104">Несколько параметров конфигурации влияют на поведение модуля аренды активов.</span><span class="sxs-lookup"><span data-stu-id="06094-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="06094-105">Эти параметры включают в себя имена журналов, общие параметры и настройки профиля разноски.</span><span class="sxs-lookup"><span data-stu-id="06094-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="06094-106">Перейдите в раздел **Аренда активов \> Настройка \> Параметры аренды активов**.</span><span class="sxs-lookup"><span data-stu-id="06094-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="06094-107">На вкладке **Аренды** выберите экспресс-вкладку **Общие**.</span><span class="sxs-lookup"><span data-stu-id="06094-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="06094-108">Параметр **Разрешить переопределение классификации вручную** определяет, можно ли переопределить классификацию аренды до подтверждения графика оплаты.</span><span class="sxs-lookup"><span data-stu-id="06094-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="06094-109">Параметр **Пакетная обработка между юридическими лицами** определяет, можно ли выполнять разноску других юридических лиц из текущего юридического лица.</span><span class="sxs-lookup"><span data-stu-id="06094-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="06094-110">Если этот параметр включен, можно создавать записи журнала для юридических лиц, к которым имеется доступ.</span><span class="sxs-lookup"><span data-stu-id="06094-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="06094-111">Установите для параметра **Разрешить удаление подтвержденных аренд** значение **Да**, чтобы разрешить удаление аренд, для которых подтверждены графики платежей.</span><span class="sxs-lookup"><span data-stu-id="06094-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="06094-112">Аренды не могут быть удалены, если с ними связаны разнесенные или неразнесенные проводки, независимо от значения этого параметра.</span><span class="sxs-lookup"><span data-stu-id="06094-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="06094-113">Восстановить запись аренды после ее удаления невозможно.</span><span class="sxs-lookup"><span data-stu-id="06094-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="06094-114">При отправке любых записей для удаленной аренды, вручную или через сущности данных, отправленная информация рассматривается как новая, а не как обновление существующей аренды.</span><span class="sxs-lookup"><span data-stu-id="06094-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="06094-115">Если для этого параметра задано значение **Да**, а тип перехода книги — **Накопительное дополнение, параметр A или B**, система устанавливает в поле **Приростная ставка процента на заемный капитал** значение поля **Приростная ставка процента на заемный капитал при переходе** на странице **Настройка книги**.</span><span class="sxs-lookup"><span data-stu-id="06094-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="06094-116">Если этот параметр имеет значение **Нет**, ставка в головной аренде устанавливается в значение поля **Приростная ставка процента на заемный капитал** на странице **Сведения о книге**, независимо от типа перехода книги.</span><span class="sxs-lookup"><span data-stu-id="06094-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="06094-117">Установите для параметра **Разрешить сторнирования амортизации для версии закрытой книги** значение **Да**, чтобы разрешить сторнирование проводок по затратам на амортизацию.</span><span class="sxs-lookup"><span data-stu-id="06094-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="06094-118">Проводки расходов могут быть сторнированы, даже если версия книги закрыта.</span><span class="sxs-lookup"><span data-stu-id="06094-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="06094-119">Рекомендуется оставить для этого параметра значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="06094-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="06094-120">Настройка этого параметра используется в качестве проверки и управления, чтобы предотвратить случайную амортизацию закрытой версии книги.</span><span class="sxs-lookup"><span data-stu-id="06094-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="06094-121">Если для параметра установлено значение **Нет**, вы помогаете сохранить точные расчеты остаточной стоимости и будущей амортизации.</span><span class="sxs-lookup"><span data-stu-id="06094-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
