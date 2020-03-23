---
title: Обзор оптимизации планирования
description: Этот раздел содержит обзор возможностей оптимизации планирования.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9ccf00b6fcd1e3a6002086360b1a4c5c464ba054
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076163"
---
# <a name="planning-optimization-overview"></a>Обзор оптимизации планирования

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Надстройка оптимизации планирования для Microsoft Dynamics 365 Supply Chain Management включает вычисление сводного планирования вне Dynamics 365 Supply Chain Management и соответствующей базы данных SQL. Преимущества, связанные с функциональными возможностями оптимизации планирования, включают улучшенную производительность и минимальное воздействие на базу данных SQL во время выполнения сводного планирования. Быстрое планирование может выполняться даже во время работы в офисе, чтобы планировщики могли немедленно реагировать на изменения спроса или параметров.

Для использования оптимизации планирования необходимо установить надстройку оптимизации планирования из проекта в Microsoft Dynamics Lifecycle Services (LCS) и включить функцию оптимизации планирования в Supply Chain Management. Дополнительные сведения см. в разделе [Начало работы с оптимизацией планирования](get-started.md).

На следующем рисунке показано преимущество выполнения оптимизации планирования в течение часов работы в офисе.

![Преимущества выполнения оптимизации планирования в течение часов работы в офисе](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Улучшение производительности

Оптимизация планирования может использоваться в сценариях, в которых используются продолжительные сводные планы. Она разработана специально для очень быстрых вычислений очень больших объемов данных. Поскольку она создана как сверхмасштабируемая многоклиентская служба, несколько экземпляров могут одновременно работать вместе для вычисления плана. Кроме того, служба планирования снимает загрузку сводного планирования с вашей системы и работает с потоком данных, что минимизирует нагрузку на сервер.

Оптимизация планирования может помочь в достижении следующих целей:

- Повышение производительности планирования за счет сокращения времени выполнения.
- Снижение воздействия на другие процессы в ходе выполнения сводного планирования.
- Выполнение более частого планирования. (Вы не ограничены ежедневными выполнениями.)
- Уверенность, что будущее развитие бизнеса не перегрузит систему планирования.

## <a name="architecture-and-data-flow"></a>Архитектура и поток данных

При установке надстройки оптимизации планирования из LCS устанавливается безопасное подключение к службе оптимизации планирования. Служба находится в той же стране или регионе центра обработки данных, что и связанный экземпляр Supply Chain Management. После настройки оптимизации планирования при выполнении сводного планирования справочник и данные проводок отправляются из Supply Chain Management в службу оптимизации планирования.

При удалении надстройки оптимизации планирования все соответствующие данные в службе оптимизации планирования удаляются.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Поток данных высокого уровня для выполнения пересоздания

1. Клиент Supply Chain Management отправляет сигнал для запроса выполнения планирования из оптимизации планирования.
2. Оптимизация планирования запрашивает необходимые данные через интегрированный соединитель.
3. База данных SQL отправляет запрашиваемую информацию о настройке, справочнике и данных проводок в оптимизацию планирования через соединитель. Соединитель передает информацию между Supply Chain Management и службой оптимизации планирования.
4. Служба оптимизации планирования удерживает данные, имеющие отношение к планированию в памяти, и выполняет необходимые вычисления.
5. Результат планирования отсылается в базу данных Supply Chain Management через соединитель. Результаты включают в себя такие сведения, как спланированные заказы и сведения о фиксации. Оптимизация планирования отправляет сигнал в Supply Chain Management, указывая, что выполнение планирования завершено. Она также отправляет все необходимые сообщения и предупреждения.

На следующем рисунке показан поток данных.

![Поток данных для выполнения пересоздания](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Связанные ресурсы

[Начало работы с оптимизацией планирования](get-started.md)

[Анализ пригодности оптимизации планирования](planning-optimization-fit-analysis.md)

[Просмотр журнала плана и журналов планирования](plan-history-logs.md)

[Применение фильтров к плану](plan-filters.md)

[Отмена задания планирования](cancel-planning-job.md)