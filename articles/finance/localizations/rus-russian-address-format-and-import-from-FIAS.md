---
title: Российские форматы адреса
description: В этом разделе содержатся сведения о российских форматах адресов и импорте из FIAS.
author: v-nadyuz
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: roschlom
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 4a61f7e86e8403f5fdbacc79b5df5745ca28e996
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235108"
---
# <a name="russian-address-formats"></a><span data-ttu-id="aa51d-103">Российские форматы адреса</span><span class="sxs-lookup"><span data-stu-id="aa51d-103">Russian address formats</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa51d-104">Форматы адресов определяют, как будут выглядеть данные адреса при печати.</span><span class="sxs-lookup"><span data-stu-id="aa51d-104">Address formats determine how address data will appear when it's printed.</span></span> <span data-ttu-id="aa51d-105">В системе можно настроить форматы адресов для каждой страны или региона, в котором работает организация.</span><span class="sxs-lookup"><span data-stu-id="aa51d-105">In the system, you can set up address formats for every country or region where business is done.</span></span> <span data-ttu-id="aa51d-106">В России адреса имеют стандартную форму.</span><span class="sxs-lookup"><span data-stu-id="aa51d-106">In Russia, addresses have a standardized form.</span></span> <span data-ttu-id="aa51d-107">Однако могут быть включены дополнительные сведения, такие как район, код улицы, дополнение здания, здание, квартира, группа домов, группа квартир и земельный участок.</span><span class="sxs-lookup"><span data-stu-id="aa51d-107">However, additional information can be included, such as the district, street code, building complement, building, apartment, group of houses, group of flats, and land plot.</span></span>

<span data-ttu-id="aa51d-108">База данных адресов Федеральной информационной системы адресов (или FIAS) может потребоваться для предприятий в Российской Федерации.</span><span class="sxs-lookup"><span data-stu-id="aa51d-108">The Federal Informational Address System (or FIAS) address database might be required for businesses in the Russian Federation.</span></span> <span data-ttu-id="aa51d-109">Можно использовать специализированные средства для импорта FIAS в систему и поддержания ее актуальности.</span><span class="sxs-lookup"><span data-stu-id="aa51d-109">You can use specialized tools to import FIAS into your system and keep it up to date.</span></span> <span data-ttu-id="aa51d-110">В этом разделе описывается, как настроить и использовать механизмы импорта FIAS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-110">This topic explains how to set up and use the FIAS import mechanisms.</span></span>

## <a name="set-up-russian-address-formats"></a><span data-ttu-id="aa51d-111">Настройка российских форматов адресов</span><span class="sxs-lookup"><span data-stu-id="aa51d-111">Set up Russian address formats</span></span>

### <a name="set-up-the-address-format-country-or-region-state-or-province-county-city-and-postal-code"></a><span data-ttu-id="aa51d-112">Настройка формата адреса, страны или региона, региона или области, города и почтового кода</span><span class="sxs-lookup"><span data-stu-id="aa51d-112">Set up the address format, country or region, state or province, county, city and postal code</span></span>

1. <span data-ttu-id="aa51d-113">Перейдите **Администрирование организации** \> **Глобальная адресная книга** \> **Адреса** \> **Настройка адреса**, чтобы открыть страницу **Настройка адреса**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-113">Go to **Organization administration** \> **Global address book** \> **Addresses** \> **Address setup** to open the **Address setup** page.</span></span>
2. <span data-ttu-id="aa51d-114">На вкладках **Формат адреса**, **Страна/регион**, **Область/край**, **Район**, **Город** и **Почтовый индекс** можно настроить формат адреса, страну/регион, область/край, район, город и почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-114">On the **Address format**, **Country/region**, **State/province**, **County**, **City** and **ZIP/postal codes** tabs, you can set up the address format, country or region, state or province, county, city, and postal code.</span></span>

### <a name="set-up-a-new-district"></a><span data-ttu-id="aa51d-115">Настройка нового района</span><span class="sxs-lookup"><span data-stu-id="aa51d-115">Set up a new district</span></span>

1. <span data-ttu-id="aa51d-116">На странице **Настройка адреса** на вкладке **Район** выберите страну или регион, область или край, код района и код города.</span><span class="sxs-lookup"><span data-stu-id="aa51d-116">On the **Address setup** page, on the **District** tab, select the country or region, state or province, county code, and city code.</span></span>
2. <span data-ttu-id="aa51d-117">Выберите **Создать**, чтобы создать новый район для выбранной страны или региона, области или края, района и города.</span><span class="sxs-lookup"><span data-stu-id="aa51d-117">Select **New** to create a new district for the selected country or region, state or province, county, and city.</span></span>
3. <span data-ttu-id="aa51d-118">В поле **Район** введите уникальный код для района.</span><span class="sxs-lookup"><span data-stu-id="aa51d-118">In the **District** field, enter the unique code for the district.</span></span>
4. <span data-ttu-id="aa51d-119">В поле **Описание** введите официальное название района.</span><span class="sxs-lookup"><span data-stu-id="aa51d-119">In the **Description** field, enter the official name of the district.</span></span>
5. <span data-ttu-id="aa51d-120">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-120">In the **ZIP/postal code** field, select the postal code.</span></span>

    ![Вкладка "Район" на странице "Настройка адреса"](media/1%20Address%20setup.jpg)

