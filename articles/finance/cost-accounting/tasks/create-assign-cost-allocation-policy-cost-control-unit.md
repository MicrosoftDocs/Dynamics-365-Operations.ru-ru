---
title: Создание и назначение политик распределения затрат единицам управления затратами
description: Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами.
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734257"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Создание и назначение политик распределения затрат единицам управления затратами

[!include [banner](../../includes/banner.md)]

Эта процедура используется для создания политики распределения затрат с соответствующими правилами и ее назначения единице управления затратами. В этой записи используется компания с демонстрационными данными USP2.


## <a name="create-a-policy"></a>Создание политики
1. Перейдите в раздел **Учет затрат > Политики > Политики распределения затрат**.
2. Нажмите кнопку **Создать**.
3. В поле **Имя политики** введите значение.
4. В поле **Иерархия аналитик объектов затрат** введите или выберите значение.
    * Выберите "Организация".  
5. В поле **Статистическая аналитика** введите или выберите значение.
6. Нажмите кнопку **Сохранить**.

## <a name="create-allocation-rules"></a>Создание правил распределения
1. Нажмите кнопку **Создать**.
2. В списке пометьте выбранную строку.
3. В поле **Узел иерархии аналитик объектов затрат** введите или выберите значение.
4. В поле **Поведение затрат** выберите вариант Итог.
5. В поле **База распределения** введите или выберите значение.
6. Нажмите кнопку **Создать**.
7. В списке пометьте выбранную строку.
8. В поле **Узел иерархии аналитик объектов затрат** введите или выберите значение.
9. В поле **Поведение затрат** выберите вариант Итог.
10. В поле **База распределения** введите или выберите значение.
11. Нажмите кнопку **Создать**.
12. В списке пометьте выбранную строку.
13. В поле **Узел иерархии аналитик объектов затрат** введите или выберите значение.
14. В поле **Поведение затрат** выберите вариант Итог.
15. В поле **База распределения** введите или выберите значение.
    * Продолжайте, пока не будут созданы все правила.  
16. Нажмите кнопку **Сохранить**.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Назначение политики единице управления затратами
1. Щелкните **Назначения политики для единицы управления затратами**.
2. Нажмите кнопку **Создать**.
3. В списке пометьте выбранную строку.
4. В поле **Действительно с даты учета** введите дату.
    * Правила вступают в силу по дате. Пользователь или система могут пометить правило как правило с истекшим сроком действия, если создана более новая версия.  
5. В поле **Единица управления затратами** введите или выберите значение.
6. Нажмите кнопку **Сохранить**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
