---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: e39239b7434d61642ad5fcfc1f487ac5bbc5829a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728895"
---
# <span data-ttu-id="207b1-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="207b1-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="207b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="207b1-102">SYNOPSIS</span></span>
<span data-ttu-id="207b1-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="207b1-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="207b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="207b1-104">SYNTAX</span></span>

### <span data-ttu-id="207b1-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="207b1-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="207b1-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="207b1-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="207b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="207b1-107">DESCRIPTION</span></span>
<span data-ttu-id="207b1-108">Командлет **New-AzSqlDatabaseSecondary** заменяет командлет Start-AzSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="207b1-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="207b1-109">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="207b1-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="207b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="207b1-110">EXAMPLES</span></span>

### <span data-ttu-id="207b1-111">1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="207b1-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="207b1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="207b1-112">PARAMETERS</span></span>

### <span data-ttu-id="207b1-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="207b1-113">-AllowConnections</span></span>
<span data-ttu-id="207b1-114">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="207b1-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="207b1-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="207b1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="207b1-116">Нет</span><span class="sxs-lookup"><span data-stu-id="207b1-116">No</span></span>
- <span data-ttu-id="207b1-117">Весь</span><span class="sxs-lookup"><span data-stu-id="207b1-117">All</span></span>

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

### <span data-ttu-id="207b1-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="207b1-118">-AsJob</span></span>
<span data-ttu-id="207b1-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="207b1-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="207b1-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="207b1-120">-DatabaseName</span></span>
<span data-ttu-id="207b1-121">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="207b1-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="207b1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="207b1-122">-DefaultProfile</span></span>
<span data-ttu-id="207b1-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="207b1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="207b1-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="207b1-124">-LicenseType</span></span>
<span data-ttu-id="207b1-125">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="207b1-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="207b1-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="207b1-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="207b1-127">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="207b1-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="207b1-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="207b1-128">-PartnerServerName</span></span>
<span data-ttu-id="207b1-129">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="207b1-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="207b1-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="207b1-130">-ResourceGroupName</span></span>
<span data-ttu-id="207b1-131">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="207b1-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="207b1-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="207b1-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="207b1-133">Вычислено Создание вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="207b1-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="207b1-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="207b1-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="207b1-135">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="207b1-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="207b1-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="207b1-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="207b1-137">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="207b1-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="207b1-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="207b1-138">-SecondaryVCore</span></span>
<span data-ttu-id="207b1-139">Vcore номера вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="207b1-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="207b1-140">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="207b1-140">-ServerName</span></span>
<span data-ttu-id="207b1-141">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="207b1-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="207b1-142">-Теги</span><span class="sxs-lookup"><span data-stu-id="207b1-142">-Tags</span></span>
<span data-ttu-id="207b1-143">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="207b1-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="207b1-144">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="207b1-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="207b1-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="207b1-145">-Confirm</span></span>
<span data-ttu-id="207b1-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="207b1-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="207b1-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="207b1-147">-WhatIf</span></span>
<span data-ttu-id="207b1-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="207b1-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="207b1-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="207b1-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="207b1-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="207b1-150">CommonParameters</span></span>
<span data-ttu-id="207b1-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="207b1-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="207b1-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="207b1-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="207b1-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="207b1-153">INPUTS</span></span>

### <span data-ttu-id="207b1-154">System. String</span><span class="sxs-lookup"><span data-stu-id="207b1-154">System.String</span></span>

## <span data-ttu-id="207b1-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="207b1-155">OUTPUTS</span></span>

### <span data-ttu-id="207b1-156">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="207b1-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="207b1-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="207b1-157">NOTES</span></span>

## <span data-ttu-id="207b1-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="207b1-158">RELATED LINKS</span></span>

[<span data-ttu-id="207b1-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="207b1-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="207b1-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="207b1-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="207b1-161">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="207b1-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