6. <span data-ttu-id="aa51d-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-122">Select **Save**.</span></span>

### <a name="set-up-a-street-code"></a><span data-ttu-id="aa51d-123">Настройка кода улицы</span><span class="sxs-lookup"><span data-stu-id="aa51d-123">Set up a street code</span></span>

1. <span data-ttu-id="aa51d-124">На странице **Настройка адреса** на вкладке **Улица** убедитесь, что в поле **Страна/регион** выбран параметр **RUS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-124">On the **Address setup** page, on the **Street** tab, verify that **RUS** is selected in the **Country/region** field.</span></span>
2. <span data-ttu-id="aa51d-125">Выберите область или край, код района, код города и код района.</span><span class="sxs-lookup"><span data-stu-id="aa51d-125">Select the state or province, county code, city code, and district code.</span></span>
3. <span data-ttu-id="aa51d-126">Выберите **Создать**, чтобы создать новую улицу для выбранной страны или региона, области или края, района, города и микрорайона.</span><span class="sxs-lookup"><span data-stu-id="aa51d-126">Select **New** to create a new street for the selected country or region, state or province, county, city, and district.</span></span>
4. <span data-ttu-id="aa51d-127">В поле **Код улицы** введите уникальный код для улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-127">In the **Street code** field, enter the unique code for the street.</span></span>
5. <span data-ttu-id="aa51d-128">В поле **Улица** введите официальное название улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-128">In the **Street** field, enter the official name of the street.</span></span>
6. <span data-ttu-id="aa51d-129">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-129">In the **ZIP/postal code** field, select the postal code.</span></span>

    ![Вкладка "Улица" на странице "Настройка адреса"](media/2%20Address%20setup.jpg)

7. <span data-ttu-id="aa51d-131">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-131">Select **Save**.</span></span>

### <a name="set-up-a-group-of-houses"></a><span data-ttu-id="aa51d-132">Настройка группы домов</span><span class="sxs-lookup"><span data-stu-id="aa51d-132">Set up a group of houses</span></span>

1. <span data-ttu-id="aa51d-133">На странице **Настройка адреса** на вкладке **Группа домов** убедитесь, что в поле **Страна/регион** выбран параметр **RUS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-133">On the **Address setup** page, on the **Group of houses** tab, verify that **RUS** is selected in the **Country/region** field.</span></span>
2. <span data-ttu-id="aa51d-134">Выберите область или край, код района, код города, код микрорайона и код улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-134">Select the state or province, county code, city code, district code, and street code.</span></span>
3. <span data-ttu-id="aa51d-135">Выберите **Создать**, чтобы создать новую группу домов для выбранной страны или региона, области или края, района, города, микрорайона и улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-135">Select **New** to create a new group of houses for the selected country or region, state or province, county, city, district, and street.</span></span>
4. <span data-ttu-id="aa51d-136">В поле **Код группы домов** введите уникальный код для группы домов.</span><span class="sxs-lookup"><span data-stu-id="aa51d-136">In the **Group of houses code** field, enter the unique code for the group of houses.</span></span>
5. <span data-ttu-id="aa51d-137">В поле **Номера зданий** введите разделенный запятыми список номеров домов в группе.</span><span class="sxs-lookup"><span data-stu-id="aa51d-137">In the **Numbers of buildings** field, enter a comma-separated list of the building numbers of the houses in the group.</span></span>
6. <span data-ttu-id="aa51d-138">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-138">In the **ZIP/postal code** field, select the postal code.</span></span>

    ![Вкладка "Группа домов" на страниц "Настройка адреса"](media/3%20Address%20setup.jpg)

7. <span data-ttu-id="aa51d-140">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-140">Select **Save**.</span></span>

### <a name="set-up-a-group-of-flats"></a><span data-ttu-id="aa51d-141">Настройка группы квартир</span><span class="sxs-lookup"><span data-stu-id="aa51d-141">Set up a group of flats</span></span>

