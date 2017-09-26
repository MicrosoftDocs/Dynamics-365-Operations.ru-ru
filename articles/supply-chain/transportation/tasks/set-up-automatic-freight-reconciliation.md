--- 
title: "Настройка автоматической выверки фрахта"
description: "Эта процедура показывает порядок настройки данных для автоматической выверки фрахта."
author: BibiSp
manager: AnnBe
ms.date: 10/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 61b795d52d4d2586db7f42a976790ee8608e179b
ms.contentlocale: ru-ru
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-automatic-freight-reconciliation"></a>Настройка автоматической выверки фрахта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Эта процедура показывает порядок настройки данных для автоматической выверки фрахта. Это обычно выполняется менеджером склада. Эту процедуру можно выполнить, используя компанию с демонстрационными данными USMF.


## <a name="set-up-the-freight-bill-type"></a>Настройка типа векселя фрахта
1. Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Тип векселя фрахта".
    * Тип счета за фрахт определяет, как счета за фрахт и накладные перевозчика должны совпадать.  
2. Щелкните "Создать".
3. В поле "Тип векселя фрахта" введите значение.
4. В поле "Сборка механизма" введите "Microsoft.Dynamics.Ax.Tms.Bll.GenericNormalizer".
    * Это стандартная библиотека кода модуля сопоставления для управления транспортировкой.  
5. В поле "Класс механизма" введите "Microsoft.Dynamics.Ax.Tms.dll".
    * Это стандартный класс модуля сопоставления для управления транспортировкой.  
6. Щелкните "Создать".
7. В поле "Описание" выберите значение, которое должно соответствовать в счете за фрахт и накладной перевозчика.  
8. В поле "Требуется сопоставление" выберите значение "Да".
    * Если в этом поле задано значение "Да", это означает, что значение, выбранное в поле "Описание", должно совпадать как в счете за фрахт, так и в накладной перевозчика. Если задано значение "Нет", это поле может быть пустым в одном из этих документов.  
9. Нажмите кнопку "Сохранить".

## <a name="set-up-the-freight-bill-type-assignment"></a>Настройка назначения типа векселя фрахта
1. Закройте страницу.
2. Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Назначения типов векселей фрахта".
    * Назначение типа счета за фрахт используется, чтобы определить, какой тип счета за фрахт используется для определенного перевозчика.   
3. Щелкните "Создать".
4. В поле "Режим" введите или выберите значение.
5. В поле "Перевозчик, осуществляющий доставку" введите или выберите значение.
6. В поле "Тип векселя фрахта" выберите тип счета за фрахт, созданный ранее.
7. Закройте страницу.

## <a name="set-up-the-audit-master"></a>Настройка мастера аудита
1. Перейдите в раздел "Управление транспортировкой" > "Настройка" > "Выверка фрахта" > "Шаблон аудита".
    * Мастер аудита определяет лимиты отклонения для автоматической выверки фрахта. Он определяет, насколько денежные суммы в счете за фрахт и накладной перевозчика могут отличаться и при этом все еще допускать выполнение выверки. Он также определяет способ обработки несоответствий.  
2. Щелкните "Создать".
3. В поле "Код шаблона аудита" введите значение.
4. В поле "Перевозчик, осуществляющий доставку" выберите того же перевозчика, что и ранее.
5. В поле "Тип векселя фрахта" выберите тип счета за фрахт, созданный ранее.
6. Разверните раздел "Допуск".
7. В поле "Минимальный уровень отклонения" введите число.
8. В поле "Максимальный уровень отклонения" введите число.
9. Разверните раздел "Результат".
10. В поле "Код основания переплаты" введите или выберите значение.
    * Если денежные суммы отличаются в счете за фрахт и в накладной перевозчика, то коды причин переплаты и недоплаты определяют счета, на которых должна быть зарегистрирована разница, если эта разница находится в допустимых пределах.  
11. В поле "Код основания недоплаты" введите или выберите значение.
12. Закройте страницу.

