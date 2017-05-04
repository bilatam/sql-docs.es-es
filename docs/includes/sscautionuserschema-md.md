  El comportamiento de los esquemas cambió en SQL Server 2005. En consecuencia, el código que supone que los esquemas son equivalentes a los usuarios de base de datos puede dejar de devolver resultados correctos. Las antiguas vistas de catálogo, incluida sysobjects, no se deben usar en una base de datos en la que se haya utilizado alguna vez cualquiera de las siguientes instrucciones DDL: CREATE SCHEMA, ALTER SCHEMA, DROP SCHEMA, CREATE USER, ALTER USER, DROP USER, CREATE ROLE, ALTER ROLE, DROP ROLE, CREATE APPROLE, ALTER APPROLE, DROP APPROLE, ALTER AUTHORIZATION. En esas bases de datos, debe usar las nuevas vistas de catálogo. En las nuevas vistas de catálogo se tiene en cuenta la separación de entidades de seguridad y esquemas que se estableció en SQL Server 2005. Para obtener más información sobre las vistas de catálogo, vea [Vistas de catálogo &#40;Transact-SQL&#41;](../relational-databases/system-catalog-views/catalog-views-transact-sql.md).
   