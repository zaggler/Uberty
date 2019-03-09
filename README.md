![](https://github.com/zaggler/Uberty/blob/master/ubertyNuget.png)

## Uberty Documentation & Quick Start

![](https://mrcodexer.visualstudio.com/Net%20Projects/_apis/build/status/Uberty%20Build%20Release)

Uberty is a productivity helper library that eases and simplifies the development process with databases.

In order to get started, you will need to head over to NuGet [here](https://www.nuget.org/packages/Uberty/).

## Quick Start
* If using MySQL, the connector's driver (MySql.Data.dll) must reside in the parents executing directory as Uberty automatically looks for it.

### Handling multiple database's

  - Vb.Net
```vb  
  ' Create a singleton of the DataBaseManager class
   Public ReadOnly dbManager As DataBaseManager = DataBaseManager.Instance
  
  ' Add a SQLServer database definition to the store
  dbManager.DataBaseStore.TryAdd("uniquekey", New DataBaseInstance("connectionstring", DataBaseEnums.DataBaseType.SQLServer))
  
  ' Make a test connect call
  dbManager.CanConnect("uniquekey") 
```

- C#
```csharp
  // Create a singleton of the DataBaseManager class
   public readonly DataBaseManager dbManager = DataBaseManager.Instance;
  
  // Add a SQLServer database definition to the store
  dbManager.DataBaseStore.TryAdd("uniquekey", new DataBaseInstance("connectionstring", DataBaseEnums.DataBaseType.SQLServer));
  
  // Make a test connect call
  dbManager.CanConnect("uniquekey");
```

### SqlServer

  - Vb.Net
```vb  
  ' Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.SQLServer)
  
  ' ExecuteNonQuery
  Dim rowsAffected As Integer = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.SQLServer)  
```
  - C#
```csharp  
  // Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.SQLServer);
  
  // ExecuteNonQuery
  int rowsAffected = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.SQLServer);
```

### MySQL

  - Vb.Net
```vb  
  ' Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.MySQL)
  
  ' ExecuteNonQuery
  Dim rowsAffected As Integer = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.MySQL)  
```
  - C#
```csharp  
  // Check database connection
  DataBaseMediator.CanConnect("connectionstring", DataBaseEnums.DataBaseType.MySQL);
  
  // ExecuteNonQuery
  int rowsAffected = DataBaseMediator.ExecuteNonQuery("connectionstring", "command", DataBaseEnums.DataBaseType.MySQL);
```



## Issues & Problems?

If you are experiencing any troubles and or issues, please submit a new issue here or contact me on [Nuget](https://www.nuget.org/packages/Uberty/1.0.8/ContactOwners) and I'll help you sort it out.
