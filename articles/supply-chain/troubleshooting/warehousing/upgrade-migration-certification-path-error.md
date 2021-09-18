---
title: Ошибка пути сертификации при обновлении или миграции на WMS
description: Если в приложении отображается сообщение об ошибке "Не найдена привязка доверия для пути сертификации" при обновлении или миграции на WMS, на этой странице приводятся сведения о том, как устранить проблему.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477390"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>При обновлении и переходе на систему управления складом не найдена привязка доверия для пути сертификации

## <a name="symptoms"></a>Симптомы

При попытке обновления или миграции на расширенное управление складом (WMS) приложение Warehouse Management может отобразить следующее сообщение об ошибке:

> java.security.cert.certPathValidatorException: Привязка доверия для пути сертификации не найдена.

## <a name="cause"></a>Причина

Это происходит из-за того, что самозаверяющие сертификаты не являются доверенными в Android 8+ в локальных средах.

## <a name="resolution"></a>Решение

Используйте внешний (общий) центр сертификации (ЦС). Исправление для этой проблемы доступно в приложении Warehouse Management версии 1.9.0.0. Дополнительные сведения об этой проблеме и ее устранении см. в разделе [Привязка доверия для пути сертификации не найдена при настройке подключения приложения](certification-path-app-connection-error.md).
