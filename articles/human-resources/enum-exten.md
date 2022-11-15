---
title: Расширение базового перечисления полов
description: В этой статье представлен обзор расширяемости базового перечисления полов (enum).
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749320"
---
# <a name="gender-base-enum-extensibility"></a>Расширение базового перечисления полов

Перечисление **Пол** (enum) теперь является расширяемым. В этой статье описываются изменения, которые необходимо внести в базу кода, если предполагается расширить перечисление **Пол**.

## <a name="gender-vs-hcmpersongender"></a>Сравнение пола и HcmPersonGender

Для значений пола имеется два перечислимых типа:

- **Пол** (платформа приложений)
- **HcmPersonGender** (PersonnelManagement)

Перечисление **Пол** используется во всем приложении Microsoft Dynamics 365 Finance, в то время как **HcmPersonGender** относится к функциям управления людскими ресурсами (HCM). Если используются функции HCM и вы вносите какие-либо изменения в перечисление **Пол**, следует рассмотреть возможность внесения таких же изменений в **HcmPersonGender**. Например, если вы добавили **Трансгендер** в перечисление **Пол**, следует также добавить **Трансгендер** в перечисление **HcmPersonGender**.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (класс)

Был создан новый класс **HcmPersonGenderTranformUtil**, позволяющий выполнять преобразование между двумя базовыми перечислителями. В этом классе имеются два метода: **convertGenderToHcmPersonGender** и **convertHcmPersonGenderToGender**. Расширение следует создавать, используя класс **Цепочка команд** или **обработчики событий**, и расширить оба метода для сопоставления новых значений, добавляемых к базовому перечислению.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (класс)

**PayrollStateWageTaxPrepDP** является классом поставщика данных для отчета **Предоплата налога по зарплате государственных зарплат** из SQL Server Reporting Services (SSRS) Для США доступны три значения: **Мужчина**, **Женщина** и **Не указано**. В методе **populatePayrollStateWageTaxPrepTmp** имеется оператор switch, который используется для сопоставления значения перечисления **HcmPersonGender** с одним из трех полей: **IsMale**, **IsFemale** или **IsUnspecifiedGender**. Значением по умолчанию для оператора switch является **IsUnspecifiedGender**. Если вы добавляете какие-либо значения в перечисление **HcmPersonGender** для другого сопоставления, необходимо создать расширение с помощью класса **Цепочка команд** через метод **populatePayrollStateWageTaxPrepTmp** для изменения значения, если это необходимо.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (класс)

Класс интеграции **smmOutlookSync_Contact** связывает значения с **Outlook** и **Контактные лица** или из них. **Outlook** поддерживает три значения: **Мужчина**, **Женщина** и **Не указан**. У класса есть два метода, которые помогут сопоставить значения **Genders** с **OutlookGenders**. Метод по умолчанию — **NonSpecific/UnSpecified**. Если вы создаете дополнительные значения для перечисления **Пол**, вы должны создать расширение с помощью класса **Цепочка команд** через оба метода и сопоставление, если требуется.
