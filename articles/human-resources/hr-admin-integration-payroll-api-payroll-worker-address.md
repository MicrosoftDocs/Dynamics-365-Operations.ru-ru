---
title: Адрес работника зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052297"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="50f24-103">Адрес работника зарплаты</span><span class="sxs-lookup"><span data-stu-id="50f24-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="50f24-104">В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="50f24-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="50f24-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="50f24-105">Properties</span></span>

| <span data-ttu-id="50f24-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="50f24-106">Property</span></span><br><span data-ttu-id="50f24-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="50f24-107">**Physical name**</span></span><br><span data-ttu-id="50f24-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="50f24-108">**_Type_**</span></span> | <span data-ttu-id="50f24-109">Использование</span><span class="sxs-lookup"><span data-stu-id="50f24-109">Use</span></span> | <span data-ttu-id="50f24-110">описание</span><span class="sxs-lookup"><span data-stu-id="50f24-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="50f24-111">**Город**</span><span class="sxs-lookup"><span data-stu-id="50f24-111">**City**</span></span><br><span data-ttu-id="50f24-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="50f24-112">mshr_city</span></span><br><span data-ttu-id="50f24-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-113">*String*</span></span> | <span data-ttu-id="50f24-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-114">Read-only</span></span><br><span data-ttu-id="50f24-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-115">Required</span></span> | <span data-ttu-id="50f24-116">Город, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="50f24-117">**Табельный номер**</span><span class="sxs-lookup"><span data-stu-id="50f24-117">**Personnel number**</span></span><br><span data-ttu-id="50f24-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="50f24-118">mshr_personnelnumber</span></span><br><span data-ttu-id="50f24-119">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-119">*String*</span></span> | <span data-ttu-id="50f24-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-120">Read-only</span></span><br><span data-ttu-id="50f24-121">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-121">Required</span></span> | <span data-ttu-id="50f24-122">Уникальный табельный номер для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="50f24-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="50f24-123">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="50f24-123">**Country region**</span></span><br><span data-ttu-id="50f24-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="50f24-124">mshr_countryregionid</span></span><br><span data-ttu-id="50f24-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-125">*String*</span></span> | <span data-ttu-id="50f24-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-126">Read-only</span></span><br><span data-ttu-id="50f24-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-127">Required</span></span> | <span data-ttu-id="50f24-128">Страна/регион, определенные для адреса</span><span class="sxs-lookup"><span data-stu-id="50f24-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="50f24-129">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="50f24-129">**Valid from**</span></span><br><span data-ttu-id="50f24-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="50f24-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="50f24-131">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="50f24-131">*Date Time Offset*</span></span> | <span data-ttu-id="50f24-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-132">Read-only</span></span> <br><span data-ttu-id="50f24-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-133">Required</span></span> | <span data-ttu-id="50f24-134">Дата, начиная с которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="50f24-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="50f24-135">**Работал по адресу**</span><span class="sxs-lookup"><span data-stu-id="50f24-135">**Worked in address**</span></span><br><span data-ttu-id="50f24-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="50f24-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="50f24-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-137">Read-only</span></span><br><span data-ttu-id="50f24-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-138">Required</span></span> | <span data-ttu-id="50f24-139">Обозначает, находится ли адрес по месту работы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="50f24-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="50f24-140">**Райoн**</span><span class="sxs-lookup"><span data-stu-id="50f24-140">**County**</span></span><br><span data-ttu-id="50f24-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="50f24-141">mshr_county</span></span><br><span data-ttu-id="50f24-142">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-142">*String*</span></span> | <span data-ttu-id="50f24-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-143">Read-only</span></span><br><span data-ttu-id="50f24-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-144">Required</span></span> | <span data-ttu-id="50f24-145">Страна, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="50f24-146">**ИД адреса работника зарплаты**</span><span class="sxs-lookup"><span data-stu-id="50f24-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="50f24-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="50f24-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="50f24-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="50f24-148">*GUID*</span></span> | <span data-ttu-id="50f24-149">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-149">Required</span></span><br><span data-ttu-id="50f24-150">Создано системой</span><span class="sxs-lookup"><span data-stu-id="50f24-150">System generated</span></span> | <span data-ttu-id="50f24-151">Создаваемое системой значение GUID для уникальной идентификации адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="50f24-152">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="50f24-152">**Primary field**</span></span><br><span data-ttu-id="50f24-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="50f24-153">mshr_primaryfield</span></span><br><span data-ttu-id="50f24-154">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-154">*String*</span></span> | <span data-ttu-id="50f24-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-155">Read-only</span></span><br><span data-ttu-id="50f24-156">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-156">Required</span></span> |  |
| <span data-ttu-id="50f24-157">**Улица**</span><span class="sxs-lookup"><span data-stu-id="50f24-157">**Street**</span></span><br><span data-ttu-id="50f24-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="50f24-158">mshr_street</span></span><br><span data-ttu-id="50f24-159">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-159">*String*</span></span> | <span data-ttu-id="50f24-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-160">Read-only</span></span><br><span data-ttu-id="50f24-161">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-161">Required</span></span> | <span data-ttu-id="50f24-162">Улица, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-162">The street defined for the address.</span></span> |
| <span data-ttu-id="50f24-163">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="50f24-163">**Valid to**</span></span><br><span data-ttu-id="50f24-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="50f24-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="50f24-165">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="50f24-165">*Date Time Offset*</span></span> | <span data-ttu-id="50f24-166">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-166">Read-only</span></span> <br><span data-ttu-id="50f24-167">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-167">Required</span></span> | <span data-ttu-id="50f24-168">Дата, до которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="50f24-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="50f24-169">**Код местонахождения**</span><span class="sxs-lookup"><span data-stu-id="50f24-169">**Location ID**</span></span><br><span data-ttu-id="50f24-170">mshr_locationidbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="50f24-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-171">Read-only</span></span> <br><span data-ttu-id="50f24-172">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-172">Required</span></span> | <span data-ttu-id="50f24-173">ИД для адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-173">The ID for the address.</span></span>  |
| <span data-ttu-id="50f24-174">**Почтовый индекс**</span><span class="sxs-lookup"><span data-stu-id="50f24-174">**Postal code**</span></span><br><span data-ttu-id="50f24-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="50f24-175">mshr_zipcode</span></span><br><span data-ttu-id="50f24-176">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-176">*String*</span></span> | <span data-ttu-id="50f24-177">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-177">Read-only</span></span> <br><span data-ttu-id="50f24-178">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-178">Required</span></span> |<span data-ttu-id="50f24-179">Идентификационный номер, определенный для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="50f24-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="50f24-180">**Жил по адресу**</span><span class="sxs-lookup"><span data-stu-id="50f24-180">**Lived in address**</span></span><br><span data-ttu-id="50f24-181">mshr_islivedinaddressbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="50f24-182">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-182">Read-only</span></span><br><span data-ttu-id="50f24-183">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-183">Required</span></span> | <span data-ttu-id="50f24-184">Обозначает, находится ли адрес там, где живет сотрудник.</span><span class="sxs-lookup"><span data-stu-id="50f24-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="50f24-185">**Область/штат/провинция**</span><span class="sxs-lookup"><span data-stu-id="50f24-185">**State**</span></span><br><span data-ttu-id="50f24-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="50f24-186">mshr_state</span></span><br><span data-ttu-id="50f24-187">*Строка*</span><span class="sxs-lookup"><span data-stu-id="50f24-187">*String*</span></span> | <span data-ttu-id="50f24-188">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="50f24-188">Read-only</span></span><br><span data-ttu-id="50f24-189">Требуется</span><span class="sxs-lookup"><span data-stu-id="50f24-189">Required</span></span> | <span data-ttu-id="50f24-190">Регион, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="50f24-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="50f24-191">Пример запроса</span><span class="sxs-lookup"><span data-stu-id="50f24-191">Example query</span></span>

<span data-ttu-id="50f24-192">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="50f24-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="50f24-193">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="50f24-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
