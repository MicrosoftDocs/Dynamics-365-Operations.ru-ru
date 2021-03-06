---
title: Процесс обновления
description: Microsoft Dynamics 365 Human Resources — это действительное программное обеспечение как услуга (SaaS), которое обеспечивает непрерывное обновление служб для изменений приложения и платформы.
author: andreabichsel
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2466c53885340991aeeb0a07af83517473b332b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053643"
---
# <a name="update-process"></a>Процесс обновления

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources — это действительное программное обеспечение как услуга (SaaS), которое обеспечивает непрерывное обновление служб. Эти обновления содержат как изменения приложений, так и платформ, которые часто обеспечивают важные улучшения службы, в том числе обновления нормативных документов.

## <a name="update-policy"></a>Политика обновления

Обновления выпускаются регулярно для всех сред. Human Resources поддерживается в соответствии с [политикой жизненного цикла поддержки Майкрософт](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), которая обеспечивает единообразную и предсказуемую поддержку продукта.

## <a name="release-cadence"></a>Ритмичность выпуска 

Обновления Human Resources автоматически применяются ко всем средам. Human Resources предоставляет два типа выпусков:

- **Обновления служб**: обновления выполняются через каждые две недели, которые включают исправления ошибок и новые возможности. Обновления службы также включают применимые обновления платформы при их выпуске. Сведения о том, как выпускаются обновления платформы, см. в [Таблица 3: выпуски платформы](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md#table-3-platform-releases). Осуществляемой раз в две недели обновления имеют поэтапное глобальное развертывание по регионам. Дополнительные сведения об обновлениях раз в две недели см. в разделе [Что нового и что изменилось в Dynamics 365 Human Resources](hr-admin-whats-new.md).

    Все поддерживаемые центры обработки данных обновляются раз в две недели, если не указано иное. Регионы США, Австралия, Европа, Соединенное Королевство, Азия и Канада включены в обновления раз в две недели. 

- **Обновления решения Dataverse**: при необходимости эти обновления выполняются примерно каждые шесть недель. Они включают в себя новые объекты и изменения существующих объектов в Dataverse. Эти обновления выпускаются в тех же регионы, что и обновления раз в две недели, и для их репликации по всем центрам данных им требуется около шести недель. Обновления решения могут не соответствовать обновлениям раз в две недели службы.

> [!NOTE]
> Обновления решения доступны во всех центрах обработки данных после их выпуска. Если вы не ходите ждать автоматической репликации обновлений, можно вручную применить эти обновления к любой среде в любом центре обработки данных.

При необходимости Human Resources также предоставляет следующие типы исправлений:

- **Редакция (исправление)**: исправления ошибок, которые могут возникать либо в выпуске, либо отдельно от выпуска обновления служб раз в две недели

- **Экстренное исправление**: прогнозные и активные исправления, которые являются самостоятельными, могут включать только изменения конфигурации или кода для решения проблем в масштабе активного узла и могут происходить отдельно от выпуска обновлений служб раз в две недели

Выпуски анализируются, тестируются и проверяются во внутренней среде. После завершения построений они разворачиваются в производство.

## <a name="release-cadence-exceptions-in-2021"></a>Исключения из ритмичности выпуска в 2021 г.

Для учета праздников график выпуска для ноября и декабря 2021 выглядит следующим образом:

- Ноябрьский выпуск: 1 ноября –14 ноября
- Декабрьский выпуск: 29 ноября –12 декабря
 
Ритмичность в две недели будет возобновлена в обычном порядке 10 января 2022 года.

## <a name="communications"></a>Связь

Можно узнать, что есть в работе для модуля Human Resources и что мы сделали в следующих местах:

- [Дорожная карта Dynamics 365 Human Resources](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Планы выпуска Dynamics 365](/dynamics365/release-plans/)

- [Что нового и что изменилось в Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Поиск проблем в Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (только для связанных с платформой ошибок)

- [Блог Human Resources](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Сообщество Human Resources Yammer](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Предварительный просмотр функций в среде песочницы

Можно проверять функции предварительного просмотра в среде песочницы перед их включением в производственную среду. Дополнительные сведения об включении функций см. в разделе [Обзор управления функциями](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Все новые возможности остаются в виде предварительного просмотра по крайней мере на 30 дней, а обычно 30-60 дней. Основные функции обычно доступны в октябре и апрель каждого года, следующего за периодом предварительного просмотра. После отображения новых возможностей в рабочей области Управление функциями их можно включить. Некоторые функции могут быть включены по умолчанию.

Время от времени неотъемлемая функция будет включена по умолчанию и не может быть отключена (например, в рабочей области Управление функциями).

Когда функция обычно доступна, она может быть включена или выключена в производственных средах. Рабочая область Управление функциями показывает, что функция предварительного просмотра станет обязательной. Эта дата обычно приходится на 1 октября или 1 апреля, чтобы соответствовать полугодовым плановым выпускам. Вы не можете отключить обязательные функции. До тех пор, пока она не станет обязательной, можно включать и выключать функцию во всех средах.

Настоятельно рекомендуется предварительный просмотр функций в песочнице или в испытательной среде. Лучше всего создать копию текущей производственной среды или базы данных в среде песочницы, чтобы иметь возможность полного создания новых функций с данными.

Дополнительные сведения о подготовке среды песочницы см. в разделе [Подготовка проекта Human Resources](hr-admin-setup-provision.md). Чтобы удалить тестовую среду, см. раздел [Удаление экземпляра](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Отчет об ошибках

При проверке функций предварительного просмотра или попытке использовать новые возможности что-то может работать неправильно. Сообщите об ошибках через [Поддержку Microsoft Dynamics 365](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>См. также

[Планы выпусков Dynamics 365 и Power Platform](/dynamics365/release-plans)</br>
[Что нового и что изменилось в Dynamics 365 Human Resources](hr-admin-whats-new.md)</br>
[Политика жизненного цикла программного обеспечения](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]