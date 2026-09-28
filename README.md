# Acme-SF — Gestión de una fábrica de software

Aplicación académica para una empresa ficticia de consultoría y desarrollo de software. Modela la gestión de proyectos, historias de usuario, contratos, seguimiento, auditorías y patrocinios, con operaciones diferenciadas por rol.

Desarrollada en equipo sobre Acme Framework, en el contexto de Diseño y Pruebas 2 de la Universidad de Sevilla.

## Explorar el proyecto

La rama predeterminada `master` contiene el código de la aplicación y el POM de la entrega D4. El repositorio conserva también la rama histórica **`(S4)-ACME-SF-D4`**.

- [Código de la aplicación](src/).
- [Informes de las entregas](reports/).
- [Rama histórica D4](https://github.com/carlosmdpb/Acme-SF/tree/%28S4%29-ACME-SF-D4).

La descripción siguiente corresponde al código disponible en `master`.

## Funcionalidades del proyecto

- Proyectos e historias de usuario.
- Contratos y registros de progreso.
- Auditorías de código y registros de auditoría.
- Formación mediante módulos y sesiones.
- Patrocinios y facturas.
- Avisos, banners, reclamaciones, riesgos y objetivos.
- Dashboards por rol y configuración del sistema.

El código organiza las operaciones según perfiles como administrador, manager, developer, client, auditor y sponsor.

## Tecnologías y arquitectura

Java, Maven y **Acme Framework 24.4.0**. La aplicación se empaqueta como WAR y hereda la configuración de `Acme:Parent-Pom:24.4.0`.

```text
src/main/java/acme/entities/  Entidades del dominio
src/main/java/acme/features/  Controladores, servicios y repositorios por rol
src/main/java/acme/roles/     Perfiles de usuario
src/main/webapp/             Recursos y vistas
src/test/                   Pruebas de la entrega
reports/                    Informes grupales e individuales
pom.xml                     Dependencias y construcción
```

Los servicios separan las operaciones de listar, mostrar, crear, actualizar y eliminar entidades. La organización por rol permite localizar cada caso de uso y sus condiciones de acceso.

## Obtener la entrega

```sh
git clone --branch master https://github.com/carlosmdpb/Acme-SF.git
cd Acme-SF
```

**No basta con clonar e invocar Maven en un entorno vacío.** El `pom.xml` depende de Acme Framework y de un POM padre externo con ruta relativa `../../pom-24.4.0.xml`, que no se distribuyen en esta rama.

Para ejecutar o construir la aplicación es necesario disponer del entorno docente Acme 24.4.0, sus artefactos y la configuración de servidor y base de datos correspondiente. Debe conservarse la estructura de carpetas prevista por ese entorno.

Los informes de `reports/` y los casos de prueba documentan las entregas. Este README no afirma que el proyecto sea ejecutable de forma independiente ni que se hayan ejecutado sus pruebas en esta revisión.

## Contexto y licencia

El trabajo se desarrolló en equipo. Los integrantes constan en `CONTRIBUTORS.txt` de la rama D4. La base Acme mantiene la atribución a Rafael Corchuelo.

La rama incluye [LICENSE.txt](LICENSE.txt) con licencia MIT para el trabajo del grupo. Los archivos de la base Acme conservan avisos propios de uso y redistribución no comercial; consultar ambos textos al compartir el proyecto y mantener sus atribuciones.
