---
title: Регистрация номенклатур для расширенных складских процессов с использованием журнала прихода номенклатуры
description: В этой процедуре показано, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при расширенного управления складами.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c25fb55afb01ed59b66045f24400e03e2ec60b2a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238902"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="09cbe-103">Регистрация номенклатур для расширенных складских процессов с использованием журнала прихода номенклатуры</span><span class="sxs-lookup"><span data-stu-id="09cbe-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="09cbe-104">В этой процедуре показано, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при расширенного управления складами.</span><span class="sxs-lookup"><span data-stu-id="09cbe-104">This procedure shows you how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="09cbe-105">Обычно эту задачу выполняет сотрудник, ответственный за приемку.</span><span class="sxs-lookup"><span data-stu-id="09cbe-105">This would usually be done by a receiving clerk.</span></span> 

<span data-ttu-id="09cbe-106">Чтобы выполнить эту процедуру, используйте компанию с демонстрационными данными USMF или собственные данные.</span><span class="sxs-lookup"><span data-stu-id="09cbe-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="09cbe-107">Необходимо иметь подтвержденный заказ на покупку с открытой строкой заказа на покупку перед началом выполнения этого руководства.</span><span class="sxs-lookup"><span data-stu-id="09cbe-107">You need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="09cbe-108">Номенклатура в строке должна быть учтена в запасах, в ней не должны использоваться варианты продукта, и она не должна иметь аналитики отслеживания.</span><span class="sxs-lookup"><span data-stu-id="09cbe-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="09cbe-109">Кроме того, номенклатура должна быть связана с процессом управления складами, включенной группой аналитик хранения.</span><span class="sxs-lookup"><span data-stu-id="09cbe-109">And the item needs to be associated with a warehouse management process enabled storage dimension group.</span></span> <span data-ttu-id="09cbe-110">Склад, который используется, необходимо разрешить для процессов управления складом, а местонахождение, которое используется для поступления, должно управляться номерными знаком.</span><span class="sxs-lookup"><span data-stu-id="09cbe-110">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span> <span data-ttu-id="09cbe-111">При использовании USMF можно использовать компанию 1001, склад 51 и номенклатуру M9200 для создания своего заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="09cbe-111">If you're using USMF, you can use company account 1001, Warehouse 51, and item M9200 to create your PO.</span></span> 

<span data-ttu-id="09cbe-112">Запишите номер созданного заказа на покупку, а также запишите код номенклатуры и сайта, используемых для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="09cbe-112">Make a note of the number of the purchase order that you create, and also note the item number and the site that you used for your purchase order line.</span></span>


## <a name="create-an-item-arrival-journal-header"></a><span data-ttu-id="09cbe-113">Создание заголовка журнала прибытия номенклатур</span><span class="sxs-lookup"><span data-stu-id="09cbe-113">Create an item arrival journal header</span></span>
1. <span data-ttu-id="09cbe-114">Перейдите к прибытию номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="09cbe-114">Go to Item arrival.</span></span>
2. <span data-ttu-id="09cbe-115">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="09cbe-115">Click New.</span></span>
3. <span data-ttu-id="09cbe-116">В поле "Имя" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-116">In the Name field, type a value.</span></span>
    * <span data-ttu-id="09cbe-117">При использовании USMF можно ввести WHS.</span><span class="sxs-lookup"><span data-stu-id="09cbe-117">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="09cbe-118">При использовании других данных журнал, имя которого выбрано, должен иметь следующие свойства: для параметра "Проверять ячейки комплектации" должно быть задано значение "Нет", для параметра "Управление карантином" должно быть задано значение "Нет".</span><span class="sxs-lookup"><span data-stu-id="09cbe-118">If you're using other data, the journal whose name you choose has to have the following properties: Check picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="09cbe-119">В поле "Число" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-119">In the Number field, type a value.</span></span>
