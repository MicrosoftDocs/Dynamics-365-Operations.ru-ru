---
title: Обзор профиля учета
description: В этой статье приводятся сведения о профиле учета, который предназначен для реализации и учета передвижений и запасов в наличии в связи с деятельностью.
author: AdamTrukawka
ms.date: 05/11/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Russia
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b33f487dba8ff6fd00a86818ab70240f5cae0523
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274483"
---
# <a name="inventory-profile-overview"></a>Обзор профиля учета
[!include [banner](../includes/banner.md)]


Профиль учета предназначен для реализации и учета передвижений и запасов в наличии в зависимости от вида деятельности. Вид деятельности определяет способ получения номенклатуры организацией и ограничения, накладываемые на обработку номенклатуры. Ниже приведено несколько примеров видов деятельности:

- Покупка номенклатуры в соглашении для дальнейшей продажи или обработки
- Приемка номенклатур в рамках комиссионного соглашения
- Приемка сырья для обработки

Во всех этих случаях передвижения и запасы в наличии для одной и той же номенклатуры, получаемой организацией в результате различных видов деятельности, должны различаться в следующих аспектах:

- **Управление запасами** — количественный запас в наличии номенклатуры для различных видов деятельности не должен быть смешанным.
- **Учет** — передвижения и запасы в наличии для номенклатуры для различных видов деятельности должны быть отражены в разных счетах ГК.

Функции профилей учета позволяют выполнять следующие задачи:

