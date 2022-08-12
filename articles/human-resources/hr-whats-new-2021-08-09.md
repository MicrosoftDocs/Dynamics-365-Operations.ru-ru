---
title: Что нового и что изменилось в Dynamics 365 Human Resources (9 августа 2021 г.)
description: В этой статье описываются новые или измененные функции в Microsoft Dynamics 365 Human Resources от 9 августа 2021 года.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58926e5a6c1476db84fa41945dc92196eb24f4bf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068465"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Что нового и что изменилось в Dynamics 365 Human Resources (9 августа 2021 г.)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В этой статье описываются новые, измененные или ожидаемые в ближайшее время функции в Microsoft Dynamics 365 Human Resources.

Дополнительные сведения о нашем процессе обновления и графике см. в разделе [Процесс обновления](hr-admin-setup-update-process.md).

Дополнительные сведения о новых функциях и ожидаемых датах общей доступности см. в разделе [Обзор волны 2 выпуска Dynamics 365 Human Resources 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>В данном выпуске

Этот выпуск включает следующие новые функции и исправления ошибок. Изменения применяются для номера сборки 8.1.4393.

### <a name="bug-fixes"></a>Исправления ошибок

Этот выпуск содержит следующие исправления ошибок.

> [!NOTE]
> Наша цель — предоставить эту информацию вам как можно скорее. Мы можем обновить эту статью для включения в нее исправлений ошибок, которые были сделаны в сборке после первоначальной публикации этой статьи.

| Номер проблемы | Проблема | Описание |
| --- | --- | --- |
| 558385 | При включенном параметре **Автоматически выбирать кандидатов** для кандидатов по умолчанию кандидат по умолчанию не выбирается. | Этот проблема исправлена. Несколько кандидатов по умолчанию автоматически выбираются в подходящих планах, когда включен параметр **Автоматически выбирать кандидатов** на странице **Общие параметры Human Resources**. |
| 589617 | На странице **Отгул** балансы **Доступно для покупки** и **Доступно для продажи** остаются пустыми, если доступ ограничен конкретной компанией. | Этот проблема исправлена. На странице **Отгул** показаны правильные **Доступно для покупки** и **Доступно для продажи**, если доступ пользователя ограничен конкретной компанией. |

## <a name="in-preview"></a>В режиме предварительного просмотра

В предварительной версии доступны следующие новые функции. Дополнительные сведения о порядке включения и выключения функций см. в разделе [Управление функциями](hr-admin-manage-features.md).

| Функция | План выпуска | Документация |
| --- | --- | --- |
| Рабочая область управления льготами | [Рабочая область управления льготами (предварительная версия)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Рабочая область управления льготами](hr-benefits-management-workspace.md) |
| Включить упрощенную интеграцию зарплаты (API интеграции зарплаты) | [Включение упрощенной интеграции с поставщиками зарплаты](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API интеграции зарплаты](hr-admin-integration-payroll-api-introduction.md)|
| Использование менеджера отсутствия для управления отпуском | [Использование менеджера отсутствия для управления отпуском](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | В этом выпуске обновляется представление рабочей области менеджера отсутствия. Дополнительные сведения см. в разделе [Настройка роли менеджера отсутствия](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Настройка требования вложения для типа отпуска | [Настройка требования вложения для типа отпуска](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Настройка типов отпусков и отсутствий](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Настройка единиц измерения отпуска для каждого типа отпуска | [Настройка единиц измерения отпуска для каждого типа отпуска](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Настройка типов отпусков и отсутствий](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Разрешение маркировки сотрудников как готовых к оплате | [Разрешение маркировки сотрудников как готовых к оплате](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Готовы платить](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Скоро

Полный список запланированных функций и их запланированных выпусков см. в разделе [Обзор выпуска волны 2 Dynamics 365 Human Resources от 2021 года](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Функция | Подробности |
| --- | --- |
| Обновление платформы 10.0.21 (45) | Планируется начать развертывание обновления платформы 10.0.21 с сервисным выпуском 4 октября 2021 года. Дополнительные сведения см. в разделе [Обновления платформы для версии 10.0.21 приложений для управления финансами и операциями (октябрь 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>См. также

[Что нового и что изменилось в Управление персоналом](hr-admin-whats-new.md)</br>
[Обзор выпуска Dynamics 365 Human Resources 2021, волна 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Процесс обновления](hr-admin-setup-update-process.md)</br>
[Управление функциями](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

