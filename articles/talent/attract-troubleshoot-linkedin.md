---
title: Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent - Attract
description: В этой теме объясняется, как устранять неполадки при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 06/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 79f138ad9aeb203bce19cc93237fca96bffd015f
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008228"
---
# <a name="troubleshoot-integration-with-linkedin"></a>Устранение неполадок интеграции с LinkedIn

[!include [banner](../includes/banner.md)]

Следующие сведения помогут в устранении неполадок, которые могут возникнуть при попытке публикации объявлений о вакансиях в LinkedIn из Microsoft Dynamics 365 Talent: Attract.

## <a name="you-cant-sign-in-to-linkedin-from-attract"></a>Нельзя войти в LinkedIn из Attract

Если вы не можете войти в LinkedIn из Attract, попробуйте следующие действия:

1. Убедитесь, что учетные данные LinkedIn, введенные в Attract, действительные и правильные.
2. Если учетные данные действительные и правильные, обратитесь в [службу поддержки LinkedIn](https://www.linkedin.com/help/linkedin).
3. Если неполадка не устранена, обратитесь в [службу поддержки Майкрософт](./talent-support.md).

## <a name="job-posts-from-attract-dont-appear-on-linkedin"></a>Объявления о вакансиях из Attract не отображаются в LinkedIn

Если вакансия не появилось в LinkedIn через 24 часа, попробуйте выполнить следующие действия:

1. Убедитесь, что код LinkedIn вашей компании отображается на странице компании LinkedIn и правильно введен в центре администрирования Attract. Дополнительные сведения об изменении настроек LinkedIn в центре администрирования см. в разделе [Настройка интеграции с LinkedIn](attract-admin-linkedin.md). Дополнительные сведения о кодах компании LinkedIn см. в разделе [Назначение кода компании LinkedIn с доской вакансий LinkedIn — часто задаваемые вопросы](https://www.linkedin.com/help/linkedin/answer/98972).
2. Проверьте сведения о вакансии в LinkedIn, чтобы убедиться в том, что адрес заполнен. Для успешной публикации объявления о вакансии в LinkedIn требуется, по крайней мере, город и страна или регион вакансии.
3. Убедитесь, что вакансия не дублирует другую вакансию, которая была опубликована в LinkedIn. LinkedIn не публикует вакансии, которые являются дубликатами премиальных рекламных мест вакансий или ограниченных списков LinkedIn из другого источника. Убедитесь, что другой сотрудник компании не опубликовал эту вакансию вручную.

## <a name="see-also"></a>См. также

[Вопросы и ответы по LinkedIn](./attract-linkedin-faq.md)

[Публикация вакансий в LinkedIn из Attract](./attract-post-jobs-to-linkedin.md)

[Поиск кандидатов с помощью LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Создание вакансий](./creating-jobs-attract.md)

[Устранение неполадок интеграции с LinkedIn](./attract-troubleshoot-linkedin.md)
