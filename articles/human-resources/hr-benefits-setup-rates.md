---
title: Настройка ставок
description: Ставки в Microsoft Dynamics 365 Human Resources определяют, сколько работодатели и сотрудники вкладывают для льготы.
author: andreabichsel
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2b6767df573260f32de8409e487f649bdc4779b0
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266665"
---
# <a name="configure-rates"></a>Настройка ставок

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Ставки в Microsoft Dynamics 365 Human Resources определяют, сколько работодатели и сотрудники вкладывают для льготы. Значением может быть сумма или гибкие кредиты в зависимости от конфигурации.

Используйте ставки, чтобы определить, сколько сотрудники и работодатели платят для каждой льготы на основе нескольких факторов. Ставки покрытия зависят от даты, поэтому можно хранить запись журнала ставок. 

## <a name="set-up-rates"></a>Настройка ставок

1. В рабочей области **Управление льготами** в разделе **Настройка** выберите **Ставки**.

2. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | Описание |
   | --- | --- |
   | **Курс** | Уникальное имя, идентифицирующее ставку льготы. |
   | **Описание** | Описание ставки льготы. |
   | **Действует** | Дата, с которой ставка действует. Значение по умолчанию — текущая системная дата. 
   | **Истечение срока действия** | Дата окончания ставки. Значение по умолчанию — 12/31/2154, что означает "никогда". |
   | **Использовать уровни** | Уровень, используемый для расчета ставки льготы. Один уровень для одного уровня ставки льготы или двойной уровень для двух уровней ставки льготы. Примером двойного уровня является уровень, основанный по полу и возрасту. |
   | **Частота платежей** | Частота платежей, которая определяет частоту, с которой премия по льготе выплачивается поставщику льготы. Например, если частота платежей — ежемесячно, то ставка льготы представляет сумму ежемесячного платежа. |
   | **Округление коэффициента частоты платежей** | Методы округления ставки: стандартный, усеченный, нормальный, нисходящий и округление в большую сторону. </br></br><ul><li>**Стандартный** — всегда округлять. Например, 10,611 будет округлено до 10,62. –10,231 будет округлено до –10,23. </li><li>**Усечено** — всегда округляется в меньшую сторону. Например, 10,619 будет округлено до 10,61. –10,231 будет округлено до –10,24. </li><li>**Нормально** — десятичные значения, заканчивающиеся или больше 5, будут округляться в сторону от нуля. Десятичные значения, заканчивающиеся на или меньше 4, округляются в сторону нуля. Например, 10,615 будет округлено до 10,62. –10,235 будет округлено до –10,24. 10,614 будет округлено до 10,61. –10,234 будет округлено до –10,23. </li><li>**В меньшую сторону** — округление в сторону нуля. Например, 10,619 будет округлено до 10,61. –10,231 будет округлено до –10,23. </li><li>**В большую сторону** — округление от нуля. Например, 10,619 будет округлено до 10,62. –10,231 будет округлено до –10,24. |
   | **Сумма сотрудника для некурящего** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма работодателя для некурящего** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма курящего сотрудника** | Сумма, которую поставщик льготы выплачивает за курящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма работодателя для курящего** | Сумма, которую поставщик льготы выплачивает за курящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Административная сумма** | Административная сумма, взимаемая сторонним администратором. Это сумма, которую работодатель платит стороннему администратору и которая должна основываться на частоте платежей для настройки ставки. |
   | **Ставка Flex Credit** | Количество гибких кредитов для стоимости льготы. Это применимо только к ставкам, которые относятся к планам льгот, которые связаны с гибкими кредитными программами. При использовании ставок уровней ставка гибкого кредита определяется в "Действия" > "Ставки уровней". |
   | **Дата вступления изменения в силу** | Дата вступления в силу изменения ставки льготы. Система автоматически изменит ставку льготы и обновит все планы льгот, связанные с данной ставкой, при условии, что выполняется обработка обновления изменения ставки. Не устанавливайте эту дату, если не требуется, чтобы система автоматически обновила планы льгот сотрудника на основе этой ставки. Обычно это значение зарезервировано для автоматической обработки будущего изменения ставки. Дата вступления изменений в силу должна быть в пределах дат вступления в силу и даты окончания ставки льготы. |
   | **Изменение ставки завершено** | Флажок **Изменение ставки завершено** будет выбран автоматически после того, как изменения ставки льгот завершены с помощью обработки обновления изменения ставки. |

4. Чтобы отследить и настроить изменения настройки ставки льгот, выберите **Действия**, а затем выберите **Управление версиями**.

5. Нажмите **Сохранить**. 

## <a name="set-up-tier-rates"></a>Настройка ставок

Можно использовать ставки уровней в настройке ставок, если ставка может различаться в зависимости от различных факторов. Например, можно настроить ставки уровня так, чтобы, например, если возраст достигает 34,99, то сумма для некурящего равна 2. Если возраст достигает 39,99, то сумма для некурящего равна 3.

Можно также использовать два уровня. Если выбрано значение **Двойной уровень** для значения **Использовать уровни** в форме **Настройка ставки**, можно определить ставки на основе двух аналитик. Например, можно настроить систему двойного уровня так, чтобы, например, если вы мужчина и ваш возраст достигает 34,99, то сумма для некурящего равна 2. Если вы мужчина и ваш возраст достигает 39,99, то сумма для некурящего равна 3. Если вы женщина и ваш возраст достигает 34,99, то сумма для некурящего равна 1,8. Если вы женщина и ваш возраст достигает 39,99, то сумма для некурящего равна 2,8.

