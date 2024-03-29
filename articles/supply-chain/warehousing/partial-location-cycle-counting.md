---
title: Частичный подсчет циклов местонахождений
description: Планы подсчета циклов регулируют фактические операции подсчета. Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.
author: perlynne
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f06b39f3c2d2f5a0bdfef1da9395c71686ed46968a1143305b5a10787f7e85f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778442"
---
# <a name="partial-location-cycle-counting"></a>Частичный подсчет циклов местонахождений

[!include [banner](../includes/banner.md)]

Планы подсчета циклов регулируют фактические операции подсчета. Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении.

С помощью планов подсчета циклов для создания работы подсчета можно регулировать фактические операции подсчета. Можно запросить, чтобы только конкретные продукты и варианты продуктов подчитывались вместо всех запасов в наличии в местонахождении. С помощью фильтрации по конкретным продуктам менеджер склада может уменьшить накладные расходы для рассмотрения, избежать ошибок консолидации и сэкономить время.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Настройка частичного цикличного подсчета местонахождений

При использовании рабочего процесса склада для операций подсчета для каждого местонахождения создается заголовок работы. При определении плана подсчета циклов можно использовать запрос **Выберите местонахождения** для ограничения создаваемой работы подсчета циклов. При выборе продуктов для плана подсчета циклов можно выбрать запросы продукта и вариантов продукта для уточнения того, что подсчитывается.

Можно связать **шаблон работы** с план подсчета циклов, чтобы определить способ создания работы подсчета циклов. На шаблон работы для операций подсчета напрямую ссылается план подсчета циклов.

При определении сведений шаблона работы можно использовать параметр **Разрывы строки работы**, чтобы указать, следует ли группировать строки работы подсчета по номеру номенклатуры или номеру варианта продукта. Эта настройка необходима, если следует выполнить подсчет запасов в наличии только для определенных продуктов в местонахождении. Создаваемые строки работы подсчета циклов будут иметь уровень информации, определенный здесь, и операция подсчета обрабатывается на основе этого уровня.

Если связать планы подсчета циклов с шаблонами работ с помощью параметра **Разрывы строки работы** поле **Частичный подсчет циклов** выбирается для создаваемой работы подсчета циклов и несколько строк работы подсчета циклов создается на основе определения шаблона работы.

Перед обработкой работы частичного подсчета циклов необходимо как минимум выбрать **Отображение кода номенклатуры** для элемента меню мобильного устройства как части настройки подсчета циклов. Оператору склада будет предложено записать только сведения о подсчете, относящиеся к строкам подсчета (номера номенклатур и аналитики "продукт"). Все другие складские запасы в наличии будут игнорироваться для этого процесса подсчета.

Для процесса подсчета частичных циклов дата и время для поля **Последний цикличный подсчет** не обновляются для местонахождения, даже если подсчитываются все номенклатуры в наличии в данном местонахождении. Частичный цикличный подсчет не учитывает параметр **Дней между цикличными подсчетами** на странице **Планы подсчета циклов**. Частичный цикличный подсчет не поддерживает одновременный подсчет нескольких номенклатур в одном местонахождении. Функция частичного цикличного подсчета может приводить к многократным подсчетам в одном местонахождении для номенклатуры, когда выполняется команда **Обработать план подсчета циклов**. Чтобы избежать возникновения такой ситуации, необходимо указать фильтры в поле **Выбрать местоположения**.

> [!NOTE]
> Мобильное приложение управления складом не предоставляет кнопки **Добавить НЗ или номенклатуру** при использовании процесса частичного подсчета циклов.

## <a name="example"></a>Пример

В этом примере только номер номенклатуры A0001 следует подсчитывать на складе 61.

1. Создается новый шаблон работы для подсчета циклов. Параметр **Разрывы строки работы** используется для группировки строк работы подсчета по коду номенклатуры. Таким образом, создаваемая работа подсчета циклов будет содержать строки по коду номенклатуры. Можно также сгруппировать строки по номеру варианта продукта.
1. Создается новый план подсчета циклов, который ссылается на только что созданный шаблон работы. План подсчета циклов включает в себя все местонахождения на складе 61 (запрос **Выберите местонахождения** запрос), содержащие запасов для кода номенклатуры A0001. Выбор конкретных продуктов определяется в разделе **Выбор продуктов плана подсчета циклов**.
1. Можно выбрать продукты для планов подсчета циклов, установив в поле **Пустые местоположения** значение **Исключить пустые**. При обработке плана подсчета циклов создается работа частичного подсчета циклов для номера номенклатуры A0001. Фактический процесс подсчета можно выполнить с помощью пункта меню мобильного устройства для подсчета циклов.

## <a name="additional-resources"></a>Дополнительные ресурсы

[Цикличный подсчет](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]