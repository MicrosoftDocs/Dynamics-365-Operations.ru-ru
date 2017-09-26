--- 
title: "Настройка типов документов I-9"
description: "В этой процедуре показано, как просмотреть и настроить типы документов, которые используются для проверки формы I-9."
author: ShielaSogge
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: be0ae31e32e243874a58f37500ade097c7951ec2
ms.contentlocale: ru-ru
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-i-9-document-types"></a>Настройка типов документов I-9

[!include[task guide banner](../../../includes/task-guide-banner.md)]

В этой процедуре показано, как просмотреть и настроить типы документов, которые используются для проверки формы I-9. Прежде чем настраивать типы документов для I-9, необходимо также настроить типы удостоверений личности и выдающие их организации. Для этой процедуры используется компания с демонстрационными данными USMF. Демонстрационные данные включают примеры типов удостоверений личности и выдающих их организаций, необходимые для выполнения процедуры.

1. Перейдите в раздел "Управление персоналом" > "Работники" > "I-9" > "Типы документа I-9".
2. Щелкните "Создать".
3. В поле "Тип документа I-9" введите значение.
    * Пример: "Удостоверение личности, выданное учебным заведением".  
4. Выберите тип удостоверения личности.  Пример: "Удостоверение личности, выданное учебным заведением"
    * Примеры типов удостоверений личности — номер социального обеспечения (SSN), номер визы, паспорт или водительское удостоверение.  
5. Выберите список документов для I-9, используемый для документов этого типа.
    * В рамках процесса оформления I-9 сотрудники обязаны предоставить документы, по которым работодатель может убедиться в их личности и наличии у них разрешения на трудоустройство. На веб-сайте Службы гражданства и иммиграции США приведена информация о том, какие документы являются приемлемыми, а также к какому из списков они относятся.  http://www.uscis.gov  
6. В поле "Форма" введите официальный номер формы для данного типа документов. Пример: "Удостоверение личности, выданное учебным заведением".
    * Официальные номера форм можно найти на веб-сайте Службы гражданства и иммиграции США.  http://www.uscis.gov  
7. Установите или снимите флажок "Активный".
8. В поле "Срок действия" установите для даты значение ''27.10.2019".
    * Дата окончания срока действия является необязательной.  
9. Выберите организацию, выдавшую документ данного типа. Пример: район/территория
10. Нажмите кнопку "Сохранить".

