---
title: Настройка параметров управления льготами для компаний
description: Настройка параметров управления льготами для компаний в Microsoft Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 87d4f1e7580b333fd17d3b779aafa47c5baed424
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805666"
---
# <a name="configure-benefits-management-parameters-per-company"></a><span data-ttu-id="09204-103">Настройка параметров управления льготами для компаний</span><span class="sxs-lookup"><span data-stu-id="09204-103">Configure Benefits management parameters per company</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="09204-104">Для каждой организации, предлагающей льготы, необходимо настроить параметры сообщений электронной почты с подтверждением льгот.</span><span class="sxs-lookup"><span data-stu-id="09204-104">For each organization that offers benefits, you must configure settings for benefits confirmation emails.</span></span>

## <a name="configure-confirmation-email-settings"></a><span data-ttu-id="09204-105">Настройка параметров подтверждающих сообщений электронной почты</span><span class="sxs-lookup"><span data-stu-id="09204-105">Configure confirmation email settings</span></span>

1. <span data-ttu-id="09204-106">В рабочей области **Управление льготами** в **Настройка** выберите **Параметры Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="09204-106">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="09204-107">На вкладке **Управление льготами** укажите значения для следующих полей:</span><span class="sxs-lookup"><span data-stu-id="09204-107">In the **Benefits management** tab, specify values for the following fields:</span></span> 

   | <span data-ttu-id="09204-108">Поле</span><span class="sxs-lookup"><span data-stu-id="09204-108">Field</span></span> | <span data-ttu-id="09204-109">описание</span><span class="sxs-lookup"><span data-stu-id="09204-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09204-110">**Отправить подтверждение по электронной почте**</span><span class="sxs-lookup"><span data-stu-id="09204-110">**Send confirmation email**</span></span> | <span data-ttu-id="09204-111">Если эта функция включена, сотрудники будут получать подтверждающие сообщения по электронной почте, когда они выходят из интерфейса регистрации льгот в системе дистанционного обслуживания сотрудников.</span><span class="sxs-lookup"><span data-stu-id="09204-111">When this feature is on, a confirmation email will be sent to employees when they check out from the benefits enrollment experience in Employee self-service.</span></span> |
   | <span data-ttu-id="09204-112">**Шаблон подтверждения по электронной почте**</span><span class="sxs-lookup"><span data-stu-id="09204-112">**Confirmation email template**</span></span> | <span data-ttu-id="09204-113">Выберите шаблона электронной почты организации, который будет использоваться при отправке подтверждения регистрации.</span><span class="sxs-lookup"><span data-stu-id="09204-113">Select the organization email template to use when sending the enrollment confirmation.</span></span> <span data-ttu-id="09204-114">Если шаблон не выбран, будет отправлено следующее общее сообщение электронной почты:</span><span class="sxs-lookup"><span data-stu-id="09204-114">If you don't select a template, the following generic email will be sent:</span></span><br><br><span data-ttu-id="09204-115">%EmployeeFirstName%,</span><span class="sxs-lookup"><span data-stu-id="09204-115">%EmployeeFirstName%,</span></span><br><br><span data-ttu-id="09204-116">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="09204-116">Congratulations!</span></span> <span data-ttu-id="09204-117">Вы успешно завершили регистрацию на льготы.</span><span class="sxs-lookup"><span data-stu-id="09204-117">You’ve successfully completed benefits enrollment.</span></span><br><br><span data-ttu-id="09204-118">Спасибо,</span><span class="sxs-lookup"><span data-stu-id="09204-118">Thank you,</span></span><br><span data-ttu-id="09204-119">Льготы <наименование компании/организации>.</span><span class="sxs-lookup"><span data-stu-id="09204-119"><Company/Org name> Benefits.</span></span> |
   | <span data-ttu-id="09204-120">**Адрес электронной почты отправителя по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="09204-120">**Default email sender address**</span></span> | <span data-ttu-id="09204-121">Адрес электронной почты, который будет использоваться при отправке сообщения электронной почты с подтверждением.</span><span class="sxs-lookup"><span data-stu-id="09204-121">The email address to use when sending the confirmation email.</span></span> |

3. <span data-ttu-id="09204-122">Нажмите **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="09204-122">Select **Save**.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]