---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505920"
---
# <span data-ttu-id="d5e62-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d5e62-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d5e62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5e62-102">SYNOPSIS</span></span>
<span data-ttu-id="d5e62-103">Создает вторичную базу данных для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="d5e62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5e62-104">SYNTAX</span></span>

### <span data-ttu-id="d5e62-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5e62-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d5e62-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="d5e62-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5e62-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5e62-107">DESCRIPTION</span></span>
<span data-ttu-id="d5e62-108">При настройке геопроигрывательной репликации базы данных новый Start-AzSqlDatabaseCopy **AzSqlDataBaseSecondary.**</span><span class="sxs-lookup"><span data-stu-id="d5e62-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="d5e62-109">Она возвращает объект гео-репликации из основного объекта во вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="d5e62-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5e62-110">EXAMPLES</span></span>

### <span data-ttu-id="d5e62-111">Пример 1. Установить активные Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="d5e62-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="d5e62-112">Пример 2. Установить Geo-Replication и указать имя базы данных партнера, которое должно отличаться от имени базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="d5e62-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5e62-113">PARAMETERS</span></span>

### <span data-ttu-id="d5e62-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="d5e62-114">-AllowConnections</span></span>
<span data-ttu-id="d5e62-115">Указывает цель чтения вторичной базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d5e62-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="d5e62-116">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="d5e62-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5e62-117">Нет</span><span class="sxs-lookup"><span data-stu-id="d5e62-117">No</span></span>
- <span data-ttu-id="d5e62-118">Все</span><span class="sxs-lookup"><span data-stu-id="d5e62-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d5e62-119">-AsJob</span></span>
<span data-ttu-id="d5e62-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d5e62-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d5e62-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="d5e62-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="d5e62-122">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="d5e62-123">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="d5e62-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5e62-124">-DatabaseName</span></span>
<span data-ttu-id="d5e62-125">Имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="d5e62-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="d5e62-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5e62-126">-DefaultProfile</span></span>
<span data-ttu-id="d5e62-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d5e62-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5e62-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d5e62-128">-LicenseType</span></span>
<span data-ttu-id="d5e62-129">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="d5e62-129">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5e62-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="d5e62-131">Имя создаемой вторичной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-131">The name of the secondary database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e62-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d5e62-133">Задает имя группы ресурсов Azure, которой этот cmdlet назначает вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d5e62-134">-PartnerServerName</span></span>
<span data-ttu-id="d5e62-135">Имя сервера базы данных Azure SQL в качестве дополнительного.</span><span class="sxs-lookup"><span data-stu-id="d5e62-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5e62-136">-ResourceGroupName</span></span>
<span data-ttu-id="d5e62-137">Задает имя группы ресурсов Azure, которой этот cmdlet назначает основную базу данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="d5e62-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d5e62-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="d5e62-139">Вычислительное поколение дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e62-139">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d5e62-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="d5e62-141">Определяет имя эластичного пула, в который нужно поместить вложенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="d5e62-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="d5e62-143">Указывает имя цели обслуживания, которая будет назначаться вторичной базе данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="d5e62-144">-SecondaryType</span></span>
<span data-ttu-id="d5e62-145">Дополнительный тип базы данных, если она является вторичной.</span><span class="sxs-lookup"><span data-stu-id="d5e62-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="d5e62-146">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="d5e62-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="d5e62-147">-SecondaryVCore</span></span>
<span data-ttu-id="d5e62-148">Номера на vcore дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d5e62-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5e62-149">-ServerName</span></span>
<span data-ttu-id="d5e62-150">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="d5e62-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="d5e62-151">-Теги</span><span class="sxs-lookup"><span data-stu-id="d5e62-151">-Tags</span></span>
<span data-ttu-id="d5e62-152">Определяет пары "значение ключа" в форме hash table, которые нужно связать со ссылкой SQL репликации базы данных.</span><span class="sxs-lookup"><span data-stu-id="d5e62-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="d5e62-153">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d5e62-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5e62-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5e62-154">-Confirm</span></span>
<span data-ttu-id="d5e62-155">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d5e62-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5e62-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5e62-156">-WhatIf</span></span>
<span data-ttu-id="d5e62-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5e62-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5e62-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d5e62-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5e62-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5e62-159">CommonParameters</span></span>
<span data-ttu-id="d5e62-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5e62-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5e62-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5e62-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5e62-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5e62-162">INPUTS</span></span>

### <span data-ttu-id="d5e62-163">System.String</span><span class="sxs-lookup"><span data-stu-id="d5e62-163">System.String</span></span>

## <span data-ttu-id="d5e62-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5e62-164">OUTPUTS</span></span>

### <span data-ttu-id="d5e62-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d5e62-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d5e62-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5e62-166">NOTES</span></span>

## <span data-ttu-id="d5e62-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5e62-167">RELATED LINKS</span></span>

[<span data-ttu-id="d5e62-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d5e62-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d5e62-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d5e62-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d5e62-170">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="d5e62-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
