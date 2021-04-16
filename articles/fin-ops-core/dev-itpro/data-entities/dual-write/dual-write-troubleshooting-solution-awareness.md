---
title: Устранение неполадок, связанных с поддержкой решений
description: В этом разделе содержатся сведения об устранении неполадок, связанных с поддержкой решений.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 86dd8803f7560ea337f2452e9722fe0151466daf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748881"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Устранение неполадок, связанных с поддержкой решений

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Эта тема предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями Finance and Operations и Dataverse. Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с поддержкой решений.

> [!IMPORTANT]
> Для некоторых вопросов, связанных с этим разделом, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="error-on-the-dual-write-page"></a>Ошибка на странице двойной записи

На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:

*Объект с именем 'msdyn\_dualwriteentitymap' с namemapping='Logical' не найден в MetadataCache.*

Чтобы устранить проблему, убедитесь, что базовое решение двойной записи установлено в Dataverse. Базовое решение двойной записи является необходимым условием для поддержки решений.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]