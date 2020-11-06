---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557047"
---
# <span data-ttu-id="29911-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29911-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="29911-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29911-102">SYNOPSIS</span></span>
<span data-ttu-id="29911-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="29911-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29911-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29911-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="29911-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29911-105">DESCRIPTION</span></span>
<span data-ttu-id="29911-106">Командлет **New-AzureRMSqlDatabaseSecondary** заменяет командлет Start-AzureSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="29911-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="29911-107">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="29911-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="29911-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29911-108">EXAMPLES</span></span>

### <span data-ttu-id="29911-109">1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="29911-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="29911-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29911-110">PARAMETERS</span></span>

### <span data-ttu-id="29911-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="29911-111">-AllowConnections</span></span>
<span data-ttu-id="29911-112">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="29911-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="29911-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="29911-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="29911-114">Нет</span><span class="sxs-lookup"><span data-stu-id="29911-114">No</span></span>
- <span data-ttu-id="29911-115">Весь</span><span class="sxs-lookup"><span data-stu-id="29911-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29911-116">-AsJob</span></span>
<span data-ttu-id="29911-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="29911-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29911-118">-DatabaseName</span></span>
<span data-ttu-id="29911-119">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="29911-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29911-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29911-120">-DefaultProfile</span></span>
<span data-ttu-id="29911-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="29911-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29911-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="29911-123">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="29911-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="29911-124">-PartnerServerName</span></span>
<span data-ttu-id="29911-125">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="29911-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29911-126">-ResourceGroupName</span></span>
<span data-ttu-id="29911-127">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="29911-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29911-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="29911-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="29911-129">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="29911-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="29911-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="29911-131">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="29911-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="29911-132">-ServerName</span></span>
<span data-ttu-id="29911-133">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="29911-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29911-134">-Теги</span><span class="sxs-lookup"><span data-stu-id="29911-134">-Tags</span></span>
<span data-ttu-id="29911-135">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="29911-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="29911-136">Например:</span><span class="sxs-lookup"><span data-stu-id="29911-136">For example:</span></span>

<span data-ttu-id="29911-137">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="29911-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29911-138">-Confirm</span></span>
<span data-ttu-id="29911-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29911-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29911-140">-WhatIf</span></span>
<span data-ttu-id="29911-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29911-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29911-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29911-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29911-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29911-143">CommonParameters</span></span>
<span data-ttu-id="29911-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29911-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29911-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29911-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29911-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29911-146">INPUTS</span></span>

### <span data-ttu-id="29911-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="29911-147">None</span></span>
<span data-ttu-id="29911-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="29911-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29911-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29911-149">OUTPUTS</span></span>

### <span data-ttu-id="29911-150">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="29911-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="29911-151">Этот командлет возвращает объекты **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="29911-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="29911-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="29911-152">NOTES</span></span>

## <span data-ttu-id="29911-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29911-153">RELATED LINKS</span></span>

[<span data-ttu-id="29911-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29911-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="29911-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="29911-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="29911-156">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="29911-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
