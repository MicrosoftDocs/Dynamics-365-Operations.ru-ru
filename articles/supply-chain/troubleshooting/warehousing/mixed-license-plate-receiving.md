---
title: Использование смешанных грузомест не работает для всех кодов методов обработки
description: Если для поля Действие для кода метода обработки выбрано Кредит или Отходы, для обработки возвращенных номенклатур можно использовать только пункт меню Получение грузоместа со смешанными номенклатурами.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b762255bc5ef6a1e15688a9c635940e92e67db3c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477441"
---
# <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-but-credit"></a>Использование смешанных грузомест не работает для любого метода обработки, за исключением кредита

## <a name="symptoms"></a>Симптомы

Если для поля **Действие** для кода метода обработки выбрано *Кредит* или *Отходы*, для обработки возвращенных номенклатур можно использовать только пункт меню [Получение грузоместа со смешанными номенклатурами](/dynamics365/supply-chain/warehousing/mixed-license-plate-receiving).

## <a name="resolution"></a>Решение

Корпорация Майкрософт проверила эту проблему и определила, что она является ограничением функции. В настоящее время только [коды методов обработки](/dynamics365/supply-chain/service-management/set-up-disposition-codes), у которых в поле **Действие** задано значение *Кредит* или *отходы*, поддерживаются для получения грузомест со смешанными номенклатурами.
