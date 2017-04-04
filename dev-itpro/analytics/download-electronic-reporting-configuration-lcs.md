---
title: "Загрузка конфигураций электронной отчетности из Lifecycle Services"
description: "В этом разделе объясняется, как загрузить электронной отчетности (ER) конфигурации из Microsoft Dynamics Lifecycle Services (LCS)."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Загрузка конфигураций электронной отчетности из Lifecycle Services

В этом разделе объясняется, как загрузить электронной отчетности (ER) конфигурации из Microsoft Dynamics Lifecycle Services (LCS).

В этом учебнике описывается процесс загрузки последней версии конфигураций электронной отчетности из Microsoft Dynamics Lifecycle Services (LCS).

1.  Войдите в Dynamics 365 for Operations с помощью одной из следующих ролей:
    -   Разработчик электронной отчетности
    -   Консультант по функциональным возможностям электронной отчетности
    -   Системный администратор

2.  Последовательно выберите пункты **управления организацией**&gt;**электронной отчетности**.
3.  В разделе **Поставщики конфигурации** выберите плитку **Майкрософт**.
4.  На плитке **Майкрософт** щелкните **Репозитории**. [![Update-ER-FROM-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  На странице **Репозиторий конфигураций** в сетке выберите существующий репозиторий типа **LCS**. Если этот репозиторий не отображается в сетке, выполните следующие действия.
    1.  Нажмите кнопку **Добавить**, чтобы добавить новый репозиторий.
    2.  Выберите **LCS** как тип репозитория.
    3.  Щелкните **Создать репозиторий**.
    4.  Введите имя и описание репозитория.
    5.  Нажмите кнопку **ОК**, чтобы подтвердить новую запись репозитория.
    6.  В сетке выберите новый репозиторий типа **LCS**.

6.  Нажмите кнопку **Открыть** для просмотра списка конфигураций электронной отчетности для выбранного репозитория. [![Update-ER-FROM-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  В дереве конфигураций в левой области выберите требуемую конфигурацию электронной отчетности.
8.  На экспресс-вкладке **Версии** выберите требуемую версию выбранной конфигурации электронной отчетности.
9.  Нажмите кнопку **Импорт** для загрузки выбранной версии из LCS в текущий экземпляр Dynamics 365 for Operations. **Примечание.** Кнопка **Импорт** недоступна для версий конфигурации электронной отчетности, которые уже установлены в текущем экземпляре Dynamics 365 for Operations. [![Update-ER-FROM-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Примечание.** В зависимости от параметров электронной отчетности конфигурации проверяются после импорта. Возможно, вы получите уведомление об обнаруженных проблемах несоответствия. Необходимо устранить эти проблемы перед использованием импортированной версии конфигурации. Для получения дополнительных сведений см. список статей для этого раздела.

<a name="see-also"></a>См. также
--------

[Обзор электронной отчетности](general-electronic-reporting.md)


