---
title: Шаблоны спецификаций
description: В шаблоне спецификации имеется стандартизированный список компонентов объектов сервисного обслуживания, которые регулярно обслуживаются.
author: ShylaThompson
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 70b514aeed48180bb1b14be8b3d95d55d44d2ca8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824341"
---
# <a name="template-boms"></a><span data-ttu-id="b5509-103">Шаблоны спецификаций</span><span class="sxs-lookup"><span data-stu-id="b5509-103">Template BOMs</span></span>    

[!include [banner](../includes/banner.md)]


<span data-ttu-id="b5509-104">В шаблоне спецификации имеется стандартизированный список компонентов объектов сервисного обслуживания, которые регулярно обслуживаются.</span><span class="sxs-lookup"><span data-stu-id="b5509-104">A template bill of materials (BOM) provides you with a standardized list of components for service objects that are serviced regularly.</span></span> <span data-ttu-id="b5509-105">Компоненты, перечисленные в шаблоне спецификации, представляют собой индивидуальные подкомпоненты объекта сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-105">The components that are listed in the template BOM represent the individual subcomponents of the service object.</span></span> <span data-ttu-id="b5509-106">При применении шаблона спецификации к объекту сервисного обслуживания можно зафиксировать подкомпоненты, которые были заменены в объекте сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-106">By applying a template BOM to a service object, you can keep a record of the subcomponents that have been replaced on the service object.</span></span>

<span data-ttu-id="b5509-107">Чтобы применить шаблон спецификации к соглашению на обслуживание или к заказу на обслуживание, присоедините его к отношению объекта обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-107">To apply a template BOM to a service agreement or a service order, you attach it to a service object relation.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b5509-108">К объекту сервисного обслуживание применяется только один шаблон спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-108">You can apply only one template BOM to a service object.</span></span></P>

## <a name="create-a-template-bom"></a><span data-ttu-id="b5509-109">Создание шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="b5509-109">Create a template BOM</span></span>

<span data-ttu-id="b5509-110">В следующей таблице содержатся сведения о различных методах создания шаблона спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-110">The following table contains information about the various methods that you can use to create a template BOM.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b5509-111">Метод</span><span class="sxs-lookup"><span data-stu-id="b5509-111">Method</span></span></p></th>
<th><p><span data-ttu-id="b5509-112">описание</span><span class="sxs-lookup"><span data-stu-id="b5509-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5509-113">Производство</span><span class="sxs-lookup"><span data-stu-id="b5509-113">Production</span></span></p></td>
<td><p><span data-ttu-id="b5509-114">Шаблон спецификации основан на производственном заказе.</span><span class="sxs-lookup"><span data-stu-id="b5509-114">The template BOM is based on a production order.</span></span> <span data-ttu-id="b5509-115">Этот вариант применяется только в производственной среде.</span><span class="sxs-lookup"><span data-stu-id="b5509-115">This option is applicable only if you operate in a production environment.</span></span> <span data-ttu-id="b5509-116">Здесь преимуществом является то, что имеется текущий подробный список компонентов, составляющих номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b5509-116">The benefit is that you have a current, detailed listing of the components that make up an item.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5509-117">Номенклатура BOM</span><span class="sxs-lookup"><span data-stu-id="b5509-117">Item BOM</span></span></p></td>
<td><p><span data-ttu-id="b5509-118">Шаблон спецификации основан на номенклатуре спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-118">The template BOM is based on an item BOM.</span></span> <span data-ttu-id="b5509-119">Номенклатура спецификации в отличие от производственной спецификации является статическим списком компонентов, составляющих номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b5509-119">The item BOM, unlike the production BOM, is a static list of the components that make up an item.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5509-120">Существующий шаблон</span><span class="sxs-lookup"><span data-stu-id="b5509-120">Existing template</span></span></p></td>
<td><p><span data-ttu-id="b5509-121">Шаблон основан на существующем шаблоне спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-121">The template is based on an existing template BOM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5509-122">Вручную</span><span class="sxs-lookup"><span data-stu-id="b5509-122">Manual</span></span></p></td>
<td><p><span data-ttu-id="b5509-123">Если известны запасные части, которые обычно заменяются в объекте сервисного обслуживания, шаблон спецификации можно создать вручную.</span><span class="sxs-lookup"><span data-stu-id="b5509-123">If you know what spare parts are typically replaced on a service object, you can create your template BOM manually.</span></span> <span data-ttu-id="b5509-124">Этот метод гарантирует, что компоненты, включенные в шаблон, отражают фактические требования рабочего места.</span><span class="sxs-lookup"><span data-stu-id="b5509-124">This method helps make sure that the components that are included in the template reflect the actual requirements of your workplace.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a><span data-ttu-id="b5509-125">Применение шаблона спецификации к соглашению о сервисном обслуживании или к заказу на сервисное обслуживание</span><span class="sxs-lookup"><span data-stu-id="b5509-125">Apply the template BOM to a service agreement or service order</span></span>

