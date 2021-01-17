---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: e88deadc0a46aa5d89bd513a4aba1b93e22fbb5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409036"
---
# <span data-ttu-id="26458-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="26458-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="26458-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26458-102">SYNOPSIS</span></span>
<span data-ttu-id="26458-103">Обновив атрибуты учетной записи в ПараметрахDB.</span><span class="sxs-lookup"><span data-stu-id="26458-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="26458-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26458-104">SYNTAX</span></span>

### <span data-ttu-id="26458-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26458-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26458-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="26458-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26458-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="26458-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26458-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26458-108">DESCRIPTION</span></span>
<span data-ttu-id="26458-109">Обновив свойства учетной записи ВайссDB.</span><span class="sxs-lookup"><span data-stu-id="26458-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="26458-110">Не удается обновить регионы учетной записи одновременно с другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="26458-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="26458-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26458-111">EXAMPLES</span></span>

### <span data-ttu-id="26458-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26458-112">Example 1</span></span>
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

<span data-ttu-id="26458-113">Обновлено значение DefaultConsistencyLevel на "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations и Enabled VirtualNetwork forБ Учетная запись Скайп с именем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="26458-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="26458-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26458-114">PARAMETERS</span></span>

### <span data-ttu-id="26458-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26458-115">-AsJob</span></span>
<span data-ttu-id="26458-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="26458-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26458-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26458-117">-Confirm</span></span>
<span data-ttu-id="26458-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26458-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26458-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="26458-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="26458-120">Стандартный уровень согласованности для учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26458-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="26458-121">Принятые значения: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="26458-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="26458-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26458-122">-DefaultProfile</span></span>
<span data-ttu-id="26458-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26458-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26458-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="26458-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="26458-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров и пропускной способности) с помощью ключей учетных записей</span><span class="sxs-lookup"><span data-stu-id="26458-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="26458-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="26458-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="26458-127">Следует указать, включена ли в учетной записи аналитическая система аналитики.</span><span class="sxs-lookup"><span data-stu-id="26458-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="26458-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="26458-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="26458-129">Включает автоматический отбой области записи в редких случаях, когда регион недоступен из-за простоя.</span><span class="sxs-lookup"><span data-stu-id="26458-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="26458-130">При автоматическом отписи для учетной записи будет новый регион записи, который выбирается с учетом приоритетов отключки, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="26458-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="26458-131">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26458-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26458-132">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="26458-132">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="26458-133">Включить несколько мест записи.</span><span class="sxs-lookup"><span data-stu-id="26458-133">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="26458-134">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26458-134">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26458-135">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="26458-135">-EnableVirtualNetwork</span></span>
<span data-ttu-id="26458-136">Включает виртуальную сеть в учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26458-136">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="26458-137">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26458-137">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26458-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26458-138">-InputObject</span></span>
<span data-ttu-id="26458-139">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="26458-139">CosmosDB Account object</span></span>

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

### <span data-ttu-id="26458-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="26458-140">-IpRule</span></span>
<span data-ttu-id="26458-141">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="26458-141">Firewall support.</span></span> <span data-ttu-id="26458-142">Набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые нужно включить в список разрешенных IP-адресов клиентов для определенной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="26458-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="26458-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="26458-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="26458-144">URI of the KeyVault</span><span class="sxs-lookup"><span data-stu-id="26458-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="26458-145">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="26458-145">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="26458-146">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших данных (в периоде времени).</span><span class="sxs-lookup"><span data-stu-id="26458-146">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="26458-147">Диапазон для этого значения составляет 5–86400.</span><span class="sxs-lookup"><span data-stu-id="26458-147">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="26458-148">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="26458-148">-MaxStalenessPrefix</span></span>
<span data-ttu-id="26458-149">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших запросов.</span><span class="sxs-lookup"><span data-stu-id="26458-149">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="26458-150">Диапазон, который можно принимать для этого значения, составляет 1–2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="26458-150">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="26458-151">-Name</span><span class="sxs-lookup"><span data-stu-id="26458-151">-Name</span></span>
<span data-ttu-id="26458-152">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26458-152">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26458-153">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="26458-153">-PublicNetworkAccess</span></span>
<span data-ttu-id="26458-154">Разрешен ли доступ к общедоступным конечным точкам для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="26458-154">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="26458-155">Возможные значения: "Включено", "Отключено"</span><span class="sxs-lookup"><span data-stu-id="26458-155">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="26458-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26458-156">-ResourceGroupName</span></span>
<span data-ttu-id="26458-157">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26458-157">Name of resource group.</span></span>

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

### <span data-ttu-id="26458-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26458-158">-ResourceId</span></span>
<span data-ttu-id="26458-159">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="26458-159">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="26458-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="26458-160">-Tag</span></span>
<span data-ttu-id="26458-161">Теги в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="26458-161">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="26458-162">Для очистки существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="26458-162">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="26458-163">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="26458-163">-VirtualNetworkRule</span></span>
<span data-ttu-id="26458-164">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="26458-164">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="26458-165">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="26458-165">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="26458-166">Массив psVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="26458-166">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="26458-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26458-167">-WhatIf</span></span>
<span data-ttu-id="26458-168">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26458-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26458-169">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26458-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26458-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26458-170">CommonParameters</span></span>
<span data-ttu-id="26458-171">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26458-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26458-172">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26458-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26458-173">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26458-173">INPUTS</span></span>

### <span data-ttu-id="26458-174">Microsoft.Azure.Commands.ВацыDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="26458-174">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="26458-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26458-175">OUTPUTS</span></span>

### <span data-ttu-id="26458-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="26458-176">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="26458-177">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26458-177">NOTES</span></span>

## <span data-ttu-id="26458-178">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26458-178">RELATED LINKS</span></span>
