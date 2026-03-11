# 💱 Conversor de Monedas — Challenge ONE

Aplicación de consola en Java que permite convertir entre distintas monedas utilizando tasas de cambio en tiempo real obtenidas desde la [ExchangeRate-API](https://www.exchangerate-api.com/).

---

## 📋 Descripción

Este proyecto fue desarrollado como parte del Challenge del programa **Oracle Next Education (ONE)** junto a **Alura Latam**. El usuario puede seleccionar pares de monedas desde un menú interactivo, ingresar el monto a convertir y obtener el resultado actualizado al instante.

---

## ✨ Funcionalidades

- Menú interactivo en consola con 6 opciones de conversión
- Consulta de tasas de cambio en tiempo real mediante API REST
- Soporte para las siguientes monedas:
  - 🇺🇸 Dólar estadounidense (USD)
  - 🇦🇷 Peso argentino (ARS)
  - 🇧🇷 Real brasileño (BRL)
  - 🇨🇴 Peso colombiano (COP)
- Manejo de errores en entrada del usuario y en la conexión a la API
- Bucle de repetición hasta que el usuario elija salir

---

## 🛠️ Tecnologías utilizadas

| Tecnología | Versión |
|---|---|
| Java JDK | 17+ |
| Gson (Google) | 2.10.1+ |
| ExchangeRate-API | v6 |
| HttpClient (java.net.http) | Nativo Java 11+ |

---

## 📁 Estructura del proyecto

```
ConversorMonedas/
├── src/
│   └── Main.java
├── lib/
│   └── gson-2.10.1.jar
└── README.md
```

---

## ⚙️ Configuración y ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/tu-usuario/conversor-monedas.git
cd conversor-monedas
```

### 2. Obtener tu clave de API

1. Crear una cuenta en [ExchangeRate-API](https://www.exchangerate-api.com/)
2. Copiar la clave generada
3. En `src/Main.java`, reemplazar:

```java
private static final String API_KEY = "TU_CLAVE_API_AQUI";
```

### 3. Agregar la dependencia Gson

Descargar `gson-2.10.1.jar` desde [Maven Central](https://central.sonatype.com/artifact/com.google.code.gson/gson) y colocarlo en la carpeta `lib/`.

### 4. Compilar

```bash
javac -cp lib/gson-2.10.1.jar src/Main.java -d out/
```

### 5. Ejecutar

```bash
java -cp out:lib/gson-2.10.1.jar Main
```

> En Windows usar `;` en lugar de `:` como separador del classpath.

---

## 🖥️ Ejemplo de uso

```
*******************************************
  Sea bienvenido/a al Conversor de Monedas
*******************************************

Seleccione una opción de conversión:
1) Dólar (USD) => Peso argentino (ARS)
2) Peso argentino (ARS) => Dólar (USD)
3) Dólar (USD) => Real brasileño (BRL)
4) Real brasileño (BRL) => Dólar (USD)
5) Dólar (USD) => Peso colombiano (COP)
6) Peso colombiano (COP) => Dólar (USD)
7) Salir
Elija una opción válida: 3
Ingrese el valor a convertir: 100
100.00 USD equivale a 497.35 BRL
```

---

## 🔗 API utilizada

**ExchangeRate-API v6** — endpoint de consulta por pares:

```
https://v6.exchangerate-api.com/v6/{API_KEY}/pair/{MONEDA_ORIGEN}/{MONEDA_DESTINO}
```

Documentación completa: [https://www.exchangerate-api.com/docs/java-currency-api](https://www.exchangerate-api.com/docs/java-currency-api)

---

## 👨‍💻 Autor

Desarrollado como parte del **Challenge Oracle Next Education — Alura Latam**.

---

## 📄 Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
