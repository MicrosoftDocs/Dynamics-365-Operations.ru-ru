--- 
title: "Создание и связывание регистраторов"
description: "В этой процедуре показано, как создать регистр POS."
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: ru-ru
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-associate-registers"></a><span data-ttu-id="450f9-103">Создание и связывание регистраторов</span><span class="sxs-lookup"><span data-stu-id="450f9-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="450f9-104">В этой процедуре показано, как создать регистр POS.</span><span class="sxs-lookup"><span data-stu-id="450f9-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="450f9-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="450f9-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="450f9-106">Перейдите в раздел "Розничная торговля и коммерция" > "Настройка канала" > "Настройка POS" > "Кассы".</span><span class="sxs-lookup"><span data-stu-id="450f9-106">Go to Retail and commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="450f9-107">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="450f9-107">Click New.</span></span>
3. <span data-ttu-id="450f9-108">В поле "Номер регистра" введите код нового регистра.</span><span class="sxs-lookup"><span data-stu-id="450f9-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="450f9-109">Код регистра обычно включает коды, которые помогают сопоставить регистр с магазином, к которому он принадлежит, и местонахождением внутри магазина.</span><span class="sxs-lookup"><span data-stu-id="450f9-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="450f9-110">В поле "Имя" введите описательное имя регистра.</span><span class="sxs-lookup"><span data-stu-id="450f9-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="450f9-111">В поле "Номер магазина" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="450f9-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="450f9-112">В поле "Профиль оборудования" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="450f9-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="450f9-113">Профили оборудования используются для определения периферийных устройств розничной торговли, которые будут подключены к регистру, например кассовый лоток и принтер чеков.</span><span class="sxs-lookup"><span data-stu-id="450f9-113">Hardware profiles are used to specify the retail peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="450f9-114">В поле "Визуальный профиль" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="450f9-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="450f9-115">Визуальные профили используются для определения изображений, используемых для фона и страницы входа POS, а также тем POS.</span><span class="sxs-lookup"><span data-stu-id="450f9-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="450f9-116">В поле "Номер POS для электронных платежей" введите значение.</span><span class="sxs-lookup"><span data-stu-id="450f9-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="450f9-117">Номер регистра POS для электронных платежей используется для уведомления процессора платежа, которому терминал платежей отправляет запросы на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="450f9-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="450f9-118">Это значение часто называется "Код терминала" или "TID".</span><span class="sxs-lookup"><span data-stu-id="450f9-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="450f9-119">TID обычно указывается на наклейке на платежном терминале.</span><span class="sxs-lookup"><span data-stu-id="450f9-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="450f9-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="450f9-120">Click Save.</span></span>