1. <span data-ttu-id="aa51d-142">На странице **Настройка адреса** на вкладке **Группа квартир** убедитесь, что в поле **Страна/регион** выбран параметр **RUS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-142">On the **Address setup** page, on the **Group of flats** tab, verify that **RUS** is selected in the **Country/region** field.</span></span>
2. <span data-ttu-id="aa51d-143">Выберите область или край, код района, код города, код микрорайона, код улицы и код группы домов.</span><span class="sxs-lookup"><span data-stu-id="aa51d-143">Select the state or province, county code, city code, district code, street code, and group of houses code.</span></span>
3. <span data-ttu-id="aa51d-144">Выберите **Создать**, чтобы создать новую группу квартир для выбранной страны или региона, области или края, района, города, микрорайона, улицы и группы домов.</span><span class="sxs-lookup"><span data-stu-id="aa51d-144">Select **New** to create a new group of flats for the selected country or region, state or province, county, city, district, street, and group of houses.</span></span>
4. <span data-ttu-id="aa51d-145">В поле **Код группы квартир** введите уникальный код для группы квартир.</span><span class="sxs-lookup"><span data-stu-id="aa51d-145">In the **Group of flats code** field, enter the unique code for the group of flats.</span></span>
5. <span data-ttu-id="aa51d-146">В поле **Группа квартир** введите разделенный запятыми список номеров квартир в группе.</span><span class="sxs-lookup"><span data-stu-id="aa51d-146">In the **Group of flats** field, enter a comma-separate list of the flat numbers of the flats in the group.</span></span>
6. <span data-ttu-id="aa51d-147">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-147">In the **ZIP/postal code** field, select the postal code.</span></span>

    ![Вкладка "Группа квартир" на страниц "Настройка адреса"](media/4%20Address%20setup.jpg)

7. <span data-ttu-id="aa51d-149">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-149">Select **Save**.</span></span>

### <a name="set-up-land-plots"></a><span data-ttu-id="aa51d-150">Настройка земельных участков</span><span class="sxs-lookup"><span data-stu-id="aa51d-150">Set up land plots</span></span>

1. <span data-ttu-id="aa51d-151">На странице **Настройка адреса** на вкладке **Земельные участки** убедитесь, что в поле **Страна/регион** выбран параметр **RUS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-151">On the **Address setup** page, on the **Land plots** tab, verify that **RUS** is selected in the **Country/region** field.</span></span>
2. <span data-ttu-id="aa51d-152">Выберите область или край, код района, код города, код микрорайона и код улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-152">Select the state or province, county code, city code, district code, and street code.</span></span>
3. <span data-ttu-id="aa51d-153">Выберите **Создать**, чтобы создать новый земельный участок для выбранной страны или региона, области или края, района, города, микрорайона и улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-153">Select **New** to create a new land plot for the selected country or region, state or province, county, city, district, and street.</span></span>
4. <span data-ttu-id="aa51d-154">В поле **Код земельного участка** введите уникальный код для земельного участка.</span><span class="sxs-lookup"><span data-stu-id="aa51d-154">In the **Land plot code** field, enter the unique code for the land plot.</span></span>
5. <span data-ttu-id="aa51d-155">В поле **Номера земельных участков** введите список разделенных запятой номеров земельных участков.</span><span class="sxs-lookup"><span data-stu-id="aa51d-155">In the **Numbers of land plots** field, enter a comma-separated list of the numbers of the land plots.</span></span>
6. <span data-ttu-id="aa51d-156">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-156">In the **ZIP/postal code** field, select the postal code.</span></span>

    ![Вкладка "Земельные участки" на странице "Настройка адреса"](media/5%20Address%20setup.jpg)

7. <span data-ttu-id="aa51d-158">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-158">Select **Save**.</span></span>

## <a name="create-an-address-for-a-customer"></a><span data-ttu-id="aa51d-159">Создание адреса для клиента</span><span class="sxs-lookup"><span data-stu-id="aa51d-159">Create an address for a customer</span></span>

1. <span data-ttu-id="aa51d-160">Перейдите в раздел **Расчеты с клиентами** \> **Клиенты** \> **Все клиенты**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-160">Go to **Accounts receivable** \> **Customers** \> **All customers**.</span></span>
2. <span data-ttu-id="aa51d-161">Откройте запись клиента, а затем на экспресс-вкладке **Адреса** выберите **Дополнительные параметры \> Дополнительно**, чтобы открыть страницу **Управление адресами**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-161">Open a customer record, and then, on the **Addresses** FastTab, select **More options \> Advanced** to open the **Manage addresses** page.</span></span>

    ![Экспресс-вкладка "Адреса" в записи клиента](media/6%20All%20customers.jpg)

