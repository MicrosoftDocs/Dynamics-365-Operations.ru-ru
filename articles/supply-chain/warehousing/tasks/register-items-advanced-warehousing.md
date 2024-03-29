---
title: Регистрация номенклатур с поддержкой процессов управления складом с использованием журнала прихода номенклатуры
description: В этой статье представлен сценарий, который показывает, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при использовании процессов управления складами (WMS).
author: Mirzaab
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66fc9e21b79d70ec14750440c74d354bb8ec0695
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219609"
---
# <a name="register-items-enabled-for-warehouse-management-processes-using-an-item-arrival-journal"></a>Регистрация номенклатур с поддержкой процессов управления складом с использованием журнала прихода номенклатуры

[!include [banner](../../includes/banner.md)]

В этой статье представлен сценарий, который показывает, как зарегистрировать номенклатуры с помощью журнала прибытия номенклатур при использовании процессов управления складами (WMS). Обычно эту задачу выполняет сотрудник, ответственный за приемку.

## <a name="enable-sample-data"></a>Включение демонстрационных данных

Для работы с этим сценарием с помощью образцов записей и значений, указанных в этой статье, необходимо использовать систему, в которой установлены стандартные [демонстрационные данные](../../../fin-ops-core/fin-ops/get-started/demo-data.md), и перед началом необходимо выбрать юридическое лицо *USMF*.

Вместо этого можно работать с этим сценарием, подставив значения из собственных данных, если имеются следующие доступные данные:

- Необходимо иметь подтвержденный заказ на покупку с открытой строкой заказа на покупку.
- Номенклатуру в строке необходимо учитывать в запасах. Не должны использоваться варианты продукта, и не должны иметься аналитики отслеживания.
- Номенклатура должна быть связана с группой аналитик хранения, в которой включен процесс управления складом.
- Склад, который используется, необходимо разрешить для WMS, а местонахождение, которое используется для поступления, должно управляться номерными знаком.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Создание заголовка журнала поступления номенклатуры, в котором используется управление складом

Следующий сценарий показывает, как создать заголовок журнала поступления номенклатуры, в котором используется управление складом:

1. Убедитесь, что ваша система содержит подтвержденный заказ на покупку, удовлетворяющий требованиям, описанным в предыдущем разделе. В этом сценарии используется заказ на покупку для компании *USMF*, счет поставщика *1001*, склад *51* со строкой заказа для *10 PL* (10 палет) номера номенклатуры *M9200*.
1. Запишите номер заказа на покупку, который вы будете использовать.
1. Перейдите в раздел **Управление запасами \> Записи журнала \> Прибытие номенклатуры \> Прибытие номенклатуры**.
1. На панели операций выберите **Создать**.
1. Откроется диалоговое окно **Создание журнала управления складом**. Выберите имя журнала в поле **Имя**.
    - При использовании демонстрационных данных *USMF* выберите *WHS*.
    - Если вы используете собственные данные, в выбранном журнале для параметра **Проверять ячейки комплектации** должно быть установлено значение *Нет*, и для параметра **Управление карантином** — значение *Нет*.
1. Задайте в поле **Ссылка** значение *Заказ на покупку*.
1. Задайте в поле **Номер счета** значение *1001*.
1. Задайте в поле **Номер** номер заказа на покупку, указанного для данного упражнения.

    ![Журнал прихода номенклатуры.](../media/item-arrival-journal-header.png "Журнал прихода номенклатуры")

1. Выберите **ОК**, чтобы создать заголовок журнала.
1. В разделе **Строки журнала** выберите **Добавить строку** и введите следующие данные:
    - **Номер номенклатуры** — задан *M9200*. Параметры **Сайт**, **Склад** и **Количество** устанавливаются на основе данных проводки запасов на 10 палет (1000 шт.).
    - **Местоположение** — установлено значение *001*. В этом указанном местоположении не отслеживаются грузоместа.

    ![Строка журнала поступления номенклатур.](../media/item-arrival-journal-line.png "Строка журнала поступления номенклатур")

    > [!NOTE]
    > Поле **Дата** определяет дату, когда количество в наличии этой номенклатуры будет зарегистрировано в запасах.  
    >
    > **Номер лота** заполняется системой, если его можно однозначно идентифицировать по указанной информации. В противном случае необходимо ввести его вручную. Это обязательное поле, которое связывает эту регистрацию с конкретной строкой документа-источника.  

1. Выберите **Проверить** на панели операций. При этом проверяется, готов ли журнал к разноске. Если проверка завершилась ошибкой, потребуется исправить ошибки, прежде чем можно будет разнести журнал.  
1. Откроется диалоговое окно **Проверить журнал**. Нажмите **ОК**.
1. Просмотрите строку сообщений. Должно отобразиться сообщение о том, что операция была завершена.  
1. Выберите **Разнести** на панели операций.
1. Откроется диалоговое окно **Разнести журнал**. Нажмите **ОК**.
1. Просмотрите строку сообщений. Должны отобразиться сообщения о том, что операция завершена.
1. Выберите **Функции > Поступление продуктов** на панели операций, чтобы обновить строку заказа на покупку и разнести поступление продуктов.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
