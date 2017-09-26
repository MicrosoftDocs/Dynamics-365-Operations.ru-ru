--- 
title: "Создание, расчет и разноска журнала операций для розничного магазина"
description: "В этой процедуре описано, как вручную создать, рассчитать и разнести журнал операций для магазина."
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 60bcafffc922e6d57e52a5dff104a0fbb252f6ce
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>Создание, расчет и разноска журнала операций для розничного магазина

[!include[task guide banner](../includes/task-guide-banner.md)]

В этой процедуре описано, как вручную создать, рассчитать и разнести журнал операций для магазина. Кроме того, существуют пакетные задания, которые могут быть настроены для тех же задач. Инструкции по настройке и запуску пакетных задач можно найти в других разделах. Чтобы выполнить эту процедуру, необходимо иметь проводки, которые были выполнены в кассовом терминале, а затем переданы в Dynamics AX. В этой записи используется компания с демонстрационными данными USRT. Эта процедура может ссылаться на Microsoft Dynamics AX. Обратите внимание, что теперь Dynamics AX называется Microsoft Dynamics 365 for Operations.

1. Перейдите в раздел "Все рабочие области" > .. > "Финансовая информация розничного магазина".
2. Щелкните "Новый журнал операций".
3. В поле "Номер магазина" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
4. В списке перейдите по ссылке в выбранной строке.
5. Нажмите кнопку "OК".
    * Группа "Настройка" имеет параметры, определяющие, какие проводки включаются в журнал операций и как они группируются по строкам журнала. В можете открыть группу "Настройка" и изменить эти параметры или использовать параметры по умолчанию.  
    * Поле "Метод агрегирования операций" определяет, как будут группироваться строки журнала операций.  
    * Выберите сотрудника или кассовый терминал, если вы хотите создать журнал операций только для определенного сотрудника или терминала.  
6. В поле "Способ закрытия" выберите один из вариантов.
7. Щелкните "Создать строки журнала операций".
8. Щелкните Да.
    * После расчета журнала операций должны быть созданы строки с общими суммами для каждого способа оплаты и способа агрегирования операций, который был использован.  
    * Введите рассчитанную сумму в каждую строку, если ее нужно ввести или обновить. В поле с рассчитанными значениями будут подставлены суммы их деклараций платежных средств, выполненных в кассовом терминале.  
9. Щелкните "Разнести журнал операций".
10. Щелкните "Закрыть".
11. Перейдите в раздел "Розничная торговля и коммерция" > "Каналы" > "Финансовая информация розничного магазина".
12. Щелкните вкладку "Разнесенные журналы операций".

