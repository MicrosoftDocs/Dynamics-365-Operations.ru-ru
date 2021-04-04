---
title: Миграция типа данных валюты для двойной записи
description: В этом разделе описывается, как изменить число десятичных знаков, поддерживаемое двойной записью для валюты.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 78820ff49958fc3b474038c0fcd126bcf6886d0d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560831"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="7e213-103">Миграция типа данных валюты для двойной записи</span><span class="sxs-lookup"><span data-stu-id="7e213-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7e213-104">Можно увеличить число десятичных знаков, поддерживаемое для денежных значений, до максимум 10.</span><span class="sxs-lookup"><span data-stu-id="7e213-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="7e213-105">Предел по умолчанию равен четырем десятичным знакам.</span><span class="sxs-lookup"><span data-stu-id="7e213-105">The default limit is four decimal places.</span></span> <span data-ttu-id="7e213-106">Увеличивая число десятичных разрядов, можно помочь предотвратить потерю данных при использовании двойной записи для синхронизации данных.</span><span class="sxs-lookup"><span data-stu-id="7e213-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="7e213-107">Увеличение количества десятичных разрядов является изменением по выбору.</span><span class="sxs-lookup"><span data-stu-id="7e213-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="7e213-108">Чтобы его реализовать, вам необходимо обратиться за помощью в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7e213-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="7e213-109">Процесс изменения числа знаков после запятой имеет два шага:</span><span class="sxs-lookup"><span data-stu-id="7e213-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="7e213-110">Запросите миграцию в Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7e213-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="7e213-111">Измените число знаков после запятой в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7e213-111">Change the number of decimal places in Dataverse.</span></span>

<span data-ttu-id="7e213-112">Приложение Finance and Operations и Dataverse должны поддерживать одинаковое число десятичных разрядов в значениях валют.</span><span class="sxs-lookup"><span data-stu-id="7e213-112">The Finance and Operations app and Dataverse must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="7e213-113">В противном случае при синхронизации этих данных между приложениями может произойти потеря данных.</span><span class="sxs-lookup"><span data-stu-id="7e213-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="7e213-114">Процесс миграции перенастраивает способ хранения значений валют и валютных курсов, но не изменяет никаких данных.</span><span class="sxs-lookup"><span data-stu-id="7e213-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="7e213-115">После завершения миграции можно увеличить число десятичных разрядов для кодов валют и цен, а данные, вводимые пользователями и отображаемые пользователем, могут иметь большую точность для десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="7e213-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="7e213-116">Миграция не является обязательной.</span><span class="sxs-lookup"><span data-stu-id="7e213-116">Migration is optional.</span></span> <span data-ttu-id="7e213-117">Если вам может пригодиться поддержка большего числа десятичных разрядов, рекомендуется рассмотреть возможность миграции.</span><span class="sxs-lookup"><span data-stu-id="7e213-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="7e213-118">Для организаций, в которых не требуется наличие значений, имеющих более четырех десятичных знаков, миграция не требуется.</span><span class="sxs-lookup"><span data-stu-id="7e213-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="7e213-119">Запрос миграции в Microsoft</span><span class="sxs-lookup"><span data-stu-id="7e213-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="7e213-120">Хранилище для существующих столбцов валюты в Dataverse не может поддерживать более четырех десятичных разрядов.</span><span class="sxs-lookup"><span data-stu-id="7e213-120">Storage for existing currency columns in Dataverse can't support more than four decimal places.</span></span> <span data-ttu-id="7e213-121">Таким образом, в процессе миграции значения валют копируются в новые внутренние столбцы базы данных.</span><span class="sxs-lookup"><span data-stu-id="7e213-121">Therefore, during the migration process, currency values are copied to new internal columns in the database.</span></span> <span data-ttu-id="7e213-122">Этот процесс выполняется непрерывно, пока не будут перенесены все данные.</span><span class="sxs-lookup"><span data-stu-id="7e213-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="7e213-123">Внутри в конце миграции новые типы хранилищ заменяют старые типы хранилищ, но значения данных не изменяются.</span><span class="sxs-lookup"><span data-stu-id="7e213-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="7e213-124">Столбцы валюты могут поддерживать до 10 десятичных разрядов.</span><span class="sxs-lookup"><span data-stu-id="7e213-124">The currency columns can then support up to 10 decimal places.</span></span> <span data-ttu-id="7e213-125">В процессе миграции служба Dataverse может продолжать использоваться без перерывов.</span><span class="sxs-lookup"><span data-stu-id="7e213-125">During the migration process, Dataverse can continue to be used without interruption.</span></span>