5. <span data-ttu-id="09cbe-120">В поле "Сайт" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-120">In the Site field, type a value.</span></span>
    * <span data-ttu-id="09cbe-121">Выберите сайт, используемый для строки заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="09cbe-121">Select the site that you used for your purchase order line.</span></span> <span data-ttu-id="09cbe-122">Это будет значением по умолчанию, который будет по умолчанию применено ко всем строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="09cbe-122">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="09cbe-123">Если вы использовали склад 51 в USMF, выберите сайт 5.</span><span class="sxs-lookup"><span data-stu-id="09cbe-123">If you used warehouse 51 in USMF, choose site 5.</span></span>  
6. <span data-ttu-id="09cbe-124">В поле "Склад" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-124">In the Warehouse field, type a value.</span></span>
    * <span data-ttu-id="09cbe-125">Выберите допустимый склад для сайта, который выбран.</span><span class="sxs-lookup"><span data-stu-id="09cbe-125">Select a valid warehouse for the site that you've selected.</span></span> <span data-ttu-id="09cbe-126">Это будет значением по умолчанию, который будет по умолчанию применено ко всем строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="09cbe-126">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="09cbe-127">При использовании значения из примера в USMF выберите 51.</span><span class="sxs-lookup"><span data-stu-id="09cbe-127">If you're using the example values in USMF, select 51.</span></span>  
7. <span data-ttu-id="09cbe-128">В поле "Местонахождение" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-128">In the Location field, type a value.</span></span>
    * <span data-ttu-id="09cbe-129">Выберите допустимое местонахождения на складе, который выбран.</span><span class="sxs-lookup"><span data-stu-id="09cbe-129">Select a valid location in the warehouse that you've selected.</span></span> <span data-ttu-id="09cbe-130">Местонахождение должно быть связано с профилем местонахождения, которым управляет номерной знак.</span><span class="sxs-lookup"><span data-stu-id="09cbe-130">The location has to be associated with a location profile, which is license plate controlled.</span></span> <span data-ttu-id="09cbe-131">Это будет значением по умолчанию, который будет по умолчанию применено ко всем строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="09cbe-131">This will serve as a default value, which will default to all lines in the journal.</span></span> <span data-ttu-id="09cbe-132">При использовании значения из примера в USMF выберите Bulk-008.</span><span class="sxs-lookup"><span data-stu-id="09cbe-132">If you're using the example values in USMF, select Bulk-008.</span></span>  
8. <span data-ttu-id="09cbe-133">Щелкните правой кнопкой мыши стрелку вниз в поле номерных знаках, а затем "Просмотр сведений".</span><span class="sxs-lookup"><span data-stu-id="09cbe-133">Right-click on the drop-down arrow in the License plate field and then select View details.</span></span>
9. <span data-ttu-id="09cbe-134">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="09cbe-134">Click New.</span></span>
10. <span data-ttu-id="09cbe-135">В поле номерных знаков введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-135">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="09cbe-136">Запишите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-136">Make a note of the value.</span></span>  
11. <span data-ttu-id="09cbe-137">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="09cbe-137">Click Save.</span></span>
12. <span data-ttu-id="09cbe-138">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09cbe-138">Close the page.</span></span>
13. <span data-ttu-id="09cbe-139">В поле номерных знаков введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-139">In the License plate field, type a value.</span></span>
    * <span data-ttu-id="09cbe-140">Введите значение только что созданного номерного знака.</span><span class="sxs-lookup"><span data-stu-id="09cbe-140">Enter the value of the license plate that you just created.</span></span> <span data-ttu-id="09cbe-141">Это будет значением по умолчанию, который будет по умолчанию применено ко всем строкам журнала.</span><span class="sxs-lookup"><span data-stu-id="09cbe-141">This will serve as a default value, which will default to all lines in the journal.</span></span>  
