---
title: "Incorporación de una columna de un ejemplo en Power BI Desktop"
description: "Creación rápida de una columna en Power BI Desktop usando como ejemplos las que ya existen"
services: powerbi
documentationcenter: 
author: davidiseminger
manager: kfile
backup: 
editor: 
tags: 
qualityfocus: no
qualitydate: 
ms.service: powerbi
ms.devlang: NA
ms.topic: article
ms.tgt_pltfrm: NA
ms.workload: powerbi
ms.date: 09/06/2017
ms.author: davidi
ms.openlocfilehash: b425e7ea2cffeff31cc8cf49330ca3835d92165c
ms.sourcegitcommit: 284b09d579d601e754a05fba2a4025723724f8eb
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 11/15/2017
---
# <a name="add-a-column-from-an-example-in-power-bi-desktop"></a>Incorporación de una columna de un ejemplo en Power BI Desktop
A partir de la versión de abril de 2017 de **Power BI Desktop**, puede agregar nuevas columnas de datos al modelo mediante el **Editor de consultas** simplemente proporcionando uno o varios valores de ejemplo para la nueva columna. Puede crear un ejemplo de columna a partir de una selección actual, o bien proporcionando datos de todas las columnas (o las seleccionadas) de una tabla determinada.

![](media/desktop-add-column-from-example/add-column-from-example_01.png)

Este enfoque ayuda a crear columnas de forma sencilla y rápida, y es muy útil para las situaciones siguientes:

* Conoce el resultado de datos que desea en la nueva columna, pero no está seguro de qué transformación (o colección de transformaciones) le ayudará a conseguirlo.
* Ya sabe qué transformaciones necesita, pero no sabe dónde hacer clic o qué seleccionar en la interfaz de usuario para que se realicen.
* Sabe todas las transformaciones que necesita usando una expresión *Columna personalizada* en **M**, pero una (o varias) de esas expresiones no están disponibles para hacer clic en ellas o agregarlas en la interfaz de usuario.

Con la característica **Agregar columna a partir de los ejemplos** es muy sencillo. En las siguientes secciones, veremos lo fácil que es.

## <a name="use-query-editor-to-add-a-new-column-from-examples"></a>Uso del Editor de consultas para agregar una nueva columna a partir de los ejemplos
Para crear una columna de un ejemplo, inicie el **Editor de consultas**. También puede hacerlo seleccionando la opción **Editar consultas** de la cinta de opciones **Inicio** de **Power BI Desktop**.

![](media/desktop-add-column-from-example/add-column-from-example_02.png)

En este artículo, vamos a usar datos procedentes del siguiente artículo de Wikipedia (que es un vínculo, por lo que puede hacer clic en él para obtener los datos y continuar):