<span data-ttu-id="7e213-126">В то же время валютные курсы изменяются таким образом, чтобы они поддерживали до 12 десятичных разрядов вместо текущего предельного значения 10.</span><span class="sxs-lookup"><span data-stu-id="7e213-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="7e213-127">Это изменение необходимо для того, чтобы число знаков после запятой было одинаковым как в приложении Finance and Operations, так и в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="7e213-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Dataverse.</span></span>

<span data-ttu-id="7e213-128">При миграции никакие данные не изменяются.</span><span class="sxs-lookup"><span data-stu-id="7e213-128">Migration doesn't change any data.</span></span> <span data-ttu-id="7e213-129">После преобразования столбцов валюты и валютного курса администраторы могут настроить систему на использование до 10 десятичных разрядов для столбцов валюты, указав число десятичных знаков для каждой валюты проводки и для цены.</span><span class="sxs-lookup"><span data-stu-id="7e213-129">After the currency and exchange rate columns are converted, admins can configure the system to use up to 10 decimal places for currency columns by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="7e213-130">Запрос на миграцию</span><span class="sxs-lookup"><span data-stu-id="7e213-130">Request a migration</span></span>

<span data-ttu-id="7e213-131">Чтобы эта функция была доступна, отправьте сообщение электронной почты по адресу **CDSExpandDecimal@microsoft.com** и включите следующую информацию:</span><span class="sxs-lookup"><span data-stu-id="7e213-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="7e213-132">**Тема:** Запрос на включение расширенной десятичной поддержки для \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="7e213-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="7e213-133">**Текст:** Я хочу включить расширенную поддержку десятичных знаков для моей организации \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="7e213-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="7e213-134">Представитель корпорации Майкрософт свяжется с вами в течение двух-трех рабочих дней для выполнения следующих шагов.</span><span class="sxs-lookup"><span data-stu-id="7e213-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="7e213-135">При запросе на миграцию необходимо ознакомиться со следующими подробностями и спланировать их соответствующим образом:</span><span class="sxs-lookup"><span data-stu-id="7e213-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="7e213-136">Время, необходимое для переноса данных, зависит от объема данных в системе.</span><span class="sxs-lookup"><span data-stu-id="7e213-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="7e213-137">Миграция больших баз данных может занять несколько дней.</span><span class="sxs-lookup"><span data-stu-id="7e213-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="7e213-138">Размер базы данных временно увеличивается во время выполнения миграции, так как для индексов требуется дополнительное пространство.</span><span class="sxs-lookup"><span data-stu-id="7e213-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="7e213-139">Большая часть дополнительного пространства освобождается после завершения миграции.</span><span class="sxs-lookup"><span data-stu-id="7e213-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="7e213-140">Если в процессе миграции возникают ошибки, которые не позволят выполнить миграцию, система создает оповещения в службе технической поддержки Майкрософт, так что сотрудники службы поддержки могут вмешаться.</span><span class="sxs-lookup"><span data-stu-id="7e213-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="7e213-141">Однако даже в том случае, если во время миграции возникают ошибки, служба Dataverse остается полностью доступной для обычного использования.</span><span class="sxs-lookup"><span data-stu-id="7e213-141">However, even if errors occur during the migration, Dataverse remains fully available for regular use.</span></span>
+ <span data-ttu-id="7e213-142">Процесс миграции не является обратимым.</span><span class="sxs-lookup"><span data-stu-id="7e213-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="7e213-143">Изменение числа десятичных знаков</span><span class="sxs-lookup"><span data-stu-id="7e213-143">Changing the number of decimal places</span></span>

