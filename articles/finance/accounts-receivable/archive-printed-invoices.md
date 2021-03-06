---
title: Архивировать напечатанные счета клиентов с хэш-номерами
description: В этом разделе описывается, как включить архивирование для хранения распечатанных накладных клиентов с хеш-числами.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018986"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a>Архивировать напечатанные счета клиентов с хэш-номерами

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

В некоторых странах имеется законное требование о хранении рассчитанных хеш-чисел в системе вместе с распечаткой некоторых документов. Хэш-числа могут использоваться для отчетности в органы власти и во время аудита.

В этом разделе описывается, как настроить архивирование для хранения распечатанных накладных клиентов с хеш-числами.

## <a name="prerequisites"></a>Необходимые условия

- В рабочей области **управления функциями** включите функцию, **Архивировать распечатанные накладные клиента с хеш-числами**. Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Настройте подходящие для печати форматы необходимых документов в **управлении печатью**.

Эти функции применимы к следующим документам.

**Расчеты с клиентами**
- Накладная клиента
- Кредит-нота клиента
- Накладная с произвольным текстом
- Кредит-нота с произвольным текстом

**Управление и учет по проектам**
- Накладная по проекту
- Кредит-нота по проекту

## <a name="configure-customer-master-data"></a>Настройка справочника клиентов
Выполните следующие шаги, чтобы настроить данные клиента и включить возможность автоматического сохранения распечатанных накладных в качестве вложений.

1. Перейдите в раздел **Расчеты с клиентами** > **Все клиенты**. 
2. Выберите клиента и на вкладке **Накладные и поставка** в разделе **E-INVOCE** в поле **вложение электронной накладной** выберите **Да**.

## <a name="print-invoices"></a>Печать накладных
Можно выполнить разноску и печать любого произвольного текста, клиента, накладной по проекту или кредит-ноты для клиента, настроенного в предыдущей процедуре.

Открывает страницу **вложения** для распечатанной накладной. На экспресс-вкладке **вложения** в группе полей **дополнительные сведения** в поле **хэш-число документа** найдите сохраненное хеш-число, рассчитанное для напечатанной накладной.

![Хэш-число вложения](media/attach-hash-num.jpg)

