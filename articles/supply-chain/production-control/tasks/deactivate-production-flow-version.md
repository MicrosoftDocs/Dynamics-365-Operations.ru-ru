---
title: Деактивация версии производственного потока
description: Когда активная версия производственного потока больше не требуется, ее можно отключить.
author: cvocph
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e47cb950ce488d8b6170f829e1fedc664b921a1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811566"
---
# <a name="deactivate-a-production-flow-version"></a>Деактивация версии производственного потока

[!include [banner](../../includes/banner.md)]

Когда активная версия производственного потока больше не требуется, ее можно отключить. Необходимо использовать эту возможность только в том случае, если правила канбана и действия завершены и не будут активированы снова. Обратите внимание, что дата окончания срока действия всех правил канбана, связанных с этой версии производственного потока, будет обновлена на текущую дату и время. 

Для изменения активной версии производственного потока рекомендуется установить дату окончания для активной версии и создать новую версию. Это позволит вам продолжать ваши производственные операции, пока подготавливается новая версия и связанные правила канбана. 

Чтобы завершить срок действия активной версии производственного потока, необходимо задать дату окончания. В этом смысле деактивация больше похожа на исключение, чем на правило. 

Для этой процедуры требуется производственный поток с версией, которую можно отключить. Не попробуйте выполнить это в производственной среде, пока не будете на 100% уверены, что данная версия является полностью устаревшей.


## <a name="deactivate-a-production-flow-version"></a>Деактивация версии производственного потока
1. Перейдите в раздел "Управление производством" > "Настройка" > "Поток бережливого производства" > "Производственные потоки".
2. В списке найдите и выберите требуемую запись.
3. В списке перейдите по ссылке в выбранной строке.
4. В списке найдите и выберите требуемую запись.
5. Нажмите кнопку "Деактивировать".
    * Не продолжайте, если вы не уверены на 100%, что эта версия производственного потока является устаревшей. При нажатии ОК истекает срок действия всех активных правил канбана и происходит немедленная остановка всех действий по производству и пополнению этой версии производственного потока.  
6. Нажмите кнопку "OК".



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]