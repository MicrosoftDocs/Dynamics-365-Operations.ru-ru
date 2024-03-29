---
title: Назначение и переопределения налога
description: В этой процедуре показано, как назначить налоговые группы коммерческим каналам.
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTaxOverrideCode, RetailTaxOverrideGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbc987ba7f0026f011a04a27d00bd3833453514b
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675075"
---
# <a name="sales-tax-assignment-and-overrides"></a>Назначение и переопределения налога

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как назначить налоговые группы коммерческим каналам. В ней также представлен процесс создания нового переопределения налога и его назначения существующей группе переопределений налога. В этой процедуре используется компания с демонстрационными данными USRT.

1. Перейдите в раздел Retail и Commerce > Каналы > Магазины > Все магазины.
2. В списке перейдите по ссылке "Код канала" для канала "Хьюстон".
3. Выберите Изменить.
    * В поле "Налоговая группа" содержится список налоговых групп для текущей компании. Группа, назначенная в настоящее время, является универсальной налоговой группой "Техас". Также имеются налоговые группы для "Вашингтон" и "Вашингтон, округ Кинг". Налоговые группы могут включать применимые налоги для нескольких муниципалитетов.  
    * В поле "Переопределение налога" можно сопоставить группы переопределений налога с каналом. Группы переопределений налога можно использовать для группировки переопределений налога, которые работают для нескольких магазинов. Вместо того, чтобы вручную назначать переопределения налога по одному, можно создать группу и назначить ее непосредственно каналам для экономии времени.  
4. Нажмите кнопку Сохранить.
5. Закройте страницу.
6. Перейдите в раздел "Retail и Commerce" > "Настройка канала" > "Налоги" > "Переопределение налогов".
7. Щелкните "Создать".
8. В поле "Переопределение налога" введите имя нового переопределения.
9. В поле "Описание" введите описание переопределения.
10. Установите статус "Включено".
11. Разверните или сверните раздел "Переопределение".
12. В поле "Тип" выберите один из вариантов.
    * Налоговые группы номенклатур можно использовать для переопределения налогов для конкретных номенклатур, которые принадлежат группе. Например, продукты питания обычно облагаются налогом не так, как товары длительного пользования, и, вероятно, будут иметь собственную налоговую группу. Налоговые группы — это группы налогов, которые применяются к определенному каналу. Например, если канал продает в розницу и розничный канал и по схеме "предприятие-предприятие", могут использоваться различные налоговые группы номенклатур. Все применимые налоги будут сопоставлены с налоговой группой.  
    * Теперь можно выбрать налоги "Из" и "В" или "Начальная налоговая группа" и "Конечная налоговая группа" для создания переопределения налога. В поле "Из" указывается налог или налоговая группа, которая должна быть переопределена. При переопределении по налоговой группе номенклатур доступны другие параметры, чем при переопределении по налоговой группе. Переопределения налога можно настроить для переопределения налогов во всех проводках или в определенных строках проводки.  
13. Нажмите кнопку Сохранить.
14. Закройте страницу.
15. Перейдите в раздел "Retail и Commerce" > "Настройка канала" > "Налоги" > "Группы переопределений налога".
    * На этом шаге вы назначите созданное переопределение налога группе переопределений налога, назначенной каналу "Хьюстон".  
16. Щелкните "Изменить".
17. Разверните или сверните раздел "Настройка".
18. Нажмите кнопку Добавить.
19. В поле "Переопределение налога" нажмите кнопку раскрывающегося списка, чтобы открыть поиск.
20. Выберите ранее созданное переопределение налога из списка.
21. В списке перейдите по ссылке в выбранной строке.
22. Нажмите кнопку "Сохранить".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]