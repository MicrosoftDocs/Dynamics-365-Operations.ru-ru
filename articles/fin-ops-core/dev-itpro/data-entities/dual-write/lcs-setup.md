---
title: Настройка двойной записи из Lifecycle Services
description: В этой теме объясняется, как настроить подключение с двойной записью между новой средой Finance and Operations и новой средой Common Data Service из Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
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
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173000"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Настройка двойной записи из Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

В этой теме объясняется, как настроить подключение с двойной записью между новой средой Finance and Operations и новой средой Common Data Service из Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Необходимые условия

Для настройки подключения с двойной записью необходимо иметь права администратора.

+ Вы должны иметь доступ к клиенту.
+ Вы должны быть администратором в обеих средах Finance and Operations и Common Data Service.

## <a name="set-up-a-dual-write-connection"></a>Настройка подключения двойной записи

Выполните эти шаги для настройки подключения двойной записи.

1. В LCS перейдите к своему проекту.
2. Выберите **Настройка** для развертывания новой среды.
3. Выберите версию. 
4. Выберите топологию. Если доступна только одна топология, она выбирается автоматически.
5. Выполните первые шаги в мастере **Параметры развертывания**.
6. На вкладке **Common Data Service** выполните одно из следующих действий:

    - Если среда Common Data Service уже подготовлена для клиента, его можно выбрать.

        1. Установите для параметра **Настроить Common Data Service** значение **Да**.
        2. В поле **Доступные среды** выберите среду, которую необходимо интегрировать с данными Finance and Operations. Список включает в себя все среды, для которых у вас имеются привилегии администратора.
        3. Установите флажок **Принимаю**, чтобы указать, что вы принимаете условия.

        ![Вкладка Common Data Service, когда среда Common Data Service уже подготовлена для клиента](../dual-write/media/lcs_setup_1.png)

    - Если у клиента еще нет среды Common Data Service, будет подготовлена новая среда.

        1. Установите для параметра **Настроить Common Data Service** значение **Да**.
        2. Введите имя для среды Common Data Service.
        3. Выберите регион, в котором требуется развернуть среду.
        4. Выберите язык и валюту по умолчанию для среды.

            > [!NOTE]
            > Изменить язык и валюту позже нельзя.

        5. Установите флажок **Принимаю**, чтобы указать, что вы принимаете условия.

        ![Вкладка Common Data Service, если у клиента еще нет среды Common Data Service](../dual-write/media/lcs_setup_2.png)

7. Выполните оставшиеся шаги в мастере **Параметры развертывания**.
8. После того как среда имеет статус **Развернуто**, откройте страницу сведений о среде. В разделе **Сведения о среде Common Data Service** показаны имена среды Finance and Operations и среды Common Data Service, которые связаны.

    ![Раздел сведений о среде Common Data Service](../dual-write/media/lcs_setup_3.png)

9. Администратор среды Finance and Operations должен войти в систему LCS и выбрать пункт **Связать с CDS для приложений**, чтобы завершить связь. На странице сведений о среде отображаются контактные данные администратора.

    После завершения установления связи статус обновляется до **Связывание среды успешно выполнено**.

10. Чтобы открыть рабочую область **Интеграция данных** в среде Finance and Operations и управлять доступными шаблонами, выберите **Связать с CDS для приложений**.

    ![Кнопка "Связать с CDS для приложений" в разделе сведения о среде Common Data Service](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Невозможно удалить связь среды с помощью LCS. Чтобы отменить связь среды, откройте рабочую область **Интеграция данных** в среде Finance and Operations, затем выберите **Удалить ссылку**.
