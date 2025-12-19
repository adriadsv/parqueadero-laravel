# ParkingExpress - Parqueadero del Centro (CRUD Laravel)

## Objetivo
Desarrollar un CRUD completo en Laravel aplicando arquitectura MVC, como preparación para el examen práctico.

## Caso
**Sistema:** ParkingExpress - Parqueadero del Centro  
**Usuario:** Don Ramiro (administrador del parqueadero)

## Requisitos funcionales cumplidos
- Registrar vehículo con: **placa**, **tipo**, **propietario (opcional)**, **observaciones**
- Fecha/hora de ingreso automática
- Ver listado de vehículos
- Editar un registro
- Eliminar un registro (política elegida: **eliminación física**)
- Interfaz usable en móvil (Bootstrap 5)

## Decisiones de diseño
### Política de eliminación
Se implementó **eliminación física (DELETE)** para simplificar el flujo de uso del administrador (Don Ramiro), ya que en el enunciado se indica que él normalmente “borra el registro cuando el carro se va”, aunque se menciona como alternativa marcar salida.

### Base de datos
- Motor: **MySQL**
- Tabla principal: **vehiculos**
- Campos:
  - `placa` (string, 10)
  - `tipo` (string, 20)
  - `propietario` (string, 100, nullable)
  - `observaciones` (text, nullable)
  - `created_at` y `updated_at` (timestamps)

### Interfaz
- Se usó **Bootstrap 5** por CDN para asegurar una interfaz rápida, limpia y responsive (usable desde celular).

## Capturas requeridas (mínimo 3)
Incluye en tu entrega capturas de:
1. Listado de vehículos
2. Formulario de creación
3. Vista móvil (modo responsive)

## Cómo ejecutar el proyecto (local)
### Requisitos
- PHP 8+
- Composer
- MySQL
- Laravel Herd (o servidor local equivalente)

### Pasos
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/adriadsv/parqueadero-laravel.git
   cd parqueadero-laravel
