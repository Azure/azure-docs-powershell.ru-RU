---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabasefromfailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabaseFromFailoverGroup.md
ms.openlocfilehash: a8f147b4e2c8a1f4525585f8622b7195ed759022
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566373"
---
# <span data-ttu-id="319e0-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-101">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>

## <span data-ttu-id="319e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="319e0-102">SYNOPSIS</span></span>
<span data-ttu-id="319e0-103">Удаление одной или нескольких баз данных из группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="319e0-103">Removes one or more databases from an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="319e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="319e0-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabaseFromFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 -Database <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel]>
 [-Force] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="319e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="319e0-105">DESCRIPTION</span></span>
<span data-ttu-id="319e0-106">Удаление одной или нескольких баз данных из указанной группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="319e0-106">Removes one or more databases from the specified Azure SQL Database Failover Group.</span></span> <span data-ttu-id="319e0-107">Базы данных и связи между репликацией остаются неизменными, но они больше не будут доступны через конечные точки группы для отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-107">The databases and replication relationships are left intact, but they will no longer be accessible through the Failover Group endpoints.</span></span>
<span data-ttu-id="319e0-108">Чтобы получить объекты базы данных, с помощью которых заполните параметр "-Database", используйте командлет Get-AzureRmSqlDatabase (например).</span><span class="sxs-lookup"><span data-stu-id="319e0-108">To obtain database objects with which to populate the '-Database' parameter, use (for example) the Get-AzureRmSqlDatabase cmdlet.</span></span>
<span data-ttu-id="319e0-109">Для выполнения команды необходимо использовать основной сервер группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-109">The Failover Group's primary server must be used to execute the command.</span></span>

## <span data-ttu-id="319e0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="319e0-110">EXAMPLES</span></span>

### <span data-ttu-id="319e0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="319e0-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabase -ResourceGroupName rg -ServerName primaryserver -DatabaseName db1 | Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="319e0-112">Эта команда удаляет одну базу данных из группы отработки отказа, направив ее по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="319e0-112">This command removes one database from a Failover Group by piping it in.</span></span>

### <span data-ttu-id="319e0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="319e0-113">Example 2</span></span>
```
PS C:\> $primaryServer = Get-AzureRmSqlServer -ResourceGroupName rg -ServerName primaryserver
PS C:\> $failoverGroup = $primaryServer | Remove-AzureRmSqlDatabaseFromFailoverGroup -FailoverGroupName fg -Database ($primaryServer | Get-AzureRmSqlDatabase)
```

<span data-ttu-id="319e0-114">Эта команда удаляет все базы данных из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-114">This command removes all databases from a Failover Group.</span></span>

### <span data-ttu-id="319e0-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="319e0-115">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
PS C:\> $databases = Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName rg -ServerName primaryserver -ElasticPoolName pool1
PS C:\> $failoverGroup = $failoverGroup | Remove-AzureRMSqlDatabaseFromFailoverGroup -Database $databases
```

<span data-ttu-id="319e0-116">Эта команда удаляет все базы данных из эластичного пула из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-116">This command removes all databases in an Elastic Pool from a Failover Group.</span></span>

## <span data-ttu-id="319e0-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="319e0-117">PARAMETERS</span></span>

### <span data-ttu-id="319e0-118">-База данных</span><span class="sxs-lookup"><span data-stu-id="319e0-118">-Database</span></span>
<span data-ttu-id="319e0-119">Одна или несколько баз данных SQL Azure на основном сервере группы, на которую отработки отказа, которые нужно удалить из группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-119">One or more Azure SQL Databases on the Failover Group's primary server to be removed from the Failover Group.</span></span>

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

### <span data-ttu-id="319e0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="319e0-120">-DefaultProfile</span></span>
<span data-ttu-id="319e0-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="319e0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="319e0-122">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="319e0-122">-FailoverGroupName</span></span>
<span data-ttu-id="319e0-123">Имя группы отработки отказа базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="319e0-123">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="319e0-124">-Force</span><span class="sxs-lookup"><span data-stu-id="319e0-124">-Force</span></span>
<span data-ttu-id="319e0-125">Пропустить предупреждающее сообщение для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="319e0-125">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="319e0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="319e0-126">-ResourceGroupName</span></span>
<span data-ttu-id="319e0-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="319e0-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="319e0-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="319e0-128">-ServerName</span></span>
<span data-ttu-id="319e0-129">Имя основного сервера базы данных Azure SQL для группы отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="319e0-129">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="319e0-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="319e0-130">-Confirm</span></span>
<span data-ttu-id="319e0-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="319e0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="319e0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="319e0-132">-WhatIf</span></span>
<span data-ttu-id="319e0-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="319e0-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="319e0-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="319e0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="319e0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="319e0-135">CommonParameters</span></span>
<span data-ttu-id="319e0-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="319e0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="319e0-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="319e0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="319e0-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="319e0-138">INPUTS</span></span>

### <span data-ttu-id="319e0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="319e0-139">System.String</span></span>

### <span data-ttu-id="319e0-140">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel, Microsoft. Azure. Commands. SQL, Version = 4.11.0.0, культура = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="319e0-140">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel, Microsoft.Azure.Commands.Sql, Version=4.11.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="319e0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="319e0-141">OUTPUTS</span></span>

### <span data-ttu-id="319e0-142">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="319e0-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="319e0-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="319e0-143">NOTES</span></span>

## <span data-ttu-id="319e0-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="319e0-144">RELATED LINKS</span></span>

[<span data-ttu-id="319e0-145">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-145">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="319e0-146">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-146">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="319e0-147">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-147">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="319e0-148">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-148">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="319e0-149">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-149">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="319e0-150">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="319e0-150">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="319e0-151">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="319e0-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
