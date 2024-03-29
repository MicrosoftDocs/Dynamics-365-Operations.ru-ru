---
title: Настройка разноски ретробонусов
description: В этой статье описывается, как настроить профили разноски. Профили разноски используются для определения записей разноски для строк расчета управления ретробонусами.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 7a519b7153b307bf7d8cc9093572ca2711432970
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873589"
---
# <a name="rebate-management-posting-setup"></a>Настройка разноски управления ретробонусами

[!include [banner](../includes/banner.md)]

Профили разноски управления ретробонусами используются для определения записей разноски для строк расчета управления ретробонусами. Когда профиль разноски выбран в заголовке сделки, он применяется ко всем строкам сделки.

Эта функция используется в компаниях (юридических лицах). Можно указать компанию, которой будут начисляться обеспечения и которая будет оплачивать требования. Можно также настроить другие дебетовые счета обеспечения и кредитные счета списания для каждой исходной компании разноски.

Для настройки профилей разноски управления ретробонусами для клиентов и поставщиков перейдите в раздел **Управление ретробонусами \> Настройка разноски управления ретробонусами \> Профили разноски управления ретробонусами**. Страница **Профили разноски управления ретробонусами** включает в себя панель списка, в которой отображаются все существующие профили. Вы можете использовать кнопки на панели действий, чтобы добавить профили в сетку или удалить их.

В остальных разделах этой статьи описывается, как использовать доступные поля при создании или редактировании профиля.

## <a name="posting-profile-header"></a>Заголовок профиля разноски

В следующей таблице описаны параметры, доступные в разделе заголовка каждого профиля разноски управления ретробонусами.

