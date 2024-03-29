---
title: Настройка налога для интернет-заказов
description: В этой статье представлен обзор выбора налоговой группы для различных типов интернет-заказов в Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: c899bd020ec9536a906a98635a6c70fac1355789
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819278"
---
# <a name="configure-sales-tax-for-online-orders"></a>Настройка налога для интернет-заказов

[!include [banner](includes/banner.md)]

В этой статье представлен обзор выбора налоговой группы для различных типов интернет-заказов с использованием настроек налога на основе места назначения или счета клиента. 

Возможно, вы захотите, чтобы канал электронной коммерции поддерживал такие возможности, как доставка или самовывоз для интернет-заказов. Применимость налога базируется на параметре, выбранном интерактивными клиентами. 

## <a name="destination-based-taxes-for-online-orders"></a>Налоги по месту назначения для интернет-заказов

В общем случае налоги для интернет-заказов, доставляемых по адресу клиентов, определяются пунктом назначения. Каждая налоговая группа имеет конфигурацию налога на основе места назначения розничной доставки, в которой предприятие может определить сведения о месте назначения, такие как страна или регион, область, район и город в иерархической форме.

Конфигурация для **Налога на основе розничной торговли** находится в разделе **Налоговый модуль > Косвенные налоги > Налог > Налоговые группы**.

### <a name="orders-delivered-to-customer-address"></a>Заказы доставлены на адрес покупателя

При размещении интернет-заказа налоговый механизм Commerce использует адрес доставки каждой номенклатуры строки в заказе и находит налоговые группы с соответствующими критериями налогов на основе пункта назначения. Например, для интернет-заказа с адресом поставки номенклатуры строки в Сан-Франциско, Калифорния, налоговая система найдет налоговую группу и налоговый код для Калифорнии, а затем рассчитает налог для каждой номенклатуры строки соответствующим образом.

### <a name="order-pick-up-in-store"></a>Получение заказа в магазине

Для строк заказа с указанным получением в магазине или в окне выдачи будет применяться налоговая группа из выбранного магазина самовывоза. Дополнительные сведения о настройке налогов для данного магазина см. в разделе [Задание других параметров налогов для магазинов](/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Налоги на основе счета клиента для интернет-заказов

Может существовать бизнес-сценарий, в котором необходимо настроить налоговую группу на конкретном счете клиента в Commerce Headquarters. В Commerce Headquarters имеется два места, где можно настроить налог по счету клиента. Чтобы получить доступ к этим сведениям, необходимо сначала перейти на страницу сведений о клиенте, перейдя на **Retail и Commerce \> Клиенты \> Все клиенты**, а затем выбрав клиента.

Налог счету клиента настраивается в двух местах:

- **Налоговая группа** на экспресс-вкладке **Накладные и поставка** на странице сведения о клиенте. 
- **Налог** на экспресс-вкладке **Общие** на странице **Управление адресами**. Чтобы получить его на странице сведения о клиенте, выберите конкретный адрес на экспресс-вкладке **адреса**, а затем выберите **Расширенный**.

> [!TIP]
> Для заказов интерактивных клиентов, если требуется применить только налоги по месту назначения и исключить налоги по счету клиента, убедитесь, что поле **Налоговая группа** пусто на вкладке **Накладные и поставка** на странице сведения о клиенте. Чтобы новые клиенты, которые подписываются с помощью интернет-канала, не унаследовали настройки налоговой группы из настроек клиента или группы клиентов по умолчанию, убедитесь в том, что поле **Налоговая группа** также пусто для настроек клиентов интернет-канала по умолчанию и настройки группы клиентов (**Retail и Commerce \> Клиенты \> Группы клиентов**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Определить применимость налога на основе места назначения или налога на основе счета клиента 

В следующей таблице объясняется, применяются ли налоги по месту назначения или налоги на основе счета клиента для интернет-заказов. 

| Тип клиента | Адрес доставки                   | Клиент > Накладные и поставка > Налоговая группа? | Адрес для счета клиента в headquarters? | Адрес клиента > Расширенный > Общие > Налоговая группа?                                              | Применена налоговая группа      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Гость         | Манхэттен, Нью-Йорк                      | Нет (пусто)                                                | Нет (пусто)                              | Нет (пусто)                                                                                                   | Нью-Йорк (налоги по месту назначения) |
| Вход выполнен     | Остин, Техас                          | Нет (пусто)                                             | Да                               | Не допускается<br/><br/>Новый адрес добавлен через интернет-канал.                                                            | Техас (налоги по месту назначения) |
| Вход выполнен     | Сан-Франциско, Калифорния (самовывоз в магазине) | Да (Нью-Йорк)                                            | Неприменимо                              | Неприменимо                                                                                                    | Калифорния (налоги по месту назначения) |
| Вход выполнен     | Хьюстон, Техас                         | Да (Нью-Йорк)                                            | Да                               | Да (Нью-Йорк)<br/><br/>Добавлен новый адрес через интернет-канал и налоговую группу, наследуемый от счета клиента. | Нью-Йорк (налоги на основе счета клиента)  |
| Вход выполнен     | Остин, Техас                          | Да (Нью-Йорк)                                            | Да                               | Да (Нью-Йорк)<br/><br/>Добавлен новый адрес через интернет-канал и налоговую группу, наследуемый от счета клиента. | Нью-Йорк (налоги на основе счета клиента)  |
| Вход выполнен     | Сарасота, Флорида                       | Да (Нью-Йорк)                                            | Да                               | Да (Вашингтон)<br/><br/>Вручную установлено на Вашингтон.                                                                          | Вашингтон (налоги на основе счета клиента)  |
| Вход выполнен     | Сарасота, Флорида                       | Нет (пусто)                                                | Да                               | Да (Вашингтон)<br/><br/>Вручную установлено на Вашингтон.                                                                          | Вашингтон (налоги на основе счета клиента)  |

## <a name="additional-resources"></a>Дополнительные ресурсы

[Настройка налогов для интернет-магазинов на основе места назначения](/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Обзор налога](../finance/general-ledger/indirect-taxes-overview.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Методы расчета налога в поле "Основание"](../finance/general-ledger/sales-tax-calculation-methods-origin-field.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Назначение и переопределения налога](../supply-chain/procurement/tasks/sales-tax-assignment-overrides.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Параметры расчета "Полная сумма" и "Интервал" для налоговых кодов](../finance/general-ledger/whole-amount-interval-options-sales-tax-codes.md?toc=%2fdynamics365%2fcommerce%2ftoc.json) 

[Расчет налогового освобождения](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
