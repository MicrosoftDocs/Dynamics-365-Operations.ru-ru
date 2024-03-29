---
title: Запишите номера сертификатов на предоставление налоговых льгот TDS
description: В этой статье объясняется, как записать номера сертификатов на предоставление налоговых льгот для налога, удерживаемого у источника (TDS), выданные поставщикам.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 116bc5c4b4f5f0b95d05dc73f2a012fbbc065bf2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846623"
---
# <a name="record-tds-concession-certificate-numbers"></a>Запишите номера сертификатов на предоставление налоговых льгот TDS

[!include [banner](../includes/banner.md)]

В этой статье объясняется, как записать номера сертификатов на предоставление налоговых льгот для налога, удерживаемого у источника (TDS), выданные поставщикам.

1. Перейдите в раздел **Налог \> Косвенные налоги \> Подоходный налог \> Концессии подоходного налога**.
2. В поле **Тип налога** выберите **TDS** для записи сертификатов на предоставление налоговых льгот для типа налога TDS.
3. На вкладке **Обзор** нажмите сочетание клавиш **ALT+N**, чтобы создать строку.

    [![Заголовок новой строки.](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. В поле **Код подоходного налога** выберите налоговый код TDS, для которого выпущены сертификаты на предоставление налоговых льгот для поставщиков. В поле **Имя подоходного налога** показано имя кода налога TDS.
5. В полях **Начальная дата** и **Конечная дата** укажите период действия для сертификата на предоставление налоговых льгот, который использует налоговый код TDS для расчета TDS для поставщика на основе концессии.
6. В поле **Примечания** введите любые замечания.
7. В поле **Раздел** введите код юридического раздела, к которому относится сертификат на предоставление налоговых льгот TDS.

    Если кодом раздела является 197, значение "A" появляется в обоих полях "Причина для невычета/меньшего вычета" в форме формы 26Q и в столбце "Причина невычета/уменьшение вычета/валовое исчисление (если имеется)" в форме 27Q. Если код раздела — 197A, в обоих местах появится значение "B".

8. Откройте экспресс-вкладку **Сертификат**, чтобы записать номера сертификатов на предоставление налоговых льгот TDS для поставщиков.
9. В поле **Счет поставщика** выберите номер счета поставщика, для которого выпускается сертификат на предоставление налоговых льгот TDS.
10. В полях **Начальная дата** и **Конечная дата** укажите период действия для сертификата на предоставление налоговых льгот TDS.

    Расчет TDS на основе концессий основан на периоде создания сертификата для поставщика.

11. В поле **Сертификат** введите номер сертификата на предоставление налоговых льгот TDS.

    [![Экспресс-вкладка сертификатов.](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Закройте страницу.
