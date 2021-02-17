---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 7577809134987bd1a0092e28170d5bf25ccac04e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223033"
---
# <span data-ttu-id="20663-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="20663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20663-102">SYNOPSIS</span></span>
<span data-ttu-id="20663-103">Добавляет одну или несколько баз данных в группу отбойных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="20663-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="20663-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20663-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20663-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20663-105">DESCRIPTION</span></span>
<span data-ttu-id="20663-106">Добавляет одну или несколько баз данных на основном сервере SQL отбойной базы данных Azure в эту группу.</span><span class="sxs-lookup"><span data-stu-id="20663-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="20663-107">Базы данных не должны быть дополнительными базами данных в существующих связях репликации.</span><span class="sxs-lookup"><span data-stu-id="20663-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="20663-108">Команда начнет геокопию всех добавленных баз данных на дополнительный сервер группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="20663-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="20663-109">Чтобы получить объекты базы данных, для заполнения которых нужно заполнить параметр "-Database", используйте (например,) Get-AzSqlDatabase этим Get-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="20663-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="20663-110">Для выполнения команды необходимо использовать основной сервер группы отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="20663-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="20663-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20663-111">EXAMPLES</span></span>

### <span data-ttu-id="20663-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20663-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="20663-113">Эта команда добавляет одну базу данных в группу отбойных передач, перенаправив ее.</span><span class="sxs-lookup"><span data-stu-id="20663-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="20663-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20663-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="20663-115">Эта команда добавляет все базы данных сервера в группу отбойного управления.</span><span class="sxs-lookup"><span data-stu-id="20663-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="20663-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="20663-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="20663-117">Эта команда добавляет все базы данных из пула эластичности в группу отсея.</span><span class="sxs-lookup"><span data-stu-id="20663-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="20663-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20663-118">PARAMETERS</span></span>

### <span data-ttu-id="20663-119">-Database</span><span class="sxs-lookup"><span data-stu-id="20663-119">-Database</span></span>
<span data-ttu-id="20663-120">Одна или несколько баз SQL Azure на основном сервере группы отбойных серверов, которые нужно добавить в группу отбойного сервера.</span><span class="sxs-lookup"><span data-stu-id="20663-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20663-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20663-121">-DefaultProfile</span></span>
<span data-ttu-id="20663-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20663-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20663-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="20663-123">-FailoverGroupName</span></span>
<span data-ttu-id="20663-124">Имя группы отбойного SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="20663-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20663-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20663-125">-ResourceGroupName</span></span>
<span data-ttu-id="20663-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20663-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20663-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="20663-127">-ServerName</span></span>
<span data-ttu-id="20663-128">Имя основного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="20663-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20663-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20663-129">CommonParameters</span></span>
<span data-ttu-id="20663-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20663-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20663-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20663-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20663-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20663-132">INPUTS</span></span>

### <span data-ttu-id="20663-133">System.String</span><span class="sxs-lookup"><span data-stu-id="20663-133">System.String</span></span>

### <span data-ttu-id="20663-134">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="20663-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="20663-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20663-135">OUTPUTS</span></span>

### <span data-ttu-id="20663-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="20663-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="20663-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20663-137">NOTES</span></span>

## <span data-ttu-id="20663-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20663-138">RELATED LINKS</span></span>

[<span data-ttu-id="20663-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="20663-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="20663-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="20663-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="20663-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="20663-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="20663-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="20663-145">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="20663-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