3. <span data-ttu-id="aa51d-163">На экспресс- вкладке **Адрес** в поле **Страна/регион** выберите **RUS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-163">On the **Address** FastTab, in the **Country/region** field, select **RUS**.</span></span>
4. <span data-ttu-id="aa51d-164">В поле **Почтовый индекс** выберите почтовый индекс.</span><span class="sxs-lookup"><span data-stu-id="aa51d-164">In the **ZIP/postal code** field, select the postal code.</span></span> <span data-ttu-id="aa51d-165">После выбора почтового индекса в поле **Район** отображается код и название района.</span><span class="sxs-lookup"><span data-stu-id="aa51d-165">After you select a postal code, the **District** field shows the district code and name.</span></span>
5. <span data-ttu-id="aa51d-166">В поле **Код улицы** выберите код улицы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-166">In the **Street code** field, select the street code.</span></span> <span data-ttu-id="aa51d-167">Название улицы отображается в правой части поля **Код улицы** и в поле **Улица**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-167">The street name is shown on the right side of the **Street code** field and is also entered in the **Street** field.</span></span>
6. <span data-ttu-id="aa51d-168">В поле **Дополнение здания** введите название здания.</span><span class="sxs-lookup"><span data-stu-id="aa51d-168">In the **Building complement** field, enter the name of the building.</span></span> <span data-ttu-id="aa51d-169">Название здания также вводится в поле **Улица**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-169">The building name is also entered in the **Street** field.</span></span>
7. <span data-ttu-id="aa51d-170">В поле **Здание** введите номер здания.</span><span class="sxs-lookup"><span data-stu-id="aa51d-170">In the **Building** field, enter the building number.</span></span> <span data-ttu-id="aa51d-171">Номер здания также вводится в поле **Улица**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-171">The building number is also entered in the **Street** field.</span></span>
8. <span data-ttu-id="aa51d-172">В поле **Квартира** введите номер квартиры.</span><span class="sxs-lookup"><span data-stu-id="aa51d-172">In the **Apartment** field, enter the apartment number.</span></span> <span data-ttu-id="aa51d-173">Номер квартиры также вводится в поле **Улица**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-173">The apartment number is also entered in the **Street** field.</span></span>
9. <span data-ttu-id="aa51d-174">В поле **Группа домов** выберите код группы домов.</span><span class="sxs-lookup"><span data-stu-id="aa51d-174">In the **Group of houses** field, select the group of houses code.</span></span> <span data-ttu-id="aa51d-175">Отображаются соответствующие номера зданий.</span><span class="sxs-lookup"><span data-stu-id="aa51d-175">The corresponding building numbers are shown.</span></span>
10. <span data-ttu-id="aa51d-176">В поле **Группа квартир** выберите код группы квартир.</span><span class="sxs-lookup"><span data-stu-id="aa51d-176">In the **Group of flats** field, select the group of flats code.</span></span> <span data-ttu-id="aa51d-177">Отображаются соответствующие номера квартир.</span><span class="sxs-lookup"><span data-stu-id="aa51d-177">The corresponding flat numbers are shown.</span></span>

    ![Экспресс-вкладка "Адреса" на странице "Управление адресами"](media/7%20Manage%20addresses.jpg)

11. <span data-ttu-id="aa51d-179">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-179">Select **Save**.</span></span>

## <a name="import-from-fias"></a><span data-ttu-id="aa51d-180">Импорт из FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-180">Import from FIAS</span></span>

### <a name="import-an-fias-metadata-package"></a><span data-ttu-id="aa51d-181">Импорт пакета метаданных FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-181">Import an FIAS metadata package</span></span>

1. <span data-ttu-id="aa51d-182">Загрузите файл **RU FIAS – FiasMetadataPackage** на вкладке **Пакет данных** в общей библиотеке активов в Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="aa51d-182">Download the **RU FIAS – FiasMetadataPackage** file from the **Data package** tab of the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="aa51d-183">Этот пакетный файл содержит необходимые данные для выполнения заданий импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-183">This package file contains the required data for the import jobs runtime.</span></span>

    ![Общая библиотека активов в LCS](media/8%20Shared%20asset%20library.jpg)

2. <span data-ttu-id="aa51d-185">Перейдите **Администрирование системы** \> **Рабочие области** \> **Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-185">Go to **System administration** \> **Workspaces** \> **Data management**.</span></span>
3. <span data-ttu-id="aa51d-186">В разделе **Импорт/экспорт** выберите плитку **Импорт**, чтобы создать новое задание импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-186">In the **Import / Export** section, select the **Import** tile to create a new import job.</span></span>
    
    ![Снимок экрана поста в социальной сети, автоматически создается описание](media/9%20Data%20management.jpg)

