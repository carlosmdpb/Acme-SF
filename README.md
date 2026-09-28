# Acme-SF — Gestión de una fábrica de software

Aplicación académica para una empresa ficticia de consultoría y desarrollo de software. Modela la gestión de proyectos, historias de usuario, contratos, seguimiento, auditorías y patrocinios, con operaciones diferenciadas por rol.

Desarrollada en equipo sobre Acme Framework, en el contexto de Diseño y Pruebas 2 de la Universidad de Sevilla.

## Explorar el proyecto

La rama predeterminada `master` contiene el código de la aplicación y el POM de la entrega D4. El repositorio conserva también la rama histórica **`(S4)-ACME-SF-D4`**.

- [Código de la aplicación](src/).
- [Informes de las entregas](reports/).
- [Rama histórica D4](https://github.com/carlosmdpb/Acme-SF/tree/%28S4%29-ACME-SF-D4).

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

La aplicación utiliza el entorno docente Acme 24.4.0. Su configuración de construcción se define en `pom.xml`, con el POM padre ubicado en `../../pom-24.4.0.xml`.

Los [informes](reports/) incluyen documentación de análisis, planificación, diseño y pruebas de las entregas.

## Contexto y licencia

El trabajo se desarrolló en equipo. Los integrantes constan en [CONTRIBUTORS.txt](CONTRIBUTORS.txt). La base Acme mantiene la atribución a Rafael Corchuelo.

[MIT](LICENSE.txt) para el trabajo del grupo. La base Acme conserva sus avisos de autoría y licencia.
