---
title: "Conexión a VMob con Power BI"
description: VMob para Power BI
services: powerbi
documentationcenter: 
author: joeshoukry
manager: kfile
backup: maggiesMSFT
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 10/16/2017
ms.author: yshoukry
ms.openlocfilehash: fc0c8bc1ea177e20c25a614ed1de274f70056578
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/15/2017
---
# <a name="connect-to-vmob-with-power-bi"></a>Conexión a VMob con Power BI
Explorar y realizar un seguimiento de los datos de VMob es fácil con Power BI y el paquete de contenido de VMob. Power BI recuperará los datos siguientes: estadísticas del usuario de todo el tiempo y de los últimos 30 días, el KPI comercial de los últimos 30 días y el rendimiento de la campaña de los últimos 30 días.

Conéctese al [paquete de contenido de VMob](https://app.powerbi.com/getdata/services/vmob) para Power BI.

## <a name="how-to-connect"></a>Cómo conectarse
1. Seleccione **Obtener datos** en la parte inferior del panel de navegación izquierdo.
   
    ![](media/service-connect-to-vmob/getdata.png)
2. En el cuadro **Servicios** , seleccione **Obtener**.
   
   ![](media/service-connect-to-vmob/services.png)
3. Seleccione **VMob** \> **Obtener**.
   
   ![](media/service-connect-to-vmob/vmob.png)
4. Cuando se le solicite, escriba la dirección URL de VMob y haga clic en el botón Siguiente. VMob proporciona esta dirección URL por separado.
   
    ![](media/service-connect-to-vmob/params.png)
5. Elija la opción **Básico** en la lista desplegable del método de autenticación, escriba su nombre de usuario y contraseña de VMob y haga clic en el botón **Iniciar sesión** .
   
    ![](media/service-connect-to-vmob/creds.png)
6. El proceso de importación se iniciará automáticamente y Power BI recuperará los datos de VMob para crear un informe y un panel listos para usar.
   
   ![](media/service-connect-to-vmob/dashboard2.png)

**¿Qué más?**

* Pruebe a [hacer una pregunta en el cuadro de preguntas y respuestas](service-q-and-a.md), en la parte superior del panel.
* [Cambie los iconos](service-dashboard-edit-tile.md) en el panel.
* [Seleccione un icono](service-dashboard-tiles.md) para abrir el informe subyacente.
* Aunque el conjunto de datos se programará para actualizarse diariamente, puede cambiar la programación de actualización o actualizarlo a petición mediante **Actualizar ahora**.

## <a name="next-steps"></a>Pasos siguientes
[Introducción a Power BI](service-get-started.md)

[Obtener datos en Power BI](service-get-data.md)
