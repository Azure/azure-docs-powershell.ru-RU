---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399820"
---
# <span data-ttu-id="5cd30-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="5cd30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cd30-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd30-103">Удаляет одну или несколько баз данных из группы отбойных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd30-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="5cd30-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5cd30-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cd30-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cd30-105">DESCRIPTION</span></span>
<span data-ttu-id="5cd30-106">Удаляет одну или несколько баз данных из указанной группы отбойных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd30-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="5cd30-107">Базы данных и связи репликации остались без изменений, но больше не будут доступны через конечные точки группы отополн.</span><span class="sxs-lookup"><span data-stu-id="5cd30-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="5cd30-108">Чтобы получить объекты базы данных, с помощью которых нужно заполнить параметр "-Database", используйте (например,) Get-AzSqlDatabase параметров.</span><span class="sxs-lookup"><span data-stu-id="5cd30-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="5cd30-109">Для выполнения команды необходимо использовать основной сервер группы отбойных команд.</span><span class="sxs-lookup"><span data-stu-id="5cd30-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="5cd30-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5cd30-110">EXAMPLES</span></span>

### <span data-ttu-id="5cd30-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5cd30-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="5cd30-112">Эта команда удаляет одну базу данных из группы отбойных передач, перенаправив ее.</span><span class="sxs-lookup"><span data-stu-id="5cd30-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="5cd30-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5cd30-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="5cd30-114">Эта команда удаляет все базы данных из группы отбойного управления.</span><span class="sxs-lookup"><span data-stu-id="5cd30-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="5cd30-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5cd30-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="5cd30-116">Эта команда удаляет все базы данных в группе "Эластик сбой".</span><span class="sxs-lookup"><span data-stu-id="5cd30-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="5cd30-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cd30-117">PARAMETERS</span></span>

### <span data-ttu-id="5cd30-118">-Database</span><span class="sxs-lookup"><span data-stu-id="5cd30-118">-Database</span></span>
<span data-ttu-id="5cd30-119">Одну или несколько баз SQL Azure на основном сервере группы отбойных серверов, которые нужно удалить из группы отбойных серверов.</span><span class="sxs-lookup"><span data-stu-id="5cd30-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="5cd30-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cd30-120">-DefaultProfile</span></span>
<span data-ttu-id="5cd30-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5cd30-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5cd30-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd30-122">-FailoverGroupName</span></span>
<span data-ttu-id="5cd30-123">Имя группы отбойного SQL базы данных Azure.</span><span class="sxs-lookup"><span data-stu-id="5cd30-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="5cd30-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5cd30-124">-Force</span></span>
<span data-ttu-id="5cd30-125">Пропустите сообщение с подтверждением выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="5cd30-125">Skip confirmation message for performing the action.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd30-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cd30-126">-ResourceGroupName</span></span>
<span data-ttu-id="5cd30-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5cd30-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="5cd30-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5cd30-128">-ServerName</span></span>
<span data-ttu-id="5cd30-129">Имя основного сервера баз данных Azure SQL группы failover.</span><span class="sxs-lookup"><span data-stu-id="5cd30-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5cd30-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5cd30-130">-Confirm</span></span>
<span data-ttu-id="5cd30-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd30-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd30-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cd30-132">-WhatIf</span></span>
<span data-ttu-id="5cd30-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd30-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cd30-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5cd30-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd30-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd30-135">CommonParameters</span></span>
<span data-ttu-id="5cd30-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd30-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd30-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cd30-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd30-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd30-138">INPUTS</span></span>

### <span data-ttu-id="5cd30-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5cd30-139">System.String</span></span>

### <span data-ttu-id="5cd30-140">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="5cd30-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5cd30-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5cd30-141">OUTPUTS</span></span>

### <span data-ttu-id="5cd30-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5cd30-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5cd30-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5cd30-143">NOTES</span></span>

## <span data-ttu-id="5cd30-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cd30-144">RELATED LINKS</span></span>

[<span data-ttu-id="5cd30-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5cd30-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5cd30-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5cd30-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5cd30-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5cd30-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5cd30-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5cd30-151">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="5cd30-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
