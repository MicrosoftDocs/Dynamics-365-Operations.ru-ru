---
title: "Загрузка конфигураций электронной отчетности из Lifecycle Services"
description: "В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: be77d76194e9d38589548113cc650599d5af4323
ms.contentlocale: ru-ru
ms.lasthandoff: 06/13/2017

---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Загрузка конфигураций электронной отчетности из Lifecycle Services

[!include[banner](../includes/banner.md)]


В этом разделе описывается, как загрузить конфигурации электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).

В этом учебнике описывается процесс загрузки последней версии конфигураций электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).

1.  Войдите в Finance and Operations с помощью одной из следующих ролей:
    -   Разработчик электронной отчетности
    -   Консультант по функциональным возможностям электронной отчетности
    -   Системный администратор

2.  Перейдите в раздел **Управление организацией** &gt; **Электронная отчетность**.
3.  В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.
4.  На плитке **Майкрософт** щелкните **Репозитории**. [![обновление-er-из-lcs-для-ms-открытие-списка-репозиториев-ms](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **LCS**. Если этот репозиторий не отображается в сетке, выполните следующие действия.
    1.  Нажмите кнопку **Добавить**, чтобы добавить новый репозиторий.
    2.  Выберите **LCS** как тип репозитория.
    3.  Щелкните **Создать репозиторий**.
    4. Если будет предложено, следуйте инструкциям по авторизации.
    5.  Введите имя и описание репозитория.
    6.  Нажмите кнопку **ОК**, чтобы подтвердить новую запись репозитория.
    7.  В сетке выберите новый репозиторий типа **LCS**.

6.  Нажмите кнопку **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория. [![обновление-er-из-lcs-для-ms-создание-репозитория-lcs](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  В дереве конфигураций в левой области выберите требуемую конфигурацию электронной отчетности.
8.  На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.
9.  Нажмите кнопку **Импорт** для загрузки выбранной версии из LCS в текущий экземпляр Finance and Operations. **Примечание.** Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре Finance and Operations. [![обновление-er-из-lcs-для-ms-загрузка-конфигурации](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Примечание.** В зависимости от параметров электронной отчетности конфигурации проверяются после импорта. Возможно, вы получите уведомление об обнаруженных проблемах несоответствия. Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации. Дополнительные сведения см. в списке связанных статей для этого раздела.

<a name="see-also"></a>См. также
--------

[Обзор электронной отчетности](general-electronic-reporting.md)




