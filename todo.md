# Sistema de Tickets de Servicio - TODO

## Base de Datos
- [x] Tabla `tickets` con campos: id, consecutivo, título, descripción, prioridad, cliente, categoría, estado, técnico asignado, fechas
- [x] Tabla `technicians` con campos: id, nombre, email, activo
- [x] Tabla `ticket_history` con campos: id, ticketId, campo cambiado, valor anterior, valor nuevo, fecha, usuario
- [x] Generar migración SQL con drizzle-kit y aplicar vía webdev_execute_sql

## Backend (tRPC)
- [x] Procedimiento: crear ticket con consecutivo automático (#0001, #0002...)
- [x] Procedimiento: listar tickets con filtros (estado, prioridad, técnico, fecha, búsqueda)
- [x] Procedimiento: obtener ticket por ID con historial
- [x] Procedimiento: asignar técnico a ticket
- [x] Procedimiento: cambiar estado de ticket
- [x] Procedimiento: listar técnicos
- [x] Procedimiento: crear técnico
- [x] Notificaciones al admin: nuevo ticket, cambio de estado, asignación

## Frontend - Layout y Diseño
- [x] Diseño elegante con paleta oscura/azul profesional
- [x] DashboardLayout con sidebar de navegación
- [x] Indicadores visuales de prioridad con colores (rojo/naranja/amarillo/verde)
- [x] Badges de estado con colores diferenciados

## Frontend - Páginas
- [x] Dashboard principal con estadísticas (total, por estado, por prioridad)
- [x] Página de lista de tickets con filtros y búsqueda
- [x] Formulario de creación de ticket
- [x] Vista detallada de ticket con historial de cambios
- [x] Panel de gestión de técnicos

## Funcionalidades
- [x] Consecutivo automático único (#0001, #0002...)
- [x] Formulario: título, descripción, prioridad, cliente, categoría
- [x] Asignación de técnico desde lista desplegable
- [x] Estados: Nuevo, Asignado, En Progreso, Resuelto, Cerrado
- [x] Filtros: número, estado, prioridad, técnico, fecha
- [x] Búsqueda por número de ticket
- [x] Historial de cambios de estado en vista detallada
- [x] Notificación email al admin en: creación, cambio de estado, asignación

## Tests
- [x] Test: creación de ticket con consecutivo automático
- [x] Test: cambio de estado con registro en historial
- [x] Test: asignación de técnico


## Roles Simplificados (Admin y Cliente)
- [x] Actualizar enum de roles en schema: solo admin y client
- [x] Eliminar procedimientos tRPC de trainer
- [x] Eliminar vista de TrainerDashboard
- [x] Actualizar navegación dinámica: Admin ve Dashboard/Tickets/Técnicos/Usuarios, Cliente ve Portal
- [x] Actualizar gestión de usuarios para solo mostrar admin y client


## Gestión de Usuarios (Admin)
- [x] Procedimiento tRPC: listar todos los usuarios con su rol actual
- [x] Procedimiento tRPC: cambiar rol de usuario (admin, client)
- [x] Página de gestión de usuarios con tabla de usuarios
- [x] Opción para cambiar rol de usuario desde interfaz
- [x] Crear tabla de clientes automáticamente al cambiar rol a client
- [x] Menú del Admin incluye opción de Usuarios


## Asignación Automática y Eliminación de Tickets
- [ ] Procedimiento tRPC: obtener técnico con menor carga de trabajo
- [ ] Procedimiento tRPC: asignar automáticamente ticket al técnico con menor carga
- [ ] Procedimiento tRPC: eliminar ticket (solo Admin)
- [ ] Actualizar formulario de creación de tickets para usar asignación automática
- [ ] Agregar botón de eliminar en lista de tickets
- [ ] Agregar botón de eliminar en vista detallada de ticket
- [ ] Confirmación antes de eliminar ticket
