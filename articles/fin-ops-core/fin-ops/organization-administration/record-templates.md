---
title: Обзор шаблонов записей
description: Эта статья вводит понятие шаблонов записей и описывает порядок, как их можно использовать для создания записей, совместно использующих сведения.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0b55046e6c523398b4a30e674dc9f77bb6fedf3
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693216"
---
# <a name="record-templates-overview"></a><span data-ttu-id="7d09a-103">Обзор шаблонов записей</span><span class="sxs-lookup"><span data-stu-id="7d09a-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d09a-104">Эта статья вводит понятие шаблонов записей и описывает порядок, как их можно использовать для создания записей, совместно использующих сведения.</span><span class="sxs-lookup"><span data-stu-id="7d09a-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="7d09a-105">Шаблоны записей позволяют быстрее создавать записи, но можно создавать только шаблоны записей для некоторых типов записей.</span><span class="sxs-lookup"><span data-stu-id="7d09a-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="7d09a-106">Например, представьте, что вы вводите арендную информацию для фирмы по прокату автомобилей, которая расположено в Сан-Франциско.</span><span class="sxs-lookup"><span data-stu-id="7d09a-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="7d09a-107">В виду того что большинство клиентов, скорее всего, будут из региона Сан-Франциско, было бы славно, если вы могли автоматически заполнить значения для полей **Штат**, **Страна** и **Город** в форме аренды.</span><span class="sxs-lookup"><span data-stu-id="7d09a-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="7d09a-108">Можно использовать шаблоны только в областях, к которым у вас имеется доступ.</span><span class="sxs-lookup"><span data-stu-id="7d09a-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="7d09a-109">Все заголовки шаблонов видны пользователю при создании новой записи, а также другим пользователям, если пользователь создает шаблоны, которые будут доступны для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="7d09a-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="7d09a-110">Имейте это в виду, присваивая названия шаблонам.</span><span class="sxs-lookup"><span data-stu-id="7d09a-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="7d09a-111">Например, следует избегать использования названий, включающих такие слова, как "комиссия", если не все пользователи знают, что некоторые сотрудники компании получают заработную плату на комиссионной основе.</span><span class="sxs-lookup"><span data-stu-id="7d09a-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="7d09a-112">Когда один или несколько шаблонов, к которым пользователь имеет доступ, создаются для определенной формы, а пользователь пытается создать в форме новую запись, отображается страница **Поиск шаблона для…**.</span><span class="sxs-lookup"><span data-stu-id="7d09a-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="7d09a-113">При выборе шаблона из списка, на его базе создается новая запись, содержащая информацию по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d09a-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="7d09a-114">Если вы не хотите видеть список шаблонов при создании новых записей, установите флажок **Повторно не спрашивать** на странице **Выбрать шаблон для**.</span><span class="sxs-lookup"><span data-stu-id="7d09a-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="7d09a-115">Чтобы открыть диалоговое окно выбора шаблонов, щелкните правой кнопкой мыши любую запись, выберите **Сведения о записи**, а затем щелкните **Показать выбор шаблона**.</span><span class="sxs-lookup"><span data-stu-id="7d09a-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>
