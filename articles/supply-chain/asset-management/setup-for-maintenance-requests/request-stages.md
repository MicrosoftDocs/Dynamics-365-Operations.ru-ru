---
title: Состояния жизненного цикла запроса на обслуживание
description: В этой статье описывается, как настроить состояния жизненного цикла запроса на обслуживание в «Управлении активами».
author: johanhoffmann
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetRequestLifecycleState, EntAssetRequestLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 81b30820adf11f0239ea8ff9d1886b5738e38162
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862724"
---
# <a name="maintenance-request-lifecycle-states"></a>Состояния жизненного цикла запросов на обслуживание

[!include [banner](../../includes/banner.md)]

 


Состояния жизненного цикла запроса на обслуживание определяют этапы, через которые может пройти запрос. Примеры включают **Созданные**, **Активные** и **Завершенные**. При преобразовании запроса на обслуживание в заказ на работу, состояние жизненного цикла запроса на обслуживание должно быть обновлено на **Завершено** или **Закрыто**, чтобы указать, что запрос на обслуживание больше не активен. На странице списка **Все запросы на обслуживание** можно просматривать все запросы на обслуживание, независимо от их состояния жизненного цикла.

## <a name="set-up-maintenance-request-lifecycle-states"></a>Настройка состояний жизненного цикла запроса на обслуживание

1. Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Состояния жизненного цикла**.
2. Выберите **Создать** для создания состояния жизненного цикла запроса на обслуживание.
3. В поле **Состояния жизненного цикла** введите идентификатор для состояния жизненного цикла.
4. В поле **Имя** введите имя.

    На экспресс-вкладке **Подробно** поле **Модели жизненного цикла** показывает количество моделей жизненного цикла запроса на обслуживание, которые используют это состояние жизненного цикла.

5. На экспресс-вкладке **Общее** установите параметр **Активный** на **Да**, если запрос на обслуживание должен быть активным, пока он в этом состоянии жизненного цикла.
6. Установите параметр **Установить фактическое окончание** на **Да**, если фактическая дата и время окончания должны автоматически вводиться в запрос на обслуживание, который находится в этом состоянии жизненного цикла.
7. Установите параметр **Создание заказа на работу** на **Да**, если заказ на работу может быть создан из запроса на обслуживание, который находится в этом состоянии жизненного цикла.
8. Установите параметр **Удалить** на **Да**, если запрос на обслуживание может быть удален, пока он находится в этом состоянии жизненного цикла.
9. На экспресс-вкладке **Обновление** параметры **Входящие** и **Исходящие** в разделе **Актив** являются актуальными при использовании ремонта в хранилище. Установите соответствующий параметр в значение **Да**, если состояние жизненного цикла активов для активов, выбранных в заявке на обслуживание, должно автоматически обновляться до **Входящие** или **Исходящие**, когда состояние жизненного цикла запроса на обслуживание для этого запроса на обслуживание устанавливается равным **Входящие** или **Исходящие**.

На следующем рисунке показан пример страницы **Состояния жизненного цикла запроса на обслуживание**.

![Страница состояния жизненного цикла запросов на обслуживание.](media/02-setup-for-requests.png)

> [!NOTE]
> Состояния жизненного цикла запроса на обслуживание, группы состояния жизненного цикла и типы, связанные с ними, и используемые так же, как состояния жизненного цикла запроса на работу, группы состояния жизненного цикла и типы. 

## <a name="set-up-maintenance-request-lifecycle-models"></a>Настройка моделей жизненного цикла запроса на обслуживание

После создания состояний жизненного цикла, необходимых для запросов на обслуживание, они могут быть разделены на группы состояния жизненного цикла или модели жизненного цикла. Модели жизненного цикла запроса на обслуживание используются для создания потока, который может использоваться для различных типов запросов на обслуживание. Как минимум, должна быть создана одна стандартная модель жизненного цикла запроса на обслуживание.

1. Выберите **Управление активами** \> **Настройка** \> **Запросы на обслуживание** \> **Модели жизненного цикла**.
2. Выберите **Создать** для создания модели жизненного цикла запроса на обслуживание.
3. В поле **Модель жизненного цикла** введите идентификатор для модели жизненного цикла.
4. В поле **Имя** введите имя.

    На экспресс-вкладке **Подробно** **Состояния жизненного цикла** показывает количество состояний жизненного цикла запроса на обслуживание, которые выбраны в этой модели жизненного цикла. Поле **Типы запросов на обслуживание** показывает количество типов запросов на обслуживание, которые используют эту модель жизненного цикла.

5. На экспресс-вкладке **Состояния жизненного цикла** выберите состояния жизненного цикла, которые должны быть включены в модель жизненного цикла:

    - Чтобы включить состояние жизненного цикла в модель жизненного цикла, выберите его в разделе **Осталось состояний жизненного цикла**, а затем выберите кнопку со стрелкой вправо ![Стрелка вправо.](media/03-setup-for-requests.png) чтобы переместить его в выбранный раздел **Выбранные состояния жизненного цикла**.
    - Чтобы включить все доступные состояния жизненного цикла в модель жизненного цикла, выберите кнопку **Выбрать все доступные состояния** ![Выбрать все доступные состояния.](media/04-setup-for-requests.png). Все состояния жизненного цикла перемещаются в раздел **Выбранные состояния жизненного цикла**.
    - Чтобы удалить состояние жизненного цикла из модели жизненного цикла, выберите его в разделе **Выбранные состояния жизненного цикла**, а затем выберите кнопку со стрелкой влево ![Стрелка влево.](media/05-setup-for-requests.png) чтобы переместить его в выбранный раздел **Остальные состояния жизненного цикла**.

6. На экспресс-вкладке **Общее** поля в разделе **Обновить** актуальны, если вы используете ремонт в хранилище.

    - В поле **Состояния жизненного цикла для полученного актива** выберите состояние жизненного цикла актива, на которое активы, выбранные по запросу на обслуживание, должны быть автоматически обновлены до момента, когда они будут получены для ремонта в хранилище.
    - В поле **Состояния жизненного цикла для доставленного актива** выберите состояние жизненного цикла актива, на которое активы, выбранные по запросу на обслуживание, должны быть автоматически обновлены до момента, когда они будут возвращены после ремонта в хранилище.

На следующем рисунке показан пример страницы **Модели жизненного цикла запроса на обслуживание**.

![Страница моделей жизненного цикла запроса на обслуживание.](media/06-setup-for-requests.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]