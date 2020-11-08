---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: 7fa7c09d5c6c992dfa3eab7a6f81b70e820a9ee4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073202"
---
# <span data-ttu-id="708ca-101">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-101">Remove-AzSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="708ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="708ca-102">SYNOPSIS</span></span>
<span data-ttu-id="708ca-103">Удаление одной или нескольких баз данных из группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="708ca-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="708ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="708ca-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="708ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="708ca-105">DESCRIPTION</span></span>
<span data-ttu-id="708ca-106">Удаление одной или нескольких баз данных из указанной группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="708ca-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="708ca-107">Базы данных и связи между репликацией остаются неизменными, но они больше не будут доступны через конечные точки группы для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="708ca-108">Чтобы получить объекты базы данных, с помощью которых заполните параметр "-Database", используйте командлет Get-AzSqlDatabase (например).</span><span class="sxs-lookup"><span data-stu-id="708ca-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="708ca-109">Для выполнения команды необходимо использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="708ca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="708ca-110">EXAMPLES</span></span>

### <span data-ttu-id="708ca-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="708ca-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="708ca-112">Эта команда удаляет одну базу данных из группы отработки отказа, направив ее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="708ca-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="708ca-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="708ca-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="708ca-114">Эта команда удаляет все базы данных из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="708ca-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="708ca-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="708ca-116">Эта команда удаляет все базы данных из эластичного пула из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="708ca-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="708ca-117">PARAMETERS</span></span>

### <span data-ttu-id="708ca-118">-База данных</span><span class="sxs-lookup"><span data-stu-id="708ca-118">-Database</span></span>
<span data-ttu-id="708ca-119">Одна или несколько баз данных SQL Azure на основном сервере группы, на которую отработки отказа, которые нужно удалить из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="708ca-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="708ca-120">-DefaultProfile</span></span>
<span data-ttu-id="708ca-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="708ca-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="708ca-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="708ca-122">-FailoverGroupName</span></span>
<span data-ttu-id="708ca-123">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="708ca-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="708ca-124">-Force</span><span class="sxs-lookup"><span data-stu-id="708ca-124">-Force</span></span>
<span data-ttu-id="708ca-125">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="708ca-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="708ca-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="708ca-126">-ResourceGroupName</span></span>
<span data-ttu-id="708ca-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="708ca-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="708ca-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="708ca-128">-ServerName</span></span>
<span data-ttu-id="708ca-129">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="708ca-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="708ca-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="708ca-130">-Confirm</span></span>
<span data-ttu-id="708ca-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="708ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="708ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="708ca-132">-WhatIf</span></span>
<span data-ttu-id="708ca-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="708ca-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="708ca-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="708ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="708ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="708ca-135">CommonParameters</span></span>
<span data-ttu-id="708ca-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="708ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="708ca-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="708ca-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="708ca-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="708ca-138">INPUTS</span></span>

### <span data-ttu-id="708ca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="708ca-139">System.String</span></span>

### <span data-ttu-id="708ca-140">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. SQL. Database. SQL, Version = 1.3.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="708ca-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="708ca-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="708ca-141">OUTPUTS</span></span>

### <span data-ttu-id="708ca-142">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="708ca-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="708ca-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="708ca-143">NOTES</span></span>

## <span data-ttu-id="708ca-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="708ca-144">RELATED LINKS</span></span>

[<span data-ttu-id="708ca-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="708ca-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="708ca-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="708ca-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="708ca-149">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-149">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="708ca-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="708ca-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="708ca-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="708ca-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
