---
title: Расширение Talent с помощью Power Apps и Power Automate
description: В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.
author: negudava
manager: Annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: Dynamics 365 Human Resources;PowerApps;Flow;Common Data Service
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core;Experience Apps;Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: negudava
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36b8145764338b91bfedf96c43a7137a89831742
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410112"
---
# <a name="extend-with-power-apps-and-power-automate"></a><span data-ttu-id="12597-103">Расширение с помощью Power Apps и Power Automate</span><span class="sxs-lookup"><span data-stu-id="12597-103">Extend with Power Apps and Power Automate</span></span>

<span data-ttu-id="12597-104">В этой статье описывается несколько примеров сценариев расширения для Microsoft Dynamics 365 Human Resources, использующих Microsoft Power Apps и Microsoft Power Automate.</span><span class="sxs-lookup"><span data-stu-id="12597-104">This article describes some examples of extensibility scenarios for Microsoft Dynamics 365 Human Resources that use Microsoft Power Apps and Microsoft Power Automate.</span></span> <span data-ttu-id="12597-105">Можно импортировать пакет решения, связанный с каждым примером, в среду Power Apps.</span><span class="sxs-lookup"><span data-stu-id="12597-105">You can import the solution package that is associated with each example into your Power Apps environment.</span></span> <span data-ttu-id="12597-106">Затем можно использовать эти пакеты как руководство или как основу для реализации сценариев, которые применимы к вашей организации.</span><span class="sxs-lookup"><span data-stu-id="12597-106">You can then use the packages either as guidance or as starting points to implement scenarios that are applicable to your organization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="12597-107">Если вы хотите использовать шаблоны и приложения, описанные в этом разделе, "как есть", обязательно проверьте их, чтобы убедиться в том, что они охватывают все сценарии, относящиеся к вашей реализации.</span><span class="sxs-lookup"><span data-stu-id="12597-107">If you want to use the templates and apps that are described in this topic "as is," be sure to test them to make sure that they cover all the scenarios that are specific to your implementation.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="12597-108">Необходимые условия</span><span class="sxs-lookup"><span data-stu-id="12597-108">Prerequisites</span></span>

- <span data-ttu-id="12597-109">Для импорта пакетов пользователи должны иметь разрешение **Создатель среды**.</span><span class="sxs-lookup"><span data-stu-id="12597-109">To import packages, users must have the **Environment Maker** permission.</span></span>
- <span data-ttu-id="12597-110">Для экспорта или импорта приложений пользователи должны иметь лицензию плана 2 Power Apps или пробную лицензию плана 2 Power Apps.</span><span class="sxs-lookup"><span data-stu-id="12597-110">To export or import apps, users must have a Power Apps Plan 2 license or a Power Apps Plan 2 trial license.</span></span>

## <a name="integration-with-office-365-power-automate"></a><span data-ttu-id="12597-111">Интеграция с Office 365, Power Automate</span><span class="sxs-lookup"><span data-stu-id="12597-111">Integration with Office 365, Power Automate</span></span>

<span data-ttu-id="12597-112">Приложение **Интеграция с Office 365** может использоваться для извлечения сведений о рабочей группе для выполнивших вход пользователей из Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="12597-112">The **Integration with Office 365** app can be used to extract team information for signed-in users from Microsoft Office 365.</span></span> <span data-ttu-id="12597-113">Ссылается на работников в Human Resources, чтобы извлечь типы идентификации сотрудников.</span><span class="sxs-lookup"><span data-stu-id="12597-113">It references workers in Human Resources to extract employee identification types.</span></span> <span data-ttu-id="12597-114">Менеджеры могут проверять даты окончания сроков действия типов кодов сотрудника.</span><span class="sxs-lookup"><span data-stu-id="12597-114">Managers can check expiration dates of employee ID types.</span></span> <span data-ttu-id="12597-115">Кроме того, они могут отправлять напоминаниями по электронной почте, если срок действия типа кода сотрудника истекает.</span><span class="sxs-lookup"><span data-stu-id="12597-115">They can also send an email reminder if the employee ID type is expiring.</span></span> <span data-ttu-id="12597-116">Power Automate интегрируется с Power Apps для отправки этого напоминания.</span><span class="sxs-lookup"><span data-stu-id="12597-116">Power Automate integrates with Power Apps to send this reminder.</span></span> <span data-ttu-id="12597-117">При отправке напоминания подтверждение будет отправлено обратно в Power Apps из Power Automate.</span><span class="sxs-lookup"><span data-stu-id="12597-117">Confirmation will be sent back to Power Apps from Power Automate when the reminder is sent.</span></span> <span data-ttu-id="12597-118">Типы идентификации включают водительское удостоверение, паспорт и другие приемлемые формы удостоверения личности.</span><span class="sxs-lookup"><span data-stu-id="12597-118">Identification types include driver's license, passport, and other acceptable forms of ID.</span></span>

