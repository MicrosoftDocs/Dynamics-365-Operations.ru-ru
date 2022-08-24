---
title: Загрузка конфигураций электронной отчетности из Lifecycle Services
description: В этой статье описывается, как загружать конфигурации электронной отчетности (ER) из Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.form: ERSolutionImport, ERWorkspace
ms.openlocfilehash: f48dd14bc3009550d78bd71db030c172d2ef6450
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277827"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Загрузка конфигураций электронной отчетности из Lifecycle Services

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как загрузить новейшую версию [конфигураций электронной отчетности (ER)](general-electronic-reporting.md#Configuration) из [библиотеки общих ресурсов](../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Использование LCS в качестве репозитория для конфигураций ER [устаревает](../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Дополнительные сведения см. в [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](../../../finance/localizations/rcs-lcs-repo-dep-faq.md).

1. Войдите в приложение с помощью одной из следующих ролей:

    - Разработчик электронной отчетности
    - Консультант по функциональным возможностям электронной отчетности
    - Системный администратор

2. Перейдите в раздел **Управление организацией** &gt; **Рабочие области** &gt; **Электронная отчетность**.
3. В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.
4. На плитке **Майкрософт** выберите **Репозитории**.

    [![Плитка Майкрософт на странице конфигураций локализации.](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **LCS**. Если этот репозиторий не отображается в сетке, выполните следующие действия.

    1. Выберите **Добавить**, чтобы добавить репозиторий.
    2. Выберите **LCS** как тип репозитория.
    3. Выберите **Создать репозиторий**.
    4. При появлении запроса об авторизации выполните инструкции на экране.
    5. Введите имя и описание репозитория.
    6. Выберите **ОК**, чтобы подтвердить новую запись репозитория.
    7. В сетке выберите новый репозиторий типа **LCS**.

6. Выберите **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория.

    [![Страница репозиториев конфигураций.](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > При возникновении проблем с доступом к репозиторию LCS для загрузки конфигураций из библиотеки общих активов в LCS можно загрузить конфигурации из [глобального репозитория](er-download-configurations-global-repo.md).

7. В дереве конфигураций в левой области выберите требуемую конфигурацию электронной отчетности.
8. На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.
9. Выберите **Импорт** для загрузки выбранной версии из LCS в текущий экземпляр.

    > [!NOTE]
    > Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре.

    [![Страница репозитория конфигурации.](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> В зависимости от параметров электронной отчетности конфигурации проверяются после импорта. Возможно, вы получите уведомление об обнаруженных проблемах несоответствия. Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации. Дополнительные сведения см. в списке связанных разделов для этой статьи.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности (ER)](general-electronic-reporting.md)

[Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
