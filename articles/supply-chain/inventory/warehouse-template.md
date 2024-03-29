---
title: Настройка склада с помощью шаблона конфигурации склада
description: В этой статье рассматривается настройка склада с помощью шаблона конфигурации склада.
author: yufeihuang
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: dafd51a46b19f3709963ffc12b3c8c77b6c809ac
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070450"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Настройка склада с помощью шаблона конфигурации склада

[!include [banner](../includes/banner.md)]

В этой статье рассматривается настройка склада с помощью шаблона конфигурации склада. Существует несколько предварительно заданных шаблонов конфигурации, которые можно использовать. Сведения об использовании этих шаблонов см. в разделе [Шаблоны конфигурационных данных](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Сценарии, где могут быть полезными шаблоны конфигурации

Шаблоны конфигурации могут быть полезными во многих сценариях. Далее приводятся некоторые примеры.

- Вы завершили и проверили настройку конфигурации в тестовой среде и теперь хотите скопировать настройку в производственную среду.
- Вы хотите развернуть настройку склада в нескольких юридических лицах или создать новый склад в том же юридическом лице.
- Требуется быстро подготовиться для демонстрации функций склада.
- Требуется, чтобы существующие номенклатуры и склады использовали функциональные возможности модуля управления складом вместо функциональных возможностей управления запасами.

В этой статье рассматриваются первые два из этих сценариев. В нем показано, как можно использовать шаблон конфигурации для копирования настроек конфигурации из тестовой среды в производственную среду.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Копирование настройки конфигурации из тестовой среды в производственную среду

В этом сценарии настройка конфигурации для склада и некоторых процессов транзакции уже существует в тестовой среде. Теперь требуется скопировать настройку конфигурации для склада из тестовой среды в производственную среду.

> [!NOTE]
> Важно, чтобы при копировании настройки конфигурации были включены другие связанные данные настройки. Например, необходимо настроить продукты путем копирования настройки из тестовой среды. Однако вы не можете настроить фиксированные ячейки комплектации для продукта до создания этого продукта. Хотя отдельные шаблоны конфигурации не поддерживают этот тип зависимости, существуют шаблоны данных по умолчанию, которые его поддерживают. Можно легко включить эти шаблоны данных по умолчанию в процесс настройки конфигурации.

### <a name="export-a-default-warehouse-template"></a>Экспорт шаблона склада по умолчанию 

1. Откройте рабочую область **Управление данными**.

    > [!NOTE]
    > При использовании этой рабочей области в первый раз необходимо загрузить все информационные объекты перед продолжением.

2. Выберите плитку **Шаблоны**, затем выберите **Загрузить шаблоны по умолчанию** для загрузки шаблонов по умолчанию.

    > [!NOTE]
    > Пункт **Загрузить шаблоны по умолчанию** доступен только в представлении **Расширенное**. Выберите **Параметры структуры**, затем в поле **Просмотр значений по умолчанию** выберите **Расширенное представление**.

3. После загрузки шаблонов по умолчанию их можно изменить, чтобы они соответствовали требованиям бизнеса.

    > [!NOTE]
    > Для загрузки шаблонов по умолчанию и импорта шаблонов необходимо иметь доступ администратора системы. Это требование гарантирует, что все объекты правильно загружены в шаблон.

4. Убедитесь, что вы находитесь в юридическом лице, из которого требуется экспортировать относящиеся к компании данные.
5. В рабочей области выберите **Экспорт**.
6. Создайте новый проект экспорта.
7. Выберите **+ Добавить шаблон** и найдите шаблон склада по умолчанию **400 - WMS**. Этот шаблон добавляет информационные объекты в конфигурацию склада.

    > [!NOTE]
    > Если требуется фильтрация экспортируемых данных (например, требуется экспортировать только данные, относящиеся к определенному складу), необходимо оценить каждый информационный объект и добавить фильтрацию через запрос. Можно также экспортировать все данные, а затем удалить записи, которые не требуются в конечных файлах.

8. Выберите **Экспорт**. Экспортируются данные, связанные связаны со всеми информационными объектами в проекте.

Можно загрузить файл ZIP для пакета данных. Этот файл содержит все данные в выбранном формате (например, формат Excel). Как было указано, некоторые записи в файлах пакетов данных могут потребовать обновления, прежде чем их можно будет импортировать в производственную среду. При обновлении записи убедитесь в том, что вы не изменили имя файла.

### <a name="import-a-warehouse-configuration-setup"></a>Импорт настройки конфигурации склада

1. В конечной среде убедитесь, что вы находитесь в компании, в которую необходимо импортировать данные склада.

    > [!NOTE]
    > Перед выполнением импорта необходимо определить все зависимости данных. Например, шаблон **Управление складом** включает в себя информационный объект, который называется **Коды обработки склада**. Этот объект содержит данные, относящиеся к странице настройки **Коды метода обработки** (**Управление складом** > **Настройка** > **Мобильное устройство** > **Коды метода обработки**). Если имеющаяся настройка уже обрабатывает процесс возврата для заказов на продажу, поле **Код метода обработки возврата** содержит значение. Код метода обработки в этом поле относится к информационному объекту **Код метода обработки**, который входит в состав шаблона **Продажи и маркетинг**. Если данные из информационного объекта **Код метода обработки** не будут импортированы перед данными из поля **Коды методов обработки склада**, произойдет сбой процесса импорта.

2. В рабочей области **Управление данными** выберите **Импорт**.
3. Создать новый проект импорта.
4. Выберите **+ Добавить файл** и отправьте ZIP-файл для пакета данных.
5. Выберите **Импорт**. В представлении **Расширенное** можно использовать параметр **Фильтр** для быстрого получения обзора проблем, которые могут возникнуть во время импорта.

Журнал **Просмотр выполнения** содержит подробные сведения о каждом импортированном информационном объекте. Можно использовать представление промежуточного хранения данных для быстрого перехода к целевым данным. Таким образом можно просмотреть, как выглядят импортированные данные на соответствующих страницах в приложении. При использовании шаблонов данных по умолчанию последовательность импорта для каждого информационного объекта работает заранее определенным образом, помогая гарантировать, что все зависимые данные импортируются сначала. Если проект содержит пользовательские информационные объекты, необходимо убедиться, что определена правильная последовательность. Дополнительные сведения см. в разделе [Шаблоны конфигурационных данных](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md).

Для получения дополнительных сведений об использовании складского шаблона для копирования конфигурации склада из одной организации в новую организацию в это же экземпляре см. 3-минутное видео на YouTube об [использовании шаблона склада для копирования конфигурации для приложений для управления финансами и операциями](https://www.youtube.com/watch?v=K2WIfFlqJYs).

## <a name="related-article"></a>Связанная статья

[Шаблоны данных конфигурации](../../fin-ops-core/dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
