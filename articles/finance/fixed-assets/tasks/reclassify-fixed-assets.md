---
title: Переклассификация основных средств
description: В этой статье описывается процесс переклассификации активов. Чтобы реклассифицировать основное средство, необходимо переместить его в новую группу основных средств или назначить ему новый номер основных средств в той же группе.
author: moaamer
ms.date: 05/14/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4bd901b1709f0b006cecfbbf6d8c170b56f89d19
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284374"
---
# <a name="reclassify-fixed-assets"></a>Переклассификация основных средств

[!include [banner](../../includes/banner.md)]

Чтобы реклассифицировать основное средство, необходимо переместить его в новую группу основных средств или назначить ему новый номер основных средств в той же группе. 

При реклассификации основного средства:

- Для нового основного средства создаются все книги для существующих основных средств. Вся информация, которая была настроена для исходного основного средства, копируется в новое основное средство. Книги для исходных основных средств имеют статус "Закрыто". 

- Новые книги новых основных средств содержат дату реклассификации в поле **Дата приобретения**. Дата в поле **Дата начала амортизации** копируется из исходной информации об ОС. Если амортизация уже начата, в поле **Дата последней амортизации** отображается дата реклассификации. 

- Существующие проводки по основным средствам для исходного основного средства отменяются, и создаются проводки для нового основного средства.

- При реклассификации актива с проводкой перемещения система выводит сообщение в **Центр действий**, указывая на то, что проводка перемещения не была завершена в ходе процесса реклассификации. Необходимо выполнить проводку перемещения, чтобы переместить существующие проводки реклассификации в соответствующие финансовые аналитики. 

   В процессе процесса реклассификации система выполняет следующие действия для повторной классификации баланса ОС из исходного актива в новый актив. 
   
   - Процесс реклассификации копирует данные из исходной книги основных средств в новую книгу основных средств.

   - В проводке реклассификации используются данные из первоначально разнесенного приобретения, включая информацию финансовой аналитики, включенную в проводку приобретения.  
   
   - В то же время процесс реклассификации выполняет сторнирование проводки первоначального приобретения активов и перемещения активов. 

Следующие схема и процедура содержат пример процесса реклассификации. 

[![Диаграмма, демонстрирующая процесс реклассификации.](../media/reclassification-process-01.png)](../media/reclassification-process-01.png)

Выполните следующие действия, чтобы изменить классификацию основного средства:

1. Перейдите в раздел **Основные средства > Периодические задачи > Реклассификация**.
2. В поле **Группа ОС** выберите группу, которую требуется реклассифицировать.
3. В поле **Номер основного средства** выберите основное средство для реклассификации.
4. В поле **Новая группа основных средств** выберите группу, в которую требуется переместить основное средство.
    * Если новая группа основных средств прикреплена к номерной серии, поле **Новый инвентарный номер ОС** обновляется с учетом номера из новой номерной серии группы основных средств. В противном случае поле **Новый инвентарный номер ОС** обновляется с учетом номера из новой номерной серии, настроенной на странице **Параметры основных средств**. Если номерная серия не настроена на странице **Параметры основных средств**, введите номер в поле **Новый инвентарный номер ОС**.  
5. В поле **Дата реклассификации** введите дату.
6. В поле **Серии ваучеров** введите или выберите значение.
7. Нажмите **ОК**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