* [**Lista de estados y territorios de los Estados Unidos**](https://wikipedia.org/wiki/List_of_states_and_territories_of_the_United_States)

Cuando se inicie el **Editor de consultas** y tenga algunos datos cargados, puede empezar a agregar una columna a partir de los ejemplos. Para agregar una nueva columna, en el **Editor de consultas** seleccione la pestaña **Agregar columna** de la cinta de opciones y seleccione **Columna a partir de los ejemplos**. Si elige la lista desplegable, puede seleccionar **A partir de todas las columnas** (el valor predeterminado si solo selecciona el botón en lugar de la lista desplegable) o **A partir de la selección**. En este artículo, usaremos **A partir de todas las columnas**.

![](media/desktop-add-column-from-example/add-column-from-example_03.png)

## <a name="the-add-column-from-examples-pane"></a>El panel Agregar columna a partir de los ejemplos
Una vez que realice una selección para agregar una nueva columna a partir de los ejemplos, aparece un nuevo panel que muestra las columnas de la tabla actual (puede que tenga que desplazarse para verlas todas). **Column1** también se muestra a la derecha, que es la columna que **Power BI Desktop** creará en función de los ejemplos. Después, en el nuevo encabezado **Column1** hay celdas en blanco, donde puede escribir los ejemplos que Power BI usa para crear reglas y transformaciones que coincidan con el ejemplo.

Observe también que se trata de un **paso aplicado** en el panel **Configuración de la consulta**. Como siempre, el **Editor de consultas** registrará los pasos de transformación y los aplicará a la consulta, en orden.

![](media/desktop-add-column-from-example/add-column-from-example_04.png)

Se trata de un panel llamado **Agregar columna a partir de los ejemplos** y consta de cuatro áreas principales:

1. La **barra de comandos** que incluye una breve descripción de la característica o la transformación.
2. La opción **Enviar comentarios** para ayudar a Power BI a mejorar esta característica.
3. Los botones **Aceptar** y **Cancelar**, que permiten confirmar las transformaciones y agregar la columna, o cancelar.
4. El área de la nueva columna, donde puede escribir los valores de ejemplo en cualquiera de las filas (para proporcionar a Power BI el ejemplo), con relación a otras columnas de esa fila.

![](media/desktop-add-column-from-example/add-column-from-example_05.png)

Cuando escribe el ejemplo en la nueva columna, Power BI ofrecerá una vista previa de cómo se mostrará la columna que está creando, en función de las transformaciones que detecte. Por ejemplo, escribimos *Alabama* en la primera fila correspondiente al valor *Alabama* de la primera columna de la tabla. En cuanto presionamos la tecla *Entrar*, Power BI rellena la columna basándose en ese valor.

No obstante, luego fuimos a la fila que incluía *Massachusetts [E]* y eliminamos esa última parte *[E]* (porque no la queríamos). Power BI detectó un cambio y utilizó el ejemplo para crear una transformación. Observe la explicación de la transformación en el panel superior central.

![](media/desktop-add-column-from-example/add-column-from-example_06.png)

A medida que siga proporcionando ejemplos, el **Editor de consultas** agregará a las transformaciones. Cuando esté satisfecho con los resultados, puede seleccionar **Aceptar** para confirmar los cambios.

## <a name="see-add-column-from-examples-in-action"></a>El panel Agregar columna a partir de los ejemplos en acción
¿Desea ver este trabajo? En el vídeo siguiente se muestra cómo funciona esta característica usando el origen de datos proporcionado anteriormente en este ejemplo. Échele un vistazo y luego siga usted.

<iframe width="560" height="315" src="https://www.youtube.com/embed/-ykbVW9wQfw" frameborder="0" allowfullscreen></iframe>

## <a name="considerations-and-limitations"></a>Consideraciones y limitaciones
Hay muchas transformaciones que están disponibles al utilizar **Agregar columna a partir de los ejemplos**, pero no se incluyen todas las transformaciones. En la siguiente lista se proporcionan todas las transformaciones que *se admiten*.

* **Referencia**
  
  * La referencia a una columna concreta [lo que incluye el recorte la limpieza (a fecha de junio de 2017) y las transformaciones de mayúsculas)]
* **Transformaciones de texto**
  
  * Combinar (admite la combinación de cadenas literales y valores de columnas enteras)
  * Sustituir
  * Longitud
  * Extraer
    
    * Primeros caracteres
    * Últimos caracteres
    * Intervalo
    * Texto antes del delimitador
    * Texto después del delimitador
    * Texto entre delimitadores
  * Las siguientes **transformaciones de texto** admitidas están disponibles a partir de la versión de **Power BI Desktop** de junio de 2017:
    
    * Longitud

> [!NOTE]
> Todas las transformaciones de *texto* tienen en cuenta la posible necesidad de recortar, limpiar (a fecha de junio de 2017) o aplicar una transformación de mayúsculas en el valor de columna.
> 
> 

* **Transformaciones de fecha**
  
  * Día
  * Día de la semana
  * Nombre de día de la semana
  * Día del año
  * Mes
  * Nombre del mes
  * Trimestre del año
  * Semana del mes
  * Semana del año
  * Año
* Las siguientes **transformaciones de fechas** adicionales admitidas están disponibles a partir de la versión de **Power BI Desktop** de junio de 2017:
  
  * Antigüedad
  * Inicio del año
  * Final del año
  * Inicio del mes
  * Final del mes
  * Inicio del trimestre
  * Días del mes
  * Final del trimestre
  * Inicio de la semana
  * Final de la semana
  * Día del mes
  * Inicio del día
  * Final del día
* **Transformaciones de tiempo**
  
  * Hora
  * Minuto
  * Segundo
* **Transformaciones de fecha, hora y zona horaria**: las siguientes transformaciones admitidas están disponibles a partir de la versión de **Power BI Desktop** de julio de 2017:
  
  * A la hora local

> [!NOTE]
> Todas las transformaciones de *fecha* y *tiempo* tienen en cuenta la posible necesidad de convertir el valor de columna a *Date*, *Time* o *DateTime*.
> 
> 

* **Transformaciones de números**: las siguientes transformaciones admitidas están disponibles a partir de la versión de **Power BI Desktop** de julio de 2017:
  * Valor absoluto
  * Arcocoseno
  * Arcoseno
  * Arcotangente
  * Convertir en número
  * Coseno
  * Cubo
  * Dividir
  * Exponente
  * Factorial
  * División de entero
  * Es par
  * Es impar
  * Lín
  * Logaritmo en base 10
  * Módulo
  * Multiplicar
  * Redondear a la baja
  * Redondear al alza
  * Signo
  * Seno
  * Raíz cuadrada
  * Cuadrado
  * Restar
  * Sumar
  * Tangente