- Настройте складские аналитики в соответствии с видами деятельности организации. Дополнительные сведения см. в разделе [Виды деятельности](#kinds-of-activity).
- Использование профиля учета в качестве складской аналитики. Дополнительные сведения см. в разделе [Профиль учета в виде складской аналитики](#inventory-profile-as-an-inventory-dimension).
- Настройка совместимых профилей учета. Дополнительные сведения см. в разделе [совместимые профили учета](#compatible-inventory-profiles).
- Настройка и использование счетов ГК разноски запасов в контексте профилей учета. Дополнительные сведения см. в разделе [комбинации складских проводок для профилей учета](#inventory-transaction-combinations-for-inventory-profiles).
- Указать профиль учета при настройке разноски запасов. Дополнительные сведения см. в разделе [настройка разноски запасов](#inventory-posting-setup).
- Настройка профиля учета по умолчанию и вида деятельности по умолчанию для заказов на покупку, заказов на продажу и заказов на перемещение. Дополнительные сведения см. в разделе [Настройка вида деятельности и профиля учета для заказов на покупку, заказов на продажу и заказов на перемещение](#set-up-a-kind-of-activity-and-an-inventory-profile-in-purchase-sales-and-transfer-orders).
- Разбиение строк заказа на продажу по профилю учета. Дополнительные сведения см. в разделе [разбиение строк заказа на продажу по профилю учета](#split-sales-order-lines-by-inventory-profile).
- Указывается профиль учета для строк спецификации. Дополнительные сведения см. в разделе [профиль учета в спецификациях](#inventory-profile-in-boms).
- Указывается профиль учета в прогнозе движения денежных средств в заказах на покупку и на продажу. Для получения дополнительных сведений см. в разделе [прогнозы движения денежных средств в заказах на покупку и продажу](#cash-flow-forecasts-on-purchase-and-sales-orders).
- Указывается профиль учета в прогнозах движения денежных средств, которые основаны на запланированных покупках и продажах. Для получения дополнительных сведений см. в разделе [прогнозы движения денежных средств, которые основаны на запланированных покупках и продажах](#cash-flow-forecasts-based-on-planned-purchases-and-sales).

## <a name="kinds-of-activity"></a>Виды деятельности

Имеется четыре вида деятельности:

- **Основной** — этот вид деятельности предназначен для учета номенклатур, которые не подсчитываются для других видов деятельности (например, номенклатуры, приобретаемые в рамках соглашения для перепродажи, сырья и сырья для производства).
- **Комиссионеры** — этот вид деятельности предназначен для учета товаров, которые организация получает от доверителя для дальнейшей реализации конечному покупателю от имени комиссионера.
- **Поверенные** — этот вид деятельности предназначен для учета товаров, которые организация получает от доверителя для дальнейшей реализации конечному покупателю от имени доверителя.
- **Хранитель** — этот вид деятельности предназначен для учета товаров, которые хранитель получает в процессе ответственного хранения.

## <a name="inventory-profile-as-an-inventory-dimension"></a>Профиль учета в качестве складской аналитики

Профиль учета используется для отдельного учета перемещений номенклатур и сальдо в контексте видов деятельности. Можно определить набор возможных значений для профиля учета. Для каждого профиля учета указывается вид деятельности, к которой относится данный профиль. Вид деятельности в профиле учета изменить нельзя.

Когда профиль учета активен в группе складских аналитик, на странице **Группы аналитик отслеживания** установлены следующие флажки: **первичное складирование**, **Физические запасы**, **Финансовые запасы** и **Перемещение**. Кроме того, если для продукта активен профиль учета, он должен быть указан в строках документа и не может отличаться в соответствующих складских проводках.

Дополнительные сведения см. в разделе [настройка профиля учета](rus-set-up-inventory-profile.md).

## <a name="compatible-inventory-profiles"></a>Совместимые профили учета

Параметр совместимости профилей учета используется для следующих целей:

- Автоматический выбор профилей учета из запасов в наличии при создании строк заказа на продажу путем выбора пункта **создать строки**.
- Контроль допустимости профилей учета в строках заказа на продажу, если в заголовке заказа указан конкретный профиль учета.

Дополнительные сведения см. в [Настройка совместимых профилей учета](rus-set-up-inventory-profile.md#set-up-compatible-inventory-profiles).

## <a name="inventory-transaction-combinations-for-inventory-profiles"></a>Комбинации проводок по запасам для профилей учета

Для настройки и использования счетов ГК разноски запасов в контексте профилей учета необходимо активировать комбинации складских проводок для профилей учета.

Дополнительные сведения см. в разделе [Активация сочетаний проводок для профилей учета](rus-set-up-inventory-profile.md#activate-transaction-combinations-for-inventory-profiles).

## <a name="inventory-posting-setup"></a>Настройка разноски запасов

Можно указать профиль учета при настройке разноски запасов. Счет ГК, на который разносится перемещение номенклатуры, определяется значением профиля учета, который указан для перемещения.

Разноска запасов может быть настроена для следующих значений профиля учета:

- Конкретное значение профиля учета
- Группа значений профиля учета, имеющих одинаковый вид деятельности
- Все значения профиля учета (по умолчанию значение разноски запасов также используется для продуктов, которые не учитываются в контексте профиля учета.)

Возможность установки разноски для конкретного вида деятельности и профиля учета управляется настройками для активации комбинаций складских проводок.

Дополнительные сведения см. в [Настройка профиля учета в контексте профиля учета](rus-set-up-inventory-profile.md#set-up-inventory-posting-in-the-context-of-an-inventory-profile).

## <a name="set-up-a-kind-of-activity-and-an-inventory-profile-in-purchase-sales-and-transfer-orders"></a>Настройка вида деятельности и профиля учета для заказов на покупку, заказов на продажу и заказов на перемещение

Вид деятельности и складская аналитика может быть указан в заголовке заказа на покупку, заказа на продажу и заказа на перемещение. Если вид деятельности указан в заказе, в заголовке заказа, в строках заказа и в складских проводках по данному заказу могут быть указаны только значения профиля учета, соответствующие данному видам деятельности. Если профиль учета указан в заголовке заказа на продажу и в строках заказа на продажу, в строках заказа и в складских проводках могут быть указаны только этот профиль и совместимые профили учета. Дополнительные сведения см. в разделе [Настройка профиля учета по умолчанию для заказов на покупку](rus-set-up-inventory-profile.md#set-up-a-default-inventory-profile-for-purchase-orders).

Можно указать вид деятельности и профиль учета в основной записи поставщика, клиента или соглашения. Если указан вид деятельности и профиль учета, они считаются значениями аналитики по умолчанию для заголовков заказов на покупку и заказов на продажу. Если вид деятельности уже указан для основной записи поставщика, клиента или соглашения, можно указать только значение профиля учета, соответствующее виду деятельности, указанному в этой основной записи. Дополнительные сведения см. в [Настройка вида деятельности и профиля учета по умолчанию для поставщиков, клиентов, договоров и складов](rus-set-up-inventory-profile.md#set-up-a-default-kind-of-activity-and-inventory-profile-for-vendors-customers-agreements-and-warehouses).

В документах других типов, таких как журналы запасов и производственные заказы, профиль учета, аналогичный другим складским аналитикам, указан в строках документа. Дополнительные сведения см. в разделе [Настройка профиля учета по умолчанию для спецификаций](rus-set-up-inventory-profile.md#set-up-a-default-inventory-profile-for-boms).

Невозможно изменить значение профиля учета во время комплектации или регистрации запасов. Значение профиля учета, указанное в строке документа, остается тем же, что и в складских проводках до тех пор, пока выполняется финансовая разноска.

## <a name="split-sales-order-lines-by-inventory-profile"></a>Разбиение строк заказа на продажу по профилю учета

При создании строк заказа на продажу, если указано количество, но не указан профиль учета, система может автоматически скомплектовать физически доступные запасы в наличии в контексте профилей учета.

Некоторые значения профиля учета могут также указывать на то, что они не могут использоваться для автоматического разбиения строк. Для разноски исходящего складской проводки с данным типом профиля учета необходимо указать значение профиля учета в строке заказа на продажу или в строке журнала запасов.

Если вид деятельности указан в заказе на продажу, строка заказа на продажу может быть разделена только значениями профиля учета, которые связаны с этим видом деятельности.

Дополнительные сведения см. в разделе [Создание строк заказа на продажу](rus-use-inventory-profile-documents-queries.md#create-sales-order-lines).

## <a name="split-documents-by-inventory-profile"></a>Разбиение документов по профилю учета

Разнесенные отборочные накладные, поступления продуктов, накладные и счета-фактуры по накладным для заказов на покупку и заказов на продажу делятся на отдельные документы на основе видов деятельности, которые соответствуют профилям учета в строках заказа, а также для соответствующих профилей разноски по клиентам и поставщикам.

Значение вида деятельности хранится в накладных и счетах-фактурах по накладным.

Разнесенные документы делятся на основе количества уникальных комбинаций вида деятельности и профиля разноски по клиентам и поставщикам. Номенклатуры, не учитываемые в контексте профилей учета, включаются в накладные, а **основной** вид деятельности и профиль разноски по клиентам и поставщикам определяются в заголовке заказа. Разбиение по видам деятельности и профилям разноски по клиенту и поставщику осуществляется независимо от настроек сводного обновления.

Дополнительные сведения см. в разделе [Настройка профиля учета по умолчанию для заказов на покупку](rus-set-up-inventory-profile.md#set-up-a-default-inventory-profile-for-purchase-orders), [Настройка профиля учета по умолчанию для заказов на продажу](rus-set-up-inventory-profile.md#set-up-a-default-inventory-profile-for-sales-orders), [заказы на покупку](rus-use-inventory-profile-documents-queries.md#purchase-orders) и [заказы на продажу](rus-use-inventory-profile-documents-queries.md#sales-orders).

## <a name="inventory-profile-in-boms"></a>Профиль учета в спецификациях

Можно указать профиль учета в строке спецификации. Профиль учета будет дополнительно указан в следующих местах:

- В строке журнала спецификации при принятии спецификации
- В строке заказа на продажу или заказа на покупку при развертывании спецификации
- В строке спецификации производственного заказа при создании производственного заказа

Поле **Профиль учета** в строках журнала спецификации заполнится из одного из двух мест:

- Строки спецификации
-  Поле **Профиль учета** на вкладке **спецификации** на странице **Параметры модуля "Управление запасами и складами"** (если профиль учета активен для номенклатуры и не указан в строке спецификации)

Поле **Профиль учета** в строках заказа спецификации заполнится из одного из двух мест:

- Строки спецификации
- Поле **Профиль учета** на странице **Параметры управления запасами и складами**

Дополнительные сведения см. в разделе [Настройка профиля учета по умолчанию для спецификаций](rus-set-up-inventory-profile.md#set-up-a-default-inventory-profile-for-boms).

## <a name="cash-flow-forecasts-on-purchase-and-sales-orders"></a>Прогнозы движения денежных средств в заказах на покупку и продажу

При создании прогноза движения денежных средств для заказов на покупку или заказов на продажу, профили учета, указанные в строках заказа, учитываются при определении счетов разноски складских перемещений, а также проводок по клиенту и поставщику. Счета ГК для проводок по клиенту и поставщику определяются из профилей разноски, которые соответствуют профилям учета, указанным в строках заказа. Для строк заказа, где не указан профиль учета, используется **основной** вид деятельности и профиль разноски, указанный в заголовке заказа.

Для получения дополнительных сведений см. раздел [Прогнозы движения денежных средств в заказах на покупку и продажу](rus-use-inventory-profile-documents-queries.md#cash-flow-forecasts-on-purchase-and-sales-orders) далее в этой статье.

## <a name="cash-flow-forecasts-based-on-planned-purchases-and-sales"></a>Прогнозы движения денежных средств на основе запланированных покупок и продаж

При создании прогноза движения денежных средств для запланированных продаж и покупок учитываются профили учета, указанные в строках прогноза поставок и в спланированных заказах.

Более подробную информацию см. в следующих разделах:

- [Настройка профиля учета](rus-set-up-inventory-profile.md)
- [Использование профиля учета в документах и запросах](rus-use-inventory-profile-documents-queries.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
