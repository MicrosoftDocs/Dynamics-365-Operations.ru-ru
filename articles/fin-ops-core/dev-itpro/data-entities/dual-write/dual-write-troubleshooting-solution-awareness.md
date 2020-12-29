---
title: Устранение неполадок, связанных с поддержкой решений
description: В этом разделе содержатся сведения об устранении неполадок, связанных с поддержкой решений.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 79b2920b80ce4a8b419c2a146e15babc061cf64d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683579"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a><span data-ttu-id="c80bd-103">Устранение неполадок, связанных с поддержкой решений</span><span class="sxs-lookup"><span data-stu-id="c80bd-103">Troubleshoot issues related to solution awareness</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="c80bd-104">Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c80bd-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="c80bd-105">Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с поддержкой решений.</span><span class="sxs-lookup"><span data-stu-id="c80bd-105">Specifically, it provides information that can help you fix issues that are related to solution awareness.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c80bd-106">Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="c80bd-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="c80bd-107">В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c80bd-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="error-on-the-dual-write-page"></a><span data-ttu-id="c80bd-108">Ошибка на странице двойной записи</span><span class="sxs-lookup"><span data-stu-id="c80bd-108">Error on the Dual-write page</span></span>

<span data-ttu-id="c80bd-109">На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:</span><span class="sxs-lookup"><span data-stu-id="c80bd-109">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="c80bd-110">*Объект с именем 'msdyn\_dualwriteentitymap' с namemapping='Logical' не найден в MetadataCache.*</span><span class="sxs-lookup"><span data-stu-id="c80bd-110">*The entity with a name 'msdyn\_dualwriteentitymap' with namemapping='Logical' was not found in the MetadataCache.*</span></span>

<span data-ttu-id="c80bd-111">Чтобы устранить проблему, убедитесь, что базовое решение двойной записи установлено в Dataverse.</span><span class="sxs-lookup"><span data-stu-id="c80bd-111">To fix the issue, make sure that the dual-write core solution is installed in Dataverse.</span></span> <span data-ttu-id="c80bd-112">Базовое решение двойной записи является необходимым условием для поддержки решений.</span><span class="sxs-lookup"><span data-stu-id="c80bd-112">The dual-write core solution is a prerequisite for solution awareness.</span></span>
