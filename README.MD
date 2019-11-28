Установить
	1. sqlite-netFx46-setup-bundle-x86-2015-1.0.112.0.exe
	2. extension.vsix

Установить в nuget
	System.Data.SQLite.Core

Автоматически с ней в зависимостях должны установиться
	Entity Framework
	System.Data.SQLite
	System.Data.SQLite.EF6
	System.Data.SQLite.Linq

добавить в App.config запись
	<provider invariantName="System.Data.SQLite" type="System.Data.SQLite.EF6.SQLiteProviderServices, System.Data.SQLite.EF6" />

добавить в проект клас EntityFramework в соединении указать путь к уже созданной базе данных (только Database first)
следовать указаниям визарда
