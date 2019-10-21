---
title: Руководство по устранению неполадок при интеграции данных
description: Эта тема предоставляет информацию по устранению неполадок для интеграции данных между приложениями Finance and Operations и Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: c16268338085d414468f17362294fb7e933d1b57
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249117"
---
# <a name="troubleshooting-guide-for-data-integration"></a>Руководство по устранению неполадок при интеграции данных

## <a name="enable-plug-in-trace-logs-in-common-data-service-and-inspect-the-dual-write-plug-in-error-details"></a>Включение журналов трассировки подключаемых модулей в Common Data Service и проверка сведений об ошибках подключаемого модуля двойной записи

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Если возникла проблема или ошибка во время синхронизации с двойной записью, выполните следующие действия для проверки ошибок в журнале трассировки.

1. Прежде чем можно будет исследовать ошибки, необходимо включить журналы трассировки подключаемых модулей. Инструкции см. в разделе "Просмотр журналов трассировки" в разделе [Учебник: создание и регистрация подключаемого модуля](https://docs.microsoft.com/powerapps/developer/common-data-service/tutorial-write-plug-in#view-trace-logs).

    Теперь вы можете проверить ошибки.

2. Войдите в Microsoft Dynamics 365 Sales.
3. Выберите кнопку **Настройки** (символ шестеренки), затем выберите **Дополнительные параметры**.
4. В меню **Настройки** выберите **Настройка \> Журнал трассировки подключаемых модулей**.
5. Выберите имя типа **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**, чтобы отобразить детали ошибки.

## <a name="inspect-dual-write-synchronization-errors"></a>Проверка ошибок синхронизации двойной записи

Чтобы исследовать ошибки во время тестирования, выполните следующие действия.

1. Выполните вход в Microsoft Dynamics Lifecycle Services (LCS).
2. Откройте проект LCS, для которого требуется выполнить тестирование двойной записи.
3. Выберите **Размещенные в облаке среды**.
4. Создайте подключение удаленного рабочего стола к виртуальной машине (ВМ) приложения, используя локальную учетную запись, отображаемую в LCS.
5. Откройте средство просмотра событий. 
6. Выберите **Журналы приложений и служб \> Microsoft \> Dynamics \> AX-DualWriteSync \> Операционные**. Отображаются ошибки и детали.

## <a name="unlink-one-common-data-service-environment-from-the-application-and-link-another-environment"></a>Отмена привязки одной среды Common Data Service к приложению и привязка другой среды

Выполните эти шаги, чтобы обновить ссылки.

1. Перейдите в среду приложения.
2. Откройте управление данными.
3. Выберите **Ссылка на CDS для приложений**.
4. Выберите все выполняющиеся сопоставления, затем выберите **Остановить**.
5. Выберите все сопоставления, затем выберите **Удалить**.

    > [!NOTE]
    > Вариант **Удалить** недоступен, если выбран шаблон **CustomerV3-Account**. При необходимости отмените выбор этого шаблона. **CustomerV3-Account** — это старый подготовленный шаблон, который работает с решением "Перспективный клиент в наличные деньги". Поскольку он выпущен глобально, он отображается под всеми шаблонами.

6. Выберите **Удалить связь со средой**.
7. Выберите **Да**, чтобы подтвердить операцию.
8. Чтобы связать новую среду, выполните шаги из [руководства по установке](https://aka.ms/dualwrite-docs).
