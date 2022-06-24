---
title: Включение управления качеством и несоответствием
description: В этой статье представлен обзор процесса настройки и конфигурирования контроля качества и функций управления несоответствиями в Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome, InventParameters, InventProblemType, InventProblemTypeSetup, InventQuarantineZone, InventTestDiagnosticType, InventTestReportSetup, SysUserManagement, InventTestRelatedOperations
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66229e3692e87f774c553eae955794330602598c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874053"
---
# <a name="enable-quality-and-nonconformance-management"></a>Включение управления качеством и несоответствием

[!include [banner](../includes/banner.md)]

В этой статье представлен обзор процесса настройки и конфигурирования контроля качества и функций управления несоответствиями в Microsoft Dynamics 365 Supply Chain Management.

## <a name="enable-quality-and-nonconformance-management"></a><a name="enable-qm"></a>Включение управления качеством и несоответствием

Выполните следующие действия, чтобы включить управление качеством в системе.

1. Перейдите в раздел **Управление запасами \> Настройка \> Параметры управления запасами и складами**.
1. На вкладке **Управление качеством** установите для параметра **Использовать управление качеством** значение *Да*.
1. В поле **Почасовая ставка** введите почасовую ставку в местной валюте. Почасовая ставка используется для расчета затрат на операции, связанные с несоответствием. Почасовая ставка и вычисленная стоимость являются справочной информацией для несоответствия. Они не взаимодействуют с другими функциями.
1. Выберите **Настройка отчетов**.
1. Добавьте новые строки для различных типов отчетов и выберите тип документа, который будет использоваться для каждого отчета.
1. Закройте страницу.
1. Закройте страницу.

## <a name="quality-management-configuration-process"></a>Процесс настройки управления качеством

Прежде чем можно будет начать пользоваться функциями управления качеством и создавать заказы для контроля качества, необходимо настроить систему и необходимые компоненты. Ниже приводится список шагов, необходимых для настройки управления качеством.

1. [Включение управления качеством и несоответствием](#enable-qm).
1. Необязательно: [Настройка инструментов тестирования](quality-test-instruments.md).
1. [Настройка тестов](quality-tests.md).
1. [Настройка переменных тестирования и результаты](quality-test-variables.md).
1. [Настройка групп тестирования](quality-test-groups.md).
1. Необязательно: [Настройка групп контроля качества и связь с продуктами](quality-groups.md).
1. Необязательно: [Настройка связей контроля качества](quality-associations.md).

После завершения настройки можно начать создавать и обрабатывать заказы для контроля качества. Для получения дополнительной информации о том, как создавать и работать с заказами для контроля качества фрагменты, см. [Заказ на контроль качества](quality-orders.md).

## <a name="nonconformance-management-configuration-process"></a>Процесс настройки управления несоответствиями

Прежде чем можно будет начать пользоваться функциями управления несоответствиями и создавать несоответствия, необходимо настроить систему и необходимые компоненты. Ниже приводится список шагов, необходимых для настройки управления несоответствиями.

1. [Включение управления качеством и несоответствием](#enable-qm).
1. [Настройка работников, ответственных за утверждение несоответствий](quality-responsible-workers.md).
1. [Настройка типов проблем](quality-problem-types.md).
1. [Настройка зон карантина](quality-quarantine-zones.md).
1. [Настройка типов диагностики](quality-diagnostic-types.md).
1. [Настройка операций](quality-operations.md).
1. Необязательно: [Настройка расходов по контролю качества](quality-charges.md).

После завершения настройки можно начать создавать и обрабатывать несоответствия. Дополнительные сведения о способе создания и работы с несоответствиями см. в разделе [Создание и обработка несоответствий](tasks/create-process-non-conformance.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

- [Обзор управления качеством](quality-management-processes.md)
- [Включение управления качеством и несоответствием](enable-quality-management.md)
- [Управление качеством для складских процессов](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
