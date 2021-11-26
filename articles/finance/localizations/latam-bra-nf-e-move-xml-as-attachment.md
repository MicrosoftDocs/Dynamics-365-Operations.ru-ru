---
title: Перемещение файлов XML NF-e как вложений
description: В этой теме описано, как перемещать файлы XML NF-e из базы данных Microsoft Dynamics 365 Finance или Dynamics 365 Supply Chain Management и делать их доступными в качестве вложений.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: c7b82d486cecf6b20f1283fa609c360b3003efca
ms.sourcegitcommit: ebf6546835e4d6a80aea1dfae81e119e294387f0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/12/2021
ms.locfileid: "7799452"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Перемещение файлов XML NF-e как вложений

[!include [banner](../includes/banner.md)] 


При выдаче электронных финансовых документов (NF-e) XML-файлы создаются и сохраняются в базах данных Microsoft Dynamics 365 Finance и Dynamics 365 Supply Chain Management. В локализации для Бразилии можно использовать функцию **Перемещение файлов XML NF-e как вложений**, чтобы освободить место в базе данных, занимаемое этими файлами XML.

Для конкретного диапазона дат и финансового учреждения функция переместит XML-файлы NF-e из базы данных Finance или Supply Chain Management в хранилище больших двоичных объектов из вашей подписки Azure. Это перемещение делает файлы доступными только как вложения. После успешного переноса файлов XML в хранилище больших двоичных объектов исходные файлы удаляются из базы данных Finance или Supply Chain Management. Таким образом, пространство базы данных, занимаемое этими файлами, освобождается.

Выполните эти шаги, чтобы включить функцию **Перемещение файлов XML NF-e как вложений**.

1. В Finance или Supply Chain Management откройте рабочую область **Управление функциями**.
2. На вкладке **Все** найдите и выберите функцию **Перемещение файлов XML NF-e как вложений**.
3. Выберите **Включить**.

Выполните следующие действия, чтобы переместить файлы XML NF-e как вложения.

1. Перейдите в раздел **Расчеты с клиентами** \> **Финансовые документы** \> **Электронные финансовые документы** \> **Перемещение файлов XML NF-e как вложений**.
2. В полях **Дата от** и **Дата до** выберите начальную и конечную даты.
3. В поле **Идентификатор финансового учреждения** выберите значение.
4. Нажмите **ОК**.

> [!IMPORTANT]
> Этот процесс необратим. После перемещения файлов XML NF-e пользователи могут просматривать их только путем выбора пункта **Вложения** в верхней части страницы **Финансовый документ**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
