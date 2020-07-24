# CRUD DE MANTENIMIENTO EN PYTHON
## Script de base de dato Mysql plan_cuenta.sql
Acceso al link del Script [plan_cuenta.sql](plan_cuenta.sql)
## Instalación
Para instalar y ejecutar este proyecto tendra que ejecutar:
```bash
ejecutar el scripts de Mysql plan_cuenta.sql
```
Clonar el repositorio en Visual Studio Code abriendo Paleta de comando y escribir:
```bash
git: Clone
https://github.com/izambranod/CRUD-GUPAL-PYHTON.git
```
## Crear base de dato
```bash
-- Volcando estructura de base de datos para plan_cuenta
CREATE DATABASE IF NOT EXISTS `plan_cuenta` /*!40100 DEFAULT CHARACTER SET utf8 COLLATE utf8_spanish_ci */;
USE `plan_cuenta`;

-- Volcando estructura para tabla plan_cuenta.cuentas
CREATE TABLE IF NOT EXISTS `cuentas` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `codigo` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  `grupo` int(11) NOT NULL,
  `descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  `naturaleza` varchar(1) COLLATE utf8_spanish_ci NOT NULL,
  `estado` tinyint(1) DEFAULT 1,
  PRIMARY KEY (`id`),
  KEY `grupo` (`grupo`),
  CONSTRAINT `cuentas_ibfk_1` FOREIGN KEY (`grupo`) REFERENCES `grupo` (`id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci;

-- Volcando estructura para tabla plan_cuenta.grupo
CREATE TABLE IF NOT EXISTS `grupo` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `descripcion` varchar(50) COLLATE utf8_spanish_ci NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB AUTO_INCREMENT=25 DEFAULT CHARSET=utf8 COLLATE=utf8_spanish_ci;

```
## Integrantes
* Jose Arreaga
* William Garcia
* Israel Zambrano
