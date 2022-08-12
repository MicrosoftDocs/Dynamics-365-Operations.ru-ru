---
title: Устранение неполадок, связанных с поддержкой решений
description: В этой статье содержатся сведения об устранении неполадок, которые могут быть полезны при разрешении проблем, связанных с поддержкой решений.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 6866956efcc76a7da6c3aa5fb36058de78d5472e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111309"
---
# <a name="troubleshoot-issues-related-to-solution-awareness"></a>Устранение неполадок, связанных с поддержкой решений

[!include [banner](../../includes/banner.md)]





Эта статья предоставляет информацию по устранению неполадок для интеграции двойной записи между приложениями для управления финансами и операциями и Dataverse. Конкретно, в этом разделе содержатся сведения об устранении неполадок, связанных с поддержкой решений.

> [!IMPORTANT]
> Для устранения некоторых проблем, рассмотренных в этой статье, может потребоваться роль системного администратора или учетные данные администратора клиента Microsoft Azure Active Directory (Azure AD). В разделе для каждого выпуска объясняется, требуются ли конкретная роль или учетные данные.

## <a name="error-on-the-dual-write-page"></a>Ошибка на странице двойной записи

На странице **Двойная запись** может быть выведено сообщение об ошибке, подобное следующему примеру:

*Объект с именем 'msdyn\_dualwriteentitymap' с namemapping='Logical' не найден в MetadataCache.*

Чтобы устранить проблему, убедитесь, что базовое решение двойной записи установлено в Dataverse. Базовое решение двойной записи является необходимым условием для поддержки решений.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
