# Servidor de Scraping y API de Criptomonedas

Este repositorio contiene un servidor escrito en Go que realiza scraping de datos de criptomonedas desde Binance y ofrece una API para consultar estos datos categorizados.

## Funcionalidades Implementadas

- **Scraping Automático**: Utiliza Colly para extraer información actualizada de criptomonedas desde [Binance Markets](https://www.binance.com/es/markets/trading_data/rankings).
- **Categorización de Datos**: Agrupa los resultados en categorías como Populares, Ganadores, Perdedores y Mayor Volumen.
- **Servidor API**: Implementa un servidor HTTP que sirve los resultados categorizados como respuestas JSON.
- **Descarga de Imágenes**: Descarga y almacena localmente las imágenes de las criptomonedas para su uso en la API.

## Configuración y Uso

1. **Instalación de Dependencias**:
   - Asegúrate de tener Go instalado en tu sistema.
   - Instala las dependencias usando:
     ```bash
     go get -u github.com/gin-gonic/gin
     go get -u github.com/gocolly/colly/v2
     ```

2. **Ejecución del Servidor**:
   - Ejecuta el servidor Go:
     ```bash
     go run main.go
     ```
   - El servidor estará disponible en `http://localhost:8080`.

3. **Consulta de Datos**:
   - Puedes acceder a los datos categorizados visitando las siguientes rutas:
     - `/`: Devuelve los datos categorizados como JSON.
     - `/images`: Sirve las imágenes descargadas de las criptomonedas.

## Ejemplo de Respuesta JSON

```json
{
  "Populares": [],
  "Ganadores": [],
  "Perdedores": [],
  "MayorVolumen": []
}
```
