---
title: Обзор решения Invoice Capture
description: В этой статье содержится информация о решении Invoice Capture.
author: sunfzam
ms.date: 09/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: VendorInvoiceWorkspace, VendInvoiceInfoListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "13971"
- intro-internal
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: zezhangzhao
ms.search.validFrom: 2022-09-28
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76441220b93744527f412110db536601a2fa1dd9
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691209"
---
# <a name="invoice-capture-solution"></a>Решение Invoice Capture

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

В этой статье приводятся сведения о решении Invoice Capture, которое автоматически создает накладные поставщиков из изображений цифровых накладных.

Сотрудник отдела расчетов с поставщиками (AP) управляет накладными для полученных товаров и услуг и обрабатывает их. Бухгалтер отдела AP проверяет данные на накладных поставщиков по следующим причинам:

- Чтобы избежать лишних усилий, если корректировки или исправления требуются во время закрытия периода
- Чтобы своевременно оплачивать накладные поставщиков и избежать финансовых убытков из-за ошибки или мошенничества

Оптическое распознавание текста (OCR) стало широко использоваться в различных отраслях в последние годы. Напечатанные тексты обычно переводятся в цифровой формат, чтобы их можно было редактировать, искать, сохранять в более сжатом виде и отображать по сети. Цифровой текст может использоваться в компьютерных процессах, таких как когнитивные вычисления, машинный перевод, преобразование текста в речь, ключевые данные и интеллектуальный анализ текста.

Развитие технологии искусственной интеллекта (ИИ) позволило современным решениям OCR читать различные форматы накладных от разных поставщиков, не требуя значительного вмешательства человека. Большее число компаний считают, что они могут сэкономить усилия и улучшить точность путем обработки накладных с помощью автоматизации вместо выполнения обработки вручную.

## <a name="system-landscape"></a>Системный ландшафт

На следующем рисунке показаны основные компоненты и шаги решения Invoice Capture.

[![Компоненты и шаги в решении Invoice Capture.](./media/Invoice-capture2.png)](./media/Invoice-capture2.png)

## <a name="required-roles"></a>Обязательные роли

В следующей таблице показаны роли, необходимые для настройки и использования решения Invoice Capture.

| Роль          | Действия | Системы | Имена ролей |
|---------------|---------|---------|-----------|
| Администратор | <ul><li>Настройка сред в Microsoft Power Platform.</li><li>Развертывание решений в Microsoft Power Platform.</li><li>Настройка подключений между Dynamics 365 и AI Builder.</li><li>Настройка мест хранения Azure Data Lake Storage.</li></ul> | <ul><li>Dynamics 365</li><li>Microsoft Power Platform</li><li>Azure Data Lake Storage</li></ul> | <ul><li>Администратор Dynamics 365</li><li>Администратор Power Platform</li><li>Владелец данных BLOB-объектов хранилища</li></ul> |
| AI Maker      | <ul><li>Поддержка потоков.</li><li>Создание пользовательских моделей ИИ.</li></ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Непрофессиональные разработчики</li></ul> |
| Клерк AP      | <ul><li>Проверка и выполнение действий в области промежуточного хранения накладной поставщика.</li><ul> | <ul><li>Microsoft Power Platform</li></ul> | <ul><li>Новая роль клерка AP в Power Platform</li></ul> |
| Клерк AP      | <ul><li>Выполнение ежедневных операций в качестве клерка AP.</li><li>Переход в область промежуточного хранения накладных поставщика.</li></ul> | <ul><li>Dynamics 365</li></ul> | <ul><li>Сотрудник отдела расчетов с поставщиками</li></ul> |
  
Дополнительные сведения об установке Invoice Capture см. в разделе [Установка Invoice Capture](../accounts-payable/install-invoice-capture.md).  