4. <span data-ttu-id="aa51d-188">В поле **Имя группы** введите **ImportFiasMetadata**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-188">In the **Group name** field, enter **ImportFiasMetadata**.</span></span>
5. <span data-ttu-id="aa51d-189">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="aa51d-189">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="aa51d-190">На экспресс-вкладке **Выбранные объекты** выберите **Добавить файл** для добавления следующих файлов из скачанного ранее файла пакета:</span><span class="sxs-lookup"><span data-stu-id="aa51d-190">On the **Selected entities** FastTab, select **Add file** to add the following files from the package file that you downloaded earlier:</span></span>

    - <span data-ttu-id="aa51d-191">Сокращения адресов</span><span class="sxs-lookup"><span data-stu-id="aa51d-191">Abridgements of addresses</span></span>
    - <span data-ttu-id="aa51d-192">FiasEstateStatusEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-192">FiasEstateStatusEntity</span></span>
    - <span data-ttu-id="aa51d-193">FiasFlatTypeEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-193">FiasFlatTypeEntity</span></span>
    - <span data-ttu-id="aa51d-194">FIASOperationStatusesEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-194">FIASOperationStatusesEntity</span></span>
    - <span data-ttu-id="aa51d-195">FiasStructureStatusEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-195">FiasStructureStatusEntity</span></span>
  
   <span data-ttu-id="aa51d-196">После выбора каждого файла выберите **Отправить и добавить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-196">After you select each file, select **Upload and add**.</span></span>

7. <span data-ttu-id="aa51d-197">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-197">Select **Save**.</span></span>

    ![Снимок экрана поста в социальной сети, автоматически создается описание](media/10%20Import.jpg)

### <a name="set-up-a-template-to-import-fias-data"></a><span data-ttu-id="aa51d-199">Настройка шаблона для импорта данных FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-199">Set up a template to import FIAS data</span></span>

1. <span data-ttu-id="aa51d-200">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-200">Go to **System administration \> Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="aa51d-201">В разделе **Импорт/экспорт** выберите плитку **Шаблоны**, чтобы открыть страницу **Шаблон**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-201">In the **Import / Export** section, select the **Templates** tile to open the **Template** page.</span></span>
3. <span data-ttu-id="aa51d-202">Выберите **Создать** для создания нового шаблона.</span><span class="sxs-lookup"><span data-stu-id="aa51d-202">Select **New** to create a new template.</span></span>
4. <span data-ttu-id="aa51d-203">В поле **Код шаблона** введите уникальный идентификационный номер шаблона.</span><span class="sxs-lookup"><span data-stu-id="aa51d-203">In the **Template ID** field, enter the identification number of the template.</span></span>
5. <span data-ttu-id="aa51d-204">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="aa51d-204">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="aa51d-205">В поле **Статус шаблона** выберите **Проверен**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-205">In the **Template status** field, select **Validated**.</span></span>
7. <span data-ttu-id="aa51d-206">На экспресс-вкладке **Объекты** выберите **Добавить объект** для добавления следующих объектов данных:</span><span class="sxs-lookup"><span data-stu-id="aa51d-206">On the **Entities** FastTab, select **Add entity** to add the following data entities:</span></span>

    - <span data-ttu-id="aa51d-207">FiasAddressObjectEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-207">FiasAddressObjectEntity</span></span>
    - <span data-ttu-id="aa51d-208">FiasHouseEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-208">FiasHouseEntity</span></span>
    - <span data-ttu-id="aa51d-209">FiasSteadEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-209">FiasSteadEntity</span></span>
    - <span data-ttu-id="aa51d-210">FiasRoomEntity</span><span class="sxs-lookup"><span data-stu-id="aa51d-210">FiasRoomEntity</span></span>

    <span data-ttu-id="aa51d-211">После выбора каждого объекта в поле **Имя объекта** выберите **Добавить объект**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-211">After you select each entity in the **Entity name** field, select **Add entity**.</span></span>

8. <span data-ttu-id="aa51d-212">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-212">Select **Save**.</span></span>

    ![Снимок экрана поста в социальной сети, автоматически создается описание](media/11%20Template.jpg)

### <a name="set-up-a-job-for-a-full-fias-import"></a><span data-ttu-id="aa51d-214">Настройка задания для полного импорта FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-214">Set up a job for a full FIAS import</span></span>

<span data-ttu-id="aa51d-215">При первом импорте данных FIAS в систему следует создать задание для полного импорта FIAS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-215">When you import FIAS data into the system the first time, you should create a job for a full FIAS import.</span></span>

