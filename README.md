# CHIC BROWS · Demo del sistema de gestión

Demo navegable del sistema de gestión de **CHIC BROWS**, estudio de cejas y pestañas en Cuenca (Av. Fray Vicente Solano y Gonzalo Cordero Dávila). Todo corre en una sola página `index.html` con CSS y JavaScript inline: no hay backend, base de datos ni dependencias más allá de Google Fonts.

## Qué incluye

- **Entrada simulada**: usuario demo precargado y botón «Entrar en modo demostración».
- **Escritorio**: turnos del día, ocupación de las cuatro profesionales, ingresos, próximas clientas y avisos (WhatsApp sin responder, citas por confirmar, retoques que vencen, por cobrar).
- **Agenda**: vista de día por profesional con bloques cuyo ancho y alto corresponden a la duración real del servicio (30 min a 2 h 30), vista de semana por profesional y detalle de cada turno. «Nueva cita» agrega el turno a la agenda y avisa si se cruza con otro de la misma profesional.
- **Mensajes / WhatsApp**: bandeja compartida con un agente de IA que responde precios, horarios y disponibilidad, toma reservas, envía recordatorios y pasa la conversación a una persona. Incluye la cola «Requiere una persona» y el flujo consulta → reserva confirmada → recordatorio 24 h antes.
- **Clientas**: buscador, ficha con contacto, historial por fecha y profesional, ficha técnica de cejas y pestañas (tipo de piel, medidas, tinturas, adhesivo, notas y fotos simuladas), packs de sesiones y próximo retoque con vencimiento.
- **Caja**: cobros del día y del mes, medios de pago (efectivo, transferencia, tarjeta) y estado de cada movimiento.
- **Informes**: turnos por semana, servicios más pedidos, ingresos por mes, ocupación por profesional y confirmadas vs. canceladas, todo con SVG y CSS.
- **Ajustes**: catálogo de servicios con precio y duración en minutos, profesionales y horarios, recordatorios (horas antes del turno y semanas para el retoque).

## Datos de ejemplo

Se generan en el navegador en relación con la fecha en que se abre el demo: 40 clientas de Cuenca, más de 90 turnos del mes, 6 packs, 4 profesionales (Karla, Doménica, Anahí y Andrea) y 8 fichas técnicas. No se envía ningún mensaje ni se guarda nada fuera de la pantalla.

## Uso local

```bash
docker build -t chicbrows-demo .
docker run -p 8080:80 chicbrows-demo
# abrir http://localhost:8080
```

También se puede abrir `index.html` directamente en el navegador.

## Demo publicada

- Sistema: https://clientes-sistema-chicbrows.rddxeh.easypanel.host/
- Web pública de referencia (menú «Ver la web pública»): https://clientes-demo-chicbrows.rddxeh.easypanel.host/

---

Demo de referencia hecho por Nocodeveloper. Los datos son de ejemplo; en el sistema real se cargan los del estudio.