---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad55de4b660de89d323f32a1ce2911d880c24ec5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793569"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="21c7e-103">Расширение с помощью Power Apps и Power Automate</span><span class="sxs-lookup"><span data-stu-id="21c7e-103">Extend with Power Apps and Power Automate</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="21c7e-104">В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="21c7e-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="21c7e-105">Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="21c7e-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="21c7e-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="21c7e-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21c7e-107">Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="21c7e-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="21c7e-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="21c7e-108">Prerequisites</span></span>

- <span data-ttu-id="21c7e-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="21c7e-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="21c7e-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.</span><span class="sxs-lookup"><span data-stu-id="21c7e-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-microsoft-365-power-automate"></a><span data-ttu-id="21c7e-111">Интеграция с Microsoft 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="21c7e-111">Integration with Microsoft 365, Power Automate</span></span>

<span data-ttu-id="21c7e-112">Приложение **Интеграция с Microsoft 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="21c7e-112">The **Integration with Microsoft 365** app can be used to extract team information for signed-in users from Microsoft 365.</span></span> <span data-ttu-id="21c7e-113">Ссылается на работников в Human Resources, чтобы извлечь типы идентификации сотрудников.</span><span class="sxs-lookup"><span data-stu-id="21c7e-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="21c7e-114">Менеджеры могут проверять даты окончания сроков действия типов кодов сотрудника.</span><span class="sxs-lookup"><span data-stu-id="21c7e-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="21c7e-115">Кроме того, они могут отправлять напоминаниями по электронной почте, если срок действия типа кода сотрудника истекает.</span><span class="sxs-lookup"><span data-stu-id="21c7e-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="21c7e-116">Power Automate интегрируется с Power Apps для отправки этого напоминания.</span><span class="sxs-lookup"><span data-stu-id="21c7e-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="21c7e-117">При отправке напоминания подтверждение будет отправлено обратно в Power Apps из Power Automate.</span><span class="sxs-lookup"><span data-stu-id="21c7e-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="21c7e-118">Типы идентификации включают водительское удостоверение, паспорт и другие приемлемые формы удостоверения личности.</span><span class="sxs-lookup"><span data-stu-id="21c7e-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="21c7e-119">Это приложение можно расширить для использования в других сценариях.</span><span class="sxs-lookup"><span data-stu-id="21c7e-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="21c7e-120">Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="21c7e-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="21c7e-121">Чтобы загрузить приложение **Интеграция с Microsoft 365, Power Automate** перейдите к пункту [Интеграция с Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="21c7e-121">To download the **Integration with Microsoft 365, Power Automate** app, go to [Integration with Microsoft 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="21c7e-122">Power Automate — подключение и выполнение SQL</span><span class="sxs-lookup"><span data-stu-id="21c7e-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="21c7e-123">Шаблон **Power Automate — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="21c7e-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="21c7e-124">Хотя этот шаблон считывает и обновляет таблицы SQL, его можно расширить и использовать в других сценариях.</span><span class="sxs-lookup"><span data-stu-id="21c7e-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="21c7e-125">Например, он может использоваться для заполнения промежуточной таблицы в Dataverse с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21c7e-125">For example, you can use it to fill a staging table in Dataverse with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="21c7e-126">Расширенный запрос интегрируется с Flow, чтобы включить преобразование данных и выполнить инкрементную принудительную отправку.</span><span class="sxs-lookup"><span data-stu-id="21c7e-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="21c7e-127">Для загрузки шаблона **Power Automate — подключение и выполнение SQL** перейдите к пункту [Power Automate — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="21c7e-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21c7e-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="21c7e-128">Additional resources</span></span>

[<span data-ttu-id="21c7e-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="21c7e-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]