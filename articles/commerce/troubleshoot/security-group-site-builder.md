---
title: Во время начального развертывания невозможно настроить группу безопасности для конструктора сайтов Commerce
description: В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда группа безопасности Microsoft Azure Active Directory (Azure AD) для конструктора сайтов Commerce не отображается в качестве параметра при создании компонентов электронной коммерции в Microsoft Dynamics Lifecycle Services (LCS) в ходе начального развертывания нового клиента электронной коммерции.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 36ea43e19f395e3914d3eda1a9b8f5487b0926c5
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585504"
---
# <a name="cant-configure-a-security-group-for-commerce-site-builder-during-initial-deployment"></a><span data-ttu-id="133f5-103">Во время начального развертывания невозможно настроить группу безопасности для конструктора сайтов Commerce</span><span class="sxs-lookup"><span data-stu-id="133f5-103">Can't configure a security group for Commerce site builder during initial deployment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="133f5-104">В этом разделе приведены инструкции по устранению неполадок, которые могут помочь, когда группа безопасности Microsoft Azure Active Directory (Azure AD) для конструктора сайтов Commerce не отображается в качестве параметра при создании компонентов электронной коммерции в Microsoft Dynamics Lifecycle Services (LCS) в ходе начального развертывания нового клиента электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="133f5-104">This topic provides troubleshooting guidance that can help when the Microsoft Azure Active Directory (Azure AD) security group for Commerce site builder doesn't appear as an option when you create e-commerce components in Microsoft Dynamics Lifecycle Services (LCS) during initial deployment of a new e-commerce tenant.</span></span>

## <a name="description"></a><span data-ttu-id="133f5-105">описание</span><span class="sxs-lookup"><span data-stu-id="133f5-105">Description</span></span>

<span data-ttu-id="133f5-106">При создании компонентов электронной коммерции в рамках процесса развертывания нового клиента электронной коммерции, который содержит компонент конструктора сайтов Commerce, группа безопасности Azure AD не отображается в диалоговом окне в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="133f5-106">When you create the e-commerce components as part of the process of deploying a new e-commerce tenant that includes the Commerce site builder component, the Azure AD security group doesn't appear as an option in the dialog box.</span></span>

## <a name="resolution"></a><span data-ttu-id="133f5-107">Приказ</span><span class="sxs-lookup"><span data-stu-id="133f5-107">Resolution</span></span>

### <a name="provision-the-e-commerce-site-with-a-user-in-the-correct-tenant"></a><span data-ttu-id="133f5-108">Предоставьте сайту электронной коммерции пользователя в надлежащем клиенте</span><span class="sxs-lookup"><span data-stu-id="133f5-108">Provision the e-commerce site with a user in the correct tenant</span></span>

1. <span data-ttu-id="133f5-109">Перейдите в раздел [порталу Azure](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="133f5-109">Go to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="133f5-110">В рамках клиента, для которого был предоставлен проект LCS для вашего сайта электронной коммерции, следуйте указаниям в разделе [Создание базовой группы и добавление участников с помощью Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span><span class="sxs-lookup"><span data-stu-id="133f5-110">Under the tenant that the LCS project for your e-commerce site was provisioned for, follow the instructions in [Create a basic group and add members using Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal).</span></span>
1. <span data-ttu-id="133f5-111">Перейдите в раздел [LCS](https://lcs.dynamics.com/) и выполните вход, используя учетную запись, которая использует тот же клиент, что и только что созданная группа безопасности Azure AD.</span><span class="sxs-lookup"><span data-stu-id="133f5-111">Go to [LCS](https://lcs.dynamics.com/), and sign in by using an account that shares the same tenant as the Azure AD security group that you just created.</span></span> <span data-ttu-id="133f5-112">Учетная запись должна иметь доступ для просмотра группы безопасности Azure AD.</span><span class="sxs-lookup"><span data-stu-id="133f5-112">The account must have access to view the Azure AD security group.</span></span>
1. <span data-ttu-id="133f5-113">Выполните шаги настройки для настройки сайта электронной коммерции.</span><span class="sxs-lookup"><span data-stu-id="133f5-113">Complete the setup steps to configure the e-commerce site.</span></span> <span data-ttu-id="133f5-114">При подготовке компонентов электронной коммерции в диалоговом окне теперь группа безопасности должна отображаться как параметр.</span><span class="sxs-lookup"><span data-stu-id="133f5-114">When you provision the e-commerce components, the security group should now appear as an option in the dialog box.</span></span>

> [!NOTE]
> <span data-ttu-id="133f5-115">Чтобы поле в диалоговом окне было заполнено списком групп безопасности, необходимо выбрать **Ввод** после ввода имени созданной группы безопасности Azure AD.</span><span class="sxs-lookup"><span data-stu-id="133f5-115">To ensure that the field in the dialog box is filled with the list of security groups, you must select **Enter** after you enter the name of the Azure AD security group that you created.</span></span> <span data-ttu-id="133f5-116">В результатах поиска будут перечислены все группы безопасности Azure AD, которые начинаются с текста поиска, и к которым пользователь имеет доступ.</span><span class="sxs-lookup"><span data-stu-id="133f5-116">The search results will list all the Azure AD security groups that start with the search text, and that the user has access to.</span></span> <span data-ttu-id="133f5-117">Можно использовать более короткое условие поиска, чтобы иметь возможность расширить результаты поиска.</span><span class="sxs-lookup"><span data-stu-id="133f5-117">You can use a shorter search term to allow for broader search results.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="133f5-118">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="133f5-118">Additional resources</span></span>

[<span data-ttu-id="133f5-119">Создание базовой группы и добавление участников с помощью Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="133f5-119">Create a basic group and add members using Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-groups-create-azure-portal)

[<span data-ttu-id="133f5-120">Развертывание нового арендатора электронной коммерции</span><span class="sxs-lookup"><span data-stu-id="133f5-120">Deploy a new e-commerce tenant</span></span>](../deploy-ecommerce-site.md)