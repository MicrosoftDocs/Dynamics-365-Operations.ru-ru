---
title: Настройка параллельных ветвей в workflow-процессе
description: Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7dac62abe080ac362abc3456a7760bbd3f790fd
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066501"
---
# <a name="configure-parallel-branches-in-a-workflow"></a>Настройка параллельных ветвей в workflow-процессе

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Чтобы настроить параллельную ветвь, необходимо выполнить следующие действия в редакторе workflow-процессов.

Параллельная ветвь — это по сути workflow-процесс, который выполняется в контексте родительского workflow-процесса.

## <a name="name-a-branch"></a>Имя ветви

Чтобы ввести название параллельной ветви, необходимо выполнить следующие действия.

1. Щелкните правой кнопкой мыши параллельную ветвь и выберите пункт **Свойства**. Будет открыта форма **Свойства**.
2. В левой области нажмите **Основные настройки**.
3. В поле **Имя** введите уникальное имя для параллельной ветви.
4. Нажмите кнопку **Закрыть**.

## <a name="design-and-configure-the-elements-of-a-branch"></a>Создание и настройка элементов ветви

Выполните следующие действия, чтобы создать и настроить элементы параллельной ветви.

1. Дважды щелкните параллельную ветвь.
2. Перетащите элементы workflow-процесса на холст, а затем настройте элементы, как и любой другой workflow-процесс. Дополнительные сведения см. в разделе [Обзор создания бизнес-правил](create-workflow.md).

## <a name="additional-resources"></a>Дополнительные ресурсы

[Обзор создания бизнес-правил](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]