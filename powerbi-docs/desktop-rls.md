---
title: Restricción del acceso a datos con seguridad de nivel de fila (RLS) en Power BI Desktop
description: Cómo configurar la seguridad de nivel de fila para conjuntos de datos importados, y DirectQuery, en Power BI Desktop.
author: davidiseminger
ms.author: davidi
ms.reviewer: ''
ms.service: powerbi
ms.subservice: powerbi-desktop
ms.topic: conceptual
ms.custom: ''
ms.date: 01/31/2020
LocalizationGroup: Create reports
ms.openlocfilehash: 7a9aa0ca62ae4f1008d4cf47caa909841f9ec495
ms.sourcegitcommit: cde65bb8b1bed1ee8cf512651afeb829ddc155de
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "77464472"
---
# <a name="restrict-data-access-with-row-level-security-rls-for-power-bi-desktop"></a>Restricción del acceso a datos con seguridad de nivel de fila (RLS) en Power BI Desktop

Puede usar la seguridad de nivel de fila (RLS) con Power BI Desktop para restringir el acceso a los datos a determinados usuarios. Los filtros restringen los datos en el nivel de fila. Puede definir filtros en roles.

Ahora puede configurar RLS para los modelos de datos que se han importado en Power BI con Power BI Desktop. También puede configurar RLS en conjuntos de datos en los que se usa [DirectQuery](desktop-use-directquery.md), como SQL Server. Anteriormente, solo podía implementar RLS en modelos locales de Analysis Services fuera de Power BI. Para las conexiones activas de Analysis Services, la seguridad de nivel de fila se configura en el modelo local. La opción de seguridad no se muestra para conjuntos de datos de conexión dinámica.

> [!IMPORTANT]
> Si ha definido roles y reglas dentro del servicio Power BI, tiene que volver a crear esos roles dentro de Power BI Desktop y publicar el informe en el servicio. Obtenga más información sobre las opciones de [RLS dentro del servicio Power BI](service-admin-rls.md).

[!INCLUDE [include-short-name](./includes/rls-desktop-define-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-desktop-view-as-roles.md)]

[!INCLUDE [include-short-name](./includes/rls-limitations.md)]

[!INCLUDE [include-short-name](./includes/rls-faq.md)]

## <a name="next-steps"></a>Pasos siguientes

[Seguridad de nivel de fila (RLS) con el servicio Power BI](service-admin-rls.md)  

¿Tiene más preguntas? [Pruebe a preguntar a la comunidad de Power BI](https://community.powerbi.com/).