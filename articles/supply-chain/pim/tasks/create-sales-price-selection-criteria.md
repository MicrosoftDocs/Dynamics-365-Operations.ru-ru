---
title: Создание критериев выбора цены продажи
description: Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60a7c7230d4eb57d840121f6ee490bf829e0dc8f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999664"
---
# <a name="create-sales-price-selection-criteria"></a>Создание критериев выбора цены продажи

[!include [banner](../../includes/banner.md)]

Эта процедура демонстрирует порядок создания критерия выбора цены продажи для моделей цены продажи, основанных на атрибутах. Для этой процедуры требуется наличие не менее одной модели цены продажи. В этом примере используется модель цены для модели цены продажи решения динамика в демонстрационных данных компании USMF. Обычно менеджер по продуктам использует эту процедуру.


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a>Добавьте новый критерий для существующей модели цены продажи
1. Щелкните "Определение модели вариантов продукта".
2. Щелкните "Модели конфигурации продукта".
3. В списке выберите строку для модели продукта решения динамика, но не нажимайте ссылку для имя модели.
4. В области действий щелкните "Модель".
5. Щелкните "Критерии модели цены".
6. Нажмите Создать.
7. В поле "Имя" введите "Группа клиентов 10".
    * Имя критерия модели цены используется, чтобы помочь определить лежащие в основе критерии выбора.  
8. В поле "Модель цены" введите или выберите значение.
9. В поле "Тип заказа" выберите "Заказ на продажу".
    * Тип заказа определяет поля базы данных, которые будут доступны для запроса выбора.  
10. Введите дату в поле "Действительно с".
11. В поле "Срок действия истекает" введите дату.
12. Нажмите кнопку "Сохранить".

## <a name="create-the-query-for-the-selection-criteria"></a>Создайте запрос для критериев выбора
1. Щелкните "Изменить".
2. В поле "Таблица" выберите "Клиенты". 
3. В поле "Поле" выберите "Группа клиентов".
    * В этом примере будет использоваться предоставленная группы клиентов для критериев выбора.  
4. В поле "Критерии" выберите "Группа клиентов 10". 
5. Нажмите кнопку "OК".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]