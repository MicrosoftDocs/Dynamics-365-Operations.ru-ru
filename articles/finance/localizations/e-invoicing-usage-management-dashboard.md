---
title: Панель мониторинга управления использованием
description: В этой теме объясняется, как использовать панель мониторинга управления использованием для отслеживания использования службы электронных накладных и поддержания соответствия требованиям.
author: gionoder
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 411c2d33c81738dcacfb7c8feec991d0fd06fb78
ms.sourcegitcommit: 9069a8511dfe11d09a2b51d32547ba10fea48bed
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/02/2021
ms.locfileid: "6130514"
---
# <a name="usage-management-dashboard"></a>Панель мониторинга управления использованием

[!include [banner](../includes/banner.md)]

Панель мониторинга **Управление использованием** помогает отслеживать использование службы электронных накладных и, таким образом, помогает организации соответствовать требованиям ежемесячного использования. Соответствие определяется путем расчета отправляемого объема и его сравнения с полученным объемом отправленных данных для выявления отклонений между приобретенным объемом и использованным объемом.

Панель мониторинга содержит следующие индикаторы:

- Один индикатор затрат, который можно использовать для отслеживания потребления для целей соответствия лицензированию:

    - Использование в месяц (экспорт)

- Три рабочих индикатора, которые можно использовать для отслеживания использования службы электронных накладных для целей управления:

    - Использование по функции
    - Использование по среде
    - Использование в месяц (импорт)

## <a name="measurement-scope"></a>Область измерения

- Единица измерения: 

    Панель мониторинга **Управление использованием** подсчитывает отправку бизнес-документов и импортированных электронных накладных.

- Организация: 

    Подсчет суммируется по коду клиента вашей организации, независимо от числа экземпляров Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management или числа юридических лиц, в которых активирована служба электронных накладных.


## <a name="indicator-usage-per-month-export"></a>Индикатор: использование в месяц (экспорт)

Этот индикатор предоставляет подробные сведения об электронных накладных, которые ваша организация выставила в течение определенного периода.

### <a name="scope"></a>Результат
- Число деловых документов, отправленных из Finance и Supply Chain Management в службу электронного выставления накладных, независимо от количества строк, содержащихся в этих деловых документах.
- Число отправленных бизнес-документов, успешно обработанных службой электронных накладных. Документ считается успешно обработанным, когда завершен поток действий, определенных в настройке функций.

> [!NOTE]
> При отправке электронной накладной на внешнюю веб-службу подсчет не зависит от результатов обработки веб-службой (принята, отклонена или ошибка проверки схемы). Если веб-служба получила и ответила на запрос из службы электронных накладных, отправка считается допустимой для подсчета.

- **Исключение:** деловые документы не подсчитываются, если они повторно передаются из Finance и Supply Chain Management в электронную службу выставления накладных, например в сценариях, в которых для изменения статуса электронной накладной требуется повторная отправка одного и того же делового документа. Например, выдача электронной накладной для Бразилии (налоговый документ) учитывается как действительная, но запрос отмены для нее не учитывается.


### <a name="calculation"></a>Расчет

Сальдо рассчитывается следующим образом:

Сальдо = Бесплатно + Куплено - Использовано

Где:

- Бесплатно:
  
    Бесплатный объем деловых документов, которые клиент может отправлять в месяц. Он включает в себя пакет из 100 деловых документов, которые могут быть отправлены в службу электронного выставления накладных. Бесплатный объем не является накопительным, и оставшееся сальдо не переносится на следующий период.
  
- Куплено:
  
    Пакет из 1000 деловых документов, которые могут быть отправлены в службу электронного выставления накладных. Этот пакет необходимо ежемесячно приобрести в вашей организации. Приобретенный объем не является накопительным, и оставшееся сальдо не переносится на следующий период.
  
- Использовано: 

    Число отправок деловых документов в службу электронного выставления накладных в соответствии с определенными критериями.
   
> [!IMPORTANT]
> Если ваша организация планирует превысить месячный объем 100 бесплатных отправок, приобретите пиковый объем, чтобы обеспечить, что вы сохранили соответствие политике лицензирования Майкрософт для службы электронных накладных.
>
> В настоящее время приобретенный объем должен вводиться вручную, в соответствии с датой приобретения, в качестве нескольких пакетов по 1000 отправок.

## <a name="indicator-usage-by-feature"></a>Индикатор: использование по функциям

Этот индикатор показывает использование функций электронного выставления накладных для выдачи электронных накладных за определенный период.

- Расчет:
  
    Использовано = сколько раз каждая функция электронного выставления накладных была использована при отправке деловых документов в службу электронных накладных.

## <a name="indicator-usage-by-environment"></a>Индикатор: использование по средам

Этот индикатор показывает использование сред электронного выставления накладных в течение определенного периода.

- Расчет:
    
    Использовано = сколько раз каждая среда службы электронного выставления накладных была использована при отправке деловых документов в службу электронных накладных.

## <a name="indicator-usage-per-month-import"></a>Индикатор: использование в месяц (импорт)

Этот индикатор показывает объем импорта электронных накладных с помощью службы электронного выставления накладных в Finance и Supply Chain Management в течение определенного периода времени.

- Область:

    Электронные накладные, которые импортированы в Finance и Supply Chain Management, независимо от количества строк, содержащихся в электронных накладных.

- Расчет:

    Получено = число импортированных электронных накладных в Finance и Supply Chain Management.

## <a name="functions"></a>Функции
### <a name="purchase"></a>Покупка

На вкладке **Использование в месяц (экспорт)** выберите **Покупка**, чтобы вручную зарегистрировать сумму приобретенных отправок.

Для заданной даты выберите **Создать** и введите число **Пакетов**, приобретенных на эту дату.

**Количество** рассчитывается следующим образом:

Количество = Пакеты * 1000

Рассчитанное **Количество** отражается в поле **Приобретено** из индикатора **Использование в месяц (экспорт)**.

### <a name="update"></a>Обновить 

В области действий выберите **Обновить**, чтобы обновить вычисление и обновить данные, отображаемые на странице и в диаграмме.

### <a name="reset-history-data"></a>Сбросить исторические данные

В области действий выберите **Сбросить исторические данные**, чтобы обновить базу данных, из которой будут рассчитываться индикаторы.




> [!NOTE]
> На панели мониторинга **Управление использованием** не отображаются денежные суммы. Вместо этого отображается только объем подсчитанных отправок и импортированных документов.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