1. <span data-ttu-id="aa51d-216">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-216">Go to **System administration \> Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="aa51d-217">В разделе **Импорт/экспорт** выберите плитку **Импорт**, чтобы создать новое задание импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-217">In the **Import / Export** section, select the **Import** tile to create a new import job.</span></span>
3. <span data-ttu-id="aa51d-218">В поле **Имя группы** введите **FiasFullImportJob**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-218">In the **Group name** field, enter **FiasFullImportJob**.</span></span>
4. <span data-ttu-id="aa51d-219">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="aa51d-219">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="aa51d-220">На экспресс-вкладке **Выбранные объекты** выберите **Добавить шаблон**, чтобы добавить ранее созданный шаблон.</span><span class="sxs-lookup"><span data-stu-id="aa51d-220">On the **Selected entities** FastTab, select **Add template** to add the template that you created earlier.</span></span>
6. <span data-ttu-id="aa51d-221">В группе полей **Замена или объединение объекта** выберите **Объединить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-221">In the **Entity replace or merge** field group, select **Merge**.</span></span>
7. <span data-ttu-id="aa51d-222">В поле **Формат исходных данных** выберите **VerticalBarSeparated-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-222">In the **Source data format** field, select **VerticalBarSeparated-Unicode**.</span></span>
8. <span data-ttu-id="aa51d-223">Выберите **ОК**, затем выберите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-223">Select **OK**, and then select **Save**.</span></span>

    ![Снимок экрана поста в социальной сети, автоматически создается описание](media/12%20Import.jpg)

### <a name="set-up-a-job-to-import-fias-delta"></a><span data-ttu-id="aa51d-225">Настройка задания для импорта дельты FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-225">Set up a job to import FIAS delta</span></span>

<span data-ttu-id="aa51d-226">Для обновления существующих данных адреса следует создать задание для импорта дельты FIAS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-226">To update existing address data, you should create a job to import FIAS delta.</span></span>

1. <span data-ttu-id="aa51d-227">Загрузите файл **RU FIAS – FiasTransformations** на вкладке **Пакет данных** в общей библиотеке активов в LCS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-227">Download the **RU FIAS – FiasTransformations** file from the **Data package** tab of the Shared asset library in LCS.</span></span>
2. <span data-ttu-id="aa51d-228">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-228">Go to **System administration \> Workspaces \> Data management**.</span></span>
3. <span data-ttu-id="aa51d-229">В разделе **Импорт/экспорт** выберите плитку **Импорт**, чтобы создать новое задание импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-229">In the **Import / Export** section, select the **Import** tile to create a new import job.</span></span>
4. <span data-ttu-id="aa51d-230">В поле **Имя группы** введите **FiasDeltaImportJob**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-230">In the **Group name** field, enter **FiasDeltaImportJob**.</span></span>
5. <span data-ttu-id="aa51d-231">В поле **Описание** введите описание.</span><span class="sxs-lookup"><span data-stu-id="aa51d-231">In the **Description** field, enter a description.</span></span>
6. <span data-ttu-id="aa51d-232">На экспресс-вкладке **Выбранные объекты** выберите **Добавить шаблон**, чтобы добавить ранее созданный шаблон.</span><span class="sxs-lookup"><span data-stu-id="aa51d-232">On the **Selected entities** FastTab, select **Add template** to add the template that you created earlier.</span></span>
7. <span data-ttu-id="aa51d-233">В группе полей **Замена или объединение объекта** выберите **Объединить**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-233">In the **Entity replace or merge** field group, select **Merge**.</span></span>
8. <span data-ttu-id="aa51d-234">В поле **Формат исходных данных** выберите **XML-Attribute**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-234">In the **Source data format** field, select **XML-Attribute**.</span></span>
9. <span data-ttu-id="aa51d-235">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-235">Select **OK**.</span></span>

    ![Автоматически создается снимок экрана описания мобильного телефона](media/13%20Import.jpg)

10. <span data-ttu-id="aa51d-237">Для каждого объекта выберите кнопку в столбце **Просмотр карты**, чтобы открыть страницу **Сопоставить исходные данные с промежуточными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-237">For each entity, select the button in the **View map** column to open the **Map source to staging** page.</span></span>

    ![Автоматически создается снимок экрана описания мобильного телефона](media/14%20Map%20source%20to%20staging.jpg)