1. В рабочей области **Управление льготами** в разделе **Настройка** выберите **Ставки**.

2. Выберите одну или несколько ставок из списка, выберите **Действия**, а затем выберите **Ставки уровней**.

3. Выберите **Создать**.

3. Укажите значения для следующих полей:

   | Поле | описание |
   | --- | --- | 
   | **Описание** | Значение поля **Описание** применяется из описания в записи настройки ставки. Это позволяет определить, с какой ставкой связаны ставки уровней. |
   | **Код уровня** | Выберите код уровня. Коды уровней определяются в форме кодов уровней. Система автоматически отобразит описание кода уровня в сетке слева. |
   | **Тип уровня** | Указывает, какое поле должно использоваться в качестве критерия выбора для процесса расчета ставки уровня. Пример:</br></br><ul><li>Если используется **Возраст**, система использует дату рождения сотрудника в процессе расчета ставки льготы.</li><li>Если используется **Зарплата**, система использует ежегодную зарплату по льготе сотрудника в процессе расчета ставки льготы.</li><li>Если используется **Тип должности**, система будет использовать текущую запись активной должности сотрудника, чтобы определить тип должности по записи должности, связанной с позицией.</li></ul></br></br>Типы уровней — это **Возраст**, **Зарплата**, **Физический**, **Пол**, **Эквивалент полного времени**, **Тип должности**, **Регион компенсации** и **Уровень**. | 
   | **Уровень** | Значение, используемое с типом уровня во время процесса расчета ставки льготы. Пример:</br></br><ul><li>Если тип уровня — **Возраст**, это будет значение возраста.</li><li>Если тип уровня — **Зарплата**, это будет сумма зарплаты.</li><li> Если тип уровня — **Тип должности**, это будет тип должности.</li></ul></br></br>При типе уровня **Возраст** или **Зарплата**, значение в поле **Уровень** соответствует верхней границе уровня. В качестве уровня **Тип должности** система использует точный метод соответствия при выборе ставки уровня. |
   | **Тип расчета** | Указывает, как использовать сумму в поле суммы расчета и какой математический расчет следует выполнять в случае необходимости. Если типом расчета является фиксированная сумма, система использует поля сумм как есть. Если типом расчета является $ суммы зарплаты или покрытия, система использует сумму расчета и направление расчета в математических расчетах.</br></br>Если типом расчета является "сумма зарплаты за $", система использует следующее математическое уравнение:</br></br>Готовая зарплата по льготе, разделенная на сумму расчета (с округлением вверх или вниз), умноженная на суммы для курящих или некурящих для сотрудника или работодателя.</br></br>Если типом расчета является "сумма покрытия за $", система использует следующее математическое уравнение:</br></br>Сумма покрытия, разделенная на сумму расчета (с округлением вверх или вниз), умноженная на суммы для курящих или некурящих для сотрудника или работодателя.</br></br>В обоих расчетах направление расчета используется, чтобы определить, следует ли округлить годовую зарплату по льготе или сумму покрытия, деленную на сумму расчета, вверх или вниз. |
   | **Расчет суммы** | Сумма, используемая во время процесса расчета ставки льготы. Эта сумма будет делителем во время математического расчета ставки уровня. |
   | **Направление расчета** | Направление, для которого рассчитанная сумма результата должна быть округлена. Система поддерживает три направления вычислений: пустой (точный метод), **Увеличение** и **Уменьшение**.</br></br><ul><li>Если поле пусто, система будет использовать точный расчет суммы заработной платы/покрытия, деленной на сумму расчета. Если это значение имеет дробную часть, она будет использоваться системой в расчете.</li><li>При **Увеличении** система увеличит математическое вычисление суммы зарплаты/покрытия, деленной на сумму расчета, до следующего целого числа, что означает, что 12,25 увеличится до 13.</li><li>При **Уменьшении** система уменьшит математическое вычисление суммы зарплаты/покрытия, деленной на сумму расчета, до текущего целого числа, что означает, что 12,25 уменьшится до 12.</li></ul> |
   | **Сумма сотрудника для некурящего** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма работодателя для некурящего** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма курящего сотрудника** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Сумма работодателя для курящего** | Сумма, которую поставщик льготы выплачивает за некурящего сотрудника. Это сумма, которую работодатель платит поставщику льгот и которая должна основываться на частоте платежей для настройки ставки. |
   | **Административная сумма** | Административная сумма, взимаемая сторонним администратором. Это сумма, которую работодатель платит стороннему администратору и которая должна основываться на частоте платежей для настройки ставки. |
   | **Ставка гибкого кредита для некурящих** | Количество гибких кредитов, которые зависят от стоимости льготы, на основе расчета, определенного для уровня для некурящих. Например, если типом расчета является **на $ суммы покрытия**, сумма расчета составляет 10 000, а ставка гибкого кредита для некурящих равна 6, это означает, что если некурящий сотрудник выбирает $10 000 покрытия, у него будет 6 гибких кредитов. Если он выбирает $20 000 покрытия, это приведет к стоимости 12 гибких кредитов и т. д. |
   | **Ставка гибких кредитов для курящих** | Количество гибких кредитов, которые зависят от стоимости льготы, на основе расчета, определенного для уровня для курящих. |

5. Нажмите **Сохранить**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
