flyway_howto
============

The latest version of Flyway
http://flywaydb.org/getstarted/download.html


Getting Started
①settings
edit settingfile [ /conf/flyway.properties]
	required setting is ...
		flyway.url(Jdbc url to use to connect to the database)
		flyway.user(User to use to connect to the database)
		flyway.password(Password to use to connect to the database)

②initialize database
	enter [ flyway init ]
	the table [ schema_version ] is created.
		migration infomations are saved in this table.

Migrate database
①add sql files
	add sql files to [ /sql ] directory.
	There are some nameing rules.
		please check [ http://flywaydb.org/documentation/migration/sql.html ]

②migrate
	enter [ flyway migrate ]
	sql files in /sql directory are executed from lowest to highest of these version number.


If failed to migrate
①repair database
	enter [ flyway repair ]
