---
title: Удаленные или устаревшие функции в Dynamics 365 Finance
description: В этой статье описываются функции, которые были удалены или которые планируется удалить из Dynamics 365 Finance.
author: kfend
ms.date: 10/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 25d13aa26565e5753b87c843b43cf46f8276b642
ms.sourcegitcommit: 6c05bcd27e6ee72f01cb66e2cfd1e929e0365830
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/16/2022
ms.locfileid: "9854088"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Удаленные или устаревшие функции в Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

В этой статье описываются функции, которые были удалены или которые планируется удалить из Dynamics 365 Finance.

- *Удаленная* функция больше недоступна в продукте.
- *Устаревшая* функция не находится в активной разработке и может быть удалена в следующем обновлении.

Этот список поможет вам учитывать эти удаления и устаревания при своем собственном планировании. 

> [!NOTE]
> Подробные сведения об объектах в приложениях для управления финансами и операциями можно найти в документе [Технический справочник по отчетам](/dynamics/s-e/global/axtechrefrep_61). Можно сравнить различные версии этих отчетов, чтобы получить сведения об объектах, которые были изменены или были исключены в каждой версии приложений для управления финансами и операциями.

## <a name="features-removed-or-deprecated-in-the-finance-10031-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.31

### <a name="edifact-paymul-at-configuration-under-payment-model"></a>Конфигурация EDIFACT PAYMUL (AT) в разделе "Модель оплаты"

| &nbsp;  | &nbsp;  |
|---|---|
| **Причина устаревания/удаления** | Заменено на новый формат, основанный на ISO 20022 pain.001.001.09. | 
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Приложение |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: банки в Австрии прекратят поддержку EDICFACT-PAYMUL для транснациональных платежей к ноябрю 2022 г. и заменят его на версию XML pain.001.001.09N. Новая конфигурация добавлена в Глобальный репозиторий конфигураций, что позволит пользователям выполнять запрос на транснациональные платежи. |

## <a name="features-removed-or-deprecated-in-the-finance-10030-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.30

### <a name="revenue-recognition"></a>Признание выручки

