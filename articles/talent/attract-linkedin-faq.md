---
title: Вопросы и ответы по интеграции с LinkedIn
description: Этот раздел содержит ответы на вопросы, которые могут возникнуть в связи с интеграцией между LinkedIn и Microsoft Microsoft Dynamics 365 Talent - Attract.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462321"
---
# <a name="linkedin-integration-faq"></a>Вопросы и ответы по интеграции с LinkedIn

[!include [banner](includes/banner.md)]

LinkedIn — это крупнейшая в мире профессиональная сеть в Интернете. Microsoft Dynamics Talent: Attract интегрируется с LinkedIn для получения доступа к лучшим специалистам мира. Attract позволяет размещать объявления о вакансиях непосредственно в LinkedIn, а также позволяет вам извлекать сведения о кандидатах из LinkedIn в Attract.

## <a name="for-recruiters-and-hiring-managers"></a>Для специалистов по найму персонала и менеджеров по найму

Здесь приведены ответы на часто задаваемые вопросы об использовании Attract и LinkedIn совместно.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Какие функции LinkedIn можно получить с Attract?

Интеграция Attract с LinkedIn позволяет выполнять следующие задачи:

- [Размещение объявления о вакансиях в LinkedIn](./attract-post-jobs-to-linkedin.md) (в виде бесплатных ограниченных списков).
- [Поиск кандидатов с помощью LinkedIn Recruiter в Microsoft Dynamics 365 Talent — Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Что необходимо, чтобы можно было размещать объявления о вакансиях в LinkedIn?

Администратор должен [настроить интеграцию LinkedIn в Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). После этого можно приступать к работе.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Как публиковать объявления о вакансиях в LinkedIn из Attract?

После создания должности в Attract нужно просто выбрать кнопку **Опубликовать**, которая соответствует LinkedIn. Дополнительные сведения см. в разделе [Публикация вакансий в LinkedIn из Microsoft Dynamics 365 Talent — Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Можно ли получить сведения о кандидатах из LinkedIn в Attract?

Да. Если вы видите хорошего кандидата на LinkedIn, вы можете легко экспортировать информацию о кандидате в Attract. Дополнительные сведения см. в разделе [Поиск кандидатов с помощью LinkedIn Recruiter в Microsoft Dynamics 365 Talent — Attract](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Как можно получить помощь по доступу к LinkedIn из Attract?

Если вы не можете войти в систему или опубликовать объявления о вакансиях в LinkedIn из Attract, см. раздел [Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract](./attract-troubleshoot-linkedin.md).

Другие проблемы, связанные с Attract, см. в разделе [Получение поддержки по Microsoft Dynamics 365 Talent](./talent-support.md). Для получения помощи по LinkedIn см. [страницу поддержки LinkedIn](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>Для администраторов и разработчиков

Здесь приведены ответы на часто задаваемые вопросы об конфигурации интеграции между Attract и LinkedIn.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Как настроить Attract, чтобы специалисты по найму и менеджеры по найму могли размещать объявления о вакансиях в LinkedIn?

Можно настроить доступные параметры на вкладке **Интеграция с LinkedIn** в центре администрирования. Дополнительные сведения см. в разделе [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Можно ли экспортировать сведения о кандидатах из LinkedIn?

Да, но сначала необходимо настроить интеграцию с LinkedIn Recruiter. Дополнительные сведения см. в разделе [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Как можно размещать объявления о вакансиях на премиальных рекламных местах вакансий в LinkedIn?

Хотя у Attract есть мощное решение для публикации объявлений о вакансиях в LinkedIn, может оказаться необходимым обеспечить дополнительную гибкость. Например, может потребоваться, чтобы в дополнение к бесплатным ограниченным спискам можно было размещать объявления на премиальных рекламных местах вакансий, или может потребоваться, чтобы LinkedIn обрабатывал ваши размещения объявлений с помощью пакетных заданий более одного раза в день.

#### <a name="types-of-linkedin-job-posts"></a>Типы объявлений о вакансиях в LinkedIn

В LinkedIn предусмотрены следующие типы объявлений о вакансиях:

- **Ограниченный список** — бесплатные объявления о вакансиях, которые появляются в результатах поиска, когда кандидаты ищут вакансии в LinkedIn и на странице компании в LinkedIn. Ограниченные списки предназначены для лиц, активно ищущих вакансии. Этот тип списка — это тип, который Attract предоставляет в LinkedIn. В LinkedIn невозможно повысить уровень вакансий из ограниченного списка. Если требуется повысить уровень ограниченных списков, следует работать с LinkedIn для включения сканирования объявлений о вакансиях. Дополнительные сведения о сканировании объявлений о вакансиях см . в разделах [Ограниченные списки и премиальные рекламные места вакансий для сканирования объявлений о вакансиях](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) и [Сканирование объявлений о вакансиях плюс — вопросы и ответы](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Премиальные рекламные места вакансий** — закупленные объявления, которые появляются в различных местах в LinkedIn, таких как канал LinkedIn, сообщения электронной почты и область **Вакансии, которые могут вас заинтересовать**. Премиальные рекламные места вакансий предназначены для пассивных кандидатов, но они также отображаются при поиске вакансий.

Attract размещает объявления о вакансиях в LinkedIn в виде бесплатных ограниченных списков. Если необходимо использовать премиальные рекламные места вакансий, необходимо использовать сканирование объявлений о вакансиях с помощью LinkedIn Recruiter. Для сканирования объявлений о вакансиях требуется контракт сканирования объявлений о вакансиях с LinkedIn. Для получения дополнительных сведений см. раздел [Сканирование объявлений о вакансиях с помощью LinkedIn Recruiter — обзор](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Частота пакетной обработки в LinkedIn

LinkedIn обрабатывает объявления о вакансиях в пакете через Attract один раз в день. Таким образом, после размещения объявлений через Attract они могут появиться в LinkedIn с задержкой до 48 часов. Если требуется, чтобы вакансии в LinkedIn отображались быстрее, или если требуется дополнительная гибкость, можно воспользоваться интерфейсом прикладного программирования (API) Recruiter System Connect из LinkedIn. Дополнительные сведения см. в разделе [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Таблица параметров для размещения объявлений о вакансиях в LinkedIn

В следующей таблице описываются различные варианты размещения объявлений о вакансиях в LinkedIn. Это включает преимущества каждого варианта и дополнительную информацию.

|  | Attract | Сканирование объявлений о вакансиях с помощью LinkedIn Recruiter | API-интерфейс Recruiter System Connect |
|---|---|---|---|
| **Описание** | Attract размещает объявления о вакансиях в LinkedIn в виде XML-канала. | Компания заключает контракт с LinkedIn и предоставляет XML-канал для размещения объявлений о вакансиях. | Клиент использует API для синхронизации данных между Attract и LinkedIn Recruiter. |
| **Какие типы вакансий можно размещать?** | Ограниченный список | Премиальные рекламные места вакансий или ограниченный список | Ограниченный список |
| **Можно ли повысить уровень вакансии в LinkedIn?** | Нет | Премиальные рекламные места вакансий: Да<br>Ограниченные списки: Нет | Нет |
| **Как часто LinkedIn размещает объявления о вакансиях?** | Раз в день | Раз в день | Несколько раз в день, как определено в API |
| **Рекомендовано LinkedIn?** | Нет | Да | Нет |
| **Что требуется?** | Покупка Attract | Контракт сканирования объявлений о вакансиях с LinkedIn и покупка премиальных рекламных мест вакансий | Соглашение API с LinkedIn | 
| **Где можно найти дополнительные сведения?** | [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md) | [Сканирование объявлений о вакансиях с помощью LinkedIn Recruiter — обзор](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Вам не нужна лицензия LinkedIn Recruiter System Connect для размещения объявлений о вакансиях в LinkedIn с помощью Attract.

## <a name="see-also"></a>См. также

[Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md)

[Публикация вакансий в LinkedIn из Microsoft Dynamics 365 Talent — Attract](./attract-post-jobs-to-linkedin.md)

[Поиск кандидатов с помощью LinkedIn Recruiter в Microsoft Dynamics 365 Talent — Attract](./attract-linkedin-recruiter.md)

[Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]