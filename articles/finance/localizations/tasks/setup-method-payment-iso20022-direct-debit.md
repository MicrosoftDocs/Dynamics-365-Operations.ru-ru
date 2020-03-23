---
title: Настройка способа оплаты для прямого дебетования ISO20022
description: Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7d3c6d8157803e0a8d33520a0cd64fb725e8c9a3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175011"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Настройка способа оплаты для прямого дебетования ISO20022

[!include [task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает, как настроить метод платежей клиентов для прямого дебетования ISO20022 или любого другого типа платежа с использованием электронной отчетности. 



Прежде чем можно будет выполнить эту задачу, необходимо настроить конфигурации формата экспорта и счета платежей.



Эта процедура была создана с использованием демонстрационных данных компании DEMF.



Это третья процедура из пяти, которые демонстрируют процесс платежа клиентов с помощью конфигурации электронной отчетности.

1. Перейдите в раздел "Расчеты с клиентами" > "Настройка платежей" > "Способы оплаты".
2. Используйте экспресс-фильтр для поиска записей. Например, отфильтруйте поле "Способ оплаты" по значению "ELECTRONIC".
3. Выберите Изменить.
4. В поле "Счет оплаты" укажите значения "DEMF OPER".
5. Разверните раздел "Форматы файлов".
6. В поле "Общая электронная отчетность" выберите значение "Да".
7. В поле "Экспорт конфигурации формата" введите или выберите значение.
    * В списке выберите "Прямое дебетование ISO20022 (DE)".  Если список пуст, конфигурация формата экспорта платежей клиента не импортирована и не активна.  
8. Выберите значение "Да" в поле "Требуется поручение".
    * Выберите параметр "Требуется поручение" для форматов платежей клиентов, который требуют включения информации о поручении в сообщение платежа, например прямое дебетование SEPA.  
9. Нажмите кнопку "Сохранить".
