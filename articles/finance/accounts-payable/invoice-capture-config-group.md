---
title: Конфигурационные группы решения Invoice Capture
description: В этой статье содержится общая информация о конфигурационных группах в решении Invoice Capture.
author: sunfzam
ms.date: 09/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfe5ae35b4f87a350d944b30a49251081766ad27
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691220"
---
# <a name="invoice-capture-solution-configuration-groups"></a>Конфигурационные группы решения Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Пользователи могут управлять списком полей накладной и параметром проверки вручную для юридических лиц, используя конфигурационные группы. Пользователи могут настроить конфигурации накладных для разных юридических лиц в группах. Все юридические лица в одной конфигурационной группе используют одинаковые поля накладной и параметр ручной проверки.

## <a name="manage-configuration-groups"></a>Управление конфигурационными группами

Чтобы управлять конфигурационными группами с помощью приложения, перейдите в раздел **Настройка**, затем выберите **Настройка системы \> Определение компонента конфигурационных групп**.

На странице **Определение конфигурационных групп** на главной вкладке отображается список конфигурационных групп, которые были определены. Здесь также показана конфигурационная группа по умолчанию. Для каждой группы конфигурации доступны следующие действия:

- **Копировать конфигурационную группу** — можно создать новую конфигурационную группу путем копирования существующей группы. Новая группа имеет те же значения, что и исходная группа для всех полей, за исключением **Имя группы** и **Описание группы**. После дублирования конфигурационной группы выберите **ОК**.
- **Удаление конфигурационных групп** — чтобы удалить конфигурационную группу, выберите ее, затем выберите **Удалить**.

    > [!NOTE]
    > Конфигурационную группу по умолчанию нельзя удалить.

- **Изменить код конфигурационной группы** — для редактирования кода конфигурационной группы выберите поле **Код группы** и обновите значение. Код группы не должен содержать пробелов и специальных символов и его длина не должна превышать 20 символов.

    > [!NOTE]
    > Значение поля **Код группы** можно обновить только один раз.

- **Изменить описание конфигурационной группы** — для редактирования описания конфигурационной группы выберите поле **Описание** и обновите значение.
- **Изменить настройку проверки вручную** — пользователи могут определять, следует ли проверять накладную вручную. Чтобы изменить настройку проверки вручную, выберите параметр **Требуется проверка вручную**. Имеются следующие варианты:

    - **Всегда проверять вручную** — выберите этот параметр, если накладные в конфигурационной группе всегда требуют проверки вручную.
    - **Для ошибок и предупреждений** — выберите этот параметр, если накладные, содержащие сообщения об ошибках или предупреждающие сообщения, требуют проверки вручную.
    - **Для ошибок** — выберите этот параметр, если накладные, содержащие сообщения об ошибках, требуют проверки вручную.

- **Изменить параметр оценки достоверности** — показатель достоверности представляет собой метаданные, которые предоставляет решение Invoice Capture, чтобы сообщить точность распознанных данных накладных. Чем выше оценка, тем точнее могут быть распознанные данные. Конфигурация позволяет пользователям определять, когда необходимо проводить проверку вручную, на основе показателя достоверности. Пользователи могут изменять пороговый показатель достоверности для накладных. Чтобы обновить параметр оценки достоверности, выберите поле **Показатель достоверности** и обновите значение.

    Имеется два типа оповещений для оценок достоверности:

    - **Предупреждение** — поля накладной, уровень достоверности которых выше порога предупреждения, рассматриваются как правильные. Порог предупреждения должен быть больше порога ошибки и меньше 100.
    - **Ошибка** — поля накладной, уровень достоверности которых ниже порога ошибки, рассматриваются как распознанные неправильно. Пользователю будут выведены сообщения об ошибках. Порог ошибок должен быть больше 0 (нуля) и меньше порога предупреждений. Будут отображаться предупреждающие сообщения для полей накладной, имеющих показатель достоверности между пороговым значением предупреждения и пороговым значением ошибки.

- **Управление полями накладной** — пользователи могут управлять списком полей накладной, которые отображаются в средстве параллельного просмотра. На вкладке **Управление полями накладной** выберите символ шестеренки, выберите поля накладной, которые требуется добавить, затем выберите **Сохранить**. Выбранные поля будут добавлены в список. Чтобы удалить поле накладной из списка, выберите **Удалить** в поле.

### <a name="manage-file-filters-optional"></a>Управление фильтрами файлов (необязательно)

Управление фильтрами файлов позволяет пользователям определять дополнительные фильтры для файлов входящих накладных. Файлы, которые не удовлетворяют критерию фильтрации, будут получены и будут отображаться в списке **Полученные файлы**, но они будут показывать ошибки проверки файлов. Это поведение отличается от поведения для фильтров, определенных в канале. Для тех фильтров файлы, которые не удовлетворяют критерию, вообще не будут получены. Пользователи могут просматривать входящие файлы и определять, является ли каждый из них недействительной накладной, и они могут исключить файл или вручную включить его для распознавания и включения в распознанные накладные.

При установке решения Invoice Capture определяется фильтр файлов по умолчанию. Этот фильтр файлов является глобальным. Если необходимо использовать другие параметры фильтрации, можно обновить фильтр по умолчанию. Если поле является обязательным, выберите **Обязательно**. 

### <a name="accepted-file-size"></a>Допустимый размер файла

Можно выбрать допустимый размер файла.

> [!NOTE]
> Файлы размером более 20 480 килобайт (КБ) не поддерживаются.

### <a name="supported-file-types"></a>Поддерживаемые типы файлов

В настоящее время поддерживаются следующие типы файлов:

- PDF
- PNG
- JPG
- JPEG
- TIF
- TIFF