<span data-ttu-id="b5509-126">Шаблон спецификации можно применить к соглашению о сервисном обслуживании и к заказу на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b5509-126">You can apply a template BOM to a service agreement, a service order, or both.</span></span> <span data-ttu-id="b5509-127">Соглашение на обслуживание обычно охватывает долгосрочные отношения с клиентом.</span><span class="sxs-lookup"><span data-stu-id="b5509-127">The service agreement usually covers a long-term relationship with a customer.</span></span> <span data-ttu-id="b5509-128">История замен, записанная в спецификации сервисного обслуживания, содержит полезные данные для соглашения о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="b5509-128">The history of replacements that is recorded in the service BOM is useful data to have for the service agreement.</span></span>

<span data-ttu-id="b5509-129">Шаблон спецификации также применяется к заказу на сервисное обслуживание для записи истории обслуживания, выполненного для объекта сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-129">You can also apply a template BOM to a service order to record the history of the service that has been performed on a service object.</span></span>

## <a name="copy-the-history-of-a-service-bom"></a><span data-ttu-id="b5509-130">Копирование истории спецификации обслуживания</span><span class="sxs-lookup"><span data-stu-id="b5509-130">Copy the history of a service BOM</span></span>

<span data-ttu-id="b5509-131">Историю строки спецификации сервисного обслуживания можно скопировать из одного соглашения о сервисном обслуживании в другое соглашение о сервисном обслуживании.</span><span class="sxs-lookup"><span data-stu-id="b5509-131">You can copy the history of a service BOM line from one service agreement to another service agreement.</span></span> <span data-ttu-id="b5509-132">Копирование истории сервисного обслуживания между соглашениями о сервисном обслуживании позволяет сохранить записи замен для номенклатуры.</span><span class="sxs-lookup"><span data-stu-id="b5509-132">By copying the service history between service agreements, you can preserve the record of replacements for an item.</span></span>

<span data-ttu-id="b5509-133">**Пример**</span><span class="sxs-lookup"><span data-stu-id="b5509-133">**Example**</span></span>

<span data-ttu-id="b5509-134">Пользователь установил трехлетнее соглашение на обслуживание машины клиента.</span><span class="sxs-lookup"><span data-stu-id="b5509-134">You have set up a three-year service agreement for a customer's car.</span></span> <span data-ttu-id="b5509-135">Во время этого периода клиент привык к хорошему обслуживанию, предоставляемому компанией.</span><span class="sxs-lookup"><span data-stu-id="b5509-135">During that period, the customer becomes accustomed to the good service that the company provides.</span></span> <span data-ttu-id="b5509-136">Поэтому по истечении срока действия договора он захотел заключить новый.</span><span class="sxs-lookup"><span data-stu-id="b5509-136">Therefore, after the agreement expires, the customer wants to set up a new one.</span></span> <span data-ttu-id="b5509-137">Пользователь имеет теперь возможность обсудить более выгодное соглашение для компании.</span><span class="sxs-lookup"><span data-stu-id="b5509-137">You are now able to negotiate a more favorable agreement for the company.</span></span> <span data-ttu-id="b5509-138">Поскольку запись замененных компонентов может оказаться полезной в будущем, историю спецификации сервисного обслуживания копируется в новое соглашение.</span><span class="sxs-lookup"><span data-stu-id="b5509-138">Because the record of replaced components might be useful in the future, you copy the history of the service BOM to the new agreement.</span></span>