| Поле | описание |
|---|---|
| Профиль разноски | Введите уникальное имя профиля. |
| описание | Введите описание профиля. |
| Модуль | Выберите модуль, с которым связаны ретробонусы и роялти профиля (*Клиент* или *Поставщик*). |
| Вид | Выберите типа профиля (*Ретробонус* или *Роялти*). |
| Вид платежа | <p>Это поле определяет формат вывода разнесенного ретробонуса.<p><p>Когда для поля **Тип** установлено значение *Ретробонус*, доступны следующие значения:</p><ul><li>*Оплата с использованием расчетов с поставщиками* — при разноске ретробонусов клиентов создается накладная поставщика для поставщика, которому предъявляется оплата, который настроен для клиента ретробонусов. При разноске ретробонусов поставщиков создается накладная поставщика для учетной записи ретробонусов поставщика.</li><li>*Клиентские вычеты* — при разноске ретробонуса создается журнал вычетов клиента для клиента ретробонусов.</li><li>*Клиентские вычеты налоговой накладной* — при разноске ретробонуса создается накладная с произвольным текстом для клиента ретробонусов.</li><li>*Торговые расходы* — при разноске ретробонуса создается журнал вычетов клиента для клиента ретробонусов.</li><li>*Отчетность* — при разноске ретробонуса создается журнал вычетов клиента для клиента ретробонусов.</li></ul><p>Когда для поля **Тип** установлено значение *Роялти*, доступны следующие значения:</p><ul><li>*Оплата с использованием расчетов с поставщиками* — при разноске ретробонусов создается накладная поставщика для учетной записи ретробонусов поставщика.</li><li>*Отчетность* — при разноске ретробонусов создается накладная поставщика для учетной записи ретробонусов поставщика.</li></ul><p>Дополнительные сведения см. в разделе [Типы платежей](#payment-types) ниже. |
| Организация | Выберите компанию (юридическое лицо), которой будут начисляться обеспечения и которая будет оплачивать требования. |

### <a name="payment-types"></a>Типы платежей

В следующей таблице приведена сводка, как различные настройки поля **Тип платежа** влияют на место разноски платежей. Платежи могут разноситься на счет клиента, счет поставщика или счет предъявления к оплате, в зависимости от целевой проводки и типа ретробонуса.

| Вид платежа | Тип целевой проводки | Тип ретробонуса программы | Платеж на (счет накладной) |
|---|---|---|---|
| Оплата с помощью модуля "Расчеты с поставщиками" | Журнал накладных поставщиков | Ретробонус клиента | Счет поставщика предъявления к оплате клиента |
| Оплата с помощью модуля "Расчеты с поставщиками" | Журнал накладных поставщиков | Роялти клиента | Счет поставщика |
| Оплата с помощью модуля "Расчеты с поставщиками" | Журнал накладных поставщиков | Ретробонус поставщика | Счет поставщика |
| Клиентские вычеты | Ежедневный журнал | Ретробонус клиента | Счет клиента |
| Вычеты клиента по налоговой накладной | Накладная с произвольным текстом | Ретробонус клиента | Счет клиента |
| Торговые расходы | Ежедневный журнал | Ретробонус клиента | Счет клиента |
| Отчетность | Ежедневный журнал | Ретробонус клиента | Счет клиента |
| Отчетность | Журнал накладных поставщиков | Роялти клиента | Счет поставщика |
| Отчетность | Журнал накладных поставщиков | Ретробонус поставщика | Счет поставщика |

> [!NOTE]
> При настройке [сделок управления ретробонусами](rebate-management-deals.md) необходимо учитывать следующие моменты:
>
> - Для сделок, в которых в поле **Выверка по** задано значение *Сделка*, в процессе разноски нельзя использовать динамический счет по сделкам. Следует использовать указанный счет клиента или поставщика.
> - Для сделок, в которых в поле **Выверка по** выбрано значение *Строка*, можно использовать профиль разноски, который корреспондируется на динамический счет проводок в строке сделки, поскольку клиент или поставщик настроен для каждой строки сделки.

## <a name="posting-fasttab"></a>Экспресс-вкладка разноски

В следующей таблице описаны поля, доступные на экспресс-вкладке **Разноска** каждого профиля разноски управления ретробонусами.

| Поле | описание |
|---|---|
| Тип кредитования | Выберите, следует ли выполнять кредитование счета ГК или клиента. Если в поле **Тип платежа** в заголовке задано значение *Вычеты клиента по налоговой накладной*, в этом поле устанавливается значение *Счет ГК*. Для ретробонусов поставщика в этом поле устанавливается значение *Счет ГК*. |
| Кредитовый счет | Выберите счет, на который разносятся кредитовые суммы при выполнении обеспечения ретробонусов. Этот счет также будет использоваться в качестве корр. счета при разноске ретробонусов для кредитования клиента или дебетования поставщика. |
| Наименование журнала<br>(В разделе **Обеспечение**) | Выберите имя журнала, который будет использоваться для записи разнесенного обеспечения. |
| Вид | Выбор того, следует ли разносить ретробонусы на счет ГК либо на клиента или поставщика. Если в поле **Тип платежа** в заголовке задано значение *Вычеты клиента по налоговой накладной*, в этом поле устанавливается значение *Клиент/Поставщик*. |
| Использование исходного счета | <p>Выберите одно из следующих значений:</p><ul><li>*Счет основных средств* — если выбрано это значение, необходимо указать счет в поле **Счет ретробонусов**.</li><li>*Счет строки сделки* — используется счет клиента или поставщика, указанный в строке ретробонусов. Это значение можно выбрать только для сделок, в которых в поле **Выверка по** выбрано значение *Строка*, и строк сделок, для которых в поле **Код счета** установлено значение *Таблица*. Не применяется к профилям разноски роялти клиента и ретробонусам поставщика, основанным на заказах на продажу.</li></ul> |
| Счет ретробонусов | Счет, на который будут разнесены фактические расходы по ретробонусам. |
| Наименование журнала<br>(В группе полей **Управление ретробонусами**) | Выберите имя журнала, который будет использоваться для разноски кредит-ноты для суммы ретробонуса для клиента или поставщика. Это поле недоступно, когда в поле **Тип платежа** в заголовке задано значение *Вычеты клиента по налоговой накладной*. Для ретробонусов клиента будут доступны имена журналов типа журнала *Ежедневно*. Для роялти клиента и ретробонусов поставщика будут доступны имена журналов типа журнала *Регистрация накладной от поставщика*. |
| Налоговая группа номенклатур | Укажите, является ли ретробонус налогооблагаемым. |
| Наименование журнала<br>(В группе полей **Списание**) | Если ретробонус, который должен быть разнесен, не совпадает с обеспечением, разница может быть списана. Выберите имя журнала, который будет использоваться для записи разнесенного списания. |

## <a name="posting-by-company-fasttab"></a>Экспресс-вкладка разноски по компаниям

Экспресс-вкладка **Разноска по компаниям** для каждого профиля разноски управления ретробонусами позволяет указать счет разноски, используемый каждой компанией (юридическим лицом) в сетке.

Используйте кнопки на панели инструментов, чтобы добавить компании в сетку или удалить их. Каждый раз, когда добавляется строка в сетку, используйте поле **Компания**, чтобы указать юридическое лицо для этой строки. Поле **Наименование** затем устанавливается автоматически.

Выберите строку для каждой компании, а затем введите следующие сведения, используя поля, расположенные под сеткой:

- **Тип дебета** — выбор того, следует ли выполнять дебетование счета ГК или поставщика. Для ретробонусов клиента и роялти в этом поле устанавливается значение *Счет ГК*.
- **Дебетовый счет** — введите счет, на который разносится сумма дебета, когда выполняются обеспечение ретробонусов.
- **Счет ГК** — выберите счет ГК для списаний.
