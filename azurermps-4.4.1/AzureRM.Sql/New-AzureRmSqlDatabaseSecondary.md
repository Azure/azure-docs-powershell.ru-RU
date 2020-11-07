---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732190"
---
# <span data-ttu-id="798c0-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="798c0-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="798c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="798c0-102">SYNOPSIS</span></span>
<span data-ttu-id="798c0-103">Создает базу данных-получатель для существующей базы данных и запускает репликацию данных.</span><span class="sxs-lookup"><span data-stu-id="798c0-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="798c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="798c0-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="798c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="798c0-105">DESCRIPTION</span></span>
<span data-ttu-id="798c0-106">Командлет **New-AzureRMSqlDatabaseSecondary** заменяет командлет Start-AzureSqlDatabaseCopy при использовании для настройки георепликации для базы данных.</span><span class="sxs-lookup"><span data-stu-id="798c0-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="798c0-107">Он возвращает объект ссылки Geo-Replication из источника в базу данных-получатель.</span><span class="sxs-lookup"><span data-stu-id="798c0-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="798c0-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="798c0-108">EXAMPLES</span></span>

### <span data-ttu-id="798c0-109">1: Установка активного Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="798c0-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="798c0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="798c0-110">PARAMETERS</span></span>

### <span data-ttu-id="798c0-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="798c0-111">-AllowConnections</span></span>
<span data-ttu-id="798c0-112">Указывает цель чтения для вспомогательной базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="798c0-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="798c0-113">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="798c0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="798c0-114">Нет</span><span class="sxs-lookup"><span data-stu-id="798c0-114">No</span></span>
- <span data-ttu-id="798c0-115">Весь</span><span class="sxs-lookup"><span data-stu-id="798c0-115">All</span></span>

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

### <span data-ttu-id="798c0-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="798c0-116">-DatabaseName</span></span>
<span data-ttu-id="798c0-117">Указывает имя базы данных, которая будет выступать в качестве основного.</span><span class="sxs-lookup"><span data-stu-id="798c0-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="798c0-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798c0-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="798c0-119">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="798c0-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="798c0-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="798c0-120">-PartnerServerName</span></span>
<span data-ttu-id="798c0-121">Указывает имя сервера базы данных SQL Azure, который будет выступать в качестве получателя.</span><span class="sxs-lookup"><span data-stu-id="798c0-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="798c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="798c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="798c0-123">Указывает имя группы ресурсов Azure, к которой этот командлет назначает базу данных PRIMARY.</span><span class="sxs-lookup"><span data-stu-id="798c0-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="798c0-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="798c0-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="798c0-125">Указывает имя эластичного пула, в который нужно разместить базу данных получателя.</span><span class="sxs-lookup"><span data-stu-id="798c0-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="798c0-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="798c0-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="798c0-127">Указывает имя цели обслуживания, назначаемой базе данных получателя.</span><span class="sxs-lookup"><span data-stu-id="798c0-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="798c0-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="798c0-128">-ServerName</span></span>
<span data-ttu-id="798c0-129">Указывает имя SQL Server основной базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="798c0-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="798c0-130">-Теги</span><span class="sxs-lookup"><span data-stu-id="798c0-130">-Tags</span></span>
<span data-ttu-id="798c0-131">Определяет пары "ключ-значение" в форме хэш-таблицы, которую нужно связать с ссылкой для репликации базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="798c0-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="798c0-132">Например:</span><span class="sxs-lookup"><span data-stu-id="798c0-132">For example:</span></span>

<span data-ttu-id="798c0-133">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="798c0-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="798c0-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="798c0-134">-Confirm</span></span>
<span data-ttu-id="798c0-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="798c0-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="798c0-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="798c0-136">-WhatIf</span></span>
<span data-ttu-id="798c0-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="798c0-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="798c0-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="798c0-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="798c0-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="798c0-139">-DefaultProfile</span></span>
<span data-ttu-id="798c0-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="798c0-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="798c0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="798c0-141">CommonParameters</span></span>
<span data-ttu-id="798c0-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="798c0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="798c0-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="798c0-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="798c0-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="798c0-144">INPUTS</span></span>

## <span data-ttu-id="798c0-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="798c0-145">OUTPUTS</span></span>

### <span data-ttu-id="798c0-146">Microsoft. Azure. Commands. SQL. Replication. Model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="798c0-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="798c0-147">Этот командлет возвращает объекты **ReplicationLink** .</span><span class="sxs-lookup"><span data-stu-id="798c0-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="798c0-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="798c0-148">NOTES</span></span>

## <span data-ttu-id="798c0-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="798c0-149">RELATED LINKS</span></span>

[<span data-ttu-id="798c0-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="798c0-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="798c0-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="798c0-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="798c0-152">Документация по базам данных SQL</span><span class="sxs-lookup"><span data-stu-id="798c0-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
