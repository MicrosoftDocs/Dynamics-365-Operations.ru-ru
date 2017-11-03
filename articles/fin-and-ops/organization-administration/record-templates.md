---
title: "Шаблоны записей"
description: "Эта статья вводит понятие шаблонов записей и описывает порядок, как их можно использовать для создания записей, совместно использующих сведения."
author: pvillads
manager: AnnBe
ms.date: 08/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ef5e95d9d6beed10cd6c80aa131c5cbef85c07a8
ms.contentlocale: ru-ru
ms.lasthandoff: 11/03/2017

---

# <a name="record-templates"></a><span data-ttu-id="429a0-103">Шаблоны записей</span><span class="sxs-lookup"><span data-stu-id="429a0-103">Record templates</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="429a0-104">Эта статья вводит понятие шаблонов записей и описывает порядок, как их можно использовать для создания записей, совместно использующих сведения.</span><span class="sxs-lookup"><span data-stu-id="429a0-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="429a0-105">Шаблоны записей позволяют быстрее создавать записи в системе Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="429a0-105">Record templates can help you to create records more quickly in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="429a0-106">Шаблоны записей могут быть созданы только для определенных типов записей в Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="429a0-106">You can create record templates for only some of the record types in Microsoft Dynamics 365 for Finance and Operations.</span></span> 

<span data-ttu-id="429a0-107">Например, представьте, что вы вводите арендную информацию для фирмы по прокату автомобилей, которая расположено в Сан-Франциско.</span><span class="sxs-lookup"><span data-stu-id="429a0-107">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="429a0-108">В виду того что большинство клиентов, скорее всего, будут из региона Сан-Франциско, было бы славно, если вы могли автоматически заполнить значения для полей **Штат**, **Страна** и **Город** в форме аренды.</span><span class="sxs-lookup"><span data-stu-id="429a0-108">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span> 

> [!Note]
> <span data-ttu-id="429a0-109">Вы можете применять шаблоны только для тех областей Finance and Operations., к которым у вас есть доступ.</span><span class="sxs-lookup"><span data-stu-id="429a0-109">You can apply templates only for the areas of Finance and Operations that you have access to.</span></span> <span data-ttu-id="429a0-110">Все заголовки шаблонов видны пользователю при создании новой записи, а также другим пользователям, если пользователь создает шаблоны, которые будут доступны для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="429a0-110">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="429a0-111">Имейте это в виду, присваивая названия шаблонам.</span><span class="sxs-lookup"><span data-stu-id="429a0-111">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="429a0-112">Например, следует избегать использования названий, включающих такие слова, как "комиссия", если не все пользователи знают, что некоторые сотрудники компании получают заработную плату на комиссионной основе.</span><span class="sxs-lookup"><span data-stu-id="429a0-112">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span> 

<span data-ttu-id="429a0-113">Когда один или несколько шаблонов, к которым пользователь имеет доступ, создаются для определенной формы, а пользователь пытается создать в форме новую запись, отображается страница **Поиск шаблона для…**.</span><span class="sxs-lookup"><span data-stu-id="429a0-113">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="429a0-114">При выборе шаблона из списка, на его базе создается новая запись, содержащая информацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="429a0-114">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="429a0-115">Если вы не хотите видеть список шаблонов при создании новых записей, установите флажок **Повторно не спрашивать** на странице **Выбрать шаблон для**.</span><span class="sxs-lookup"><span data-stu-id="429a0-115">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="429a0-116">Чтобы открыть диалоговое окно выбора шаблонов, щелкните правой кнопкой мыши любую запись, выберите **Сведения о записи**, а затем щелкните **Показать выбор шаблона**.</span><span class="sxs-lookup"><span data-stu-id="429a0-116">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>




