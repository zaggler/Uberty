## Uberty Documentation & Quick Start

Uberty is a productivity helper library that eases and simplifies the development process with databases.

In order to get started, you will need to head over to NuGet [here](https://www.nuget.org/packages/Uberty/) or if you want through the Package Manager:

```markdown
Install-Package Uberty -Version 1.0.8
```

## Quick Start
* If using MySQL, the connector's driver (MySql.Data.dll) must reside in the parents executing directory as Uberty automatically looks for it.

### Handling multiple database's

  - Vb.Net
```markdown  
  ' Create a singleton of the DataBaseManager class
   Public ReadOnly dbManager As DataBaseManager = DataBaseManager.Instance
  
  ' Add a SQLServer database definition to the store
  dbManager.DataBaseStore.TryAdd("uniquekey", New DataBaseInstance("connectionstring", DataBaseEnums.DataBaseType.SQLServer))
  
  ' Make a test connect call
  dbManager.CanConnect("uniquekey") 
```

- C#
```markdown  
  ' Create a singleton of the DataBaseManager class
   public readonly DataBaseManager dbManager = DataBaseManager.Instance;
  
  ' Add a SQLServer database definition to the store
  dbManager.DataBaseStore.TryAdd("uniquekey", new DataBaseInstance("connectionstring", DataBaseEnums.DataBaseType.SQLServer));
  
  ' Make a test connect call
  dbManager.CanConnect("uniquekey");
```

### SqlServer

  - Vb.Net
```markdown  
  ' Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.SQLServer)
  
  ' ExecuteNonQuery
  Dim rowsAffected As Integer = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.SQLServer)  
```
  - C#
```markdown  
  // Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.SQLServer);
  
  // ExecuteNonQuery
  int rowsAffected = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.SQLServer);
```

### MySQL

  - Vb.Net
```markdown  
  ' Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.MySQL)
  
  ' ExecuteNonQuery
  Dim rowsAffected As Integer = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.MySQL)  
```
  - C#
```markdown  
  // Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.MySQL);
  
  // ExecuteNonQuery
  int rowsAffected = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.MySQL);
```



## Issues & Problems?

If you are experiencing any troubles and or issues, please submit a new issue here or contact me on [Nuget](https://www.nuget.org/packages/Uberty/1.0.8/ContactOwners) and I'll help you sort it out.
