# Reto2_POO
### Katherine Restrepo
Elija un problema de la vida real (sistema de gestion de biblioteca, negocio de compra-venta, automovil, etc) que se pueda modelar a traves de objetos y clases. Plantee las relaciones de clases, composiciones, propiedades y comportamientos del sistema en uno mas diagramas tipo UML.

```mermaid
classDiagram
        Cliente -- Reserva : hace
        Cliente -- Pago: hace
        Reserva <|-- Lugar
        Reserva <|-- Servicio
        Reserva <|-- Pago
        Cliente: -str nombre
        Cliente: -int numero_cc
        Cliente: -str correo
        Cliente: -int telefono
        Cliente: -hacer_reserva()
        Cliente: -cancelar_reserva()
        Cliente: -corregir_datos()
        Reserva : -int numero_reservacion
        Reserva : -Date Fecha
        Reserva : -Time Hora inicio
        Reserva : -Time Hora fin
        Reserva: -confirmar_reserva()
        Reserva: -cancelar_reserva()
        Reserva: -modificar_datos_reserva()
        class Lugar {
          +str nombre
          +str direccion
          +bool esta_disponible
          +int precio
          +int capacidad
          +marcar_ocupado()
          +marcar_desocupado()
        }
        class Servicio {
          -str tipo
          -str proveedor
          -int costo
        }
        class Pago {
          +str metodo_pago
          -int monto_pago
          -str fecha_pago
          +registrar_pago()
        }
```