<span data-ttu-id="12597-119">Это приложение можно расширить для использования в других сценариях.</span><span class="sxs-lookup"><span data-stu-id="12597-119">You can extend this app for other scenarios.</span></span> <span data-ttu-id="12597-120">Например, оно может использоваться для отображения сведений об отпусках рабочей группы, события календаря и любых других событиях, связанных с рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="12597-120">For example, you can use it to show team vacation information, calendar events, and any team-specific events.</span></span>

<span data-ttu-id="12597-121">Чтобы загрузить шаблон приложение **Интеграция с Office 365, Power Automate**, перейдите [Интеграция с Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="12597-121">To download the **Integration with Office 365, Power Automate** app, go to [Integration with Office 365](https://go.microsoft.com/fwlink/?linkid=2081787) on the Microsoft Download Center.</span></span>

## <a name="power-automate--sql-connect-and-execute"></a><span data-ttu-id="12597-122">Power Automate — подключение и выполнение SQL</span><span class="sxs-lookup"><span data-stu-id="12597-122">Power Automate – SQL Connect and execute</span></span>

<span data-ttu-id="12597-123">Шаблон **Power Automate — подключение и выполнение SQL** подключается к Microsoft SQL Server и позволяет выполнять запросы SQL.</span><span class="sxs-lookup"><span data-stu-id="12597-123">The **Power Automate – SQL Connect and execute** template connects to Microsoft SQL Server and enables SQL queries to be run.</span></span>

<span data-ttu-id="12597-124">Хотя этот шаблон считывает и обновляет таблицы SQL, его можно расширить и использовать в других сценариях.</span><span class="sxs-lookup"><span data-stu-id="12597-124">Although this template reads and updates SQL tables, you can extend it and use it for other scenarios.</span></span> <span data-ttu-id="12597-125">Например, он может использоваться для заполнения промежуточной таблицы в Common Data Service с записями из SQL Server, а также для периодической синхронизации промежуточной таблицы с помощью инкрементной принудительной отправки из SQL Server.</span><span class="sxs-lookup"><span data-stu-id="12597-125">For example, you can use it to fill a staging table in Common Data Service with records from SQL Server, and to periodically synchronize the staging table by using an incremental push from SQL Server.</span></span>

<span data-ttu-id="12597-126">Расширенный запрос интегрируется с Flow, чтобы включить преобразование данных и выполнить инкрементную принудительную отправку.</span><span class="sxs-lookup"><span data-stu-id="12597-126">Advanced Query is integrated with Flow to enable Data transformation and incremental push.</span></span>

<span data-ttu-id="12597-127">Для загрузки шаблона **Power Automate — подключение и выполнение SQL** перейдите к пункту [Power Automate — подключение и выполнение SQL](https://go.microsoft.com/fwlink/?linkid=2081789) в центре загрузки Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="12597-127">To download the **Power Automate – SQL Connect and execute** template, go to [Power Automate – SQL Connect and execute](https://go.microsoft.com/fwlink/?linkid=2081789) on the Microsoft Download Center.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12597-128">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="12597-128">Additional resources</span></span>

[<span data-ttu-id="12597-129">Microsoft Power Platform</span><span class="sxs-lookup"><span data-stu-id="12597-129">The Microsoft Power Platform</span></span>](https://docs.microsoft.com/power-platform/admin/admin-documentation)</br>