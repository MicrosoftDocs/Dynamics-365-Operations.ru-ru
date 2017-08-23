--- 
title: "Настройка формата платежной квитанции для накладных проекта"
description: "Компании обычно вкладывают распечатанные платежные квитанции к накладным, чтобы помочь клиентам и предоставить ссылку на платеж для разноски и сопоставления."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 02/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 8afbcf781e917f48136e06692234d49302b077fb
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-payment-slip-format-for-project-invoices"></a>Настройка формата платежной квитанции для накладных проекта

[!include[task guide banner](../../includes/task-guide-banner.md)]

Компании обычно вкладывают распечатанные платежные квитанции к накладным, чтобы помочь клиентам и предоставить ссылку на платеж для разноски и сопоставления. Платежную квитанцию можно использовать для накладных проекта или услуги, писем-напоминаний, процент-нот и выписок по счету в дополнение к накладным по продаже и накладным с произвольным текстом. Для обработки платежных квитанций сначала необходимо задать идентификационный номер кредитора и форматы вложений платежных квитанций.

В данной процедуре используется демонстрационная компания DEMF. 

Эта функция доступна для юридических лиц, основной адрес которых находится в Дании.


## <a name="set-up-a-creditor-id-number"></a>Настройка кода кредитора
1. Перейдите в раздел "Управление организацией" > "Организации" > "Юридические лица".
2. Разверните или сверните раздел "Сведения о банковском счете".
3. Щелкните "Изменить".
4. В поле "Код финансового учреждения-кредитора" введите значение.
5. Нажмите кнопку "Сохранить".
6. Закройте страницу.

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a>Настройка формата платежной квитанции для накладных, примечаний, писем и выписок
1. Выберите "Расчеты с клиентами" > "Настройка" > "Формы" > "Настройка форм".
2. Щелкните вкладку Накладная.
3. В поле "Вложение со связанным платежом по накладной клиента" выберите параметр.
    * Нет — не печатать платежную квитанцию. Выберите этот параметр, если сумма платежа представлена в валюте, отличной от датских крон (DKK).   FIK 751 — Печать платежной квитанции FIK 751, если планируется вручную указать сумму оплаты и срок оплаты на платежной квитанции.   FIK 752 — печать платежной квитанции FIK 752, если планируется использовать созданную системой платежную квитанцию с уже распечатанными суммой оплаты и сроком.  
4. Нажмите кнопку "Сохранить".
5. Перейдите на вкладку "Free text invoice".
6. В поле "Вложение со связанным платежом в накладной с произвольным текстом" выберите параметр.
    * Нет — не печатать платежную квитанцию. Выберите этот параметр, если сумма платежа представлена в валюте, отличной от датских крон (DKK).   FIK 751 — печать платежной квитанции FIK 751, если планируется вручную указать сумму оплаты и срок оплаты на платежной квитанции.   FIK 752 — печать платежной квитанции FIK 752, если планируется использовать созданную системой платежную квитанцию с уже распечатанными суммой оплаты и сроком.  
7. Нажмите кнопку "Сохранить".
8. Перейдите на вкладку "Процент-нота".
9. В поле "Вложение со связанным платежом по процент-ноте" выберите параметр.
    * Нет — не печатать платежную квитанцию. Выберите этот параметр, если сумма платежа представлена в валюте, отличной от датских крон (DKK).   FIK 751 — печать платежной квитанции FIK 751, если планируется вручную указать сумму оплаты и срок оплаты на платежной квитанции.   FIK 752 — печать платежной квитанции FIK 752, если планируется использовать созданную системой платежную квитанцию с уже распечатанными суммой оплаты и сроком.  
10. Нажмите кнопку "Сохранить".
11. Перейдите на вкладку "Письмо-напоминание".
12. В поле "Вложение со связанным платежом в письме-напоминании" выберите параметр.
    * Нет — не печатать платежную квитанцию. Выберите этот параметр, если сумма платежа представлена в валюте, отличной от датских крон (DKK).   FIK 751 — печать платежной квитанции FIK 751, если планируется вручную указать сумму оплаты и срок оплаты на платежной квитанции.   FIK 752 — печать платежной квитанции FIK 752, если планируется использовать созданную системой платежную квитанцию с уже распечатанными суммой оплаты и сроком.  
13. Нажмите кнопку "Сохранить".
14. Откройте вкладку "Выписка по счету".
15. В поле "Вложение со связанным платежом для выписки по счету" выберите параметр.
    * Нет — не печатать платежную квитанцию. Выберите этот параметр, если сумма платежа представлена в валюте, отличной от датских крон (DKK).   FIK 751 — печать платежной квитанции FIK 751, если планируется вручную указать сумму оплаты и срок оплаты на платежной квитанции.   FIK 752 — печать платежной квитанции FIK 752, если планируется использовать созданную системой платежную квитанцию с уже распечатанными суммой оплаты и сроком.  
16. Нажмите кнопку "Сохранить".
17. Закройте страницу.

