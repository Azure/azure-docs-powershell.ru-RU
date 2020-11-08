---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 76df37703882e799eb42542cd08d105f62787419
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072565"
---
# <span data-ttu-id="0ca51-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="0ca51-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="0ca51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0ca51-102">SYNOPSIS</span></span>
<span data-ttu-id="0ca51-103">Создайте новую учетную запись CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="0ca51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0ca51-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork] [-IpRangeFilter <String[]>]
 [-Location <String[]>] [-LocationObject <PSLocation[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-ApiKind <String>] [-PublicNetworkAccess <String>]
 [-DisableKeyBasedMetadataWriteAccess] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ca51-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ca51-105">DESCRIPTION</span></span>
<span data-ttu-id="0ca51-106">Создание новой учетной записи CosmosDB в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ca51-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="0ca51-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0ca51-107">EXAMPLES</span></span>

### <span data-ttu-id="0ca51-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ca51-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name databaseAccountName  -Location "East US"

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : False
EnableAutomaticFailover       : False
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {databaseAccountName-eastus}
ReadLocations                 : {databaseAccountName-eastus}
FailoverPolicies              : {databaseAccountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : False
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/databaseAccountName
Name                          : databaseAccountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="0ca51-109">Новая учетная запись CosmosDB с именем databaseAccountName создается в разделе ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="0ca51-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="0ca51-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0ca51-110">PARAMETERS</span></span>

### <span data-ttu-id="0ca51-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="0ca51-111">-ApiKind</span></span>
<span data-ttu-id="0ca51-112">Тип создаваемой учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="0ca51-113">Допустимые значения: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="0ca51-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="0ca51-114">Значение по умолчанию: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="0ca51-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="0ca51-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ca51-115">-AsJob</span></span>
<span data-ttu-id="0ca51-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0ca51-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0ca51-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0ca51-117">-Confirm</span></span>
<span data-ttu-id="0ca51-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0ca51-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="0ca51-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="0ca51-120">Уровень согласованности по умолчанию для учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="0ca51-121">Допустимые значения: BoundedStaleness, ConsistentPrefix,,,,,,,, сессия, сеанс, прочее</span><span class="sxs-lookup"><span data-stu-id="0ca51-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="0ca51-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ca51-122">-DefaultProfile</span></span>
<span data-ttu-id="0ca51-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ca51-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="0ca51-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="0ca51-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров, пропускной способности) с помощью ключей учетной записи</span><span class="sxs-lookup"><span data-stu-id="0ca51-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="0ca51-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="0ca51-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="0ca51-127">Включает автоматический переход области ввода в редких случаях, когда область недоступна из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="0ca51-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="0ca51-128">Автоматический переход на другой ресурс приведет к новому региону записи для учетной записи и будет выбран на основе приоритетов перемещения при сбое, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0ca51-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="0ca51-129">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="0ca51-129">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0ca51-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="0ca51-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="0ca51-131">Включите несколько местоположений для ввода.</span><span class="sxs-lookup"><span data-stu-id="0ca51-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="0ca51-132">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="0ca51-132">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0ca51-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0ca51-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="0ca51-134">Включает виртуальную сеть в учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="0ca51-135">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="0ca51-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="0ca51-136">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="0ca51-136">-IpRangeFilter</span></span>
<span data-ttu-id="0ca51-137">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="0ca51-137">Firewall support.</span></span>
<span data-ttu-id="0ca51-138">Указывает набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые должны быть включены в список разрешенных клиентских IP-адресах для указанной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="0ca51-138">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-139">-Location</span><span class="sxs-lookup"><span data-stu-id="0ca51-139">-Location</span></span>
<span data-ttu-id="0ca51-140">Добавьте расположение в учетную запись базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-140">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="0ca51-141">Массив строк, упорядоченный по приоритету отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="0ca51-141">Array of strings, ordered by failover priority.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-142">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="0ca51-142">-LocationObject</span></span>
<span data-ttu-id="0ca51-143">Добавьте расположение в учетную запись базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-143">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="0ca51-144">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="0ca51-144">Array of PSLocation objects.</span></span>

```yaml
Type: PSLocation[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="0ca51-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="0ca51-146">Это значение представляет время, в течение которого допускается устаревшая версия (в TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="0ca51-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="0ca51-147">Допустимый диапазон для этого значения — 5-86400.</span><span class="sxs-lookup"><span data-stu-id="0ca51-147">Accepted range for this value is 5-86400.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="0ca51-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="0ca51-149">Это значение представляет собой количество устаревших запросов, которые можно использовать для согласованности ограниченных устаревших значений.</span><span class="sxs-lookup"><span data-stu-id="0ca51-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="0ca51-150">Допустимый диапазон для этого значения: 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="0ca51-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0ca51-151">-Name</span></span>
<span data-ttu-id="0ca51-152">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="0ca51-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="0ca51-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0ca51-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="0ca51-154">Разрешено ли доступ к общедоступной конечной точке для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="0ca51-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="0ca51-155">Возможные значения: "включено", "отключено"</span><span class="sxs-lookup"><span data-stu-id="0ca51-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="0ca51-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ca51-156">-ResourceGroupName</span></span>
<span data-ttu-id="0ca51-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0ca51-157">Name of resource group.</span></span>

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

### <span data-ttu-id="0ca51-158">-Тег</span><span class="sxs-lookup"><span data-stu-id="0ca51-158">-Tag</span></span>
<span data-ttu-id="0ca51-159">Хэш-таблицы тегов в виде пар "ключ — значение".</span><span class="sxs-lookup"><span data-stu-id="0ca51-159">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="0ca51-160">Для удаления существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="0ca51-160">Use empty string to clear existing tag.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-161">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0ca51-161">-VirtualNetworkRule</span></span>
<span data-ttu-id="0ca51-162">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0ca51-162">Array of string values of ACL's for virtual network.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-163">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="0ca51-163">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="0ca51-164">Массив PSVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0ca51-164">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ca51-165">-WhatIf</span></span>
<span data-ttu-id="0ca51-166">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0ca51-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ca51-167">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0ca51-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ca51-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ca51-168">CommonParameters</span></span>
<span data-ttu-id="0ca51-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0ca51-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ca51-170">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ca51-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ca51-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0ca51-171">INPUTS</span></span>

### <span data-ttu-id="0ca51-172">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="0ca51-172">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="0ca51-173">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ca51-173">OUTPUTS</span></span>

### <span data-ttu-id="0ca51-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="0ca51-174">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="0ca51-175">Пуск</span><span class="sxs-lookup"><span data-stu-id="0ca51-175">NOTES</span></span>

## <span data-ttu-id="0ca51-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ca51-176">RELATED LINKS</span></span>
