---
title: Установка, настройка и обновление клиентского портала
description: В этой теме приведены сведения о лицензировании и инструкции по установке для клиентского портала.
author: dasani-madipalli
manager: tfehr
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e61fc5f7151a0bb61d496d47f4ad4e727a2a1d65
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529538"
---
# <a name="install-set-up-and-update-the-customer-portal"></a>Установка, настройка и обновление клиентского портала

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="licensing-requirements"></a>Требования к лицензированию

Для реализации клиентского портала необходимы следующие лицензии:

- **Порталы Power Apps** — данная лицензия необходима для размещения клиентского портала. Порталы лицензируются в зависимости от использования. Дополнительные сведения см. в разделе [Требования к лицензированию порталов Power Apps](https://docs.microsoft.com/power-platform/admin/powerapps-flow-licensing-faq#portals).
- **Двойная запись** — у вас должны быть необходимые лицензии, чтобы включить двойную запись для объектов Supply Chain Management. Дополнительную информацию см. в [системных требованиях для двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req.md).

## <a name="dependencies-on-dual-write-and-power-apps-portals"></a>Зависимости двойной записи и порталов Power Apps

Клиентский портал зависит от порталов Power Apps и двойной записи, как показано на следующем рисунке.

![Зависимости клиентского портала](media/customer-portal-elements.png "Зависимости клиентского портала")

В отличие от других функций Supply Chain Management шаблон клиентского портала размещается на порталах Power Apps. Таким образом, клиентский портал ограничивается функциями и возможностями порталов Power Apps и объектов в двойной записи.

## <a name="required-setup-to-enable-the-customer-portal"></a><a name="required-setup"></a>Необходимая настройка для включения клиентского портала

Убедившись в наличии необходимых лицензий, можно настроить двойную запись, как описано в [инструкциях по начальной синхронизации двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/initial-sync.md).

Убедитесь, что следующие сопоставления объектов активированы в двойной записи:

- Заголовок заказа на продажу
- Сведения по заказам на продажу
- Счета
- Контактные лица
- Товары

После завершения настройки можно подготовить шаблон клиентского портала.

## <a name="provision-the-customer-portal"></a>Подготовка клиентского портала

Перед началом убедитесь, что [требуемая настройка](#required-setup) уже выполнена. Затем выполните следующие действия, чтобы подготовить клиентский портал.

1. Перейдите к [make.powerapps.com](https://make.powerapps.com/).
2. Убедитесь, что используете среду, в которой включена двойная запись.
3. На вкладке **Создать** перейдите к разделу **Начать из шаблона** и выберите шаблон с именем **Клиентский портал**.
4. Следуйте инструкциям на экране.

После завершения подготовки к порталу клиента можно получить доступ в разделе **Ваши приложения** на **домашней странице**.

> [!NOTE]
> Если решение с двойной записью не установлено в рабочей среде, будет выведено сообщение об ошибке и клиентский портал не будет подготовлен.

## <a name="update-the-customer-portal"></a>Обновление клиентского портала

Дополнительные возможности могут быть добавлены на клиентский портал позже. Любые изменения, вносимые корпорацией Майкрософт в соответствующие компоненты решения, будут автоматически отображаться в вашей среде. Однако для сайта, настроенного в вашей среде, изменения, внесенные в данные конфигурации, не будут автоматически отражены. Эти изменения потребуется применить вручную, получив код из нового шаблона и объединив его с подготовленным сайтом.

## <a name="additional-resources"></a>Дополнительные ресурсы

Чтобы узнать, как настроить клиентский портал, следует начать с изучения следующей документации по используемым технологиям:

- [Документация по порталам Power Apps](https://docs.microsoft.com/powerapps/maker/portals/overview)
- [Документация по двойной записи](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md)

Для эффективного управления порталами необходимо понимать порталы Power Apps и жизненный цикл Common Data Service. Дополнительные сведения см. на следующих ресурсах:

- [О жизненном цикле портала](https://docs.microsoft.com/powerapps/maker/portals/admin/portal-lifecycle)
- [Обновление портала](https://docs.microsoft.com/powerapps/maker/portals/admin/upgrade-portal)
- [Миграция конфигурации портала](https://docs.microsoft.com/powerapps/maker/portals/admin/migrate-portal-configuration)
- [Управление жизненным циклом решения: Dynamics 365 для приложений Customer Engagement](https://www.microsoft.com/download/details.aspx?id=57777)
