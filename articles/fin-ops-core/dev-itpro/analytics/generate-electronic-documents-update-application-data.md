---
title: Создание электронных документов и обновление данных приложений с помощью электронной отчетности (ER)
description: Можно разработать форматы электронной отчетности (ER), которые могут использоваться в приложении для создания исходящих электронных документов. Можно также создать форматы ER, которые анализируют входящие электронные документы и используют содержимое в таких документах для обновления данных приложения.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 333f91cef12b6564ca9bc668732b4cc038f0fa7e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/27/2019
ms.locfileid: "2181872"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a>Создание электронных документов и обновление данных приложений с помощью электронной отчетности (ER)

[!include [banner](../includes/banner.md)]

Можно разработать форматы электронной отчетности (ER), которые могут использоваться в приложении для создания исходящих электронных документов. Можно также создать форматы ER, которые анализируют входящие электронные документы и используют содержимое в таких документах для обновления данных приложения.

С помощью этой функции можно использовать один формат ER для создания исходящих электронных документов, а затем обновить данные приложения. Эта функция может использоваться в следующих случаях:

- Чтобы предотвратить повторяющееся использование данных приложения в последующих процессах, можно пометить данные приложения сразу же после их использования для создания электронных документов. Например, можно пометить проводки по оплате можно пометить как обработанные сразу же после их включения в созданное сообщение по платежу.
- Чтобы сохранить подробные сведения об обработке электронных документов, которые были созданы с использованием логики ER. Например, уникальный идентификатор сообщения об оплате, создаваемый с помощью выражения ER. Выражение основывается на информации, введенной в диалоговом окне ER, когда формат ER используется для создания документов.

Для получения дополнительных сведений о данной функции, компоненте, см. ряд руководств "Создание документов электронной отчетности с обновлением данных" (часть бизнес-процесса 7.5.4.3 "Приобретение/разработка компонентов ИТ-услуг и решений" (10677)), в которых дано описание отчетности и архивирования Интрастат. Для выполнения определенных действий в этих руководствах необходимы следующие файлы. Загрузите и сохраните эти файлы на локальный компьютер.

- [Конфигурация модели данных: Интрастат (модель)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Конфигурация сопоставления модели ER: Интрастат (сопоставление)](https://go.microsoft.com/fwlink/?linkid=849038)
- [Конфигурация формата ER: Интрастат (формат)](https://go.microsoft.com/fwlink/?linkid=849038)