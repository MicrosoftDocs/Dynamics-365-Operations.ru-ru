---
title: Отправка конфигурации в Lifecycle Services
description: В этой статье описывается, как создать новую конфигурацию электронной отчетности (ER) и отправить ее в Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
ms.openlocfilehash: 28ad20956b4b621abdb74332187d8601c10ac164
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290075"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a>Отправка конфигурации в Lifecycle Services

[!include [banner](../../includes/banner.md)]

В этой статье поясняется, как пользователь с ролью системного администратора или разработчика электронной отчетности может создать новую [конфигурацию электронной отчетности (ER)](../general-electronic-reporting.md#Configuration) и отправить ее в [библиотеку ресурсов уровня проекта](../../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Использование LCS в качестве репозитория для конфигураций ER [устаревает](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Дополнительные сведения см. в [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

В этом примере вам предстоит создать конфигурацию и отправить ее в LCS для демонстрационной компании под названием Litware, Inc. Эти шаги можно выполнить в любой компании, поскольку конфигурации электронной отчетности являются общими для всех компаний. Для выполнения этих шагов необходимо сначала выполнить шаги в теме [Создание поставщиков конфигурации и установка их в качестве активных](er-configuration-provider-mark-it-active-2016-11.md). Также требуется доступ к LCS.

1. Войдите в приложение с помощью одной из следующих ролей:

    - Разработчик электронной отчетности
    - Системный администратор

2. Перейдите в раздел **Управление организацией** \> **Рабочие области** \> **Электронная отчетность**.
3. Выберите компанию **Litware, Inc.** и пометьте ее как **Активная**.
4. Выберите **Конфигурации**.

<a name="accessconditions"></a>
> [!NOTE]
> Убедитесь, что текущий пользователь Dynamics 365 Finance является членом проекта LCS, содержащего [библиотеку активов](../../lifecycle-services/asset-library.md#asset-library-support), которая используется для импорта конфигураций электронной отчетности.
>
> Невозможно получить доступ к проекту LCS из репозитория электронной отчетности, который представляет другой домен, отличный от домена, используемого в Finance. При попытке будет отображен пустой список проектов LCS, и вы не сможете импортировать конфигурации электронной отчетности из библиотеки активов уровня проекта в LCS. Чтобы получить доступ к библиотекам активов уровня проекта из репозитория электронной отчетности, который используется для импорта конфигураций электронной отчетности, выполните вход в Finance, используя учетные данные пользователя, принадлежащего к клиенту (домену), для которого была выполнена подготовка текущего экземпляра Finance.

## <a name="create-a-new-data-model-configuration"></a>Создать новой конфигурации модели данных

1. Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.
2. На странице **Конфигурации** выберите **Создать конфигурацию**, чтобы открыть раскрывающееся диалоговое окно.

    В этом примере вам предстоит создать конфигурацию, которая содержит пример модели данных для электронных документов. Эта конфигурация модели данных будет отправлена в LCS позже.

3. В поле **Имя** введите **Пример конфигурации модели**.
4. В поле **Описание** введите **Пример конфигурации модели**.
5. Выберите **Создать конфигурацию**.
6. Выберите **Конструктор моделей**.
7. Выберите **Создать**.
8. В поле **Имя** введите **Точка входа**.
9. Выберите **Добавить**.
10. Нажмите **Сохранить**.
11. Закройте страницу.
12. Выберите **Изменить статус**.
13. Выберите **Завершено**.
14. Нажмите **ОК**.
15. Закройте страницу.

## <a name="register-a-new-repository"></a>Регистрация нового репозитория

1. Перейдите в раздел **Управление организацией \> Рабочие области \> Электронная отчетность**.

2. В разделе **Поставщики конфигурации** выберите плитку **Litware, Inc.**

3. На плитке **Litware, Inc.** выберите **Репозитории**.

    Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.

4. Выберите **Добавить**, чтобы открыть раскрывающееся диалоговое окно.

    Теперь можно добавить новый репозиторий.

5. В поле **Тип репозитория конфигурации** выберите **LCS**.
6. Выберите **Создать репозиторий**.
7. В поле **Проект** введите или выберите значение.

    В данном примере выберите требуемый вариант LCS. Вы должны иметь [доступ](#accessconditions) к проекту.

8. Нажмите **ОК**.

    Заполните новую запись репозитория.

9. В списке пометьте выбранную строку.

    В данном примере выберите запись репозитория **LCS**.

    Обратите внимание, что зарегистрированный репозиторий помечается текущим поставщиком. Другими словами, в этот репозиторий можно поместить только конфигурации, принадлежащие данному поставщику, и, следовательно, отправить их в выбранный проект LCS.

10. Выберите **Открыть**.

    Вы открываете репозиторий для просмотра списка конфигураций электронной отчетности. Если выбранный проект еще не использовался для совместного использования конфигураций электронной отчетности, список будет пустым.

11. Закройте страницу.
12. Закройте страницу.

## <a name="upload-a-configuration-into-lcs"></a>Отправка конфигурации в LCS

1. Перейдите в раздел **Управление организацией \> Электронная отчетность \> Конфигурации**.
2. На странице **Конфигурации** в дереве конфигураций выберите пункт **Пример конфигурации модели**.

    Вы должны выбрать созданную конфигурацию, которая уже завершена.

3. В списке найдите и выберите требуемую запись.

    Для этого примера выберите версию выбранной конфигурации со статусом **Завершено**.

4. Выберите **Изменить статус**.
5. Выберите **Поделиться**.

    Статус конфигурации изменяется с **Завершено** на **Общие**, когда конфигурация публикуется в LCS.

6. Нажмите **ОК**.
7. В списке найдите и выберите требуемую запись.

    Для этого примера выберите версию конфигурации со статусом **Общие**.

    Обратите внимание, что статус выбранной версии изменился с **Завершено** на **Общие**.

8. Закройте страницу.
9. Выберите **Репозитории**.

    Теперь можно открыть список репозиториев для поставщика конфигурации Litware, Inc.

10. Выберите **Открыть**.

    В данном примере выберите репозиторий **LCS** и откройте его.

    Обратите внимание, что выбранная конфигурация отображается как актив выбранного проекта LCS.

11. Откройте LCS, перейдя на <https://lcs.dynamics.com>.
12. Откройте проект, который использовался ранее для регистрации репозитория.
13. Откройте библиотеку активов проекта.
14. Выберите тип актива **Конфигурация GER**.

    В списке должна быть указана отправленная вами конфигурация электронной отчетности.

    Обратите внимание, что отправленную конфигурацию LCS можно импортировать в другой экземпляр, если поставщики имеют доступ к этому проекту LCS.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
