--- 
title: "Создание документа перемещения для внутреннего перемещения запасов"
description: "Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0fe3d735d6309bf87047a27f9e68c579ca052012
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="generate-a-transfer-document-for-an-internal-inventory-transfer"></a>Создание документа перемещения для внутреннего перемещения запасов

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура демонстрирует порядок создания документов перемещения для перемещения товаров внутри компании. Эта процедура доступна только для юридических лиц с основным адресом в Литве. Процедура была создана с использованием компании с демонстрационными данными DEMF с основным адресом в Литве. Перед выполнением данной процедуры необходимо завершить процедуру "Настройка документов переноса для перемещения товаров в компании". Эта процедура предназначена для бухгалтеров по складскому учету. Эта процедура предназначена для функции, которая была добавлена в версии 1611 Dynamics 365 for Operations.


## <a name="create-a-transfer-order"></a>Создание заказа на перемещение
1. Перейдите в раздел "Управление запасами" > "Входящие заказы" > "Заказ на перемещение".
2. Щелкните "Создать".
3. В поле "Со склада" введите или выберите значение.
4. В поле "На склад" введите или выберите значение.
5. Нажмите кнопку Добавить.
6. В списке пометьте выбранную строку.
7. В поле "Код номенклатуры" введите или выберите значение.

## <a name="enter-transportation-details-for-the-transfer-order"></a>Ввод сведений о транспортировке для заказа на перемещение
1. Нажмите кнопку "Сохранить".
2. В области действий щелкните "Отгрузить".
3. Щелкните "Сведения о транспортировке".
4. Выберите "Да" в поле "Печать сведений о транспортировке".
5. В поле "Товары выдал" введите или выберите значение.
6. В поле "Упаковка" введите значение.
7. В поле "Уровень риска для груза" введите значение.
8. В поле "Перевозчик" введите или выберите значение.
9. В поле "Модель" введите или выберите значение.
10. В поле "Регистрационный номер" введите значение.
11. В поле "Регистрационный номер прицепа" введите значение.
12. В поле "Водитель" введите или выберите значение.
13. В поле "Имя водителя" введите значение.
14. Нажмите кнопку "Сохранить".
15. Закройте страницу.

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a>Просмотр отборочной накладной для неразнесенного заказа на перемещение
1. Щелкните "Отборочная накладная".
2. Нажмите кнопку "OК".
3. Закройте страницу.

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a>Просмотр отборочной накладной для разнесенного заказа на перемещение
1. В области действий щелкните "Заказ на перемещение".
2. В области действий щелкните "Отгрузить".
3. Щелкните "Отгрузить заказ на перемещение".
4. Перейдите на вкладку "Общие".
5. В поле "Обновить" выберите вариант.
6. Перейдите на вкладку "Обзор".
7. В поле "Отборочная накладная" введите значение.
8. Нажмите кнопку "OК".
9. В области действий щелкните "Отгрузить".
10. Щелкните "Отборочная накладная".
11. Нажмите кнопку "OК".