[Признание выручки](../../finance/accounts-receivable/revenue-recognition-overview.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Причина устаревания/удаления** |Заменяется улучшенной функциональностью [Выставление счетов по подпискам](../../finance/accounts-receivable/subscription-billing-summary.md)
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта** | Приложение |
| **Вариант развертывания** | Все |
| **Состояние** | Устарело: после апреля 2023 функция признания выручки в Dynamics 365 Finance больше не будет получать поддержку с исправлением ошибок. Клиентам будет предложено использовать улучшенную функцию [Выставление счетов по подпискам](../../finance/accounts-receivable/subscription-billing-summary.md). В октябре 2023 функция признания выручки больше не будет доступна. Клиентам будет предложено перейти на улучшенную функцию выставления счетов по подпискам. Для функции объединения в качестве признания выручки сейчас не планируется никакой функции на замену.|

## <a name="features-removed-or-deprecated-in-the-finance-10029-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.29

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Заказы на перемещение запасов, включающие налог в трансферной цене

[Заказы на перемещение запасов, включающие налог в трансферной цене](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md)

| &nbsp;  | &nbsp;  |
|---|---|
| **Причина устаревания/удаления** | Замена на улучшенные функции; [Заказы на перемещение запасов для Индии](../../finance/localizations/apac-ind-stock-transfer.md)|
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта** | Приложение |
| **Вариант развертывания** | Все |
| **Состояние** | Устареет: после апреля 2023 года функция **Заказы на перемещение запасов, включающие налог в трансферной цене** больше не будет получать техническую поддержку с исправлениями ошибок и исправлениями системы безопасности. Клиентам будет предложено использовать улучшенные функции; [Заказы на перемещение запасов для Индии](../../finance/localizations/apac-ind-stock-transfer.md). После октября 2023 года функция **Заказы на перемещение запасов, включающие налог в трансферной цене** станет недоступна и клиентам будет предложено перейти к улучшенным функциям. |

### <a name="bank-statement-import-and-export-of-positive-pay-file"></a>Импорт банковских выписок и экспорт файлов положительных платежей

| &nbsp;  | &nbsp;  |
|---|---|
| **Причина устаревания/удаления** |Замещено усовершенствованной функцией, импорт банковских выписок и экспорт файлов положительных платежей.| 
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Приложение |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: функциональность XSLT для импорта и экспорта файлов больше не будет получать поддержку с исправлением ошибок и исправлениями безопасности. Клиентам будет предложено использовать улучшенную функциональность: [Настройка файлов положительных платежей с помощью электронной отчетности](../../finance/accounts-payable/set-up-positive-pay-er.md) и [Настройка расширенного импорта банковской выверки с помощью электронной отчетности](../../finance/accounts-payable/import-bai2-er.md). После сентября 2022 года функция XSLT больше не будет доступна, и клиентам будет предложено перейти к усовершенствованной функциональной возможности.|


## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.26

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Отчет по налогам для Финляндии (разработка на основе кодов отчетности)

[Отчет о налоге для Финляндии](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новой структурой декларации по НДС, [Декларация по НДС для Финляндии](../localizations/emea-fin-vat-declaration.md). |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Приложение |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревшие: с 1 марта 2023 г. корпорация Майкрософт планирует больше не поддерживать налоговый отчет для Финляндии (макет отчета для Финляндии). Новые форматы электронной отчетности **TXT-документ декларации по НДС (FI)** и **Excel декларации по НДС (FI)** введены в качестве модели **Налоговая декларация**. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.24

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Отчет по налогам для Швеции (разработка на основе кодов отчетности)

[Отчет по налогам для Швеции](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новой структурой декларации по НДС, [Декларация по НДС для Швеции](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревшие: с 1 декабря 2022 г. корпорация Майкрософт планирует больше не поддерживать налоговый отчет для Швеции (макет отчета для Швеции). Новые форматы электронной отчетности **XML-документ декларации по НДС (SE)** и **Excel декларации по НДС (SE)** введены в качестве модели **Налоговая декларация**. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>Отчет по НДС для Австрии (разработка на основе кодов отчетности)

[Сведения выписки по НДС для Австрии](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новой структурой декларации по НДС, [Декларация по НДС для Австрии](../localizations/emea-aut-vat-declaration-austria.md) |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревшие: с 1 декабря 2022 г. корпорация Майкрософт планирует больше не поддерживать формат электронной отчетности **Декларация по НДС (AT)** в пункте **Модель декларации по НДС**. Новые форматы **XML-документ декларации по НДС (AT)** и **Excel декларации по НДС (AT)** введены в качестве модели **Налоговая декларация**. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes-electronic-tax-declaration-log-menu-item-and-page-electronic-tax-declaration-setup-menu-item-and-page-german-report-layout-taxreport_de-ssrs-format"></a>Декларация ELSTER для Германии (разработка на основе кодов отчетности), пункт меню и страница \"Журнал электронных налоговых деклараций\", пункт меню и страница \"Настройка электронной налоговой декларации\", формат SSRS шаблона отчета для Германии (TaxReport_DE)

[Отчет по НДС](../localizations/emea-de-vat-declaration.md)</br>
[Настройка электронной налоговой декларации для Германии](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новой структурой декларации по НДС, [Декларация по НДС для Германии](../localizations/emea-deu-vat-declaration-germany.md) |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревшие: с 1 декабря 2022 г. корпорация Майкрософт больше не будет поддерживать формат электронной отчетности **Elster (DE)** и **Модель Elster**. Новые форматы электронной отчетности **XML-документ декларации по НДС (DE)** и **Excel декларации по НДС (DE)** введены в качестве модели **Налоговая декларация**. Кроме того, мы больше не будем поддерживать пункт меню и страницу **Налог** \> **Декларации** \> **Налог** \> **Журнал электронных налоговых деклараций**, пункт меню и страницу **Налог** \> **Настройка** \> **Налог** \> **Настройка электронной налоговой декларации**, пункт меню и страницу **Налог** \> **Настройка** \> **Налог** \> **Электронные налоговые сертификаты** и формат SQL Server Reporting Services (SSRS) макета отчета для Германии (TaxReport\_DE). Процесс отчетности по НДС в Германии поддерживается в функции [Обмен электронными сообщениями](../general-ledger/electronic-messaging.md). Дополнительные сведения см. в разделе [Декларация по НДС для Германии](../localizations/emea-deu-vat-declaration-germany.md). |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes-electronic-ob-declaration-menu-item-and-page-dutch-report-layout-taxreport_nl-ssrs-format"></a>Декларация OB для Нидерландов (разработка на основе кодов отчетности), пункт меню и странице \"Электронная декларация OB\", формат SSRS шаблон отчета для Нидерландов (TaxReport_NL)

[Декларация OB](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новой структурой декларации по НДС, [Декларация по НДС для Нидерландов](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревшие: с 1 декабря 2022 г. корпорация Майкрософт больше не будет поддерживать формат электронной отчетности **Декларация OB (NL)** и **Модель декларации OB**. Новые форматы электронной отчетности **XML-документ декларации по НДС (NL)** и **Excel декларации по НДС (NL)** введены в качестве модели **Налоговая декларация**. Кроме того, мы больше не будем поддерживать пункт меню и страницу **Налог** \> **Декларации** \> **Налог** \> **Электронная декларация OB** и формат SSRS макета отчета для Нидерландов (TaxReport_NL). Процесс отчетности по НДС в Нидерландах поддерживается в функции [Обмен электронными сообщениями](../general-ledger/electronic-messaging.md). Дополнительные сведения см. в разделе [Декларация по НДС для Нидерландов](../localizations/emea-nl-vat-declaration-netherlands.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.20

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>Конфигурация формата электронной отчетности запроса данных накладных RTIR (HU)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Исключение из обработки электронных сообщений при взаимодействии с венгерской интерактивной системой выставления накладных |
| **Заменена другой функцией?**   | Нет |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: к 15 апреля 2022 года мы планируем больше не поддерживать конфигурацию формата запроса данных накладных RTIR (HU). |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>Формат электронной отчетности "Французский файл аудита FEC" для Франции в формате "Выходные данные файла аудита Германии"

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новым форматом "Файл аудита FEC (FR)" |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: с 1 мая 2022 г. корпорация Майкрософт планирует больше не поддерживать формат электронной отчетности "Французский файл аудита FEC" для Франции в формате "Выходные данные файла аудита Германии". Новый формат файла аудита FEC (FR) будет представлен в "Модель экспорта данных". |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.17

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>Хранилище LCS в качестве параметра хранения для конфигураций электронной отчетности

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новым глобальным репозиторием Regulatory Configuration Services (RCS) |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Продукты Dynamics 365 Finance, Supply Chain Management и Project Operations|
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устаревший: с 01 апреля 2022 года планируется прекратить поддержку репозитория Microsoft Dynamics Lifecycle Services (LCS) в качестве параметра хранения для конфигураций электронной отчетности (ER). Новые конфигурации Microsoft ER будут опубликованы для загрузки только из глобального репозитория. Доступ к глобальному репозиторию осуществляется из продуктов Dynamics 365 и RCS. Дополнительные сведения см. в разделе [Импорт конфигураций электронной отчетности из RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) и [Regulatory Configuration Service (RCS) — устаревание хранилища Lifecycle Services (LCS)](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.16

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>Форматы электронной отчетности "Декларация по НДС (CZ)" и "Экспорт инструкций управления (CZ)" Чешской Республики

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяются новыми форматами |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: 22 января 2022 года корпорация Майкрософт планирует больше не поддерживать форматы электронной отчетности "Декларация по НДС (CZ)", "Экспорт управляющей инструкции (CZ)". Новые форматы XML-документа декларации по НДС (CZ), Excel декларации по НДС (CZ), XML-документа управляющей инструкции по НДС (CZ) введены в качестве модели налоговой декларации. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>Формат электронной отчетности "Формат экспорта проводок книги учета (BE)" и соответствующая модель "Экспорт проводок книги учета (BE)" для Бельгии

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменено новым форматом электронной отчетности в модели "Стандартный файл аудита (SAF-T)".  |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: 1 декабря 2021 г. мы планируем больше не поддерживать формат электронной отчетности "Формат экспорта проводок книги учета (BE)" и соответствующую модель "Экспорт проводок книги учета (BE)". Новый формат "Экспорт данных главной книги (BE)" вместе с "Сопоставление модели данных главной книги" вводятся в соответствии с моделью "Стандартный файл аудита (SAF-T)". |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>Отчет "НДС 100" для Соединенного Королевства в формате SSRS

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Заменяется новым форматом электронной отчетности — формат "Декларации по НДС в Excel (UK)" в модели "Модель налоговой декларации".  |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: с 1 декабря 2021 г. планируется прекратить поддержку отчет "НДС 100" в формате SSRS. Новый формат "Декларация НДС в Excel (UK)" в модели "Модель налоговой декларации" была введена в [функции НДС MTD](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.15

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Поддержка Internet Explorer 11 для Dynamics 365 устарела

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Начиная с декабря 2020 года поддержка Microsoft Internet Explorer 11 всех продуктов Dynamics 365 устарела, и Internet Explorer 11 не будет поддерживаться после августа 2021 года.<br><br>Это повлияет на клиентов, использующих продукты Dynamics 365, которые разработаны для использования с помощью интерфейса Internet Explorer 11. После августа 2021 года Internet Explorer 11 не будет поддерживаться для подобных продуктов Dynamics 365. |
| **Заменена другой функцией?**   | Мы рекомендуем пользователям переходить на Microsoft Edge.|
| **Затрагиваемые области продукта**         | Все продукты Dynamics 365 |
| **Вариант развертывания**              | Все|
| **Состояние**                         | Устарело. Internet Explorer 11 не будет поддерживаться после августа 2021 года.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.12

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Не устарело: польские отчеты SSRS: Регистр НДС по продажам, Регистр НДС по покупкам, сводный отчет ЕС по НДС – Справочник по функциям PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Юридически не требуется.  |
| **Заменена другой функцией?**   | Да (формат Excel для стандартного файла аудита с декларацией НДС — JPK_VDEK) |
| **Затрагиваемые области продукта**         | Заявление |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Не устарело: 27 апреля 2021 г. планируется по-прежнему поддерживать отчеты SSRS: **Регистр НДС по продажам, Регистр НДС по покупкам, сводный отчет ЕС по НДС — справочник по функциям PL-00014**. Также будет представлен пример формата Excel для стандартного файла аудита с декларацией НДС (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.11

### <a name="norwegian-standard-main-accounts"></a>Норвежские стандартные счета ГК

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Перепроектирование  |
| **Заменена другой функцией?**   | Да (заменяется на параметры формата электронной отчетности, зависящие от приложения) |
| **Затрагиваемые области продукта**         | Приложение |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: с 1 апреля 2021 мы планируем больше не поддерживать функции, связанные со стандартными счетами главной книги: поле ссылки, связанная таблица, информационный объект. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Функции, удаленные или устаревшие в выпуске Finance 10.0.7

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Диалоговое окно "запрос на изменение бизнес-правила" больше не включает раскрывающийся список выбора пользователя

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Причина устаревания/удаления** | Изменение функции с выбором группы счетов.  |
| **Заменена другой функцией?**   | Да |
| **Затрагиваемые области продукта**         | Рабочий процесс |
| **Вариант развертывания**              | Все |
| **Состояние**                         | Устарело: на 1 декабря 2020 г. корпорация Майкрософт не планирует поддерживать настройку китайских типов ваучеров без выбора групп счетов. Более подробные сведения о новом дизайне можно найти в разделе [Что нового в 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Предыдущие объявления об удаленных или устаревших функциях
Для получения дополнительных сведений о функциях, которые были удалены или устарели в предыдущих выпусках, см [Удаленные или устаревшие функции в предыдущих выпусках](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

