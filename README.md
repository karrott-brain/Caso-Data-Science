# Prueba de Selección - Cargo Data Scientist
Uno de los clientes actuales de **Karrott**, Banco Faladeuda, le ha pedido a usted que lo ayude a descubrir quiénes serán los próximos clientes en no pagar su crédito, para ello necesitará estimar la propensión de morosidad (o sea una probabilidad), a continuación una descripción de las variables presentes en el set de datos.

- **Mora-90-02**: Variable a predecir, es un flag que indica si es que la persona tiene más de 90 días de morosidad en los últimos dos años
- **Porcentaje-Linea**: Porcentaje de saldo utilizado en línea de crédito, esto es el cupo utilizado en tarjetas y línea dividido por el cupo total en ambas.
- **Edad**
- **VecesMora30-59**: Número de veces que el cliente ha estado con más de 30 días vencida la deuda pero menos de 60 días en los últimos 2 años.
- **PorcentajeDeuda**: Razón entre gastos, pago de deudas y costo de vida con el ingreso bruto
- **Ingreso**
- **Cantidad-Creditos**: Número de créditos y tarjetas vigentes
- **PagoMora90**: Número de veces en que el cliente pagó después de 90 días
- **Cantidad-Hipotecarios**: Número de créditos hipotecarios
- **VecesMora60-89**: Cantidad de veces que el cliente ha estado atrasado entre 60 y 89 días en los últimos dos años.
- **Cargas**: Integrantes en el hogar excluyendo al cliente.

Para ello procederemos como sigue:

1. Cargue la base de datos desde la tabla Prestamos de la base de datos Empresa alojada en un servidor MySQL.
Los datos de conexión son los siguientes:
- Host: callegaridev.ceb41j4bmnqe.us-east-1.rds.amazonaws.com
- Base de datos: Empresa
- Tabla: Prestamos
- Usuario: Postulante
- Pass: Karrott2021_

2. Aparte un 30% al azar de los datos del archivo en un archivo aparte para ser utilizado como test.
3. Agregue un método que grafique densidades y las guarde en una carpeta llamada *Analisis* en la raíz de su proyecto, así como también guarde un resumen de estadísticos descriptivos (media, mediana, desviación estándar, asimetría). A partir de los resultados obtenidos ¿Qué variables requieren ser transformadas?
4. Cree un método que transforme las variables a logaritmo y aplique sobre las variables que deberían ser transformadas.
5. Ajuste un modelo de regresión logística, un random forest, un catboost y un modelo de su elección.
6. Agregue un método de evaluación(llamado evaluation), que calcule la curva ROC, así como el accuracy, recall, precisión y puntaje F1. Para el caso del accuracy, precisión y recall de la logística, calcúlelo usando como punto de corte el con mejor puntaje F1.
7. Calcule la importancia de las variables según el criterio que usted prefiera (debe explicar el elegido) ¿Qué variables son más relevantes a la hora de definir un cliente moroso? Interprete.
8. Compare los modelos y elija al que a su juicio, ajuste mejor.
9. ¿Cómo se podría aplicar esto si este modelo se ejecuta una vez al mes?

La entrega es en un Jupyter Notebook en Python o R a los correos rodrigo@karrott.cl y jorge@karrott.cl en un plazo de 48 horas recibido el correo de notificación. El tiempo de trabajo es acotado, al igual que con los clientes en la vida real, los invitamos a enviar sus respuestas aunque no estén todas las preguntas contestadas.

> **Nota**: En la carpeta data de este repositorio se pueden encontrar los datos a utilizar, sin embargo, se recomienda obtener los datos desde el servidor MySQL indicado.
