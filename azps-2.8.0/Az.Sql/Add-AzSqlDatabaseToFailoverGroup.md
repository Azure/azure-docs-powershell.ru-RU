---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqldatabasetofailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: aaf2063d82e0140e9abe07b7343a2c314e2fbd7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903710"
---
# <span data-ttu-id="c3071-101">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-101">Add-AzSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="c3071-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3071-102">SYNOPSIS</span></span>
<span data-ttu-id="c3071-103">Добавляет одну или несколько баз данных в группу отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c3071-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="c3071-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3071-104">SYNTAX</span></span>

```
Add-AzSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3071-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3071-105">DESCRIPTION</span></span>
<span data-ttu-id="c3071-106">Добавляет одну или несколько баз данных на основном сервере базы данных Azure SQL для перемещения в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="c3071-107">Базы данных не должны быть дополнительными базами данных в существующих отношениях репликации.</span><span class="sxs-lookup"><span data-stu-id="c3071-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="c3071-108">Команда будет запускать георепликацию баз данных, добавленных на сервер-получатель отказоустойчивой группы.</span><span class="sxs-lookup"><span data-stu-id="c3071-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>
<span data-ttu-id="c3071-109">Чтобы получить объекты базы данных, с помощью которых заполните параметр "-Database", используйте командлет Get-AzSqlDatabase (например).</span><span class="sxs-lookup"><span data-stu-id="c3071-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzSqlDatabase cmdlet.</span></span>
<span data-ttu-id="c3071-110">Для выполнения команды необходимо использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="c3071-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3071-111">EXAMPLES</span></span>

### <span data-ttu-id="c3071-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3071-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="c3071-113">Эта команда добавляет одну базу данных в группу отработки отказа с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="c3071-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="c3071-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c3071-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzSqlDatabase)
```

<span data-ttu-id="c3071-115">Эта команда добавляет все базы данных сервера в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="c3071-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c3071-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="c3071-117">Эта команда добавляет все базы данных из эластичного пула в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="c3071-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3071-118">PARAMETERS</span></span>

### <span data-ttu-id="c3071-119">-База данных</span><span class="sxs-lookup"><span data-stu-id="c3071-119">-Database</span></span>
<span data-ttu-id="c3071-120">Одна или несколько баз данных SQL Azure на сервере-источнике отказоустойчивой группы, которые нужно добавить в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="c3071-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3071-121">-DefaultProfile</span></span>
<span data-ttu-id="c3071-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c3071-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3071-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="c3071-123">-FailoverGroupName</span></span>
<span data-ttu-id="c3071-124">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c3071-124">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="c3071-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3071-125">-ResourceGroupName</span></span>
<span data-ttu-id="c3071-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c3071-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="c3071-127">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="c3071-127">-ServerName</span></span>
<span data-ttu-id="c3071-128">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c3071-128">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="c3071-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3071-129">CommonParameters</span></span>
<span data-ttu-id="c3071-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3071-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3071-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3071-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3071-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3071-132">INPUTS</span></span>

### <span data-ttu-id="c3071-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c3071-133">System.String</span></span>

### <span data-ttu-id="c3071-134">System. Collections. Generic. List "1 [[Microsoft. Azure. Commands. SQL. Database. SQL, Version = 1.3.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="c3071-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.PowerShell.Cmdlets.Sql, Version=1.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c3071-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3071-135">OUTPUTS</span></span>

### <span data-ttu-id="c3071-136">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c3071-136">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="c3071-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3071-137">NOTES</span></span>

## <span data-ttu-id="c3071-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3071-138">RELATED LINKS</span></span>

[<span data-ttu-id="c3071-139">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-139">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c3071-140">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-140">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c3071-141">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-141">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c3071-142">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-142">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="c3071-143">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-143">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c3071-144">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c3071-144">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="c3071-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="c3071-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
