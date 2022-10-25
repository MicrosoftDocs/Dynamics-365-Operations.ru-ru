---
title: Принятые файлы Invoice Capture
description: В этой статье объясняется, как собирать файлы накладных из других источников в Invoice Capture.
author: sunfzam
ms.date: 10/13/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3c55540d11a67d4d4c4c8477d51cb6f1f5777767
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690128"
---
# <a name="invoice-capture-received-files"></a>Принятые файлы Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В Invoice Capture страница **Полученные файлы** — это центральное место, куда поступают файлы накладных из других источников.

## <a name="upload-invoice-files"></a>Отправка файлов накладных

Служащие отдела расчетов с поставщиками (AP) могут отправлять изображения накладных, выбирая команду **Отправить файл**, чтобы открыть диалоговое окно **Отправка**. После того как клерк AP выбрал файл, становится доступной кнопка **Отправить**.

## <a name="include-or-obsolete-invoice-files"></a>Включение или устаревание файлов накладных

Пользователи могут выбирать накладные, содержащие ошибки или предупреждения, а затем либо включать накладные, либо объявлять их устаревшими, выбирая соответствующую кнопку на панели операций. Накладная, помеченная как устаревшая, не будет отображаться в представлении **Полученные файлы (устаревшие)**.

## <a name="view-captured-invoices"></a>Просмотр записанных накладных

После успешного распознавания полученного файла сведения о записанной накладной возвращаются ИИ-моделью и вводятся в Microsoft Dataverse. Сотрудник AP может затем проверить сведения накладной, выбрав **Просмотр записанных накладных**. Пользователи могут при необходимости загрузить исходный файл накладных.