<span data-ttu-id="7e213-144">После завершения миграции служба Dataverse может сохранить числа с большим числом десятичных знаков.</span><span class="sxs-lookup"><span data-stu-id="7e213-144">After the migration is completed, Dataverse can store numbers that have more decimal places.</span></span> <span data-ttu-id="7e213-145">Администраторы могут указать, сколько десятичных разрядов используется для разных кодов валют и для ценообразования.</span><span class="sxs-lookup"><span data-stu-id="7e213-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="7e213-146">Пользователи Microsoft Power Apps, Power BI и Power Automate смогут просматривать и использовать числа с большим числом знаков после запятой.</span><span class="sxs-lookup"><span data-stu-id="7e213-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="7e213-147">Для выполнения этого изменения необходимо обновить следующие параметры в Power Apps:</span><span class="sxs-lookup"><span data-stu-id="7e213-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="7e213-148">**Системные параметры: точность валюты для ценообразования** — столбец **Задать точность валюты, используемую для ценообразования во всей системе** определяет, как данная валюта будет вести себя в организации при выборе параметра **Точность цены**.</span><span class="sxs-lookup"><span data-stu-id="7e213-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** column defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="7e213-149">**Управление бизнесом: валюты** — столбец **Точность валюты** позволяет указать пользовательское число десятичных разрядов для конкретной валюты.</span><span class="sxs-lookup"><span data-stu-id="7e213-149">**Business Management: Currencies** – The **Currency Precision** column lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="7e213-150">Имеется резервный вариант настройки в масштабе всей организации.</span><span class="sxs-lookup"><span data-stu-id="7e213-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="7e213-151">Имеются некоторые ограничения:</span><span class="sxs-lookup"><span data-stu-id="7e213-151">There are some limitations:</span></span>

+ <span data-ttu-id="7e213-152">Невозможно настроить столбец валюты в таблице.</span><span class="sxs-lookup"><span data-stu-id="7e213-152">You can't configure the currency column on a table.</span></span>
+ <span data-ttu-id="7e213-153">Можно указать более четырех знаков после запятой только на уровнях **Ценообразование** и **Валюта проводки**.</span><span class="sxs-lookup"><span data-stu-id="7e213-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="7e213-154">Параметры системы: точность валюты для ценообразования</span><span class="sxs-lookup"><span data-stu-id="7e213-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="7e213-155">После завершения миграции администраторы могут задать точность валюты.</span><span class="sxs-lookup"><span data-stu-id="7e213-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="7e213-156">Перейдите к пункту **Параметры \> Администрирование** и выберите **Параметры системы**.</span><span class="sxs-lookup"><span data-stu-id="7e213-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="7e213-157">Затем на вкладке **Общие** измените значение в столбце **Задать точность валюты, используемую для ценообразования во всей системе**, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7e213-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** column, as shown in the following illustration.</span></span>

![Параметры системы для валюты](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="7e213-159">Управление бизнесом: валюты</span><span class="sxs-lookup"><span data-stu-id="7e213-159">Business Management: Currencies</span></span>

<span data-ttu-id="7e213-160">Если требуется, чтобы точность конкретной валюты отличалась от точности валюты, используемой для ценообразования, ее можно изменить.</span><span class="sxs-lookup"><span data-stu-id="7e213-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="7e213-161">Перейдите к пункту **Параметры \> Управление бизнесом**, выберите **Валюты** и выберите валюту, которую необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="7e213-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="7e213-162">Затем задайте в столбце **Точность валюты** нужное число десятичных знаков, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7e213-162">Then set the **Currency Precision** column to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Параметры валюты для определенных региональных параметров](media/specific-currency.png)

### <a name="tables-currency-column"></a><span data-ttu-id="7e213-164">таблицы: столбец валюты</span><span class="sxs-lookup"><span data-stu-id="7e213-164">tables: Currency column</span></span>

<span data-ttu-id="7e213-165">Число десятичных разрядов, которые могут быть настроены для некоторых столбцов валюты, ограничивается четырьмя.</span><span class="sxs-lookup"><span data-stu-id="7e213-165">The number of decimal places that can be configured for specific currency columns is limited to four.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]