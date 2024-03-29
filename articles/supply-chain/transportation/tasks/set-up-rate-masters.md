---
title: Настройка шаблонов ставок
description: В этой процедуре показано, как настроить справочник ставок.
author: Weijiesa
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e707d226894c3cd647094556bfcc017347cb7f6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675525"
---
# <a name="set-up-rate-masters"></a>Настройка шаблонов ставок

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как настроить справочник ставок. Справочники ставок обычно настраивает менеджер по логистике, в зависимости от контрактов, подписанных с перевозчиками. В этом сценарии вам предстоит настроить справочник ставок для авиаперевозчика. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.

## <a name="set-up-break-master"></a>Настройка шаблона градации ставки

1. Перейдите в раздел **Управление транспортировкой > Настройка > Расчет ставок > Шаблон градации ставки**. Справочники градаций используются для определения ценовой структуры и точек останова в ней. Ценовая структура предполагает использование многоуровневого ценообразования, которое основывается на физических аналитиках.  
1. Выберите **Создать**.
1. В поле **Шаблон градации ставки** введите значение.
1. В поле **Имя** введите значение.
1. В поле **Тип данных** выберите тип данных.
1. В поле **Сравнение** введите требуемый тип сравнения (с помощью операторов).
1. В поле **Единица градации ставки** введите значения единицы градации ставки.
1. В разделе **Сведения** создайте столько градаций ставки, сколько необходимо для структуры ценообразования.
1. Нажмите **Сохранить**.

## <a name="set-up-rate-master"></a>Настройка справочника ставок

1. Перейдите в раздел **Управление транспортировкой > Настройка > Расчет ставок > Шаблон ставки**.
1. Выберите **Создать**.
1. В поле **Шаблон ставки** введите значение.
1. В поле **Имя** введите значение.
1. В поле **Код метаданных оценки** выберите кнопку раскрывающегося списка, чтобы открыть подстановку. Код метаданных ставок определяет, какие данные необходимы для справочника ставок, поскольку он определяет метаданные, которых ожидает механизм управления транспортировкой при использовании этого справочника ставок.  
1. В данном примере выберите вариант P2P. Это значение уже определено в демонстрационных данных.
1. В списке выберите ссылку в выбранной строке.
1. Нажмите **Сохранить**.

## <a name="set-up-rate-base"></a>Настройка базы ставки

1. Выберите **База ставки**.
    * База ставки определяет ставку перевозчика и может использоваться для настройки структуры тарифов, поскольку она определяет изменения ставки в точках останова, определенных в справочнике градаций.  
2. Выберите **Создать**.
3. В поле **База ставки** введите значение.
4. В поле **Имя** введите значение.
5. В поле **Шаблон градации ставки** выберите раскрывающийся список, чтобы открыть подстановку.
    * Справочники градаций используются для определения ценовой структуры и точек останова в ней. Ценовая структура предполагает использование многоуровневого ценообразования, которое основывается на физических аналитиках.  
6. В этом примере будет использоваться вес. Это значение уже определено в демонстрационных данных.
7. В списке выберите ссылку в выделенной строке.
8. Разверните раздел **Сведения**.
9. Выберите **Создать**.
10. В поле **Почтовый индекс выгрузки из** введите "30301".
11. В поле **Почтовый индекс выгрузки в** введите "30318".
12. В поле **Страна/регион выгрузки** введите "США".
13. В поле **<1,00 фунта** введите "100".
    * Вставьте ставку за фунт, если общий вес груза меньше 1 фунта.  
14. В поле **<5,00 фунтов** введите "300".
    * Вставьте ставку за фунт, если общий вес груза меньше 5 фунтов.  
15. В поле **<20,00 фунтов** введите "500".
    * Вставьте ставку за фунт, если общий вес груза меньше 20 фунтов.  
16. В поле **<100,00 фунтов** введите "1000".
    * Вставьте ставку за фунт, если общий вес груза меньше 100 фунтов.  
17. В поле **<1 000,00 фунтов** введите "3000".
    * Вставьте ставку за фунт, если общий вес груза меньше 1000 фунтов.  
18. Нажмите **Сохранить**.
19. Закройте страницу.

## <a name="assign-rate-base"></a>Назначение базы ставки

1. Разверните раздел **Назначения базы ставки**.
2. Выберите **Создать**.
    * Для каждого справочника ставок может быть несколько назначений базы ставки. Это дает возможность создать для каждого перевозчика несколько различных ценовых точек в зависимости от мест назначения, услуг или разных баз ставок. В этой процедуре вам предстоит создать только одно назначение базы ставки.  
3. В поле **Имя** введите значение.
4. В поле **База ставки** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.
5. В списке выберите ссылку в выделенной строке.
6. В поле **Служба** выберите кнопку раскрывающегося списка, чтобы открыть подстановку.
7. В списке найдите и выберите требуемую запись.
8. В списке выберите ссылку в выделенной строке.
9. В поле **Почтовый индекс вывоза** введите "98052".
    * Укажите, с какого почтового индекса должно быть действительно это назначение базы ставки.
10. В поле **Страна/регион вывоза** введите "США".
11. Нажмите **Сохранить**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]