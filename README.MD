Установить

	1. sqlite-netFx46-setup-bundle-x86-2015-1.0.112.0.exe
	2. extension.vsix

Установить в nuget

	System.Data.SQLite

Автоматически с ней в зависимостях должны установиться

	Entity Framework
	System.Data.SQLite
	System.Data.SQLite.EF6
	System.Data.SQLite.Linq

```
<?xml version="1.0" encoding="utf-8"?>
<packages>
  <package id="EntityFramework" version="6.3.0" targetFramework="net46" />
  <package id="System.Data.SQLite" version="1.0.112.0" targetFramework="net46" />
  <package id="System.Data.SQLite.Core" version="1.0.112.0" targetFramework="net46" />
  <package id="System.Data.SQLite.EF6" version="1.0.112.0" targetFramework="net46" />
  <package id="System.Data.SQLite.Linq" version="1.0.112.0" targetFramework="net46" />
</packages>
```

Добавить в App.config запись

	<provider invariantName="System.Data.SQLite" type="System.Data.SQLite.EF6.SQLiteProviderServices, System.Data.SQLite.EF6" />

Добавить в проект клас EntityFramework в соединении указать путь к уже созданной базе данных (только Database first)
следовать указаниям визарда
