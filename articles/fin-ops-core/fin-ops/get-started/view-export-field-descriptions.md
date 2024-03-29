---
title: Просмотр и экспорт описаний полей
description: В этой статье описываются способы просмотра описаний полей и использования страницы "Описания полей" для экспорта описаний.
author: twheeloc
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 11534
ms.assetid: e2795f51-a8a7-4c74-bdb9-b1be93bdd358
ms.search.form: FieldDescriptions
ms.openlocfilehash: d2d59796b312d50d69bf7722b605c159a933a283
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292377"
---
# <a name="view-and-export-field-descriptions"></a>Просмотр и экспорт описаний полей

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

В этой статье описываются способы просмотра описаний полей и использования страницы "Описания полей" для экспорта описаний.

Некоторые из более сложных полей имеют описания полей. Эти описания отображаются при наведении указателя мыши на поле. Также можно просмотреть и экспортировать описания на странице **Описания полей**.

Не все страницы имеют описания полей. Мы хотим предоставить описания только для более сложных полей, а не для полей, использование которых очевидно. Таким образом, некоторые страницы не имеют описаний полей, некоторые страницы имеют несколько описаний, а некоторые из более сложных страниц, например многие страницы параметров, имеют множество описаний.

Если вы имеете доступ к среде разработки, вы можете добавить новые описания полей и настроить существующие описания. Например, можно добавить сведения о конкретной компании в описание поля. Дополнительные сведения см. в разделе [Настройка описаний полей](../../dev-itpro/user-interface/customize-field-help.md).

## <a name="see-field-descriptions-in-the-user-interface"></a>Просмотр описаний полей в пользовательском интерфейсе

Можно просматривать описания полей, наведя указатель мыши на поле. Если описание отсутствует, при наведении указателя мыши на поле отобразится имя поля.

> [!NOTE]
> В Dynamics AX 7.0 (февраль 2016 г.) описания полей можно просмотреть только на странице **Описания полей**.

На следующем рисунке показано описание поля, которое отображается при наведении указателя мыши на поле **Блокир. номенкл. при инвентаризации**.

[![Пример описания поля.](./media/field-description.png)](./media/field-description.png)

## <a name="use-the-field-descriptions-page-to-view-and-export-field-help"></a>Использование страницы "Описания полей" для просмотра и экспорта справки поля

Страница **Описания полей** позволяет просматривать и экспортировать описания полей. Можно одновременно просмотреть описания, доступные для одной страницы.

### <a name="view-the-descriptions-for-a-page"></a>Просмотр описаний для страницы

Чтобы просмотреть описания для страницы, выполните этот шаг.

- В поле **Выбор страницы** введите имя страницы. Либо щелкните стрелку, чтобы открыть список всех страниц, и просмотрите либо отфильтруйте список.

Можно использовать либо имя страницы, которое отображается в пользовательском интерфейсе (например, **Клиенты**), либо имя кода (имя AOT), доступное при щелчке страницы правой кнопкой мыши (например, **CustTable**).

Сведения о различных способах фильтрации списка страниц см. в разделе "Поиск страницы" далее в этой статье.

Если для параметра **Включить поля без описания** задать значение **Да**, будут отображаться все поля на странице независимо от того, имеют ли они описание поля.

### <a name="export-the-descriptions-for-a-page"></a>Экспорт описаний для страницы

Чтобы экспортировать описания для страницы, выполните эти шаги.

1. В поле **Выбор страницы** выберите страницу.
2. Нажмите кнопку **Открыть в Microsoft Office** в правом верхнем углу и щелкните **FieldDescriptionTmp**.

### <a name="searching-for-a-page"></a>Поиск страницы

Существует несколько способов поиска страницы в поле **Выбор страницы**. Во многих случаях вам потребуется щелкнуть стрелку в поле **Выбор страницы**, чтобы открыть раскрывающийся список, и выбрать страницу из отфильтрованного списка страниц.

- Введите часть имени и откройте раскрывающийся список, чтобы выбрать страницу из списка отфильтрованных страниц.
- Откройте раскрывающийся список и щелкните заголовок **Имя страницы** в верхней части списка или заголовок **Имя AOT страницы**. Откроется диалоговое окно, в котором можно использовать параметры расширенной фильтрации, например **Имя страницы начинается с**.
- Введите полное название страницы. При использовании этого параметра рекомендуется открыть раскрывающийся список и посмотреть, что еще есть в списке, даже если описания полей отображаются.

    - Если есть одно точное соответствие имени, будут показаны описания полей для этой страницы.
    - Если имеется несколько точных совпадений, описания не будут отображаться. Необходимо открыть раскрывающийся список и выбрать нужную страницу.
    - Если введенное имя является частью имени другой страницы, отобразятся описания для страницы. Однако при открытии раскрывающегося списка, можно просмотреть дополнительные страницы, которые содержат это имя.

Например, описания не отображаются при вводе **Инвентаризация** в поле **Выбор страницы**. Вы открываете раскрывающийся список и увидите две страницы с именем **Инвентаризация** и несколько страниц, в имени которых содержится слово "Инвентаризация". При выборе страницы с именем AOT **InventJournalCount** отобразятся описания полей для этой страницы. Однако, если снова открыть раскрывающийся список, вы увидите, что теперь список содержит все страницы, в имени AOT которых имеется InventJournalCount.

## <a name="troubleshooting"></a>Устранение неполадок

В этом разделе содержатся сведения, которые помогут устранить неполадки, с которыми можно столкнуться при использовании описаний полей.

### <a name="i-cant-find-a-field-description"></a>Не удается найти описание поля

Мы в процессе добавления описаний для более сложных полей. Если вам необходима помощь по определенному полю, дайте нам знать, добавив комментарий для этой статьи.

### <a name="the-field-description-isnt-helpful"></a>Описание полей не полезно

Дайте нам знать, добавив комментарий для этой статьи. Если возможно, укажите, какая дополнительная информация вам требуется.

### <a name="i-cant-find-a-field-on-the-field-descriptions-page"></a>Не удается найти поле на странице "Описания полей"

Для отображения всех полей на странице задайте параметру **Включить поля без описания** значение **Да**. Щелкните поле **Выбор страницы**, чтобы убедиться, что выбрана правильная страница. Если введенное имя является частью другого имени поля, возможно, вы выбрали страницу, которая имеет более длинное имя.

### <a name="i-cant-find-a-page-on-the-field-descriptions-page"></a>Не удается найти страницу на странице "Описания полей"

Сведения о различных способах поиска страниц см. в разделе "Поиск страниц" ранее в этой статье. Если вы ввели точное имя страницы, описания полей могут не отображаться, если существует несколько страниц с одинаковым именем. Щелкните стрелку в поле **Выбор страницы**, чтобы открыть отфильтрованный список доступных страниц.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка описаний полей](../../dev-itpro/user-interface/customize-field-help.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
