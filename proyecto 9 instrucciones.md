## Descripción del proyecto

Lo has hecho de maravilla en el curso de TripleTen y te han ofrecido hacer prácticas en el departamento de analítica de Showz, una empresa de venta de entradas de eventos. Tu primera tarea es ayudar a optimizar los gastos de marketing.

Cuentas con:

- registros del servidor con datos sobre las visitas a Showz desde enero de 2017 hasta diciembre de 2018;
- un archivo con los pedidos en este periodo;
- estadísticas de gastos de marketing.

Lo que vas a investigar:

- cómo los clientes usan el servicio;
- cuándo empiezan a comprar;
- cuánto dinero aporta cada cliente a la compañía;
- cuándo los ingresos cubren el costo de adquisición de los clientes.

### **Instrucciones para completar el proyecto**

**Paso 1. Acceda los datos y prepáralos para el análisis**

Almacena los datos de visitas, pedidos y gastos en variables. Optimiza los datos para el análisis. Asegúrate de que cada columna contenga el tipo de datos correcto. Rutas de archivos:

_/datasets/visits_log_us.csv [Acceda el dataset](https://code.s3.yandex.net/datasets/visits_log_us.csv)_ _/datasets/orders_log_us.csv [Acceda el dataset](https://code.s3.yandex.net/datasets/orders_log_us.csv)_ _/datasets/costs_us.csv [Acceda el dataset](https://code.s3.yandex.net/datasets/costs_us.csv)_

**Paso 2. Haz informes y calcula métricas**

1. Visitas:
    
    1. ¿Cuántas personas lo usan cada día, semana y mes?
    2. ¿Cuántas sesiones hay por día? (Un usuario puede tener más de una sesión).
    3. ¿Cuál es la duración de cada sesión?
    4. ¿Con qué frecuencia los usuarios regresan?

2. Ventas:
    
    1. ¿Cuándo empieza la gente a comprar? (En el análisis de KPI, generalmente nos interesa saber el tiempo que transcurre entre el registro y la conversión, es decir, cuando el usuario se convierte en cliente. Por ejemplo, si el registro y la primera compra ocurren el mismo día, el usuario podría caer en la categoría Conversion 0d. Si la primera compra ocurre al día siguiente, será Conversion 1d. Puedes usar cualquier enfoque que te permita comparar las conversiones de diferentes cohortes para que puedas determinar qué cohorte o canal de marketing es más efectivo.)
    2. ¿Cuántos pedidos hacen durante un período de tiempo dado?
    3. ¿Cuál es el tamaño promedio de compra?
    4. ¿Cuánto dinero traen? (LTV)
3. Marketing:
	1. ¿Cuánto dinero se gastó? (Total/por fuente de adquisición/a lo largo del tiempo) 
	2. ¿Cuál fue el costo de adquisición de clientes de cada una de las fuentes? 
	3. ¿Cuán rentables eran las inversiones? (ROMI)
    

Traza gráficos para mostrar cómo difieren estas métricas para varios dispositivos y fuentes de anuncios y cómo cambian con el tiempo.

**Paso 3. Escribe una conclusión: aconseja a los expertos de marketing cuánto dinero invertir y dónde**

¿Qué fuentes/plataformas recomendarías? Fundamenta tu selección: ¿en qué métricas te enfocaste? ¿Por qué? ¿Qué conclusiones sacaste después de encontrar los valores métricos?

**Formato:** Completa la tarea en un Jupyter Notebook. Inserta el código en las celdas _code_ y las explicaciones de texto en las celdas _markdown_. Aplica formato y encabezados.

### Descripción de los datos

La tabla `visits` (registros del servidor con datos sobre las visitas al sitio web):

- _Uid_: identificador único del usuario.
- _Device_: dispositivo del usuario.
- _Start Ts_: fecha y hora de inicio de la sesión.
- _End Ts_: fecha y hora de término de la sesión.
- _Source Id_: identificador de la fuente de anuncios de la que proviene el usuario.

Todas las fechas de esta tabla están en formato AAAA-MM-DD.

La tabla `orders` (datos sobre pedidos):

- _Uid_: identificador único del usuario que realiza un pedido.
- _Buy Ts_: fecha y hora del pedido. _Revenue_: el ingreso de Showz por el pedido.

La tabla `costs` (datos sobre gastos de marketing):

- source__id_: identificador de la fuente de anuncios.
- _dt_: fecha.
- _costs_: gastos en esta fuente de anuncios en este día.

## **¿Cómo será evaluado mi proyecto?**

Tu proyecto será evaluado según estos criterios. Léelos atentamente antes de empezar el proyecto.

Esto es lo que buscan los revisores de proyecto cuando evalúan tu proyecto:

- Cómo preparas los datos para el análisis.
- Qué gráficos trazas para las métricas.
- Cómo interpretas los gráficos resultantes.
- Cómo calculas e interpretas cada parámetro.
- Cómo fundamentas tus recomendaciones para los expertos de marketing y qué métricas utilizas.
- Si sigues la estructura del proyecto y mantienes el código ordenado.
- Las conclusiones a las que llegas.
- Si dejas comentarios en cada paso.