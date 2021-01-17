---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397015"
---
# <span data-ttu-id="053ae-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="053ae-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="053ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="053ae-102">SYNOPSIS</span></span>
<span data-ttu-id="053ae-103">Создает вторичную базу данных для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="053ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="053ae-104">SYNTAX</span></span>

### <span data-ttu-id="053ae-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="053ae-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="053ae-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="053ae-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="053ae-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="053ae-107">DESCRIPTION</span></span>
<span data-ttu-id="053ae-108">При настройке геопроигрывательной репликации базы данных новый Start-AzSqlDatabaseCopy **AzSqlDataBaseSecondary.**</span><span class="sxs-lookup"><span data-stu-id="053ae-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="053ae-109">Она возвращает объект гео-репликации из основного объекта во вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="053ae-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="053ae-110">EXAMPLES</span></span>

### <span data-ttu-id="053ae-111">Пример 1. Установить активные Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="053ae-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="053ae-112">Пример 2. Установить Geo-Replication и указать имя базы данных партнера, которое должно отличаться от имени базы данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="053ae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="053ae-113">PARAMETERS</span></span>

### <span data-ttu-id="053ae-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="053ae-114">-AllowConnections</span></span>
<span data-ttu-id="053ae-115">Указывает цель чтения вторичной базы данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="053ae-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="053ae-116">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="053ae-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="053ae-117">Нет</span><span class="sxs-lookup"><span data-stu-id="053ae-117">No</span></span>
- <span data-ttu-id="053ae-118">Все</span><span class="sxs-lookup"><span data-stu-id="053ae-118">All</span></span>

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

### <span data-ttu-id="053ae-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="053ae-119">-AsJob</span></span>
<span data-ttu-id="053ae-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="053ae-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="053ae-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="053ae-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="053ae-122">Избыточность резервного копирования хранилища, используемого для хранения резервных копий SQL базы данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="053ae-123">Доступны такие варианты: Local (Локальный), Zone (Зона) и Geo (География).</span><span class="sxs-lookup"><span data-stu-id="053ae-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="053ae-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="053ae-124">-DatabaseName</span></span>
<span data-ttu-id="053ae-125">Имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="053ae-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="053ae-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="053ae-126">-DefaultProfile</span></span>
<span data-ttu-id="053ae-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="053ae-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="053ae-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="053ae-128">-LicenseType</span></span>
<span data-ttu-id="053ae-129">Тип лицензии для базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="053ae-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="053ae-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="053ae-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="053ae-131">Имя создаемой вторичной базы данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="053ae-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="053ae-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="053ae-133">Задает имя группы ресурсов Azure, которой этот cmdlet назначает вторичную базу данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="053ae-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="053ae-134">-PartnerServerName</span></span>
<span data-ttu-id="053ae-135">Имя сервера базы данных Azure SQL в качестве дополнительного.</span><span class="sxs-lookup"><span data-stu-id="053ae-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="053ae-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="053ae-136">-ResourceGroupName</span></span>
<span data-ttu-id="053ae-137">Задает имя группы ресурсов Azure, которой этот cmdlet назначает основную базу данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="053ae-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="053ae-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="053ae-139">Вычислительное поколение дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="053ae-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="053ae-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="053ae-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="053ae-141">Определяет имя эластичного пула, в который нужно поместить вложенную базу данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="053ae-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="053ae-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="053ae-143">Указывает имя цели обслуживания, которая будет назначаться вторичной базе данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="053ae-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="053ae-144">-SecondaryType</span></span>
<span data-ttu-id="053ae-145">Дополнительный тип базы данных, если она является вторичной.</span><span class="sxs-lookup"><span data-stu-id="053ae-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="053ae-146">Допустимые значения: Geo и Named.</span><span class="sxs-lookup"><span data-stu-id="053ae-146">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="053ae-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="053ae-147">-SecondaryVCore</span></span>
<span data-ttu-id="053ae-148">Номера на vcore дополнительной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="053ae-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="053ae-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="053ae-149">-ServerName</span></span>
<span data-ttu-id="053ae-150">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="053ae-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="053ae-151">-Теги</span><span class="sxs-lookup"><span data-stu-id="053ae-151">-Tags</span></span>
<span data-ttu-id="053ae-152">Определяет пары значений ключа в форме hash table, которые нужно связать со ссылкой SQL репликации базы данных.</span><span class="sxs-lookup"><span data-stu-id="053ae-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="053ae-153">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="053ae-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="053ae-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="053ae-154">-Confirm</span></span>
<span data-ttu-id="053ae-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="053ae-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="053ae-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="053ae-156">-WhatIf</span></span>
<span data-ttu-id="053ae-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="053ae-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="053ae-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="053ae-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="053ae-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="053ae-159">CommonParameters</span></span>
<span data-ttu-id="053ae-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="053ae-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="053ae-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="053ae-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="053ae-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="053ae-162">INPUTS</span></span>

### <span data-ttu-id="053ae-163">System.String</span><span class="sxs-lookup"><span data-stu-id="053ae-163">System.String</span></span>

## <span data-ttu-id="053ae-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="053ae-164">OUTPUTS</span></span>

### <span data-ttu-id="053ae-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="053ae-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="053ae-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="053ae-166">NOTES</span></span>

## <span data-ttu-id="053ae-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="053ae-167">RELATED LINKS</span></span>

[<span data-ttu-id="053ae-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="053ae-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="053ae-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="053ae-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="053ae-170">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="053ae-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
