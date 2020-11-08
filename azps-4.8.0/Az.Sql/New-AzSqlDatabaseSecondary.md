---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 0b0934ffe9a5721ff08438ca7a24d97e2b4a34cd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078649"
---
# <span data-ttu-id="28037-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="28037-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="28037-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="28037-102">SYNOPSIS</span></span>
<span data-ttu-id="28037-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="28037-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="28037-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="28037-104">SYNTAX</span></span>

### <span data-ttu-id="28037-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="28037-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28037-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="28037-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28037-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="28037-107">DESCRIPTION</span></span>
<span data-ttu-id="28037-108">Командлет **New-AzSqlDatabaseSecondary** заменяет командлет Start-AzSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="28037-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="28037-109">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="28037-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="28037-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="28037-110">EXAMPLES</span></span>

### <span data-ttu-id="28037-111">Пример 1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="28037-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="28037-112">Пример 2: Установка активного Geo-Replication и указание имени базы данных партнера, которое отличается от имени исходной базы данных</span><span class="sxs-lookup"><span data-stu-id="28037-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="28037-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="28037-113">PARAMETERS</span></span>

### <span data-ttu-id="28037-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="28037-114">-AllowConnections</span></span>
<span data-ttu-id="28037-115">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="28037-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="28037-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28037-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28037-117">Нет</span><span class="sxs-lookup"><span data-stu-id="28037-117">No</span></span>
- <span data-ttu-id="28037-118">Весь</span><span class="sxs-lookup"><span data-stu-id="28037-118">All</span></span>

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

### <span data-ttu-id="28037-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="28037-119">-AsJob</span></span>
<span data-ttu-id="28037-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="28037-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="28037-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="28037-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="28037-122">Избыточное резервное хранилище, используемое для хранения резервных копий базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="28037-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="28037-123">Доступны следующие параметры: local, Zone и Geo.</span><span class="sxs-lookup"><span data-stu-id="28037-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="28037-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="28037-124">-DatabaseName</span></span>
<span data-ttu-id="28037-125">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="28037-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="28037-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28037-126">-DefaultProfile</span></span>
<span data-ttu-id="28037-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="28037-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28037-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="28037-128">-LicenseType</span></span>
<span data-ttu-id="28037-129">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="28037-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="28037-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="28037-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="28037-131">Имя создаваемой базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="28037-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="28037-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28037-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="28037-133">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="28037-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="28037-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="28037-134">-PartnerServerName</span></span>
<span data-ttu-id="28037-135">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="28037-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="28037-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28037-136">-ResourceGroupName</span></span>
<span data-ttu-id="28037-137">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="28037-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="28037-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="28037-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="28037-139">Вычислено Создание вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="28037-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="28037-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="28037-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="28037-141">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="28037-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="28037-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="28037-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="28037-143">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="28037-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="28037-144">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="28037-144">-SecondaryVCore</span></span>
<span data-ttu-id="28037-145">Vcore номера вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="28037-145">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="28037-146">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="28037-146">-ServerName</span></span>
<span data-ttu-id="28037-147">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="28037-147">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="28037-148">-Теги</span><span class="sxs-lookup"><span data-stu-id="28037-148">-Tags</span></span>
<span data-ttu-id="28037-149">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="28037-149">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="28037-150">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="28037-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="28037-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="28037-151">-Confirm</span></span>
<span data-ttu-id="28037-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="28037-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28037-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28037-153">-WhatIf</span></span>
<span data-ttu-id="28037-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="28037-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28037-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="28037-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28037-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28037-156">CommonParameters</span></span>
<span data-ttu-id="28037-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="28037-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28037-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28037-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28037-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="28037-159">INPUTS</span></span>

### <span data-ttu-id="28037-160">System. String</span><span class="sxs-lookup"><span data-stu-id="28037-160">System.String</span></span>

## <span data-ttu-id="28037-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="28037-161">OUTPUTS</span></span>

### <span data-ttu-id="28037-162">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="28037-162">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="28037-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="28037-163">NOTES</span></span>

## <span data-ttu-id="28037-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="28037-164">RELATED LINKS</span></span>

[<span data-ttu-id="28037-165">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="28037-165">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="28037-166">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="28037-166">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="28037-167">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="28037-167">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
