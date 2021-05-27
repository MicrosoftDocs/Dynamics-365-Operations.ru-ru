---
title: Адрес работника зарплаты
description: В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 964f04261ea95ee6fa2880b0905a669855f6c58a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020713"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="70efa-103">Адрес работника зарплаты</span><span class="sxs-lookup"><span data-stu-id="70efa-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="70efa-104">В этом разделе представлены сведения и пример запроса для сущности адреса работника заработной платы в Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="70efa-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="70efa-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="70efa-105">Properties</span></span>

| <span data-ttu-id="70efa-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="70efa-106">Property</span></span><br><span data-ttu-id="70efa-107">**Физическое имя**</span><span class="sxs-lookup"><span data-stu-id="70efa-107">**Physical name**</span></span><br><span data-ttu-id="70efa-108">**_Вид_**</span><span class="sxs-lookup"><span data-stu-id="70efa-108">**_Type_**</span></span> | <span data-ttu-id="70efa-109">Использование</span><span class="sxs-lookup"><span data-stu-id="70efa-109">Use</span></span> | <span data-ttu-id="70efa-110">описание</span><span class="sxs-lookup"><span data-stu-id="70efa-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="70efa-111">**Город**</span><span class="sxs-lookup"><span data-stu-id="70efa-111">**City**</span></span><br><span data-ttu-id="70efa-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="70efa-112">mshr_city</span></span><br><span data-ttu-id="70efa-113">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-113">*String*</span></span> | <span data-ttu-id="70efa-114">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-114">Read-only</span></span><br><span data-ttu-id="70efa-115">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-115">Required</span></span> | <span data-ttu-id="70efa-116">Город, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="70efa-117">**Табельный номер**</span><span class="sxs-lookup"><span data-stu-id="70efa-117">**Personnel number**</span></span><br><span data-ttu-id="70efa-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="70efa-118">mshr_personnelnumber</span></span><br><span data-ttu-id="70efa-119">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-119">*String*</span></span> | <span data-ttu-id="70efa-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-120">Read-only</span></span><br><span data-ttu-id="70efa-121">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-121">Required</span></span> | <span data-ttu-id="70efa-122">Уникальный табельный номер для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="70efa-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="70efa-123">**Страна/регион**</span><span class="sxs-lookup"><span data-stu-id="70efa-123">**Country region**</span></span><br><span data-ttu-id="70efa-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="70efa-124">mshr_countryregionid</span></span><br><span data-ttu-id="70efa-125">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-125">*String*</span></span> | <span data-ttu-id="70efa-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-126">Read-only</span></span><br><span data-ttu-id="70efa-127">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-127">Required</span></span> | <span data-ttu-id="70efa-128">Страна/регион, определенные для адреса</span><span class="sxs-lookup"><span data-stu-id="70efa-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="70efa-129">**Действительно с**</span><span class="sxs-lookup"><span data-stu-id="70efa-129">**Valid from**</span></span><br><span data-ttu-id="70efa-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="70efa-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="70efa-131">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="70efa-131">*Date Time Offset*</span></span> | <span data-ttu-id="70efa-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-132">Read-only</span></span> <br><span data-ttu-id="70efa-133">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-133">Required</span></span> | <span data-ttu-id="70efa-134">Дата, начиная с которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="70efa-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="70efa-135">**Работал по адресу**</span><span class="sxs-lookup"><span data-stu-id="70efa-135">**Worked in address**</span></span><br><span data-ttu-id="70efa-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="70efa-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="70efa-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-137">Read-only</span></span><br><span data-ttu-id="70efa-138">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-138">Required</span></span> | <span data-ttu-id="70efa-139">Обозначает, находится ли адрес по месту работы сотрудника.</span><span class="sxs-lookup"><span data-stu-id="70efa-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="70efa-140">**Райoн**</span><span class="sxs-lookup"><span data-stu-id="70efa-140">**County**</span></span><br><span data-ttu-id="70efa-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="70efa-141">mshr_county</span></span><br><span data-ttu-id="70efa-142">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-142">*String*</span></span> | <span data-ttu-id="70efa-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-143">Read-only</span></span><br><span data-ttu-id="70efa-144">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-144">Required</span></span> | <span data-ttu-id="70efa-145">Страна, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="70efa-146">**ИД адреса работника зарплаты**</span><span class="sxs-lookup"><span data-stu-id="70efa-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="70efa-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="70efa-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="70efa-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="70efa-148">*GUID*</span></span> | <span data-ttu-id="70efa-149">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-149">Required</span></span><br><span data-ttu-id="70efa-150">Создано системой</span><span class="sxs-lookup"><span data-stu-id="70efa-150">System generated</span></span> | <span data-ttu-id="70efa-151">Создаваемое системой значение GUID для уникальной идентификации адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="70efa-152">**Основное поле**</span><span class="sxs-lookup"><span data-stu-id="70efa-152">**Primary field**</span></span><br><span data-ttu-id="70efa-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="70efa-153">mshr_primaryfield</span></span><br><span data-ttu-id="70efa-154">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-154">*String*</span></span> | <span data-ttu-id="70efa-155">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-155">Read-only</span></span><br><span data-ttu-id="70efa-156">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-156">Required</span></span> |  |
| <span data-ttu-id="70efa-157">**Улица**</span><span class="sxs-lookup"><span data-stu-id="70efa-157">**Street**</span></span><br><span data-ttu-id="70efa-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="70efa-158">mshr_street</span></span><br><span data-ttu-id="70efa-159">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-159">*String*</span></span> | <span data-ttu-id="70efa-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-160">Read-only</span></span><br><span data-ttu-id="70efa-161">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-161">Required</span></span> | <span data-ttu-id="70efa-162">Улица, определенная для адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-162">The street defined for the address.</span></span> |
| <span data-ttu-id="70efa-163">**Действительно до**</span><span class="sxs-lookup"><span data-stu-id="70efa-163">**Valid to**</span></span><br><span data-ttu-id="70efa-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="70efa-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="70efa-165">*Смещение даты и времени*</span><span class="sxs-lookup"><span data-stu-id="70efa-165">*Date Time Offset*</span></span> | <span data-ttu-id="70efa-166">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-166">Read-only</span></span> <br><span data-ttu-id="70efa-167">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-167">Required</span></span> | <span data-ttu-id="70efa-168">Дата, до которой адрес является действительным.</span><span class="sxs-lookup"><span data-stu-id="70efa-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="70efa-169">**Код местонахождения**</span><span class="sxs-lookup"><span data-stu-id="70efa-169">**Location ID**</span></span><br><span data-ttu-id="70efa-170">mshr_locationidbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="70efa-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-171">Read-only</span></span> <br><span data-ttu-id="70efa-172">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-172">Required</span></span> | <span data-ttu-id="70efa-173">ИД для адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-173">The ID for the address.</span></span>  |
| <span data-ttu-id="70efa-174">**Почтовый индекс**</span><span class="sxs-lookup"><span data-stu-id="70efa-174">**Postal code**</span></span><br><span data-ttu-id="70efa-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="70efa-175">mshr_zipcode</span></span><br><span data-ttu-id="70efa-176">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-176">*String*</span></span> | <span data-ttu-id="70efa-177">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-177">Read-only</span></span> <br><span data-ttu-id="70efa-178">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-178">Required</span></span> |<span data-ttu-id="70efa-179">Идентификационный номер, определенный для сотрудника.</span><span class="sxs-lookup"><span data-stu-id="70efa-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="70efa-180">**Жил по адресу**</span><span class="sxs-lookup"><span data-stu-id="70efa-180">**Lived in address**</span></span><br><span data-ttu-id="70efa-181">mshr_islivedinaddressbr>*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="70efa-182">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-182">Read-only</span></span><br><span data-ttu-id="70efa-183">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-183">Required</span></span> | <span data-ttu-id="70efa-184">Обозначает, находится ли адрес там, где живет сотрудник.</span><span class="sxs-lookup"><span data-stu-id="70efa-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="70efa-185">**Область/штат/провинция**</span><span class="sxs-lookup"><span data-stu-id="70efa-185">**State**</span></span><br><span data-ttu-id="70efa-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="70efa-186">mshr_state</span></span><br><span data-ttu-id="70efa-187">*Строка*</span><span class="sxs-lookup"><span data-stu-id="70efa-187">*String*</span></span> | <span data-ttu-id="70efa-188">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="70efa-188">Read-only</span></span><br><span data-ttu-id="70efa-189">Требуется</span><span class="sxs-lookup"><span data-stu-id="70efa-189">Required</span></span> | <span data-ttu-id="70efa-190">Регион, определенный для адреса.</span><span class="sxs-lookup"><span data-stu-id="70efa-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="70efa-191">Пример запроса</span><span class="sxs-lookup"><span data-stu-id="70efa-191">Example query</span></span>

<span data-ttu-id="70efa-192">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="70efa-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="70efa-193">**Отклик**</span><span class="sxs-lookup"><span data-stu-id="70efa-193">**Response**</span></span>

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
