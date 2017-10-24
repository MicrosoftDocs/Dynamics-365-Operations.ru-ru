--- 
title: "Настройка типов документов I-9"
description: "В этой процедуре показано, как просмотреть и настроить типы документов, которые используются для проверки формы I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3b0e7f09994367f5683ed5c6d1f3b3ba3d550cc7
ms.contentlocale: ru-ru
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-i-9-document-types"></a><span data-ttu-id="56e2b-103">Настройка типов документов I-9</span><span class="sxs-lookup"><span data-stu-id="56e2b-103">Set up I-9 document types</span></span>

[!include[task guide banner](../../../includes/task-guide-banner.md)]

<span data-ttu-id="56e2b-104">В этой процедуре показано, как просмотреть и настроить типы документов, которые используются для проверки формы I-9.</span><span class="sxs-lookup"><span data-stu-id="56e2b-104">This procedure shows how to view and set up document types that are used for I-9 verification.</span></span> <span data-ttu-id="56e2b-105">Прежде чем настраивать типы документов для I-9, необходимо также настроить типы удостоверений личности и выдающие их организации.</span><span class="sxs-lookup"><span data-stu-id="56e2b-105">Before you set up I-9 document types, you must also set up the issuing agencies and identification types.</span></span> <span data-ttu-id="56e2b-106">Для этой процедуры используется компания с демонстрационными данными USMF. Демонстрационные данные включают примеры типов удостоверений личности и выдающих их организаций, необходимые для выполнения процедуры.</span><span class="sxs-lookup"><span data-stu-id="56e2b-106">The demo data company used to create this procedure is USMF, which includes examples of the issue agencies and identification types that are needed to complete the procedure.</span></span>

1. <span data-ttu-id="56e2b-107">Перейдите в раздел "Управление персоналом" > "Работники" > "I-9" > "Типы документа I-9".</span><span class="sxs-lookup"><span data-stu-id="56e2b-107">Go to Human resources > Workers > I-9 > I-9 document types.</span></span>
2. <span data-ttu-id="56e2b-108">Щелкните "Создать".</span><span class="sxs-lookup"><span data-stu-id="56e2b-108">Click New.</span></span>
3. <span data-ttu-id="56e2b-109">В поле "Тип документа I-9" введите значение.</span><span class="sxs-lookup"><span data-stu-id="56e2b-109">In the I-9 document type field, type a value.</span></span>
    * <span data-ttu-id="56e2b-110">Пример: "Удостоверение личности, выданное учебным заведением".</span><span class="sxs-lookup"><span data-stu-id="56e2b-110">Example: School ID.</span></span>  
4. <span data-ttu-id="56e2b-111">Выберите тип удостоверения личности.</span><span class="sxs-lookup"><span data-stu-id="56e2b-111">Select the identification type.</span></span>  <span data-ttu-id="56e2b-112">Пример: "Удостоверение личности, выданное учебным заведением"</span><span class="sxs-lookup"><span data-stu-id="56e2b-112">Example:  School ID</span></span>
    * <span data-ttu-id="56e2b-113">Примеры типов удостоверений личности — номер социального обеспечения (SSN), номер визы, паспорт или водительское удостоверение.</span><span class="sxs-lookup"><span data-stu-id="56e2b-113">Examples of identification types include a Social Security number (SSN), visa number, passport ID, or driver's licence.</span></span>  
5. <span data-ttu-id="56e2b-114">Выберите список документов для I-9, используемый для документов этого типа.</span><span class="sxs-lookup"><span data-stu-id="56e2b-114">Select the I-9 document list that is used for the document type.</span></span>
    * <span data-ttu-id="56e2b-115">В рамках процесса оформления I-9 сотрудники обязаны предоставить документы, по которым работодатель может убедиться в их личности и наличии у них разрешения на трудоустройство.</span><span class="sxs-lookup"><span data-stu-id="56e2b-115">As part of the I-9 process, employees must present documentation that shows the employer their identity and employment authorization.</span></span> <span data-ttu-id="56e2b-116">На веб-сайте Службы гражданства и иммиграции США приведена информация о том, какие документы являются приемлемыми, а также к какому из списков они относятся.</span><span class="sxs-lookup"><span data-stu-id="56e2b-116">The US Citizenship and Immigration Services website contains information about which documents are acceptable, and which list they belong to.</span></span>  <span data-ttu-id="56e2b-117">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="56e2b-117">http://www.uscis.gov</span></span>  
6. <span data-ttu-id="56e2b-118">В поле "Форма" введите официальный номер формы для данного типа документов.</span><span class="sxs-lookup"><span data-stu-id="56e2b-118">In the Form field, Enter the official form number for the document type.</span></span> <span data-ttu-id="56e2b-119">Пример: "Удостоверение личности, выданное учебным заведением".</span><span class="sxs-lookup"><span data-stu-id="56e2b-119">Example: School ID.</span></span>
    * <span data-ttu-id="56e2b-120">Официальные номера форм можно найти на веб-сайте Службы гражданства и иммиграции США.</span><span class="sxs-lookup"><span data-stu-id="56e2b-120">The official form numbers can be found on the US Citizenship and Immigration Services website.</span></span>  <span data-ttu-id="56e2b-121">http://www.uscis.gov</span><span class="sxs-lookup"><span data-stu-id="56e2b-121">http://www.uscis.gov</span></span>  
7. <span data-ttu-id="56e2b-122">Установите или снимите флажок "Активный".</span><span class="sxs-lookup"><span data-stu-id="56e2b-122">Check or uncheck the Active checkbox.</span></span>
8. <span data-ttu-id="56e2b-123">В поле "Срок действия" установите для даты значение ''27.10.2019".</span><span class="sxs-lookup"><span data-stu-id="56e2b-123">In the Expire field, set the date to '2019-10-27'.</span></span>
    * <span data-ttu-id="56e2b-124">Дата окончания срока действия является необязательной.</span><span class="sxs-lookup"><span data-stu-id="56e2b-124">The expiration date is optional.</span></span>  
9. <span data-ttu-id="56e2b-125">Выберите организацию, выдавшую документ данного типа.</span><span class="sxs-lookup"><span data-stu-id="56e2b-125">Select the agency that issued the document type.</span></span> <span data-ttu-id="56e2b-126">Пример: район/территория</span><span class="sxs-lookup"><span data-stu-id="56e2b-126">Example: Province/territory</span></span>
10. <span data-ttu-id="56e2b-127">Нажмите кнопку "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="56e2b-127">Click Save.</span></span>


