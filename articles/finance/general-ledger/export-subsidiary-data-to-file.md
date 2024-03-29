---
title: Экспорт данных дочерних компаний в файлы
description: В этой статье объясняется, как подготовиться к экспорту данных из Microsoft Dynamics 365 Finance и последующему их импорту в консолидированное юридическое лицо.
author: jinniew
ms.date: 11/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 30d69f9a2813621df410a29568644f264392fb49
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779970"
---
# <a name="export-subsidiary-data-to-files"></a>Экспорт данных дочерних компаний в файлы

[!include [banner](../includes/banner.md)]

Страница **Экспорт** (**Администрирование системы \> Рабочие области \> Импорт/экспорт**) используется для подготовки к экспорту данных дочерних компаний в файлы, которые затем могут быть импортированы в консолидированное юридическое лицо. Дополнительные сведения о процессах импорта и экспорта см. в разделе [Обзор заданий импорта и экспорта данных](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).

1. Создайте юридическое лицо для процесса консолидации. Сведения о порядке создания юридических лиц см. в разделе [Создание юридических лиц](../../fin-ops-core/fin-ops/organization-administration/tasks/create-legal-entity.md). Дополнительные сведения см. в разделах [Подготовка юридического лица для использования в процессе консолидации](prepare-company-for-consolidation.md) и [Настройка дочернего юридического лица для консолидации](set-up-subsidiary-company-for-consolidation.md). 

2. Перейдите в раздел **Консолидации \> Экспорт сальдо компаний**. На странице **Экспорт сальдо компаний** на вкладке **Критерии** укажите подробные сведения о консолидации, задав следующие поля.

    | Поле                             | описание |
    |-----------------------------------|-------|
    | **Счет ГК**                      | Укажите счета для консолидации. Чтобы включить все счета, оставьте это поле пустым. |
    | **Использовать счет консолидации**         | Если вы указали счета консолидации, установите для этого параметра значение **Да**. |
    | **Выбрать счет консолидации из** | Выберите **Счет ГК** или **Группа счетов консолидации**. |
    | **Группы счетов консолидации**       | Выберите группу счетов консолидации для выбранного вами счета консолидации. |
    | **Период консолидации**              | Укажите даты "С" и "По" для консолидации. |
    | **Включить фактические суммы**            | Установите для этого параметра значение **Да**, чтобы включить фактические значения. |
    | **Включить бюджетные суммы**            | Установите для этого параметра значение **Да**, чтобы включить бюджетные значения в консолидации. |
    | **Модели бюджета**                     | Укажите модель бюджета для включения. |

3. На вкладке **Финансовые аналитики** укажите подробные сведения по консолидации:

    - Укажите сведения о финансовых аналитиках, которые должны переноситься из проводок по счетам дочерних компаний в проводки консолидированного юридического лица.
    - Выберите финансовые аналитики в списке.
    - Определите правильную спецификацию для каждой консолидированной финансовой аналитики. Доступны следующие параметры: **Аналитика**, **Групповая аналитика**, **Счета компании** и **Счет**.

        > [!NOTE]
        > Параметр **Групповая аналитика** позволяет определить значение аналитики, используемое группой консолидируемых компаний.

    - Укажите порядок консолидации сегментов.

4. На вкладке **Юридические лица** выполните следующие действия, чтобы указать юридическое лицо, для которого выполняется экспорт:

    1. Выберите **Создать**.
    2. В поле **Исходное юридическое лицо** введите юридическое лицо.

        Если по отношению к нескольким дочерним компаниям из одной базы данных применяются одинаковые критерии, данные из этих компаний можно перенести в отдельные файлы экспорта в рамках одной операции:

        1. Создайте строку для каждого дочернего юридического лица, чьи счета следует экспортировать в файлы. Эти файлы в дальнейшем будут импортированы в консолидированное юридическое лицо.
        2. Для каждой дочерней компании введите наименование дочерней компании и имя файла экспорта, который будет создан во время выполнения задания экспорта.

    3. В поле **Тип счета разницы преобразования** выберите **Прибыли и убытки** или **Балансовый отчет**.
    4. Введите имя файла для файла экспорта, который будет создан.

5. Выберите **OK**, чтобы выполнить экспорт.

После завершения экспорта вы получите сообщение, которое показывает количество записей, которые были сохранены в каждом файле. Теперь можно импортировать файлы в консолидированное юридическое лицо.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
