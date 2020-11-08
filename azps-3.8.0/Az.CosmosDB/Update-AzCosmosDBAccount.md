---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: a31df71a1242f4f4e9eb01a37d31eb54ec874a99
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065022"
---
# <span data-ttu-id="77abe-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="77abe-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="77abe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77abe-102">SYNOPSIS</span></span>
<span data-ttu-id="77abe-103">Обновите атрибуты учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="77abe-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="77abe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77abe-104">SYNTAX</span></span>

### <span data-ttu-id="77abe-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77abe-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount -ResourceGroupName <String> -Name <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77abe-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77abe-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77abe-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77abe-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccount> [-DefaultConsistencyLevel <String>]
 [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-IpRangeFilter <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-DisableKeyBasedMetadataWriteAccess <Boolean>]
 [-PublicNetworkAccess <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77abe-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77abe-108">DESCRIPTION</span></span>
<span data-ttu-id="77abe-109">Обновите свойства учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="77abe-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="77abe-110">Не удается обновить области счетов simulataneously с другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="77abe-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="77abe-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77abe-111">EXAMPLES</span></span>

### <span data-ttu-id="77abe-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="77abe-112">Example 1</span></span>
```powershell
PS C:\> Update-AzCosmosDBAccount -ResourceGroupName resourceGroupName -Name accountName -DefaultConsistencyLevel "Strong" -EnableAutomaticFailover 1 -EnableMultipleWriteLocations 1 -EnableVirtualNetwork 1

Kind                          : GlobalDocumentDB
ProvisioningState             : Initializing
DocumentEndpoint              :
DatabaseAccountOfferType      : Standard
IpRangeFilter                 :
IsVirtualNetworkFilterEnabled : True
EnableAutomaticFailover       : True
ConsistencyPolicy             : Microsoft.Azure.Management.CosmosDB.Fluent.Models.ConsistencyPolicy
Capabilities                  : {}
WriteLocations                : {accountName-eastus}
ReadLocations                 : {accountName-eastus}
FailoverPolicies              : {accountName-eastus}
VirtualNetworkRules           : {}
EnableMultipleWriteLocations  : True
Location                      : East US
Tags                          : {}
Id                            : /subscriptions/{subscriptionid}/resourceGroups/resourceGroupName/providers/Microsoft.DocumentDB/databaseAccounts/accountName
Name                          : accountName
Type                          : Microsoft.DocumentDB/databaseAccounts
```

<span data-ttu-id="77abe-113">Обновлен DefaultConsistencyLevel на "strong", включены AutomaticFailover, включенные MultipleWriteLocations и Enabled VirtualNetwork для CosmosDB учетной записи с именем accountName.</span><span class="sxs-lookup"><span data-stu-id="77abe-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="77abe-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77abe-114">PARAMETERS</span></span>

### <span data-ttu-id="77abe-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77abe-115">-AsJob</span></span>
<span data-ttu-id="77abe-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="77abe-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77abe-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="77abe-117">-Confirm</span></span>
<span data-ttu-id="77abe-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="77abe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77abe-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="77abe-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="77abe-120">Уровень согласованности по умолчанию для учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="77abe-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="77abe-121">Допустимые значения: BoundedStaleness, ConsistentPrefix,,,,,,,, сессия, сеанс, прочее</span><span class="sxs-lookup"><span data-stu-id="77abe-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="77abe-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77abe-122">-DefaultProfile</span></span>
<span data-ttu-id="77abe-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77abe-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77abe-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="77abe-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="77abe-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров, пропускной способности) с помощью ключей учетной записи</span><span class="sxs-lookup"><span data-stu-id="77abe-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-126">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="77abe-126">-EnableAutomaticFailover</span></span>
<span data-ttu-id="77abe-127">Включает автоматический переход области ввода в редких случаях, когда область недоступна из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="77abe-127">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="77abe-128">Автоматический переход на другой ресурс приведет к новому региону записи для учетной записи и будет выбран на основе приоритетов перемещения при сбое, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="77abe-128">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="77abe-129">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="77abe-129">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-130">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="77abe-130">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="77abe-131">Включите несколько местоположений для ввода.</span><span class="sxs-lookup"><span data-stu-id="77abe-131">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="77abe-132">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="77abe-132">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-133">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="77abe-133">-EnableVirtualNetwork</span></span>
<span data-ttu-id="77abe-134">Включает виртуальную сеть в учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="77abe-134">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="77abe-135">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="77abe-135">Accepted values: false, true</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-136">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77abe-136">-InputObject</span></span>
<span data-ttu-id="77abe-137">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="77abe-137">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccount
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-138">-IpRangeFilter</span><span class="sxs-lookup"><span data-stu-id="77abe-138">-IpRangeFilter</span></span>
<span data-ttu-id="77abe-139">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="77abe-139">Firewall support.</span></span>
<span data-ttu-id="77abe-140">Указывает набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые должны быть включены в список разрешенных клиентских IP-адресах для указанной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="77abe-140">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account</span></span>

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

### <span data-ttu-id="77abe-141">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="77abe-141">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="77abe-142">Это значение представляет время, в течение которого допускается устаревшая версия (в TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="77abe-142">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="77abe-143">Допустимый диапазон для этого значения — 5-86400.</span><span class="sxs-lookup"><span data-stu-id="77abe-143">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="77abe-144">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="77abe-144">-MaxStalenessPrefix</span></span>
<span data-ttu-id="77abe-145">Это значение представляет собой количество устаревших запросов, которые можно использовать для согласованности ограниченных устаревших значений.</span><span class="sxs-lookup"><span data-stu-id="77abe-145">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="77abe-146">Допустимый диапазон для этого значения: 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="77abe-146">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="77abe-147">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="77abe-147">-Name</span></span>
<span data-ttu-id="77abe-148">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="77abe-148">Name of the Cosmos DB database account.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-149">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="77abe-149">-PublicNetworkAccess</span></span>
<span data-ttu-id="77abe-150">Разрешено ли доступ к общедоступной конечной точке для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="77abe-150">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="77abe-151">Возможные значения: "включено", "отключено"</span><span class="sxs-lookup"><span data-stu-id="77abe-151">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="77abe-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77abe-152">-ResourceGroupName</span></span>
<span data-ttu-id="77abe-153">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="77abe-153">Name of resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77abe-154">-ResourceId</span></span>
<span data-ttu-id="77abe-155">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="77abe-155">ResourceId of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="77abe-156">-Tag</span></span>
<span data-ttu-id="77abe-157">Хэш-таблицы тегов в виде пар "ключ — значение".</span><span class="sxs-lookup"><span data-stu-id="77abe-157">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="77abe-158">Для удаления существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="77abe-158">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="77abe-159">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="77abe-159">-VirtualNetworkRule</span></span>
<span data-ttu-id="77abe-160">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="77abe-160">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="77abe-161">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="77abe-161">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="77abe-162">Массив PSVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="77abe-162">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77abe-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77abe-163">-WhatIf</span></span>
<span data-ttu-id="77abe-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="77abe-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77abe-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="77abe-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77abe-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77abe-166">CommonParameters</span></span>
<span data-ttu-id="77abe-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77abe-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77abe-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77abe-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77abe-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77abe-169">INPUTS</span></span>

### <span data-ttu-id="77abe-170">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="77abe-170">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="77abe-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77abe-171">OUTPUTS</span></span>

### <span data-ttu-id="77abe-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="77abe-172">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="77abe-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="77abe-173">NOTES</span></span>

## <span data-ttu-id="77abe-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77abe-174">RELATED LINKS</span></span>
