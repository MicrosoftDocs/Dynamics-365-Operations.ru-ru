---
title: Импорт ваучеров с помощью объекта "Общий журнал"
description: В этой статье приводятся советы по импорту данных в общий журнал с использованием объекта "Общий журнал".
author: rcarlson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5917a047d3098875f3ab95087e761e6428c18b
ms.sourcegitcommit: 6b209919de39c15e0ebe4abc9cbcd30618f2af0b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/11/2022
ms.locfileid: "9135731"
---
# <a name="importing-vouchers-by-using-the-general-journal-entity"></a>Импорт ваучеров с помощью объекта "Общий журнал"

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

В этой статье приводятся советы по импорту данных в общий журнал с использованием объекта "Общий журнал".

Объект "Общий журнал" можно использовать для импорта ваучеров с типом счета или типом корр. счета **Главная книга**, **Клиент**, **Поставщик** или **Банк**. Ваучер может вводиться в виде одной строки, используя как поле **Счет**, так и поле **Корр. счет**, или в виде ваучера с несколькими строками, где используется только поле **Счет** (а поле **Корр. счет** остается пустым на каждой строке). Объект "Общий журнал" поддерживает не все типы счетов. Вместо этого существуют другие объекты для сценариев, в которых требуются различные комбинации типов счетов. Например, чтобы импортировать проводку по проекту используйте объект "Журнал расходов по проекту". Каждый объект разработан для поддержки определенных сценариев. Это означает, что в этих сценариях могут быть доступны дополнительные поля для объектов. Однако дополнительные поля могут быть недоступны в объектах в других сценариях.

## <a name="setup"></a>Настройка
Прежде чем выполнять импорт с помощью объекта "Общий журнал", проверьте следующие настройки:

- **Настройка номерных серий для номера партии журнала** — по умолчанию при импорте с помощью объекта "Общий журнал" номер партии журнала использует номерную серию, определенную в параметрах главной книги. Если задать для номерной серии номера пакета журнала значение **Вручную**, номер по умолчанию не применяется. Эта настройка не поддерживается.
- **Конфигурация финансовой аналитики** — каждая организация должна определить порядок финансовых аналитик при использовании объектов для импорта проводок. Порядок определяется для формата **Интеграция аналитик ГК** в разделе **Главная книга** &gt; **План счетов** &gt; **Аналитики** &gt; **Конфигурация финансовой аналитики для интеграции приложений** &gt; **Выбор информационных объектов**. Сегменты счета ГК, который импортируется, должны иметь тот же порядок. В противном случае произойдет ошибка во время импорта.

## <a name="general-journal-entity-setup"></a>Настройка объекта "Общий журнал"
Два параметра в модуле "Управление данными" влияют на способ применения номера партии журнала по умолчанию или номера ваучера:

- **Обработки на основе набора** (в информационном объекте)
- **Сгенерированный автоматически** (при сопоставлении полей)

В следующих разделах описываются результаты применения этих параметров. В них также объясняется, как система создает номера партий для журналов и кодов ваучеров.

### <a name="journal-batch-number"></a>Номер партии журнала

- Параметр **Обработка на основе набора** в объекте "Общий журнал" не влияет на способ создания номеров партий журналов.
- Если в поле **Номер партии журнала** задано значение **Сгенерировано автоматически**, новый номер партии журнала создается для каждой импортируемой строки. Это поведение не рекомендуется. Параметр **Сгенерировано автоматически** расположен в проекте импорта в разделе **Просмотр карты** на вкладке **Сведения о сопоставлении**.
- Если в поле **Номер партии журнала** не задано значение **Сгенерировано автоматически**, номер партии журнала создается следующим образом:

    - Если номер партии журнала, определенный в импортируемом файле, совпадает с существующим неразнесенным ежедневным журналом, все строки, имеющие соответствующий номер партии журнала, импортируются в существующий журнал. Строки не импортируются в номер партии разнесенного журнала. Вместо этого создается новый номер.
    - Если номер партии журнала, определенный в импортируемом файле, не совпадает с существующим неразнесенным ежедневным журналом, все строки с одинаковым номером партии журнала, группируются в новом журнале. Например, все строки, имеющие номер партии журнала 1, импортируются в новый журнал, и все строки, имеющие номер партии журнала 2, импортируются во второй новый журнал. Номер партии журнала создается с помощью номерной серии, определенной в параметрах главной книги.

### <a name="voucher-number"></a>Номер ваучера

- При использовании параметра **Обработка на основе набора** в объекте "Общий журнал" номер ваучера должен быть предоставлен в импортируемом файле. Каждой проводке в общем журнале назначается номер ваучера, который предоставляется в импортируемом файле, даже если ваучер не сбалансирован. Обратите внимание на следующие моменты, если вы хотите использовать обработку на основе набора, но также хотите использовать номерную серию, определенную для номеров ваучеров.

    - Чтобы включить эту функциональность, в имени журнала, который используется для импорта, для поля **Выделение номеров при разноске** задайте значение **Да**.
    - Номер ваучера по-прежнему должен быть определен в файле импорта. Однако этот номер является временным и будет заменен номером ваучера при разноске журнала. Убедитесь, что строки журнала сгруппированы правильно по временному номеру ваучера. Например, при разноске найдено три строки, которые имеют временный номер ваучера 1. Временный номер ваучера всех трех строк заменяется следующим номером в номерной серии. Если эти три строки не являются сбалансированным объектом, ваучер не будет разноситься. Затем, если найдены строки, имеющие временный номер ваучера 2, этот номер заменяется следующим номером ваучера в серии и т. д.

- Если вы не используете параметр **Обработка на основе набора**, не требуется предоставлять номер ваучера в импортированном файле. Номера ваучеров создаются во время импорта на основе настройки имени журнала (**Только один ваучер**, **В связи с сальдо** и так далее). Например, если имя журнала определяется как **В связи с сальдо**, первая строка получает новый номер ваучера по умолчанию. Затем система оценивает строку, чтобы определить, равны ли дебеты кредитам. Если существует корр. счет в строке, следующая импортируемая строка получает новый номер ваучера. Если корр. счет не существует, система оценивает, равны ли дебеты кредитам при импорте каждой новой строки.
- Если в поле **Номер ваучера** задано значение **Сгенерировано автоматически**, импорт завершится ошибкой. Параметр **Сгенерировано автоматически** для поля **Номер ваучера** не поддерживается.

По умолчанию объект "Общий журнал" использует обработку на основе набора. После оценки бизнес-требований организации можно изменить параметр **Обработка на основе набора**, щелкнув **Информационные объекты** в рабочей области **Управление данными**. Обработка на основе набора позволяет ускорить процесс импорта. Если вы не используете обработку на основе набора, импорт объекта "Общий журнал" будет проходить медленнее.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
