---
title: Страна происхождения
description: Многие организации выдают сертификаты своим поставщикам, чтобы гарантировать соответствие продуктов конкретным стандартам сертификации. Эти сертификаты часто зависят от страны происхождения. В этой статье приводятся сведения о функции страны происхождения, которая позволяет связать продукт с его страной происхождения и отслеживать сертификаты продуктов.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COOVendorCerts
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 60d5a2067b8e3d311af89fb09cfa3b5c007db219
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882528"
---
# <a name="country-of-origin"></a>Страна происхождения

[!include [banner](../includes/banner.md)]

Многие организации выдают сертификаты своим поставщикам, чтобы гарантировать соответствие продуктов конкретным стандартам сертификации. Эти сертификаты часто зависят от страны происхождения. Функция страны происхождения позволяет связать продукт с его страной происхождения и отслеживать сертификаты продуктов.

## <a name="turn-on-the-country-of-origin-feature"></a>Включение функции страны происхождения

В Supply Chain Management версии 10.0.21 эта функция включена по умолчанию. Администраторы могут использовать страницу [управления функциями](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) для проверки статуса компонента и включения или выключения их при необходимости. В этой статье функция указана следующим образом:

- **Модуль:** *Управление сведениями о продукте*
- **Название функции:** *Функция управления страной происхождения*

## <a name="configure-source-and-destination-countries"></a>Настройка исходных и конечных стран

Перед выпуском сертификата для продукта необходимо связать продукт с соответствующей страной назначения и его страной происхождения.

1. Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Правила страны происхождения**.
2. Выберите существующую настройку страны для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку страны.
3. Задайте следующие значения для выбранной или новой страны.

    | Поле | описание |
    |---|---|
    | Код номенклатуры | Выберите код номенклатуры для продукта. |
    | Страна/регион места назначения | Выберите страну, в которую вы отправляете продукт. |
    | Страна происхождения | Выберите страну, из которой вы доставляете продукт. |

Цель этой настройки — помочь в создании отчета по спецификации (BOM), в котором можно включить страну происхождения для каждой части, для которой указаны страны происхождения и назначения. Этот отчет поможет получить целостную картину, откуда поступают части и куда они отправляются.

## <a name="keep-track-of-vendor-certificates"></a>Отслеживание сертификатов поставщиков

Можно использовать страницу **Сертификаты поставщиков страницы происхождения** для отслеживания сертификатов, выданных поставщикам.

Необходимо решить, какие документы сертификатов вы выдаете и как они будут предоставляться клиентам. Эта функция помогает отслеживать ваши сертификаты. Она также позволяет выбрать, будут ли соответствующие номера сертификатов отображаться в накладных, отборочных накладных и/или подтверждениях заказов.

Для настройки сведений о ваших сертификатах выполните следующие действия.

1. Перейдите к пункту **Управление сведениями о продукте \> Настройка \> Соответствие продуктов \> Страна происхождения \> Сертификаты поставщика страны происхождения**.
2. Выберите существующую настройку сертификата для редактирования или выберите **Создать** на панели операций, чтобы создать новую настройку сертификата.
3. Задайте следующие настройки для выбранного или нового сертификата.

    | Поле | описание |
    |---|---|
    | Счет поставщика | Выберите поставщика, для которого выдан сертификат. |
    | Код номенклатуры | Выберите номенклатуру, для которой выдан сертификат. |
    | Страна/регион | Страна или регион назначения, для которых необходимо использовать этот сертификат. |
    | Номер сертификата | Введите идентификационный номер выданного сертификата. |
    | Действует | Выберите первую дату, когда текущий сертификат действителен.|
    | Истечение срока действия | Выберите последнюю дату, когда текущий сертификат действителен. |
    | Печать на счете | Установите этот флажок для печати номера сертификата на счетах, адресованных в указанную страну в указанном диапазоне дат. |
    | Печать на отборочной накладной | Установите этот флажок для печати номера сертификата на отборочных накладных, адресованных в указанную страну в указанном диапазоне дат. |
    | Печать на заказе на продажу | Установите этот флажок для печати номера сертификата на заказах на продажу, адресованных в указанную страну в указанном диапазоне дат. |

## <a name="include-the-country-of-origin-on-bom-reports"></a>Включение страны происхождения в отчеты по спецификации

При создании отчета по спецификации можно включить страну происхождения для каждой части, для которой были указаны исходная и конечная страны, на странице **Правила страны происхождения**.

1. Выберите **Управление сведениями о продукте \> Продукты \> Выпущенные продукты**.
1. Выберите или создайте продукт, чтобы открыть его страницу **Сведения о выпущенном продукте**.
1. В области действий на вкладке **Инженер** в группе **Спецификации** выберите **Конструктор**.
1. На открывшейся странице списка в области операций выберите **Спецификация \> Печать**.
1. В диалоговом окне **Строки спецификации** задайте в поле **Страна назначения** страну назначения, которую необходимо просмотреть в отчете.
1. Нажмите **ОК**.

Создается и отображается отчет, содержащий информацию о стране происхождения для каждой части. Ниже приведен пример отчета.

![Отчет о стране происхождения.](media/country-of-origin-report.png "Отчет о стране происхождения")


[!INCLUDE[footer-include](../../includes/footer-banner.md)]