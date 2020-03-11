---
title: Создание и связывание регистраторов
description: В этой процедуре показано, как создать регистр POS.
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ac75d390b8bbb94c6e039b374b51462d348e355
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057187"
---
# <a name="create-and-associate-registers"></a><span data-ttu-id="6550f-103">Создание и связывание регистраторов</span><span class="sxs-lookup"><span data-stu-id="6550f-103">Create and associate registers</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6550f-104">В этой процедуре показано, как создать регистр POS.</span><span class="sxs-lookup"><span data-stu-id="6550f-104">This procedure demonstrates how to create a point of sale (POS) register.</span></span> <span data-ttu-id="6550f-105">В этой процедуре используется компания с демонстрационными данными USRT.</span><span class="sxs-lookup"><span data-stu-id="6550f-105">This procedure uses the demo data company USRT.</span></span>

1. <span data-ttu-id="6550f-106">Перейдите в раздел "Retail и Commerce" > "Настройка канала" > "Настройка POS" > "Кассы".</span><span class="sxs-lookup"><span data-stu-id="6550f-106">Go to Retail and Commerce > Channel setup > POS setup > Registers.</span></span>
2. <span data-ttu-id="6550f-107">Нажмите Создать.</span><span class="sxs-lookup"><span data-stu-id="6550f-107">Click New.</span></span>
3. <span data-ttu-id="6550f-108">В поле "Номер регистра" введите код нового регистра.</span><span class="sxs-lookup"><span data-stu-id="6550f-108">In the Register number field, type an ID for the new register.</span></span>
    * <span data-ttu-id="6550f-109">Код регистра обычно включает коды, которые помогают сопоставить регистр с магазином, к которому он принадлежит, и местонахождением внутри магазина.</span><span class="sxs-lookup"><span data-stu-id="6550f-109">The register ID typically includes codes that help map the register to the store to which it belongs, and the location within the store.</span></span>  
4. <span data-ttu-id="6550f-110">В поле "Имя" введите описательное имя регистра.</span><span class="sxs-lookup"><span data-stu-id="6550f-110">In the Name field, type a descriptive name for the register..</span></span>
5. <span data-ttu-id="6550f-111">В поле "Номер магазина" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6550f-111">In the Store number field, enter or select a value.</span></span>
6. <span data-ttu-id="6550f-112">В поле "Профиль оборудования" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6550f-112">In the Hardware profile field, enter or select a value.</span></span>
    * <span data-ttu-id="6550f-113">Профили оборудования используются для определения периферийных устройств, которые будут подключены к регистру, например кассовый лоток и принтер чеков.</span><span class="sxs-lookup"><span data-stu-id="6550f-113">Hardware profiles are used to specify the peripherals that will be connected to the register, such as cash drawer and receipt printer.</span></span>  
7. <span data-ttu-id="6550f-114">В поле "Визуальный профиль" введите или выберите значение.</span><span class="sxs-lookup"><span data-stu-id="6550f-114">In the Visual profile field, enter or select a value.</span></span>
    * <span data-ttu-id="6550f-115">Визуальные профили используются для определения изображений, используемых для фона и страницы входа POS, а также тем POS.</span><span class="sxs-lookup"><span data-stu-id="6550f-115">Visual profiles are used to specify the images used in the POS background and login page as well as themes for the POS.</span></span>  
8. <span data-ttu-id="6550f-116">В поле "Номер POS для электронных платежей" введите значение.</span><span class="sxs-lookup"><span data-stu-id="6550f-116">In the EFT POS register number field, type a value.</span></span>
    * <span data-ttu-id="6550f-117">Номер регистра POS для электронных платежей используется для уведомления процессора платежа, которому терминал платежей отправляет запросы на авторизацию.</span><span class="sxs-lookup"><span data-stu-id="6550f-117">The EFT POS register number is used to inform the payment processor which payment terminal is sending authorization requests.</span></span> <span data-ttu-id="6550f-118">Это значение часто называется "Код терминала" или "TID".</span><span class="sxs-lookup"><span data-stu-id="6550f-118">This value is often called the "Terminal ID" or “TID”.</span></span> <span data-ttu-id="6550f-119">TID обычно указывается на наклейке на платежном терминале.</span><span class="sxs-lookup"><span data-stu-id="6550f-119">The TID can generally be found on a sticker on the payment device.</span></span>  
9. <span data-ttu-id="6550f-120">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="6550f-120">Click Save.</span></span>

