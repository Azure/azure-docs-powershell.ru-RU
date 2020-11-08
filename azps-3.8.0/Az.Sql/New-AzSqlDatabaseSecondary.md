---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066938"
---
# <span data-ttu-id="5fd0f-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5fd0f-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="5fd0f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fd0f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fd0f-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="5fd0f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fd0f-104">SYNTAX</span></span>

### <span data-ttu-id="5fd0f-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5fd0f-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fd0f-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="5fd0f-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fd0f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-107">DESCRIPTION</span></span>
<span data-ttu-id="5fd0f-108">Командлет **New-AzSqlDatabaseSecondary** заменяет командлет Start-AzSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="5fd0f-109">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="5fd0f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-110">EXAMPLES</span></span>

### <span data-ttu-id="5fd0f-111">1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="5fd0f-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="5fd0f-112">2. Установка активного Geo-Replication и указание имени базы данных партнера, которое отличается от имени исходной базы данных.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="5fd0f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-113">PARAMETERS</span></span>

### <span data-ttu-id="5fd0f-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="5fd0f-114">-AllowConnections</span></span>
<span data-ttu-id="5fd0f-115">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="5fd0f-116">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5fd0f-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5fd0f-117">Нет</span><span class="sxs-lookup"><span data-stu-id="5fd0f-117">No</span></span>
- <span data-ttu-id="5fd0f-118">Весь</span><span class="sxs-lookup"><span data-stu-id="5fd0f-118">All</span></span>

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

### <span data-ttu-id="5fd0f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5fd0f-119">-AsJob</span></span>
<span data-ttu-id="5fd0f-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5fd0f-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5fd0f-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-121">-DatabaseName</span></span>
<span data-ttu-id="5fd0f-122">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="5fd0f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fd0f-123">-DefaultProfile</span></span>
<span data-ttu-id="5fd0f-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5fd0f-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5fd0f-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5fd0f-125">-LicenseType</span></span>
<span data-ttu-id="5fd0f-126">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="5fd0f-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="5fd0f-128">Имя создаваемой базы данных получателя.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="5fd0f-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="5fd0f-130">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="5fd0f-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-131">-PartnerServerName</span></span>
<span data-ttu-id="5fd0f-132">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="5fd0f-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-133">-ResourceGroupName</span></span>
<span data-ttu-id="5fd0f-134">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="5fd0f-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="5fd0f-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="5fd0f-136">Вычислено Создание вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="5fd0f-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="5fd0f-138">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="5fd0f-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="5fd0f-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="5fd0f-140">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="5fd0f-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="5fd0f-141">-SecondaryVCore</span></span>
<span data-ttu-id="5fd0f-142">Vcore номера вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="5fd0f-143">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="5fd0f-143">-ServerName</span></span>
<span data-ttu-id="5fd0f-144">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="5fd0f-145">-Теги</span><span class="sxs-lookup"><span data-stu-id="5fd0f-145">-Tags</span></span>
<span data-ttu-id="5fd0f-146">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="5fd0f-147">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5fd0f-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5fd0f-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5fd0f-148">-Confirm</span></span>
<span data-ttu-id="5fd0f-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fd0f-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fd0f-150">-WhatIf</span></span>
<span data-ttu-id="5fd0f-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fd0f-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fd0f-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fd0f-153">CommonParameters</span></span>
<span data-ttu-id="5fd0f-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fd0f-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fd0f-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5fd0f-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fd0f-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fd0f-156">INPUTS</span></span>

### <span data-ttu-id="5fd0f-157">System. String</span><span class="sxs-lookup"><span data-stu-id="5fd0f-157">System.String</span></span>

## <span data-ttu-id="5fd0f-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-158">OUTPUTS</span></span>

### <span data-ttu-id="5fd0f-159">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="5fd0f-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="5fd0f-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fd0f-160">NOTES</span></span>

## <span data-ttu-id="5fd0f-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fd0f-161">RELATED LINKS</span></span>

[<span data-ttu-id="5fd0f-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5fd0f-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="5fd0f-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="5fd0f-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="5fd0f-164">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="5fd0f-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
