---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236845"
---
# <span data-ttu-id="1d8ac-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="1d8ac-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="1d8ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="1d8ac-103">Обновите атрибуты учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="1d8ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d8ac-104">SYNTAX</span></span>

### <span data-ttu-id="1d8ac-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d8ac-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8ac-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d8ac-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d8ac-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d8ac-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d8ac-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8ac-108">DESCRIPTION</span></span>
<span data-ttu-id="1d8ac-109">Обновите свойства учетной записи CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="1d8ac-110">Не удается обновить области счетов simulataneously с другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="1d8ac-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d8ac-111">EXAMPLES</span></span>

### <span data-ttu-id="1d8ac-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d8ac-112">Example 1</span></span>
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

<span data-ttu-id="1d8ac-113">Обновлен DefaultConsistencyLevel на "strong", включены AutomaticFailover, включенные MultipleWriteLocations и Enabled VirtualNetwork для CosmosDB учетной записи с именем accountName.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="1d8ac-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d8ac-114">PARAMETERS</span></span>

### <span data-ttu-id="1d8ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1d8ac-115">-AsJob</span></span>
<span data-ttu-id="1d8ac-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1d8ac-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d8ac-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d8ac-117">-Confirm</span></span>
<span data-ttu-id="1d8ac-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d8ac-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="1d8ac-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="1d8ac-120">Уровень согласованности по умолчанию для учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="1d8ac-121">Допустимые значения: BoundedStaleness, ConsistentPrefix,,,,,,,, сессия, сеанс, прочее</span><span class="sxs-lookup"><span data-stu-id="1d8ac-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="1d8ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d8ac-122">-DefaultProfile</span></span>
<span data-ttu-id="1d8ac-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d8ac-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="1d8ac-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="1d8ac-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров, пропускной способности) с помощью ключей учетной записи</span><span class="sxs-lookup"><span data-stu-id="1d8ac-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="1d8ac-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="1d8ac-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="1d8ac-127">Логическое значение, определяющее, включена ли AnalyticalStorage для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="1d8ac-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="1d8ac-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="1d8ac-129">Включает автоматический переход области ввода в редких случаях, когда область недоступна из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="1d8ac-130">Автоматический переход на другой ресурс приведет к новому региону записи для учетной записи и будет выбран на основе приоритетов перемещения при сбое, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="1d8ac-131">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="1d8ac-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="1d8ac-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="1d8ac-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="1d8ac-133">Включите несколько местоположений для ввода.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="1d8ac-134">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="1d8ac-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="1d8ac-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1d8ac-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="1d8ac-136">Включает виртуальную сеть в учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="1d8ac-137">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="1d8ac-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="1d8ac-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d8ac-138">-InputObject</span></span>
<span data-ttu-id="1d8ac-139">Объект учетной записи CosmosDB</span><span class="sxs-lookup"><span data-stu-id="1d8ac-139">CosmosDB Account object</span></span>

```yaml
Type: PSDatabaseAccountGetResults
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d8ac-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="1d8ac-140">-IpRule</span></span>
<span data-ttu-id="1d8ac-141">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-141">Firewall support.</span></span> <span data-ttu-id="1d8ac-142">Указывает набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые должны быть включены в список разрешенных адресов клиентов для данной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="1d8ac-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="1d8ac-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="1d8ac-144">Универсальный код ресурса (URI) KeyVault</span><span class="sxs-lookup"><span data-stu-id="1d8ac-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="1d8ac-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d8ac-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="1d8ac-146">Это значение представляет время, в течение которого допускается устаревшая версия (в TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="1d8ac-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="1d8ac-147">Допустимый диапазон для этого значения — 5-86400.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="1d8ac-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="1d8ac-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="1d8ac-149">Это значение представляет собой количество устаревших запросов, которые можно использовать для согласованности ограниченных устаревших значений.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="1d8ac-150">Допустимый диапазон для этого значения: 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="1d8ac-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d8ac-151">-Name</span></span>
<span data-ttu-id="1d8ac-152">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="1d8ac-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="1d8ac-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="1d8ac-154">Разрешено ли доступ к общедоступной конечной точке для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="1d8ac-155">Возможные значения: "включено", "отключено"</span><span class="sxs-lookup"><span data-stu-id="1d8ac-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="1d8ac-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d8ac-156">-ResourceGroupName</span></span>
<span data-ttu-id="1d8ac-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-157">Name of resource group.</span></span>

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

### <span data-ttu-id="1d8ac-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d8ac-158">-ResourceId</span></span>
<span data-ttu-id="1d8ac-159">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="1d8ac-160">-Тег</span><span class="sxs-lookup"><span data-stu-id="1d8ac-160">-Tag</span></span>
<span data-ttu-id="1d8ac-161">Хэш-таблицы тегов в виде пар "ключ — значение".</span><span class="sxs-lookup"><span data-stu-id="1d8ac-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="1d8ac-162">Для удаления существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="1d8ac-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1d8ac-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="1d8ac-164">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="1d8ac-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1d8ac-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="1d8ac-166">Массив PSVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="1d8ac-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d8ac-167">-WhatIf</span></span>
<span data-ttu-id="1d8ac-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d8ac-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d8ac-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d8ac-170">CommonParameters</span></span>
<span data-ttu-id="1d8ac-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d8ac-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d8ac-172">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d8ac-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d8ac-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d8ac-173">INPUTS</span></span>

### <span data-ttu-id="1d8ac-174">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="1d8ac-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="1d8ac-175">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d8ac-175">OUTPUTS</span></span>

### <span data-ttu-id="1d8ac-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="1d8ac-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="1d8ac-177">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d8ac-177">NOTES</span></span>

## <span data-ttu-id="1d8ac-178">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d8ac-178">RELATED LINKS</span></span>
