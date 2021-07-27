---
title: Загрузка конфигураций электронной отчетности из Lifecycle Services
description: В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 1e20528cd0af00c46f1376e02097bf3171100769
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358703"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Загрузка конфигураций электронной отчетности из Lifecycle Services

[!include [banner](../includes/banner.md)]

В этой теме объясняется, как загрузить новейшую версию [конфигураций электронной отчетности (ER)](general-electronic-reporting.md#Configuration) из [библиотеки общих ресурсов](../lifecycle-services/asset-library.md) в Microsoft Dynamics Lifecycle Services (LCS).

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
> В зависимости от параметров электронной отчетности конфигурации проверяются после импорта. Возможно, вы получите уведомление об обнаруженных проблемах несоответствия. Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации. Дополнительные сведения см. в списке связанных тем для этой темы.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор электронной отчетности (ER)](general-electronic-reporting.md)

[Загрузка конфигураций электронной отчетности (ER) из глобального репозитория Configuration Service](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
