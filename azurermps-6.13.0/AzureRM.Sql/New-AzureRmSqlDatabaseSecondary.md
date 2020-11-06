---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562564"
---
# <span data-ttu-id="2c401-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c401-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="2c401-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2c401-102">SYNOPSIS</span></span>
<span data-ttu-id="2c401-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="2c401-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c401-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2c401-104">SYNTAX</span></span>

### <span data-ttu-id="2c401-105">DtuBasedDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c401-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c401-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="2c401-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c401-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c401-107">DESCRIPTION</span></span>
<span data-ttu-id="2c401-108">Командлет **New-AzureRMSqlDatabaseSecondary** заменяет командлет Start-AzureSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="2c401-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="2c401-109">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="2c401-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="2c401-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2c401-110">EXAMPLES</span></span>

### <span data-ttu-id="2c401-111">1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="2c401-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="2c401-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2c401-112">PARAMETERS</span></span>

### <span data-ttu-id="2c401-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="2c401-113">-AllowConnections</span></span>
<span data-ttu-id="2c401-114">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c401-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="2c401-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="2c401-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2c401-116">Нет</span><span class="sxs-lookup"><span data-stu-id="2c401-116">No</span></span>
- <span data-ttu-id="2c401-117">Весь</span><span class="sxs-lookup"><span data-stu-id="2c401-117">All</span></span>

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

### <span data-ttu-id="2c401-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2c401-118">-AsJob</span></span>
<span data-ttu-id="2c401-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2c401-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2c401-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c401-120">-DatabaseName</span></span>
<span data-ttu-id="2c401-121">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="2c401-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="2c401-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c401-122">-DefaultProfile</span></span>
<span data-ttu-id="2c401-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2c401-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c401-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="2c401-124">-LicenseType</span></span>
<span data-ttu-id="2c401-125">Тип лицензии для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c401-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="2c401-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c401-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="2c401-127">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="2c401-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="2c401-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="2c401-128">-PartnerServerName</span></span>
<span data-ttu-id="2c401-129">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="2c401-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="2c401-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c401-130">-ResourceGroupName</span></span>
<span data-ttu-id="2c401-131">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="2c401-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="2c401-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="2c401-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="2c401-133">Вычислено Создание вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c401-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="2c401-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="2c401-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="2c401-135">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="2c401-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="2c401-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="2c401-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="2c401-137">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="2c401-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="2c401-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="2c401-138">-SecondaryVCore</span></span>
<span data-ttu-id="2c401-139">Vcore номера вторичной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="2c401-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="2c401-140">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="2c401-140">-ServerName</span></span>
<span data-ttu-id="2c401-141">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2c401-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="2c401-142">-Теги</span><span class="sxs-lookup"><span data-stu-id="2c401-142">-Tags</span></span>
<span data-ttu-id="2c401-143">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="2c401-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="2c401-144">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2c401-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2c401-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c401-145">-Confirm</span></span>
<span data-ttu-id="2c401-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2c401-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c401-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c401-147">-WhatIf</span></span>
<span data-ttu-id="2c401-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2c401-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c401-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2c401-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c401-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c401-150">CommonParameters</span></span>
<span data-ttu-id="2c401-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2c401-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c401-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c401-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c401-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2c401-153">INPUTS</span></span>

### <span data-ttu-id="2c401-154">System. String</span><span class="sxs-lookup"><span data-stu-id="2c401-154">System.String</span></span>

## <span data-ttu-id="2c401-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c401-155">OUTPUTS</span></span>

### <span data-ttu-id="2c401-156">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="2c401-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="2c401-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="2c401-157">NOTES</span></span>

## <span data-ttu-id="2c401-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c401-158">RELATED LINKS</span></span>

[<span data-ttu-id="2c401-159">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c401-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="2c401-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="2c401-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="2c401-161">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="2c401-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
