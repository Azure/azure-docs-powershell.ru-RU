---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 983291eda139793b2cc5d0fe5cd213b5d8cd69a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982024"
---
# <span data-ttu-id="a3553-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a3553-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="a3553-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3553-102">SYNOPSIS</span></span>
<span data-ttu-id="a3553-103">Создает вторичную базу данных для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="a3553-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a3553-104">SYNTAX</span></span>

### <span data-ttu-id="a3553-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a3553-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3553-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="a3553-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a3553-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3553-107">DESCRIPTION</span></span>
<span data-ttu-id="a3553-108">При настройке геопроигрывательной репликации базы данных новый Start-AzSqlDatabaseCopy **AzSqlDataBaseSecondary.**</span><span class="sxs-lookup"><span data-stu-id="a3553-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="a3553-109">Она возвращает объект гео-репликации из основного объекта во вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="a3553-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a3553-110">EXAMPLES</span></span>

### <span data-ttu-id="a3553-111">Пример 1. Установить активные Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="a3553-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="a3553-112">Пример 2. Установить Geo-Replication и указать имя базы данных партнера, которое должно отличаться от имени базы данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="a3553-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a3553-113">PARAMETERS</span></span>

### <span data-ttu-id="a3553-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="a3553-114">-AllowConnections</span></span>
<span data-ttu-id="a3553-115">Определяет цель чтения вторичной базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a3553-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="a3553-116">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="a3553-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3553-117">Нет</span><span class="sxs-lookup"><span data-stu-id="a3553-117">No</span></span>
- <span data-ttu-id="a3553-118">Все</span><span class="sxs-lookup"><span data-stu-id="a3553-118">All</span></span>

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

### <span data-ttu-id="a3553-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3553-119">-AsJob</span></span>
<span data-ttu-id="a3553-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a3553-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3553-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="a3553-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="a3553-122">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="a3553-123">Доступны такие варианты: "Локальный", "Зона" и "Гео".</span><span class="sxs-lookup"><span data-stu-id="a3553-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="a3553-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a3553-124">-DatabaseName</span></span>
<span data-ttu-id="a3553-125">Имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="a3553-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="a3553-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3553-126">-DefaultProfile</span></span>
<span data-ttu-id="a3553-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a3553-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a3553-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a3553-128">-LicenseType</span></span>
<span data-ttu-id="a3553-129">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="a3553-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="a3553-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a3553-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="a3553-131">Имя создаемой вторичной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="a3553-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3553-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a3553-133">Задает имя группы ресурсов Azure, которой этот cmdlet назначает вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="a3553-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a3553-134">-PartnerServerName</span></span>
<span data-ttu-id="a3553-135">Имя сервера базы данных Azure SQL в качестве дополнительного.</span><span class="sxs-lookup"><span data-stu-id="a3553-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="a3553-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3553-136">-ResourceGroupName</span></span>
<span data-ttu-id="a3553-137">Задает имя группы ресурсов Azure, которой этот cmdlet назначает основную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="a3553-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="a3553-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="a3553-139">Вычислительное поколение дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a3553-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="a3553-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a3553-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="a3553-141">Определяет имя эластичного пула, в который нужно поместить вложенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="a3553-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a3553-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="a3553-143">Указывает имя цели обслуживания, которая будет назначаться вторичной базе данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="a3553-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="a3553-144">-SecondaryType</span></span>
<span data-ttu-id="a3553-145">Дополнительный тип базы данных, если она является вторичной.</span><span class="sxs-lookup"><span data-stu-id="a3553-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="a3553-146">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="a3553-146">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="a3553-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="a3553-147">-SecondaryVCore</span></span>
<span data-ttu-id="a3553-148">Номера на vcore дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a3553-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="a3553-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a3553-149">-ServerName</span></span>
<span data-ttu-id="a3553-150">Определяет имя SQL Server основной SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a3553-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="a3553-151">-Теги</span><span class="sxs-lookup"><span data-stu-id="a3553-151">-Tags</span></span>
<span data-ttu-id="a3553-152">Определяет пары значений ключа в форме hash table, которые нужно связать со ссылкой SQL репликации базы данных.</span><span class="sxs-lookup"><span data-stu-id="a3553-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="a3553-153">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="a3553-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a3553-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3553-154">-Confirm</span></span>
<span data-ttu-id="a3553-155">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a3553-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3553-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3553-156">-WhatIf</span></span>
<span data-ttu-id="a3553-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3553-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3553-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a3553-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3553-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3553-159">CommonParameters</span></span>
<span data-ttu-id="a3553-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3553-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3553-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3553-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3553-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a3553-162">INPUTS</span></span>

### <span data-ttu-id="a3553-163">System.String</span><span class="sxs-lookup"><span data-stu-id="a3553-163">System.String</span></span>

## <span data-ttu-id="a3553-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a3553-164">OUTPUTS</span></span>

### <span data-ttu-id="a3553-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a3553-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="a3553-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a3553-166">NOTES</span></span>

## <span data-ttu-id="a3553-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3553-167">RELATED LINKS</span></span>

[<span data-ttu-id="a3553-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a3553-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="a3553-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a3553-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="a3553-170">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="a3553-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
