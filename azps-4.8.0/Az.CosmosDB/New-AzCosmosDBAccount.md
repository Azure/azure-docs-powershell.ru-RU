---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: f082f9390dd5a00fa5984aa2e0df26e8c3b63636
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079757"
---
# <span data-ttu-id="3f329-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="3f329-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="3f329-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f329-102">SYNOPSIS</span></span>
<span data-ttu-id="3f329-103">Создайте новую учетную запись CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="3f329-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="3f329-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f329-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>]
 [-ServerVersion <String>] [-Location <String[]>] [-LocationObject <PSLocation[]>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f329-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f329-105">DESCRIPTION</span></span>
<span data-ttu-id="3f329-106">Создание новой учетной записи CosmosDB в заданной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f329-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="3f329-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f329-107">EXAMPLES</span></span>

### <span data-ttu-id="3f329-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f329-108">Example 1</span></span>
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

<span data-ttu-id="3f329-109">Новая учетная запись CosmosDB с именем databaseAccountName создается в разделе ResourceGroup resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="3f329-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="3f329-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f329-110">PARAMETERS</span></span>

### <span data-ttu-id="3f329-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="3f329-111">-ApiKind</span></span>
<span data-ttu-id="3f329-112">Тип создаваемой учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="3f329-113">Допустимые значения: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span><span class="sxs-lookup"><span data-stu-id="3f329-113">Accepted values: GlobalDocumentDB, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="3f329-114">Значение по умолчанию: GlobalDocumentDB</span><span class="sxs-lookup"><span data-stu-id="3f329-114">Default value: GlobalDocumentDB</span></span>

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

### <span data-ttu-id="3f329-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f329-115">-AsJob</span></span>
<span data-ttu-id="3f329-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3f329-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f329-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f329-117">-Confirm</span></span>
<span data-ttu-id="3f329-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f329-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f329-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="3f329-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="3f329-120">Уровень согласованности по умолчанию для учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="3f329-121">Допустимые значения: BoundedStaleness, ConsistentPrefix,,,,,,,, сессия, сеанс, прочее</span><span class="sxs-lookup"><span data-stu-id="3f329-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="3f329-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f329-122">-DefaultProfile</span></span>
<span data-ttu-id="3f329-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f329-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f329-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="3f329-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="3f329-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров, пропускной способности) с помощью ключей учетной записи</span><span class="sxs-lookup"><span data-stu-id="3f329-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="3f329-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="3f329-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="3f329-127">Логическое значение, определяющее, включена ли AnalyticalStorage для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3f329-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="3f329-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="3f329-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="3f329-129">Включает автоматический переход области ввода в редких случаях, когда область недоступна из-за сбоя.</span><span class="sxs-lookup"><span data-stu-id="3f329-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="3f329-130">Автоматический переход на другой ресурс приведет к новому региону записи для учетной записи и будет выбран на основе приоритетов перемещения при сбое, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3f329-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="3f329-131">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="3f329-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3f329-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="3f329-132">-EnableFreeTier</span></span>
<span data-ttu-id="3f329-133">Логическое значение, определяющее, включена ли FreeTier для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3f329-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="3f329-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="3f329-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="3f329-135">Включите несколько местоположений для ввода.</span><span class="sxs-lookup"><span data-stu-id="3f329-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="3f329-136">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="3f329-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3f329-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3f329-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="3f329-138">Включает виртуальную сеть в учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="3f329-139">Допустимые значения: ложь, истина</span><span class="sxs-lookup"><span data-stu-id="3f329-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="3f329-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="3f329-140">-IpRule</span></span>
<span data-ttu-id="3f329-141">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="3f329-141">Firewall support.</span></span> <span data-ttu-id="3f329-142">Указывает набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые должны быть включены в список разрешенных адресов клиентов для данной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="3f329-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="3f329-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="3f329-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="3f329-144">Универсальный код ресурса (URI) KeyVault</span><span class="sxs-lookup"><span data-stu-id="3f329-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="3f329-145">-Location</span><span class="sxs-lookup"><span data-stu-id="3f329-145">-Location</span></span>
<span data-ttu-id="3f329-146">Добавьте расположение в учетную запись базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="3f329-147">Массив строк, упорядоченный по приоритету отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="3f329-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="3f329-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="3f329-148">-LocationObject</span></span>
<span data-ttu-id="3f329-149">Добавьте расположение в учетную запись базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="3f329-150">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="3f329-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="3f329-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="3f329-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="3f329-152">Это значение представляет время, в течение которого допускается устаревшая версия (в TimeSpan).</span><span class="sxs-lookup"><span data-stu-id="3f329-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="3f329-153">Допустимый диапазон для этого значения — 5-86400.</span><span class="sxs-lookup"><span data-stu-id="3f329-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="3f329-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="3f329-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="3f329-155">Это значение представляет собой количество устаревших запросов, которые можно использовать для согласованности ограниченных устаревших значений.</span><span class="sxs-lookup"><span data-stu-id="3f329-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="3f329-156">Допустимый диапазон для этого значения: 1-2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="3f329-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="3f329-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f329-157">-Name</span></span>
<span data-ttu-id="3f329-158">Имя учетной записи базы данных Cosmos DB.</span><span class="sxs-lookup"><span data-stu-id="3f329-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="3f329-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="3f329-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="3f329-160">Разрешено ли доступ к общедоступной конечной точке для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="3f329-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="3f329-161">Возможные значения: "включено", "отключено"</span><span class="sxs-lookup"><span data-stu-id="3f329-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="3f329-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f329-162">-ResourceGroupName</span></span>
<span data-ttu-id="3f329-163">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f329-163">Name of resource group.</span></span>

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

### <span data-ttu-id="3f329-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="3f329-164">-ServerVersion</span></span>
<span data-ttu-id="3f329-165">ServerVersion, действует только в случае с учетными записями MongoDB.</span><span class="sxs-lookup"><span data-stu-id="3f329-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="3f329-166">-Тег</span><span class="sxs-lookup"><span data-stu-id="3f329-166">-Tag</span></span>
<span data-ttu-id="3f329-167">Хэш-таблицы тегов в виде пар "ключ — значение".</span><span class="sxs-lookup"><span data-stu-id="3f329-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="3f329-168">Для удаления существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="3f329-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="3f329-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f329-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="3f329-170">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f329-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="3f329-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f329-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="3f329-172">Массив PSVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3f329-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="3f329-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f329-173">-WhatIf</span></span>
<span data-ttu-id="3f329-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f329-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f329-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f329-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f329-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f329-176">CommonParameters</span></span>
<span data-ttu-id="3f329-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f329-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f329-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f329-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f329-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f329-179">INPUTS</span></span>

### <span data-ttu-id="3f329-180">Microsoft. Azure. Commands. CosmosDB. Models. PSCorsRule []</span><span class="sxs-lookup"><span data-stu-id="3f329-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="3f329-181">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f329-181">OUTPUTS</span></span>

### <span data-ttu-id="3f329-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="3f329-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="3f329-183">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f329-183">NOTES</span></span>

## <span data-ttu-id="3f329-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f329-184">RELATED LINKS</span></span>