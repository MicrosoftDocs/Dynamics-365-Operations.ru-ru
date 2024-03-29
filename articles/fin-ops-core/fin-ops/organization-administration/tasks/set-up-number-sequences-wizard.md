---
title: Настройка номерных серий с использованием мастера
description: В этой статье поясняется, как настроить все требуемые номерные серии одновременно с помощью мастера.
author: SunilGarg
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cae739aad1166eee1abebe3c0adc7939bca55bc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847073"
---
# <a name="set-up-number-sequences-using-a-wizard"></a>Настройка номерных серий с использованием мастера

[!include [banner](../../includes/banner.md)]

Номерные серии используются для создания читаемых уникальных кодов для записей справочников и записей проводок, для которых требуются идентификаторы. Основные данные или запись проводки, для которой требуется идентификатор, называется образцом. Перед созданием новых записей для ссылки необходимо настроить номерную серию и связать ее со ссылкой. В этой статье поясняется, как настроить все требуемые номерные серии одновременно с помощью мастера. В качестве компании с демонстрационными данными для создания этой процедуры используется USMF.

1. Перейдите к **Область перехода > Модули > Управление организацией > Номерные серии" > Номерные серии**.
2. Выберите **Создать**.
3. Выберите **Далее**.

   - На этой странице можно изменить идентификационный код, наименьшее значение и самое высокое значение. Кроме того, можно указать, должна ли номерная серия быть непрерывной.   
   - Не выбирайте вариант **Непрерывная**, если необходимо предварительно распределить числа для номерной серии. Для добавления сегмента масштаба в формат номерной серии выберите формат в списке, затем выберите **Включение области в формат**. Для удаления сегмента масштаба из формата номерной серии выберите формат в списке, затем выберите **Удаление области из формата**. Чтобы исключить номерную серию из автоматического создания, выберите номерную серию в списке, затем выберите **Удалить**.  

4. Выберите **Далее**.
5. Выберите **Готово**.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