14. <span data-ttu-id="09cbe-142">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09cbe-142">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="09cbe-143">Добавление строки</span><span class="sxs-lookup"><span data-stu-id="09cbe-143">Add a line</span></span>
1. <span data-ttu-id="09cbe-144">Щелкните "Добавить строку".</span><span class="sxs-lookup"><span data-stu-id="09cbe-144">Click Add line.</span></span>
2. <span data-ttu-id="09cbe-145">В поле "Код номенклатуры" введите значение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-145">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="09cbe-146">Введите код номенклатуры, использованный в строке заказа на покупку.</span><span class="sxs-lookup"><span data-stu-id="09cbe-146">Enter the item number that you used on the purchase order line.</span></span>  
3. <span data-ttu-id="09cbe-147">В поле "Количество" введите число.</span><span class="sxs-lookup"><span data-stu-id="09cbe-147">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="09cbe-148">Введите количество, которое требуется зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="09cbe-148">Enter the quantity that you want to register.</span></span>  
    * <span data-ttu-id="09cbe-149">Поле "Дата" определяет дату, когда количество в наличии этой номенклатуры будет зарегистрировано в запасах.</span><span class="sxs-lookup"><span data-stu-id="09cbe-149">The Date field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    * <span data-ttu-id="09cbe-150">Номер лота заполняется системой, если его можно однозначно идентифицировать по указанной информации.</span><span class="sxs-lookup"><span data-stu-id="09cbe-150">The lot ID will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="09cbe-151">В противном случае необходимо добавить его вручную.</span><span class="sxs-lookup"><span data-stu-id="09cbe-151">Otherwise you will have to add this manually.</span></span> <span data-ttu-id="09cbe-152">Это обязательное поле, которое связывает эту регистрацию с конкретной строкой документа-источника.</span><span class="sxs-lookup"><span data-stu-id="09cbe-152">This is a mandatory field, which links this registration to a specific source document line.</span></span>  

## <a name="complete-the-registration"></a><span data-ttu-id="09cbe-153">Завершение регистрации</span><span class="sxs-lookup"><span data-stu-id="09cbe-153">Complete the registration</span></span>
1. <span data-ttu-id="09cbe-154">Щелкните "Проверить".</span><span class="sxs-lookup"><span data-stu-id="09cbe-154">Click Validate.</span></span>
    * <span data-ttu-id="09cbe-155">При этом проверяется, готов ли журнал к разноске.</span><span class="sxs-lookup"><span data-stu-id="09cbe-155">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="09cbe-156">Если проверка завершилась ошибкой, потребуется исправить ошибки, прежде чем можно будет разнести журнал.</span><span class="sxs-lookup"><span data-stu-id="09cbe-156">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
2. <span data-ttu-id="09cbe-157">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09cbe-157">Click OK.</span></span>
    * <span data-ttu-id="09cbe-158">После нажатия кнопки "ОК" проверьте сообщение.</span><span class="sxs-lookup"><span data-stu-id="09cbe-158">After you clicked OK, check the message.</span></span> <span data-ttu-id="09cbe-159">Должно отобразиться сообщение о том, что журнал в норме.</span><span class="sxs-lookup"><span data-stu-id="09cbe-159">There should be a message saying that the journal is OK.</span></span>  
3. <span data-ttu-id="09cbe-160">Щелкните "Разнести".</span><span class="sxs-lookup"><span data-stu-id="09cbe-160">Click Post.</span></span>
4. <span data-ttu-id="09cbe-161">Нажмите кнопку "OК".</span><span class="sxs-lookup"><span data-stu-id="09cbe-161">Click OK.</span></span>
    * <span data-ttu-id="09cbe-162">После нажатия кнопки ОК проверьте строку сообщений.</span><span class="sxs-lookup"><span data-stu-id="09cbe-162">After you have clicked OK, check the message bar.</span></span> <span data-ttu-id="09cbe-163">Должно отобразиться сообщение о том, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="09cbe-163">There should be a message saying that the operation completed.</span></span>  
5. <span data-ttu-id="09cbe-164">Закройте страницу.</span><span class="sxs-lookup"><span data-stu-id="09cbe-164">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]