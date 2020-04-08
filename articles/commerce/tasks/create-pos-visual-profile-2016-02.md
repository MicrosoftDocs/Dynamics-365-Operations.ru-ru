---
title: Создание визуальных профилей POS
description: Эта процедура содержит инструкции по созданию нового визуального профиля ККМ.
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b265a94c6d8f9e2534e1509e4f33c6f8a05eded0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140964"
---
# <a name="create-point-of-sale-pos-visual-profiles"></a><span data-ttu-id="029fb-103">Создание визуальных профилей POS</span><span class="sxs-lookup"><span data-stu-id="029fb-103">Create point of sale (POS) visual profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="029fb-104">Эта процедура содержит инструкции по созданию нового визуального профиля ККМ.</span><span class="sxs-lookup"><span data-stu-id="029fb-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="029fb-105">Визуальный профиль содержит основные сведения, которые определяют внешний вид ККМ.</span><span class="sxs-lookup"><span data-stu-id="029fb-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="029fb-106">Можно создать несколько визуальных профилей и назначить их в зависимости от конкретных ККМ.</span><span class="sxs-lookup"><span data-stu-id="029fb-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="029fb-107">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="029fb-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="029fb-108">Перейдите в раздел Retail и Commerce > Настройка канала > Профили POS > Визуальные профили.</span><span class="sxs-lookup"><span data-stu-id="029fb-108">Go to Retail and Commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="029fb-109">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="029fb-109">Click New.</span></span>
3. <span data-ttu-id="029fb-110">В поле "Номер профиля" введите значение.</span><span class="sxs-lookup"><span data-stu-id="029fb-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="029fb-111">В поле "Описание" введите значение.</span><span class="sxs-lookup"><span data-stu-id="029fb-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="029fb-112">В поле "Тип приложения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="029fb-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="029fb-113">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="029fb-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="029fb-114">В поле "Тема" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="029fb-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="029fb-115">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="029fb-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="029fb-116">В поле "Цвет выделения" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.</span><span class="sxs-lookup"><span data-stu-id="029fb-116">In the Accent color field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="029fb-117">В списке найдите и выберите требуемую запись.</span><span class="sxs-lookup"><span data-stu-id="029fb-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="029fb-118">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="029fb-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="029fb-119">Переключите расширение раздела "Фон при входе в систему".</span><span class="sxs-lookup"><span data-stu-id="029fb-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="029fb-120">В поле "Идентификатор альбомного изображения" выберите или введите код изображения</span><span class="sxs-lookup"><span data-stu-id="029fb-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="029fb-121">В поле "Код портретного изображения" выберите или введите код изображения.</span><span class="sxs-lookup"><span data-stu-id="029fb-121">In the Portrait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="029fb-122">Переключите развертывание раздела "Фон".</span><span class="sxs-lookup"><span data-stu-id="029fb-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="029fb-123">Запросите всплывающее окно кода изображения.</span><span class="sxs-lookup"><span data-stu-id="029fb-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="029fb-124">В списке перейдите по ссылке в выбранной строке.</span><span class="sxs-lookup"><span data-stu-id="029fb-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="029fb-125">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="029fb-125">Click Save.</span></span>

