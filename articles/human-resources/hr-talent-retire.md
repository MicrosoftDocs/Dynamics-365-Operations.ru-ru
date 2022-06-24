---
title: Прекращение поддержки Dynamics 365 Talent — приложения Attract и Onboard
description: В этой статье описывается прекращение поддержки приложений Dynamics 365 Talent — Attract and Onboard.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3039b0a837335a777cdd6ff22b8b6e7c014ef956
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845094"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Прекращение поддержки приложений Dynamics 365 Talent: Attract и Onboard


В декабре 2019 мы объявили о прекращении поддержки приложений Dynamics 365 Talent Attract и Onboard с 1 февраля 2022, и отвели два года планирования для наших клиентов.

Дополнительные сведения о прекращении поддержки этих приложений см. в следующих разделах:
 - [Прекращение использования приложений Dynamics 365 Talent Attract и Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Подготовка более успешных сотрудников с помощью Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Мы будем продолжать поддерживать Dynamics 365 Human Resources, что поможет нашим клиентам получить ценные сведения о сотрудниках, необходимые для создания работы, управляемой данными, в нескольких областях, например:

- Компенсация
- Выгоды
- Отпуск и отсутствие
- Соответствие
- Связь с зарплатой
- Отзыв о производительности
- Обучение и сертификация
- Программы самообслуживания

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Вопросы и ответы об устаревании приложений Dynamics 365 Talent

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Что представляет собой взаимодействие с пользователем для приложений Dynamics 365 Talent Attract и Onboard с 1 февраля 2022 года?

Пользователи не смогут использовать приложения и будут перенаправлены на страницу прекращения поддержки.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Могут ли клиенты продолжать экспортировать данные для приложений Dynamics 365 Talent Attract и Onboard после 1 февраля 2022 года?
  
Нет, прекращение поддержки было объявлено в декабре 2019 года и необходимые возможности экспорта предоставляются до 1 февраля 2022 года. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Будут ли удалены данные клиента, относящиеся к приложениям Dynamics 365 Talent Attract и Onboard в Dataverse после 1 февраля 2022 года?

Нет, объекты Dataverse останутся в среде Microsoft Dataverse клиента даже после прекращения поддержки, если только система управления человеческим капиталом Talent не будет удалена.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Я знаю название среды Talent. Как можно посмотреть данные Attract и Onboard в Dataverse?

1.  Войдите в Power Apps: https://make.powerapps.com
2.  Выберите среду, в которой требуется просмотреть данные Attract и Onboard.
3.  Перейдите **Dataverse > Таблицы**. 
4.  Введите "msdyn_" в **Поиск**. Если отображается список таблиц, начинающийся с имен "msdyn_" + имена таблиц (пример: msdyn_candidate), значит была найдена среда с данными Attract и Onboard.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Я не знаю название среды Talent. Как найти среду с данными для приложений Dynamics 365 Talent: Attract и Dynamics 365 Talent: Onboard?

1)  Войдите в центр администрирования Power Platform: https://admin.powerplatform.microsoft.com/
2)  Выберите **Среды**.
3)  Выберите конкретную среду для оценки.
4)  Выберите **Ресурсы > приложения Dynamics 365**.
5)  Если вы видите установленное решение **HCM Talent**, в этой среде должны хранится данные Attract и Onboard. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> Решение **HCM Talent** также используется в Dynamics 365 Human Resources.
