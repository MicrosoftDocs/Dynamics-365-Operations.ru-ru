---
title: Публикация вакансий в LinkedIn из Attract
description: В этом разделе объясняется, как использовать Dynamics 365 Talent - Attract для публикации объявлений о вакансиях на LinkedIn.
author: andreabichsel
manager: AnnBe
ms.date: 07/08/2019
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
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 782a2e5de6edf0e85c4d32a0910f5f3c01981a01
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462320"
---
# <a name="post-jobs-to-linkedin-from-attract"></a>Публикация вакансий в LinkedIn из Attract

[!include [banner](includes/banner.md)]

LinkedIn — это крупнейшая профессиональная сеть в Интернете, предоставляющая вам доступ к лучшим специалистам в мире. Microsoft Dynamics 365 Talent: Attract помогает получить нужных специалистов, позволяя размещать объявления о вакансиях непосредственно из Attract в LinkedIn.

Attract позволяет размещать объявления в ограниченных списках в LinkedIn без дополнительных затрат. Эти списки доступны только через партнеров программного обеспечения LinkedIn, таких как Attract. Они не отображаются в панели **Вакансии** на странице LinkedIn вашей компании, поскольку там отображаются только оплаченные списки. Однако они отображаются, когда потенциальные кандидаты просматривают все доступные вакансии. Ограниченные списки также отображаются в результатах поиска вакансий в LinkedIn.

После [создания вакансии](./creating-jobs-attract.md) в приложении Attract достаточно выбрать кнопку, чтобы эта вакансия стала доступна тысячами потенциальных кандидатов в LinkedIn.

В следующей таблице показаны действия, которые можно выполнить с LinkedIn в зависимости от роли пользователя.

| Роль | Действия, которые можно выполнить |
|---|---|
| Администрирование | Размещение, повторное размещение и отмена размещения |
| Специалист по комплектации штата | Только чтение |
| Наниматель | Размещение, повторное размещение и отмена размещения |
| Проводящий собеседование | Нет доступа |
| Только для чтения | Только чтение |

Дополнительные сведения о ролях пользователей в Attract см. в разделе [Безопасность и управление ролями в Attract](./security-attract.md).

Если вы являетесь администратором и вам нужны дополнительные сведения о настройке интеграции LinkedIn с Attract, см. раздел [Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md).

Вакансии, опубликованные в LinkedIn, отображаются на действующем сайте LinkedIn. В LinkedIn отсутствует тестовая среда для публикации вакансий. Таким образом, следите, чтобы случайно не опубликовать тестовые объявления о вакансиях.

## <a name="post-jobs-to-linkedin"></a>Публикация вакансий в LinkedIn

1. Откройте в Attract вакансию, которую необходимо разместить на сайте LinkedIn.
2. На вкладке **Объявления** выберите кнопку **Опубликовать**, которая соответствует LinkedIn.

    [![Публикация вакансий из Attract в LinkedIn](./media/attract-post-job-to-linkedin.png)](./media/attract-post-job-to-linkedin.png)

3. В диалоговом окне **Создание веб-адреса "Подать заявление"** выберите параметр в разделе **Кандидаты могут подавать заявление при помощи**. Рекомендуется выбирать **Ссылка в Attract**.
4. Выберите **Готово**.
5. В окне сообщения **Отправить для размещения** выберите **Подтвердить**.

После того как сайт LinkedIn успешно завершит подачу, раздел **Объявления** вакансии в Attract показывает статус LinkedIn как **Опубликовано**. Вакансия может появиться в LinkedIn с задержкой до 48 часов.

Когда заинтересованные кандидаты выбирают **Просмотр** рядом со списком, они увидят полные сведения о вакансии вместе со сведениями о том, как подать заявление.

Все вакансий, опубликованные через приложение Attract, публикуются в ограниченных списках. Дополнительные сведения об ограниченных списках в LinkedIn см. в разделе [Ограниченные списки и премиальные рекламные места вакансий для сканирования объявлений о вакансиях](https://www.linkedin.com/help/recruiter/answer/79049).

Если вы не можете опубликовать объявления о вакансиях в LinkedIn, см. раздел [Устранение неполадок интеграции с LinkedIn и Microsoft Dynamics 365 Talent — Attract](./attract-troubleshoot-linkedin.md).

## <a name="see-also"></a>См. также

[Вопросы и ответы по интеграции Attract с LinkedIn](./attract-linkedin-faq.md)

[Настройка интеграции с LinkedIn для Microsoft Dynamics 365 Talent — Attract](./attract-admin-linkedin.md)

[Создание, утверждение и публикация вакансий в Attract](./creating-jobs-attract.md)

[Поиск кандидатов с помощью LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Устранение неполадок интеграции с LinkedIn](./attract-troubleshoot-linkedin.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]