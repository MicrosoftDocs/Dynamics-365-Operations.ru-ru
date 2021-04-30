---
title: Адрес работника зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882062"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="28e09-103">Адрес работника зарплаты</span><span class="sxs-lookup"><span data-stu-id="28e09-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="28e09-104">В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="28e09-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="28e09-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="28e09-105">Properties</span></span>

| <span data-ttu-id="28e09-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="28e09-106">Property</span></span><br><span data-ttu-id="28e09-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="28e09-107">**Physical name**</span></span><br><span data-ttu-id="28e09-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="28e09-108">**_Type_**</span></span> | <span data-ttu-id="28e09-109">Использование</span><span class="sxs-lookup"><span data-stu-id="28e09-109">Use</span></span> | <span data-ttu-id="28e09-110">описание</span><span class="sxs-lookup"><span data-stu-id="28e09-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="28e09-111">**Город**</span><span class="sxs-lookup"><span data-stu-id="28e09-111">**City**</span></span><br><span data-ttu-id="28e09-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="28e09-112">mshr_city</span></span><br><span data-ttu-id="28e09-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-113">*String*</span></span> | <span data-ttu-id="28e09-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-114">Read-only</span></span><br><span data-ttu-id="28e09-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-115">Required</span></span> | <span data-ttu-id="28e09-116">Город, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="28e09-117">**Табельный номер**</span><span class="sxs-lookup"><span data-stu-id="28e09-117">**Personnel number**</span></span><br><span data-ttu-id="28e09-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="28e09-118">mshr_personnelnumber</span></span><br><span data-ttu-id="28e09-119">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-119">*String*</span></span> | <span data-ttu-id="28e09-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-120">Read-only</span></span><br><span data-ttu-id="28e09-121">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-121">Required</span></span> | <span data-ttu-id="28e09-122">Уникальный табельный номер для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="28e09-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="28e09-123">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="28e09-123">**Country region**</span></span><br><span data-ttu-id="28e09-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="28e09-124">mshr_countryregionid</span></span><br><span data-ttu-id="28e09-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-125">*String*</span></span> | <span data-ttu-id="28e09-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-126">Read-only</span></span><br><span data-ttu-id="28e09-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-127">Required</span></span> | <span data-ttu-id="28e09-128">Страна/регион, определенные для адреса</span><span class="sxs-lookup"><span data-stu-id="28e09-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="28e09-129">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="28e09-129">**Valid from**</span></span><br><span data-ttu-id="28e09-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="28e09-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="28e09-131">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="28e09-131">*Date Time Offset*</span></span> | <span data-ttu-id="28e09-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-132">Read-only</span></span> <br><span data-ttu-id="28e09-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-133">Required</span></span> | <span data-ttu-id="28e09-134">Дата, начиная с которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="28e09-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="28e09-135">**Работал по адресу**</span><span class="sxs-lookup"><span data-stu-id="28e09-135">**Worked in address**</span></span><br><span data-ttu-id="28e09-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="28e09-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="28e09-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-137">Read-only</span></span><br><span data-ttu-id="28e09-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-138">Required</span></span> | <span data-ttu-id="28e09-139">Обозначает, находится ли адрес по месту работы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="28e09-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="28e09-140">**Райoн**</span><span class="sxs-lookup"><span data-stu-id="28e09-140">**County**</span></span><br><span data-ttu-id="28e09-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="28e09-141">mshr_county</span></span><br><span data-ttu-id="28e09-142">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-142">*String*</span></span> | <span data-ttu-id="28e09-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-143">Read-only</span></span><br><span data-ttu-id="28e09-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-144">Required</span></span> | <span data-ttu-id="28e09-145">Страна, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="28e09-146">**ИД адреса работника зарплаты**</span><span class="sxs-lookup"><span data-stu-id="28e09-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="28e09-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="28e09-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="28e09-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="28e09-148">*GUID*</span></span> | <span data-ttu-id="28e09-149">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-149">Required</span></span><br><span data-ttu-id="28e09-150">Создано системой</span><span class="sxs-lookup"><span data-stu-id="28e09-150">System generated</span></span> | <span data-ttu-id="28e09-151">Создаваемое системой значение GUID для уникальной идентификации адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="28e09-152">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="28e09-152">**Primary field**</span></span><br><span data-ttu-id="28e09-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="28e09-153">mshr_primaryfield</span></span><br><span data-ttu-id="28e09-154">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-154">*String*</span></span> | <span data-ttu-id="28e09-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-155">Read-only</span></span><br><span data-ttu-id="28e09-156">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-156">Required</span></span> |  |
| <span data-ttu-id="28e09-157">**Улица**</span><span class="sxs-lookup"><span data-stu-id="28e09-157">**Street**</span></span><br><span data-ttu-id="28e09-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="28e09-158">mshr_street</span></span><br><span data-ttu-id="28e09-159">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-159">*String*</span></span> | <span data-ttu-id="28e09-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-160">Read-only</span></span><br><span data-ttu-id="28e09-161">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-161">Required</span></span> | <span data-ttu-id="28e09-162">Улица, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-162">The street defined for the address.</span></span> |
| <span data-ttu-id="28e09-163">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="28e09-163">**Valid to**</span></span><br><span data-ttu-id="28e09-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="28e09-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="28e09-165">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="28e09-165">*Date Time Offset*</span></span> | <span data-ttu-id="28e09-166">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-166">Read-only</span></span> <br><span data-ttu-id="28e09-167">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-167">Required</span></span> | <span data-ttu-id="28e09-168">Дата, до которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="28e09-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="28e09-169">**Код местонахождения**</span><span class="sxs-lookup"><span data-stu-id="28e09-169">**Location ID**</span></span><br><span data-ttu-id="28e09-170">mshr_locationidbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="28e09-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-171">Read-only</span></span> <br><span data-ttu-id="28e09-172">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-172">Required</span></span> | <span data-ttu-id="28e09-173">ИД для адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-173">The ID for the address.</span></span>  |
| <span data-ttu-id="28e09-174">**Почтовый индекс**</span><span class="sxs-lookup"><span data-stu-id="28e09-174">**Postal code**</span></span><br><span data-ttu-id="28e09-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="28e09-175">mshr_zipcode</span></span><br><span data-ttu-id="28e09-176">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-176">*String*</span></span> | <span data-ttu-id="28e09-177">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-177">Read-only</span></span> <br><span data-ttu-id="28e09-178">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-178">Required</span></span> |<span data-ttu-id="28e09-179">Идентификационный номер, определенный для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="28e09-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="28e09-180">**Жил по адресу**</span><span class="sxs-lookup"><span data-stu-id="28e09-180">**Lived in address**</span></span><br><span data-ttu-id="28e09-181">mshr_islivedinaddressbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="28e09-182">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-182">Read-only</span></span><br><span data-ttu-id="28e09-183">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-183">Required</span></span> | <span data-ttu-id="28e09-184">Обозначает, находится ли адрес там, где живет сотрудник.</span><span class="sxs-lookup"><span data-stu-id="28e09-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="28e09-185">**Область/штат/провинция**</span><span class="sxs-lookup"><span data-stu-id="28e09-185">**State**</span></span><br><span data-ttu-id="28e09-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="28e09-186">mshr_state</span></span><br><span data-ttu-id="28e09-187">*Строка*</span><span class="sxs-lookup"><span data-stu-id="28e09-187">*String*</span></span> | <span data-ttu-id="28e09-188">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="28e09-188">Read-only</span></span><br><span data-ttu-id="28e09-189">Требуется</span><span class="sxs-lookup"><span data-stu-id="28e09-189">Required</span></span> | <span data-ttu-id="28e09-190">Регион, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="28e09-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="28e09-191">Пример запроса</span><span class="sxs-lookup"><span data-stu-id="28e09-191">Example query</span></span>

<span data-ttu-id="28e09-192">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="28e09-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="28e09-193">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="28e09-193">**Response**</span></span>

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
