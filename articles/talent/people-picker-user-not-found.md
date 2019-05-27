---
title: Пользователь не найден в средстве выбора пользователей в Attract или Onboard
description: В этом разделе объясняется, что делать, когда пользователи в клиенте организации не видны в средстве выбора пользователей в приложениях Dynamics 365 for Talent Attract или Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-22
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d5a2c61fc21578d1db4c1bf0c3dfaf0c7a93298c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518924"
---
# <a name="azure-active-directory-users-not-found-in-people-picker"></a><span data-ttu-id="3425c-103">Пользователи Azure Active Directory отсутствуют в средстве выбора пользователей</span><span class="sxs-lookup"><span data-stu-id="3425c-103">Azure Active Directory users not found in People Picker</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="3425c-104">Выдать</span><span class="sxs-lookup"><span data-stu-id="3425c-104">Issue</span></span>

<span data-ttu-id="3425c-105">Некоторые допустимые пользователи в Microsoft Azure Active Directory (Azure AD) для клиента не отображаются при поиске имени в средстве выбора пользователей в приложениях Dynamics 365 for Talent Attract или Onboard.</span><span class="sxs-lookup"><span data-stu-id="3425c-105">Certain valid users in Microsoft Azure Active Directory (Azure AD) for the tenant do not appear when searching for the name in the People Picker in the Dynamics 365 for Talent Attract or Onboard applications.</span></span>

## <a name="cause"></a><span data-ttu-id="3425c-106">Причина</span><span class="sxs-lookup"><span data-stu-id="3425c-106">Cause</span></span>

<span data-ttu-id="3425c-107">Определенные пользователем в настоящее время не поддерживаются в приложениях Attract и Onboard.</span><span class="sxs-lookup"><span data-stu-id="3425c-107">Certain user types are not currently supported in the Attract and Onboard applications.</span></span> <span data-ttu-id="3425c-108">Убедитесь, что пользователь не является гостевым пользователем Azure AD B2B.</span><span class="sxs-lookup"><span data-stu-id="3425c-108">Verify that the user is not an Azure AD Business to Business (B2B) guest user.</span></span> <span data-ttu-id="3425c-109">Сведения "Тип пользователя" можно найти в колонке Azure Active Directory на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="3425c-109">"User Type" information can be found in the Azure Active Directory blade on the Azure portal.</span></span>

<span data-ttu-id="3425c-110">Дополнительные сведения об Azure B2B см. в разделе [Что такое доступ гостевого пользователя в Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span><span class="sxs-lookup"><span data-stu-id="3425c-110">For more information about Azure B2B, see [What is guest user access in Azure Active Directory B2B](https://docs.microsoft.com/en-us/azure/active-directory/b2b/what-is-b2b).</span></span>

<span data-ttu-id="3425c-111">Для пользователей, не являющихся пользователями B2B, имеются отдельные пользователи, которые могут иметь неполные свойства "Тип пользователя" в объекте **Пользователь**.</span><span class="sxs-lookup"><span data-stu-id="3425c-111">For non-B2B users, there are certain users who may have an incomplete "User Type" property on the **User** object.</span></span> <span data-ttu-id="3425c-112">Это можно проверить и исправить с помощью модуля Azure AD Powershell.</span><span class="sxs-lookup"><span data-stu-id="3425c-112">This can be verified and fixed using the Azure AD Powershell module.</span></span> <span data-ttu-id="3425c-113">Дополнительные сведения см. в разделе [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span><span class="sxs-lookup"><span data-stu-id="3425c-113">For more information, see [Azure AD](https://docs.microsoft.com/en-us/powershell/module/azuread/?view=azureadps-2.0).</span></span>

## <a name="resolution"></a><span data-ttu-id="3425c-114">Приказ</span><span class="sxs-lookup"><span data-stu-id="3425c-114">Resolution</span></span>

<span data-ttu-id="3425c-115">Чтобы выполнить следующие действия для устранения проблемы, необходимо иметь разрешения "Глобальный администратор" в клиенте Azure Active Directory или разрешения для **User.ReadWrite.All**.</span><span class="sxs-lookup"><span data-stu-id="3425c-115">To complete the following steps to resolve the issue, you will need to have "Global Administrator" permissions on the Azure Active Directory tenant or permissions for **User.ReadWrite.All**.</span></span>

<span data-ttu-id="3425c-116">Чтобы проверить "Тип пользователя" для затронутого пользователя.</span><span class="sxs-lookup"><span data-stu-id="3425c-116">To verify the "User Type" for the affected user.</span></span>

```
PS C:\>Get-AzureADUser -ObjectId "testUpn@tenant.com"
```
<span data-ttu-id="3425c-117">Команда возвращает следующую информацию.</span><span class="sxs-lookup"><span data-stu-id="3425c-117">The command returns the following information.</span></span>
```
ObjectId                             DisplayName UserPrincipalName      UserType
--------                             ----------- -----------------      --------
5e8b0f4d-2cd4-4e17-9467-b0f6a5c0c4d0 New user    testUpn@tenant.com     
```
<span data-ttu-id="3425c-118">Отметьте свойство **UserType** для пользователя.</span><span class="sxs-lookup"><span data-stu-id="3425c-118">Note the **UserType** property on the user.</span></span> <span data-ttu-id="3425c-119">Если свойство **UserType** не заполнено, например не имеет значение "Участник" или "Гость", обновите свойство **UserType** с помощью следующей команды.</span><span class="sxs-lookup"><span data-stu-id="3425c-119">If the **UserType** is blank, for example not "Member" or "Guest", update the **UserType** using the following command.</span></span>

```
PS C:\>Set-AzureADUser -ObjectId "testUpn@tenant.com" -UserType Member
```