11. <span data-ttu-id="aa51d-239">На вкладке **Преобразования** выберите **Создать**, а затем выберите **Отправить файл**, чтобы открыть диалоговое окно **Выбор файла**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-239">On the **Transformations** tab, select **New**, and then select **Upload file** to open the **Select a file** dialog box.</span></span>
12. <span data-ttu-id="aa51d-240">Выберите **Обзор** и выберите следующие преобразования:</span><span class="sxs-lookup"><span data-stu-id="aa51d-240">Select **Browse**, and select the following transformations:</span></span>

    - <span data-ttu-id="aa51d-241">Для объекта **FiasAddressObjectEntity** выберите преобразование **fiasAddrObjTrans**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-241">For the **FiasAddressObjectEntity** entity, select the **fiasAddrObjTrans** transformation.</span></span>
    - <span data-ttu-id="aa51d-242">Для объекта **FiasHouseEntity** выберите преобразование **fiasHousesTrans**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-242">For the **FiasHouseEntity** entity, select the **fiasHousesTrans** transformation.</span></span>
    - <span data-ttu-id="aa51d-243">Для объекта **FiasSteadEntity** выберите преобразование **fiasSteadsTrans**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-243">For the **FiasSteadEntity** entity, select the **fiasSteadsTrans** transformation.</span></span>
    - <span data-ttu-id="aa51d-244">Для объекта **FiasRoomEntity** выберите преобразование **fiasRoomsTrans**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-244">For the **FiasRoomEntity** entity, select the **fiasRoomsTrans** transformation.</span></span>

## <a name="fias-import"></a><span data-ttu-id="aa51d-245">Импорт FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-245">FIAS import</span></span>

### <a name="do-a-full-fias-import-to-an-empty-database"></a><span data-ttu-id="aa51d-246">Выполнение полного импорта FIAS в пустую базу данных</span><span class="sxs-lookup"><span data-stu-id="aa51d-246">Do a full FIAS import to an empty database</span></span>

<span data-ttu-id="aa51d-247">Так как полная база данных FIAS содержит очень большое число записей, при импорте могут возникнуть некоторые проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="aa51d-247">Because the full FIAS database contains a very large number of records, some performance issues might occur during import.</span></span> <span data-ttu-id="aa51d-248">Чтобы предотвратить возникновение этих неполадок, при первом импорте следует использовать файл базы данных FIAS в формате TXT.</span><span class="sxs-lookup"><span data-stu-id="aa51d-248">To help prevent these issues, the first time that you do an import, you should use the FIAS database file in TXT format.</span></span> <span data-ttu-id="aa51d-249">Этот файл можно найти в общей библиотеке ресурсов LCS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-249">You can find this file in the Shared asset library in LCS.</span></span> <span data-ttu-id="aa51d-250">Он содержит базу данных FIAS на 1 декабря, 2018 г.</span><span class="sxs-lookup"><span data-stu-id="aa51d-250">It contains the FIAS database on December 1, 2018.</span></span>

1. <span data-ttu-id="aa51d-251">Загрузите файл **RU FIAS - addrObjCSV** на вкладке **Пакет данных** в общей библиотеке активов в LCS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-251">Download the **RU FIAS - addrObjCSV** file from the **Data package** tab of the Shared asset library in LCS.</span></span> <span data-ttu-id="aa51d-252">Убедитесь, что файл содержит файл AS_ADDROBJ_20181216_\<number of state\>. txt и при необходимости файлы House, Stead и Room.</span><span class="sxs-lookup"><span data-stu-id="aa51d-252">Verify that the file contains the AS_ADDROBJ_20181216_\<number of state\>.txt file and, optionally, House, Stead, and Room files.</span></span>
2. <span data-ttu-id="aa51d-253">Создайте ZIP-архив, содержащий файлы из загруженного пакета для одного или нескольких состояний.</span><span class="sxs-lookup"><span data-stu-id="aa51d-253">Create a zip archive that contains the files from the downloaded package for one or more states.</span></span>
3. <span data-ttu-id="aa51d-254">Перейдите в раздел **Администрирование организации \> Глобальная адресная книга \> Импорт из FIAS**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-254">Go to **Organization administration \> Global address book \> Import from FIAS**.</span></span>
4. <span data-ttu-id="aa51d-255">Выберите **Импорт FIAS**, чтобы открыть диалоговое окно **Импорт данных**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-255">Select **Import FIAS** to open the **Import of data** dialog box.</span></span>
5. <span data-ttu-id="aa51d-256">На экспресс-вкладке **Параметры** выберите **Обзор**, чтобы выбрать архив ZIP, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="aa51d-256">On the **Parameters** FastTab, select **Browse** to select the zip archive that you created earlier.</span></span>
6. <span data-ttu-id="aa51d-257">Для параметра **Полный импорт** выберите значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-257">Set the **Full import** option to **Yes**.</span></span>
7. <span data-ttu-id="aa51d-258">Если планируется импорт домов и участков, установите для параметра **Включает дома** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-258">If you intend to import houses and steads, set the **Does include houses** option to **Yes**.</span></span>
8. <span data-ttu-id="aa51d-259">Если планируется импорт помещений, установите для параметра **Включает помещения** значение **Да**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-259">If you intend to import rooms, set the **Does include rooms** option to **Yes**.</span></span>

    ![Область импорта данных](media/15%20Import%20of%20data.jpg)

