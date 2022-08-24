---
title: Проверка настраиваемого сертификата NF-e
description: В этой статье приводятся сведения о включении и использовании пользовательского сертификата NF-e.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288555"
---
# <a name="nf-e-custom-certificate-validation"></a>Проверка настраиваемого сертификата NF-e

[!include [banner](../includes/banner.md)]

Свойство **Цель проверки подлинности сервера** из сертификатов, выданных корневым центром сертификации Бразилии, по умолчанию отключено и должно быть включено вручную. В некоторых обстоятельствах автоматическое обновление сертификатов может переключать это свойство, чтобы оно больше не было включено. В этом случае виновато TLS-подключение, и оно больше не является доверенным. Также затрагивается возможность выпуска модели электронных финансовых документов Бразилии 55 (NF-e) в рабочие среды для штатов Минас-Жерайс (MG) и Парана (PR).

Чтобы включить исправление для **проверки пользовательского сертификата NF-e**, перейдите в **Управление функциями**. Эта функция позволяет использовать альтернативное решение для проверки сертификатов V5 и V10 и разрешает доверенное соединение с веб-службами, которое необходимо для безопасной передачи NF-e и получения авторизации от SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
