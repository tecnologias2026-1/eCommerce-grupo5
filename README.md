Para Completar por grupo

🌐 Kiddo Finance – Plataforma Web de Educación Financiera para Niños

Kiddo Finance es una plataforma web educativa que permite a los niños aprender a administrar el dinero mediante un monedero virtual, registro de ingresos y gastos, y metas de ahorro. El sistema utiliza elementos visuales e interactivos para enseñar hábitos financieros básicos de forma sencilla, segura y divertida

👥 Integrantes

Maria Paula Suarez Bastias – 1202689
Paula Katalina Daza Fuentes – 1202701

🎯 1. Objetivo General

Desarrollar una plataforma web educativa que permita a los niños aprender a administrar el dinero mediante el uso de un monedero virtual y metas de ahorro, con el fin de fomentar hábitos financieros responsables desde temprana edad. El sistema busca solucionar la falta de herramientas educativas interactivas que enseñen a los niños conceptos básicos como el ahorro, el control de gastos y la organización del dinero de forma segura y fácil de entender.

🌍 2. Contexto de Uso

¿Quién va a usar el sistema?

- Niños entre 8 y 12 años (usuario principal)
- Padre o madre (responsable del registro)

¿Cómo se va a utilizar el sistema?

El sistema se utilizará desde un computador, tablet o celular con acceso a internet. El padre o madre registrará la cuenta del niño, y el niño podrá ingresar al sistema para registrar dinero, ver su saldo, crear metas de ahorro y visualizar su progreso de forma interactiva.

📋 3. Requerimientos del Sistema
3.1 Requerimientos Funcionales

RF01: El sistema debe permitir registrar usuarios.
RF02: El sistema debe permitir iniciar sesión.
RF03: El sistema debe permitir crear el perfil del niño.
RF04: El sistema debe permitir registrar ingresos de dinero.
RF05: El sistema debe permitir registrar gastos de dinero.
RF06: El sistema debe mostrar el saldo actual del usuario.
RF07: El sistema debe permitir crear metas de ahorro.
RF08: El sistema debe mostrar el progreso de las metas de ahorro.
RF09: El sistema debe mostrar el historial de movimientos.
RF10: El sistema debe mostrar recompensas o logros obtenidos.

3.2 Requerimientos No Funcionales

RNF01: La página debe ser responsive y funcionar en celular, tablet y computador.
RNF02: La interfaz debe ser amigable y fácil de usar para niños.
RNF03: El sistema debe cargar rápidamente.
RNF04: El sistema debe proteger la información del usuario.
RNF05: El sistema debe tener una interfaz visual con iconos y colores amigables.

🧠 4. Diagramas UML

Diagrama de Casos de Uso

Este diagrama muestra las interacciones entre el usuario (niño o padre/madre) y el sistema. Permite visualizar las principales funciones del sistema, como registrarse, iniciar sesión, registrar ingresos y gastos, crear metas de ahorro y ver el progreso financiero.

Diagrama de Secuencia

Este diagrama muestra el proceso que ocurre cuando el usuario registra un ingreso o gasto. Representa la interacción entre el usuario, la interfaz web y la base de datos, mostrando cómo se guarda la información y se actualiza el saldo.

🎨 5. URL del Prototipo

Colocar aquí el enlace público de Figma:
https://www.figma.com/make/hnhFjeeFNXSH2zgtuYpCka/Colorful-Kids-Finance-Page?t=15g4YsdyFJH8shao-1

🗄️ 6. Diseño de Base de Datos

<img width="1291" height="821" alt="image" src="https://github.com/user-attachments/assets/46b28d79-cd3a-47f9-9590-0a3a726ae7d5" />

Tablas principales
1. Tabla: Role (enum)
Qué es: Define los tipos de usuario del sistema.
Campos:
id: identificador único
email: correo del usuario
role: tipo de usuario
Valores posibles:
KID → Niño

2. Tabla: User
Qué es: Guarda la información de la cuenta del usuario.
Campos:
id: identificador único del usuario
email: correo electrónico
role: tipo de usuario
Función:
Permite que el usuario pueda registrarse e iniciar sesión.

3. Tabla: KidProfile
Qué es: Guarda la información del perfil del niño.
Campos:
id: identificador del perfil
email: correo asociado
role: tipo de usuario
Función:
Representa al niño dentro del sistema.

4. Tabla: WalletEntry
Qué es: Guarda todos los movimientos de dinero del niño.
Campos:
id: identificador del movimiento
kidprofile: referencia al niño
transactionType: tipo (ingreso o gasto)
amount: cantidad de dinero

5. Tabla: TransactionType
Qué es: Define el tipo de movimiento.
Tipos:
income → ingreso
expense → gasto

6. Tabla: SavingGoal
Qué es: Guarda las metas de ahorro del niño.
Campos:
id: identificador de la meta
kidprofile: niño
title: nombre de la meta
targetAmount: cantidad objetivo
dueDate: fecha límite

7. Tabla: Badge
Qué es: Guarda las recompensas o logros.
Campos:
id: identificador
name: nombre de la recompensa

8. Relación entre las tablas (cómo se conectan)
Relación principal:
- User
↓
KidProfile
↓
WalletEntry
↓
TransactionType

- KidProfile
↓
SavingGoal

- KidProfile
↓
Badge

🧩 7. Documentación del Sistema
Estructura de Carpetas

/css
Contiene los archivos de estilos de la página, como colores, diseño, botones y estructura visual.
/js
Contiene los archivos JavaScript que controlan la lógica del sistema, como registro, cálculo de saldo y manejo de datos.
/assets
Contiene imágenes, iconos y recursos gráficos utilizados en la interfaz.

Explicar brevemente qué contiene cada carpeta.

🚀 8. Instalación y Ejecución

Pasos para ejecutar el proyecto:
1. Descargar o clonar el proyecto desde el repositorio.
2. Abrir la carpeta del proyecto.
3. Abrir el archivo index.html en un navegador web.
4. Si el sistema utiliza base de datos, configurar la conexión en el archivo correspondiente.
5. Ejecutar el proyecto en el navegador.