## <a name="modify-the-template-bom"></a><span data-ttu-id="b5509-139">Изменение шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="b5509-139">Modify the template BOM</span></span>

<span data-ttu-id="b5509-140">Если шаблон спецификации не был присоединен к объекту сервисного обслуживания, его строки можно изменить или удалить.</span><span class="sxs-lookup"><span data-stu-id="b5509-140">If a template BOM has not been attached to a service object, you can modify or delete lines in it.</span></span> <span data-ttu-id="b5509-141">После присоединения шаблона спецификации к объекту сервисного обслуживания можно изменить только локальную версию спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-141">After the template BOM is attached to a service object, you can modify only the local version of the BOM.</span></span> <span data-ttu-id="b5509-142">Если нужно продублировать настройку локальной версии шаблона спецификации, создается новый шаблон спецификации на основе локальной версии</span><span class="sxs-lookup"><span data-stu-id="b5509-142">If you want to duplicate the setup of a local version of a template BOM, you can create a new template BOM based on the local version.</span></span> <span data-ttu-id="b5509-143">Дополнительные сведения см. в разделе [Изменение спецификации обслуживания](modify-service-bom.md).</span><span class="sxs-lookup"><span data-stu-id="b5509-143">For more information, see [Modify a Service BOM](modify-service-bom.md).</span></span>

<span data-ttu-id="b5509-144">При замене номенклатуры в спецификации зарегистрируйте замену в строке спецификации в конструкторе спецификаций.</span><span class="sxs-lookup"><span data-stu-id="b5509-144">If you replace an item in the BOM, you can register the replacement on the BOM line in the BOM designer.</span></span> <span data-ttu-id="b5509-145">Кроме того, можно создать строку заказа на сервисное обслуживание для заменяемого объекта.</span><span class="sxs-lookup"><span data-stu-id="b5509-145">Optionally, you can create a service order line for the replacement object.</span></span> <span data-ttu-id="b5509-146">При создании строки заказа на сервисное обслуживание выставляется накладная на заменяемую номенклатуру.</span><span class="sxs-lookup"><span data-stu-id="b5509-146">If you create a service order line, you can invoice the replacement item.</span></span> <span data-ttu-id="b5509-147">Если строка заказа на сервисное обслуживание не создается для замены, регистрация замены сохраняется для отслеживания истории объекта сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-147">If you do not create a service order line for a replacement, the replacement registration is kept to track the history of the service object.</span></span>

## <a name="change-how-information-on-the-bom-line-is-displayed"></a><span data-ttu-id="b5509-148">Изменение способа отображения сведений в сроке спецификации</span><span class="sxs-lookup"><span data-stu-id="b5509-148">Change how information on the BOM line is displayed</span></span>

<span data-ttu-id="b5509-149">Можно изменить способ отображения сведений в строке спецификации для всех шаблонов спецификации и спецификаций сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-149">You can change the way that information on the BOM line is displayed for all template and service BOMs.</span></span> <span data-ttu-id="b5509-150">Изменения применяются ко всем шаблонам спецификаций и спецификациям сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-150">The changes are applied to all template BOMs and service BOMs.</span></span> <span data-ttu-id="b5509-151">В их число входят шаблоны, присоединенные к объектам сервисного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="b5509-151">This includes those that are attached to service objects.</span></span>

