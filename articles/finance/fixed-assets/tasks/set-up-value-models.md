---
title: Настройка моделей стоимости
description: В этой процедуре показано, как создать новую модель стоимости основных средств и связать ее с группой ОС.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1131af52749854347fb92ec578e79ea601b93aed
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819586"
---
# <a name="set-up-value-models"></a>Настройка моделей стоимости

[!include [banner](../../includes/banner.md)]

В этой процедуре показано, как создать новую модель стоимости основных средств и связать ее с группой ОС. В нем используется роль бухгалтера и демонстрационные данные для юридического лица USMF.


## <a name="create-a-book"></a>Создайте книгу
1. Перейдите в раздел "Основные средства" > "Настройка" > "Книги".
2. Щелкните "Создать".
3. В поле "Книга" введите значение.
4. В поле "Описание" введите значение.
    * Если установлен флажок "Расчет амортизации", связанная модель стоимости основных средств будет включена в предложения по амортизации. В противном случае модель стоимости основных средств не будет амортизироваться автоматически.  
5. Выберите значение "Да" в поле "Расчет амортизации".
6. В поле "Профиль амортизации" введите или выберите значение.
    * Альтернативный метод амортизации также называется методом переключения амортизации. Предложение по амортизации переключается на этот метод, когда альтернативный метод рассчитывает сумму амортизации, которая больше или равна методу амортизации по умолчанию.  
    * Метод дополнительной амортизации используется для дополнительной амортизации основного средства в необычных условиях. Например, можно использовать это для записи амортизации в результате стихийного бедствия.  
    * Если установлен флажок "Создание переоценки амортизации с основными поправками", корректировки амортизации создаются автоматически при обновлении стоимости основного средства. В противном случае обновленная стоимость основного средства повлияет только на расчеты амортизации в будущем.  
7. Выберите "Да" в поле "Создание переоценки амортизации с основными поправками".
    * По умолчанию проводки модели стоимости ОС разносятся в главную книгу. Можно отключить разноску в главную книгу для этой книги, установив в поле "Разносить в главную книгу" значение "Нет". Книги, которые не разносятся в главную книгу, обычно используются для целей налоговой отчетности. Это дает дополнительную гибкость для удаления исторических проводок из модели стоимости ОС, поскольку они не фиксируются в главной книге.  
    * Поле "Слой разноски" по умолчанию имеет значение "Текущий слой", если книга разносится в главную книгу, или значение "Нет", если она не разносится в главную книгу. Обновите поле "Слой разноски", если требуется разнести проводки для данной книги на другой слой.  
8. В поле "Календарь" введите или выберите значение.
    * Производные книги будут разносить проводки по различным книгам одновременно. Вы создаете проводки в основной книге, и во время разноски точные копии проводки разносятся в производной книге. Пересчет с использованием проводок в производной книге не производится, поэтому она не должна использоваться для проводок амортизации.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Связь книги с группой основных средств
1. Щелкните "Группы ОС".
2. В поле "Группа ОС" введите или выберите значение.
3. В поле "Срок службы" введите число.
    * Обратите внимание, что поле "Периоды амортизации" рассчитывается после задания срока службы.  
    * Можно настроить соглашение по амортизации, требуемое для налогообложения.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]