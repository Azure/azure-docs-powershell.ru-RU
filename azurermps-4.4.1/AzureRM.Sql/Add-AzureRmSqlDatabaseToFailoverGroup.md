---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlDatabaseToFailoverGroup.md
ms.openlocfilehash: 2772f806ba5297ee9809a8800b25b4c42daf171e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566673"
---
# <span data-ttu-id="db3de-101">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-101">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>

## <span data-ttu-id="db3de-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db3de-102">SYNOPSIS</span></span>
<span data-ttu-id="db3de-103">Добавляет одну или несколько баз данных в группу отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="db3de-103">Adds one or more databases to an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db3de-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db3de-104">SYNTAX</span></span>

```
Add-AzureRmSqlDatabaseToFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db3de-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db3de-105">DESCRIPTION</span></span>
<span data-ttu-id="db3de-106">Добавляет одну или несколько баз данных на основном сервере базы данных Azure SQL для перемещения в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-106">Adds one or more databases on a Azure SQL Database Failover Group's primary server to that Failover Group.</span></span> <span data-ttu-id="db3de-107">Базы данных не должны быть дополнительными базами данных в существующих отношениях репликации.</span><span class="sxs-lookup"><span data-stu-id="db3de-107">The databases must not be secondary databases in existing replication relationships.</span></span> <span data-ttu-id="db3de-108">Команда будет запускать георепликацию баз данных, добавленных на сервер-получатель отказоустойчивой группы.</span><span class="sxs-lookup"><span data-stu-id="db3de-108">The command will start geo-replication of any added databases to the Failover Group's secondary server.</span></span>

<span data-ttu-id="db3de-109">Чтобы получить объекты базы данных, с помощью которых заполните параметр "-Database", используйте командлет Get-AzureRmSqlDatabase (например).</span><span class="sxs-lookup"><span data-stu-id="db3de-109">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>

<span data-ttu-id="db3de-110">Для выполнения команды необходимо использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-110">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="db3de-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db3de-111">EXAMPLES</span></span>

### <span data-ttu-id="db3de-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="db3de-112">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="db3de-113">Эта команда добавляет одну базу данных в группу отработки отказа с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="db3de-113">This command adds one database to a Failover Group by piping it in.</span></span>

### <span data-ttu-id="db3de-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="db3de-114">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Add-AzureRmSqlDatabaseToFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="db3de-115">Эта команда добавляет все базы данных сервера в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-115">This command adds all databases in a server to a Failover Group.</span></span>

### <span data-ttu-id="db3de-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="db3de-116">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Add-AzureRmSqlDatabaseToFailoverGroup -Database $databases
```

<span data-ttu-id="db3de-117">Эта команда добавляет все базы данных из эластичного пула в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-117">This command adds all databases in an Elastic Pool to a Failover Group.</span></span>

## <span data-ttu-id="db3de-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db3de-118">PARAMETERS</span></span>

### <span data-ttu-id="db3de-119">-База данных</span><span class="sxs-lookup"><span data-stu-id="db3de-119">-Database</span></span>
<span data-ttu-id="db3de-120">Одна или несколько баз данных SQL Azure на сервере-источнике отказоустойчивой группы, которые нужно добавить в группу отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-120">One or more Azure SQL Databases on the Failover Group's primary server to be added to the Failover Group.</span></span>

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

### <span data-ttu-id="db3de-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="db3de-121">-FailoverGroupName</span></span>
<span data-ttu-id="db3de-122">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="db3de-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="db3de-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db3de-123">-ResourceGroupName</span></span>
<span data-ttu-id="db3de-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db3de-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="db3de-125">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="db3de-125">-ServerName</span></span>
<span data-ttu-id="db3de-126">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="db3de-126">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="db3de-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db3de-127">-DefaultProfile</span></span>
<span data-ttu-id="db3de-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db3de-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db3de-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db3de-129">CommonParameters</span></span>
<span data-ttu-id="db3de-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db3de-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db3de-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db3de-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db3de-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db3de-132">INPUTS</span></span>

### <span data-ttu-id="db3de-133">System. String</span><span class="sxs-lookup"><span data-stu-id="db3de-133">System.String</span></span>
<span data-ttu-id="db3de-134">System. Collections. Generic. List \` 1 \[ \[ Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 2.5.0.0, культура = Neutral, PublicKeyToken = null\]\]</span><span class="sxs-lookup"><span data-stu-id="db3de-134">System.Collections.Generic.List\`1\[\[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=2.5.0.0, Culture=neutral, PublicKeyToken=null\]\]</span></span>

## <span data-ttu-id="db3de-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db3de-135">OUTPUTS</span></span>

### <span data-ttu-id="db3de-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="db3de-136">System.Object</span></span>

## <span data-ttu-id="db3de-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="db3de-137">NOTES</span></span>

## <span data-ttu-id="db3de-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db3de-138">RELATED LINKS</span></span>

[<span data-ttu-id="db3de-139">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-139">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="db3de-140">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-140">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="db3de-141">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-141">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="db3de-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-142">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="db3de-143">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-143">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="db3de-144">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="db3de-144">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="db3de-145">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="db3de-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
