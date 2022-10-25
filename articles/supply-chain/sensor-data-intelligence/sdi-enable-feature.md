---
title: Включение аналитики данных датчиков в системе
description: В этой статье объясняется, как включить аналитику данных датчиков в своей системе.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 68b9daa6ffdc50d28f746cae060efc1a97ccd57a
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689976"
---
# <a name="turn-on-sensor-data-intelligence-for-your-system"></a>Включение аналитики данных датчиков в системе

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

## <a name="video-instructions"></a>Видеоинструкции

В следующем видео показано, как включить функцию Аналитики данных датчиков и [развернуть нужные ресурсы Azure](sdi-deploy-iot-solution-on-azure.md). В другом разделе этой статьи приводятся те же инструкции в текстовом формате.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE58g3I]

## <a name="procedure"></a>Процедура

Прежде чем использовать аналитику данных датчиков, ее необходимо включить для системы.

1. Перейдите в раздел **Администрирование системы \> Рабочие области \> Управление функциями**. (Дополнительные сведения см. в разделе [Обзор управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. На вкладке **Все** используйте поле **Фильтр**, чтобы выполнить поиск функции с именем *Аналитика данных датчиков*.
1. Если в вашей системе включена функция *Аналитики данных датчиков*, выберите ее в списке, а затем выберите **Отключить**, чтобы отключить ее. Эту старую версию функции нельзя использовать вместе с новой предварительной версией, которую вы включите на следующем шаге.
1. Используйте поле **Фильтр**, чтобы выполнить поиск функции с именем *(Предварительная версия) Аналитика данных датчиков*.
1. Выберите функцию в списке, а затем выберите **Включить сейчас**, чтобы включить ее.