## <a name="set-up-number-sequences-for-template-boms"></a><span data-ttu-id="b5509-152">Настройка номерных серий для шаблонов спецификаций</span><span class="sxs-lookup"><span data-stu-id="b5509-152">Set up number sequences for template BOMs</span></span>

<span data-ttu-id="b5509-153">Для использования шаблонов спецификаций необходимо настроить две номерные серии.</span><span class="sxs-lookup"><span data-stu-id="b5509-153">To use template BOMs, you must set up two number sequences.</span></span> <span data-ttu-id="b5509-154">Настройте одну номерную серию для шаблона спецификации, а другую — для номера строки истории спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-154">Set up one number sequence for the template BOM and one for the BOM history line number.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b5509-155">Номерные серии используются для назначения идентификаторов записям, которым они необходимы.</span><span class="sxs-lookup"><span data-stu-id="b5509-155">Number sequences are used to allocate identifiers to records that require them.</span></span> <span data-ttu-id="b5509-156">Перед назначением номерной серии шаблону спецификации или строке истории спецификации следует настроить коды номерных серий.</span><span class="sxs-lookup"><span data-stu-id="b5509-156">Before you can assign a number sequence to a template BOM or a BOM history line number, you must set up number sequences codes.</span></span></P>


## <a name="set-up-number-sequences"></a><span data-ttu-id="b5509-157">Настроить номерные серии</span><span class="sxs-lookup"><span data-stu-id="b5509-157">Set up number sequences</span></span>

1.  <span data-ttu-id="b5509-158">На странице списка **Номерные серии** создайте номерные серии для шаблона спецификации и номера строки истории спецификации.</span><span class="sxs-lookup"><span data-stu-id="b5509-158">On the **Number sequences** list page, create number sequences for template BOMs and the BOM history line number.</span></span> 

2.  <span data-ttu-id="b5509-159">Щелкните **Управление сервисным обслуживанием** \> **Настройка** \> **Параметры управления сервисным обслуживанием**.</span><span class="sxs-lookup"><span data-stu-id="b5509-159">Click **Service management** \> **Setup** \> **Service management parameters**.</span></span>

3.  <span data-ttu-id="b5509-160">Щелкните **Номерные серии**, а затем выберите код номерной серии для ссылок на номерные серии, созданных в форме **Номерные серии**.</span><span class="sxs-lookup"><span data-stu-id="b5509-160">Click **Number sequences**, and then select a number sequence code for the number sequence references that you created in the **Number sequences** form.</span></span>

4.  <span data-ttu-id="b5509-161">Закройте форму, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="b5509-161">Close the form to save your changes.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b5509-162">Система использует номер строки истории спецификации для связывания проводок в истории спецификации с договором о сервисном обслуживании или заказом на сервисное обслуживание.</span><span class="sxs-lookup"><span data-stu-id="b5509-162">The BOM history line number is used by the system to associate the transactions in the BOM history with a service agreement or service order.</span></span> <span data-ttu-id="b5509-163">Номер не отображается в интерфейсе пользователя.</span><span class="sxs-lookup"><span data-stu-id="b5509-163">The number is not displayed in the user interface.</span></span></P>



## <a name="see-also"></a><span data-ttu-id="b5509-164">См. также</span><span class="sxs-lookup"><span data-stu-id="b5509-164">See also</span></span>

[<span data-ttu-id="b5509-165">Создание шаблона спецификации</span><span class="sxs-lookup"><span data-stu-id="b5509-165">Create a template BOM</span></span>](create-template-bom.md)

[<span data-ttu-id="b5509-166">Управление шаблонами спецификаций для связей объектов</span><span class="sxs-lookup"><span data-stu-id="b5509-166">Manage template BOMs on object relations</span></span>](manage-template-boms-on-object-relations.md)

[<span data-ttu-id="b5509-167">Изменение спецификации обслуживания</span><span class="sxs-lookup"><span data-stu-id="b5509-167">Modify a Service BOM</span></span>](modify-service-bom.md)

 




[!INCLUDE[footer-include](../../includes/footer-banner.md)]