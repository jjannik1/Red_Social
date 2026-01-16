# A. Historias de Usuario Técnicas  
**Proyecto: Red Social**

---

## HU-001: Registro de usuario
**Como:** Visitante  
**Quiero:** Registrarme en la plataforma  
**Para:** Poder acceder a todas las funcionalidades de la red social  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `submit` en formulario `#form-registro`  
- **Objetos involucrados:**  
  - Instancia de `AuthService`  
  - Objeto `Usuario`  
- **Resultado en el DOM:**  
  - Se muestra mensaje de registro correcto  
  - Redirección a la vista de inicio de sesión  
  - Se limpian los campos del formulario  

---

## HU-002: Inicio de sesión
**Como:** Usuario registrado  
**Quiero:** Iniciar sesión  
**Para:** Acceder a mi feed personalizado  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `submit` en formulario `#form-login`  
- **Objetos involucrados:**  
  - Instancia de `AuthService`  
  - Objeto `Usuario`  
- **Resultado en el DOM:**  
  - Se oculta la vista de login  
  - Se renderiza la vista Home con el feed  
  - Se actualiza el header con el nombre del usuario  

---

## HU-003: Ver contenido público
**Como:** Visitante  
**Quiero:** Ver publicaciones públicas  
**Para:** Explorar contenido sin registrarme  

**Detalle Técnico DWEC:**  
- **Evento disparador:** Carga de la vista principal  
- **Objetos involucrados:**  
  - Instancia de `PostService`  
- **Resultado en el DOM:**  
  - Se renderiza una lista de publicaciones públicas  
  - Cada publicación se muestra en un componente `PostCard`  

---

## HU-004: Crear publicación
**Como:** Usuario registrado  
**Quiero:** Crear una publicación  
**Para:** Compartir contenido con otros usuarios  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `submit` en formulario `#form-post`  
- **Objetos involucrados:**  
  - Instancia de `PostService`  
  - Objeto `Post`  
- **Resultado en el DOM:**  
  - Se añade la nueva publicación al inicio del feed  
  - Se limpia el formulario  
  - Se muestra un mensaje de confirmación  

---

## HU-005: Eliminar publicación propia
**Como:** Usuario registrado  
**Quiero:** Eliminar una publicación mía  
**Para:** Gestionar mi contenido  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `click` en botón `.btn-eliminar-post`  
- **Objetos involucrados:**  
  - Instancia de `PostService`  
- **Resultado en el DOM:**  
  - Se elimina el elemento HTML del post  
  - Se muestra notificación de eliminación correcta  

---

## HU-006: Dar like a una publicación
**Como:** Usuario registrado  
**Quiero:** Dar like a una publicación  
**Para:** Mostrar que me gusta ese contenido  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `click` en botón `.btn-like`  
- **Objetos involucrados:**  
  - Instancia de `PostService`  
- **Resultado en el DOM:**  
  - Se incrementa el contador de likes  
  - Se cambia el estado visual del botón (activo)  

---

## HU-007: Comentar publicación
**Como:** Usuario registrado  
**Quiero:** Escribir un comentario  
**Para:** Interactuar con otros usuarios  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `submit` en formulario `.form-comentario`  
- **Objetos involucrados:**  
  - Instancia de `CommentService`  
  - Objeto `Comentario`  
- **Resultado en el DOM:**  
  - Se añade el comentario debajo del post  
  - Se limpia el input del comentario  

---

## HU-008: Seguir usuario
**Como:** Usuario registrado  
**Quiero:** Seguir a otro usuario  
**Para:** Ver su contenido en mi feed  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `click` en botón `#btn-seguir`  
- **Objetos involucrados:**  
  - Instancia de `UserService`  
- **Resultado en el DOM:**  
  - El botón cambia a “Siguiendo”  
  - Se actualiza el contador de seguidores  

---

## HU-009: Editar perfil
**Como:** Usuario registrado  
**Quiero:** Editar mi perfil  
**Para:** Actualizar mis datos personales  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `submit` en formulario `#form-editar-perfil`  
- **Objetos involucrados:**  
  - Instancia de `UserService`  
  - Objeto `Usuario`  
- **Resultado en el DOM:**  
  - Se actualizan los datos visibles del perfil  
  - Se muestra mensaje de guardado correcto  

---

## HU-010: Bloquear / Desbloquear usuario
**Como:** Administrador  
**Quiero:** Bloquear o desbloquear un usuario  
**Para:** Mantener el control y la seguridad del sistema  

**Detalle Técnico DWEC:**  
- **Evento disparador:** `click` en botón `.btn-bloquear-usuario`  
- **Objetos involucrados:**  
  - Instancia de `AdminService`  
- **Resultado en el DOM:**  
  - Se actualiza el estado del usuario en la lista  
  - Se muestra aviso de acción realizada  

---
