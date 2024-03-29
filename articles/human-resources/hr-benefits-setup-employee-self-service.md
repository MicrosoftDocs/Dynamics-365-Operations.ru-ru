---
title: Настройка самообслуживания сотрудников
description: В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле дистанционного обслуживания сотрудников.
author: twheeloc
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cdc82c23635cc99c37aa770b996d9d2df43f5059
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324649"
---
# <a name="configure-employee-self-service"></a>Настройка самообслуживания сотрудников

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

В Microsoft Dynamics 365 Human Resources можно настроить плитки для переходов верхнего уровня в модуле **Дистанционное обслуживание сотрудников**. Плитки плана льгот направляют пользователей в планы льгот, для которых они имеют право.

## <a name="set-up-a-benefit-plans-tile"></a>Настройка плитки планов льгот

1. В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.

2. Выберите вкладку **Настройка плитки планов льгот**, а затем выберите **Создать**.

3. Укажите значения для следующих полей.

   | Поле | Описание |
   | --- | --- |
   | **Код типа плана** | Тип плана, который отображается, когда эта плитка выбрана в **Самообслуживание льгот**. |
   | **Идентификатор плитки** | Уникальный идентификатор для плитки. |
   | **Текст метки плитки** | Текст, который будет отображаться для плитки в **Самообслуживание льгот**. |
   | **описание** | Описание плитки. |
   | **Фоновое изображение плитки** | URL-адрес изображения, используемого для плитки (необязательно). |
   | **Отслеживание открытой регистрации** | Выберите этот параметр, чтобы отслеживать выполнение открытой регистрации для данного типа плана. Например, можно создать планы, в которых **Тип плана = Прочее**. Эти планы могут быть необязательными планами, для которых не требуется отслеживать ход регистрации. Если этот тип плана не выбран, этот тип плана не будет учитываться при отслеживании прогресса или завершении регистрации на вкладке **Открытая регистрация**. Этот параметр применяется к типу плана, который выбран для всех периодов и юридических лиц. |

4. Нажмите **Сохранить**.

## <a name="set-up-a-flex-credit-plan-tile"></a>Настройка плитки плана гибкого кредита

1. В рабочей области **Управление льготами** в **Настройка** выберите **Параметры дистанционного обслуживания сотрудников**.

2. Выберите вкладку **Настройка плитки плана гибкого кредита**, а затем выберите **Создать**.

3. Укажите значения для следующих полей.

   | Поле | Описание |
   | --- | --- |
   | **Код кредита льготы** | Планы гибкой кредитной программы, который будет отображаться, когда эта плитка выбрана в **Самообслуживание льгот**. |
   | **Идентификатор плитки** | Уникальный идентификатор для плитки. |
   | **Текст метки плитки** | Текст, который будет отображаться для плитки в **Самообслуживание льгот**. |
   | **описание** | Описание плитки. |
   | **Фоновое изображение плитки** | URL-адрес изображения, используемого для плитки (необязательно). |
   | **Отслеживание открытой регистрации** | Выберите этот параметр, чтобы отслеживать выполнение открытой регистрации для данного типа плана. Например, можно создать планы, в которых **Тип плана = Прочее**. Эти планы могут быть необязательными планами, для которых не требуется отслеживать ход регистрации. Если этот тип плана не выбран, этот тип плана не будет учитываться при отслеживании прогресса или завершении регистрации на вкладке **Открытая регистрация**. Этот параметр применяется к типу плана, который выбран для всех периодов и юридических лиц. |

4. Нажмите **Сохранить**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