9. <span data-ttu-id="aa51d-261">Выберите **ОК**, чтобы начать импорт.</span><span class="sxs-lookup"><span data-stu-id="aa51d-261">Select **OK** to start the import.</span></span>
10. <span data-ttu-id="aa51d-262">Выберите **Обновить** в правом верхнем углу страницы, чтобы просмотреть строку вместе с результатами полного импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-262">Select **Refresh** in the upper right of the page to view the line together with the results of the full import.</span></span>
    
    ![Вкладка "Параметры"](media/16%20Import%20from%20FIAS.jpg)

### <a name="update-addresses-from-fias"></a><span data-ttu-id="aa51d-264">Обновление адресов из FIAS</span><span class="sxs-lookup"><span data-stu-id="aa51d-264">Update addresses from FIAS</span></span>

1. <span data-ttu-id="aa51d-265">Загрузите базу данных с даты последнего обновления из <https://fias.nalog.ru/>.</span><span class="sxs-lookup"><span data-stu-id="aa51d-265">Download the database from the last update date from <https://fias.nalog.ru/>.</span></span>
2.  <span data-ttu-id="aa51d-266">Выберите загруженную базу данных в формате ZIP и выполните импорт так же, как и в предыдущем разделе</span><span class="sxs-lookup"><span data-stu-id="aa51d-266">Select the downloaded database in ZIP format, and do the import just as you did in the previous section.</span></span> <span data-ttu-id="aa51d-267">Однако в диалоговом окне **Импорт данных** задайте для параметра **Полный импорт** значение **Нет**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-267">However, in the **Import of data** dialog box, set the **Full import** option to **No**.</span></span>

### <a name="tips-for-speeding-up-the-import-process"></a><span data-ttu-id="aa51d-268">Советы по ускорению процесса импорта</span><span class="sxs-lookup"><span data-stu-id="aa51d-268">Tips for speeding up the import process</span></span>

<span data-ttu-id="aa51d-269">Время, необходимое для импорта данных FIAS, зависит от объема импортируемых данных и настройки системы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-269">The time that is required to import FIAS data depends on the amount of data that is being imported and the system setup.</span></span> <span data-ttu-id="aa51d-270">Ниже приведены несколько советов, которые могут помочь ускорить процесс импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-270">Here are some tips that might help speed up the import process.</span></span>

<span data-ttu-id="aa51d-271">Попробуйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="aa51d-271">Try the following procedure:</span></span>

1. <span data-ttu-id="aa51d-272">Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление данными**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-272">Go to **System administration \> Workspaces \> Data management**.</span></span>
2. <span data-ttu-id="aa51d-273">В разделе **Импорт/экспорт** выберите плитку **Параметры структуры**, чтобы открыть страницу **Параметры структуры импорта и экспорта данных**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-273">In the **Import / Export** section, select the **Framework parameters** tile to open the **Data import/export framework parameters** page.</span></span>
3. <span data-ttu-id="aa51d-274">На вкладке **Параметры объекта** выберите **Настройка параметров выполнения объекта**, чтобы открыть страницу **Параметры выполнения импорта объектов**.</span><span class="sxs-lookup"><span data-stu-id="aa51d-274">On the **Entity settings** tab, select **Configure entity execution parameters** to open the **Entity import execution parameters** page.</span></span>
4. <span data-ttu-id="aa51d-275">Задайте следующие поля для настройки многопоточности для объектов FIAS, используемых в заданиях импорта:</span><span class="sxs-lookup"><span data-stu-id="aa51d-275">Set the following fields to configure multithreading for FIAS entities that are used in import jobs:</span></span>

    - <span data-ttu-id="aa51d-276">В поле **Объект** выберите объект FIAS.</span><span class="sxs-lookup"><span data-stu-id="aa51d-276">In the **Entity** field, select the FIAS entity.</span></span>
    - <span data-ttu-id="aa51d-277">В поле **Счетчик пороговых записей импорта** введите пороговое количество записей для импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-277">In the **Import threshold record count** field, enter the threshold record count for import.</span></span>
    - <span data-ttu-id="aa51d-278">В поле **Счетчик задач импорта** введите количество задач импорта.</span><span class="sxs-lookup"><span data-stu-id="aa51d-278">In the **Import task count** field, enter the count of import tasks.</span></span>

      ![Параметры выполнения импорта объекта](media/17%20Entity%20import%20execution%20parameters.jpg)

<span data-ttu-id="aa51d-280">При выполнении задания полного импорта необходимо одновременно указать несколько регионов, но не все регионы.</span><span class="sxs-lookup"><span data-stu-id="aa51d-280">When you run a full import job, provide several regions, but not all regions, at the same time.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]