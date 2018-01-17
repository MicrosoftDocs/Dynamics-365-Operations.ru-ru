---
title: "Импорт данных из шаблонов информационных объектов Excel с несколькими листами"
description: "В этом разделе описывается, как импортировать данные с помощью шаблонов информационных объектов Excel в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition."
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 0ca19ab9ed7a52328c5dd5252c418bb9343bdc2b
ms.openlocfilehash: 84b9e9128d7ea6cdf9949549f4ab7a1c6c01691b
ms.contentlocale: ru-ru
ms.lasthandoff: 12/14/2017

---

# <a name="excel-templates-with-multiple-worksheets"></a>Шаблоны Excel с несколькими листами

Управление данными в Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition поддерживает шаблоны на основе Microsoft Excel для информационных объектов. Эти шаблоны могут содержать один или несколько листов. Шаблоны с несколькими листами часто используются, когда удобно управлять данными в одном файле и импортировать их в несколько информационных объектов. Примерами могут служить сайты и склады.

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>Отправка файла один раз и сопоставление его всем объектам
Рассмотрим пример, где имеется один файл Excel с листами, которые называются **Сайты** и **Склады**. Чтобы настроить проект импорта данных, следует добавить первый информационный объект, **Сайты**, затем отправить файл. Можно будет выбрать **Сайты** в качестве листа, используемого для этого объекта.

Если вы добавите второй объект **Склады**, не выходя из формы **Добавить файл**, поле подстановки листа позволит выбрать лист **Склады** без необходимости повторной отправки файла. Единственная причина отправить новый файл существовала бы, если бы данные **Склады** были в другом файле.

![Несколько листов](./media/AddFileMultipleWorkSheets.png) 

## <a name="fix-worksheet-to-entity-mapping"></a>Исправление сопоставления листов и объектов

Сопоставление листа с информационным объектом в задании импорта можно исправить из сетки. Столбец **Лист** в сетке отображает листы из файла, которые были сопоставлены. В раскрывающемся меню можно выбрать другой лист. Если выбранный лист уже сопоставлен объекту в проекте данных, система запрашивает подтверждение изменения. Рекомендуется исправить все сопоставления в сетке.

![Обновление сопоставления листов](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>Изменение сопоставления на новый файл

В случаях, когда новая версия того же файла или совершенно новый файл должен быть отправлен для существующих объектов в проекте данных, необходимо использовать процесс **Добавить файл** и снова добавить объекты, как если бы они добавлялись в первый раз. Перед продолжением система запросит подтверждение, что вы хотите перезаписать существующие объекты в проекте данные. Объекты, которые не были добавлены повторно (или перезаписаны) сохранят предыдущие сопоставления из предыдущего файла.

## <a name="upload-a-file-using-run-project"></a>Отправка файла с помощью команды "Выполнить проект"

Можно отправить файл Excel при использовании параметра **Выполнить проект** для выполнения проекта импорта. Будьте внимательны, чтобы отправить только файлы, имеющие те же листы, что и существующие сопоставления для информационных объектов в проекте данных. Если лист отсутствует в новом отправленном файле, система выводит сообщение об ошибке и останавливает импорт. Если сопоставление с листом должно быть изменено для объекта, сначала необходимо обновить сопоставления в проекте данных из проекта данных, прежде чем использовать этот файл в процессе **Выполнить проект**.

