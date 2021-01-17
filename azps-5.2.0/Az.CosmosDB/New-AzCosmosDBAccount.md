---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 4e31ae75f6fcea77c179757312988a0abbbb58f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402559"
---
# <span data-ttu-id="26b33-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="26b33-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="26b33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b33-102">SYNOPSIS</span></span>
<span data-ttu-id="26b33-103">Создайте учетную запись СкайпDb.</span><span class="sxs-lookup"><span data-stu-id="26b33-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="26b33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26b33-104">SYNTAX</span></span>

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

## <span data-ttu-id="26b33-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26b33-105">DESCRIPTION</span></span>
<span data-ttu-id="26b33-106">Создайте новую учетную запись "ДискиDB" в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26b33-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="26b33-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26b33-107">EXAMPLES</span></span>

### <span data-ttu-id="26b33-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26b33-108">Example 1</span></span>
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

<span data-ttu-id="26b33-109">В базе данных ResourceGroup ResourceGroupName создается новая учетная запись " ССDB с именем базы данныхAccountName.</span><span class="sxs-lookup"><span data-stu-id="26b33-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="26b33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b33-110">PARAMETERS</span></span>

### <span data-ttu-id="26b33-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="26b33-111">-ApiKind</span></span>
<span data-ttu-id="26b33-112">Тип учетной записи базы данных "Цы DB", который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="26b33-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="26b33-113">Принятые значения: Sql, MongoDB, Гремлин, Таблица, Юлия.</span><span class="sxs-lookup"><span data-stu-id="26b33-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="26b33-114">Значение по умолчанию: SQL</span><span class="sxs-lookup"><span data-stu-id="26b33-114">Default value: Sql</span></span>

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

### <span data-ttu-id="26b33-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26b33-115">-AsJob</span></span>
<span data-ttu-id="26b33-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="26b33-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26b33-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26b33-117">-Confirm</span></span>
<span data-ttu-id="26b33-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b33-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26b33-119">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="26b33-119">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="26b33-120">Стандартный уровень согласованности для учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26b33-120">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="26b33-121">Принятые значения: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="26b33-121">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="26b33-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b33-122">-DefaultProfile</span></span>
<span data-ttu-id="26b33-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26b33-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b33-124">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="26b33-124">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="26b33-125">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров и пропускной способности) с помощью ключей учетных записей</span><span class="sxs-lookup"><span data-stu-id="26b33-125">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="26b33-126">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="26b33-126">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="26b33-127">Следует указать, включена ли в учетной записи аналитическая система аналитики.</span><span class="sxs-lookup"><span data-stu-id="26b33-127">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="26b33-128">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="26b33-128">-EnableAutomaticFailover</span></span>
<span data-ttu-id="26b33-129">Включает автоматический отбой области записи в редких случаях, когда регион недоступен из-за простоя.</span><span class="sxs-lookup"><span data-stu-id="26b33-129">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="26b33-130">При автоматическом отписи для учетной записи будет новый регион записи, который выбирается с учетом приоритетов отключки, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="26b33-130">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="26b33-131">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26b33-131">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26b33-132">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="26b33-132">-EnableFreeTier</span></span>
<span data-ttu-id="26b33-133">Bool to indicate if FreeTier is enabled on the account.</span><span class="sxs-lookup"><span data-stu-id="26b33-133">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="26b33-134">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="26b33-134">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="26b33-135">Включить несколько мест записи.</span><span class="sxs-lookup"><span data-stu-id="26b33-135">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="26b33-136">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26b33-136">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26b33-137">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="26b33-137">-EnableVirtualNetwork</span></span>
<span data-ttu-id="26b33-138">Включает виртуальную сеть в учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26b33-138">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="26b33-139">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="26b33-139">Accepted values: false, true</span></span>

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

### <span data-ttu-id="26b33-140">-IpRule</span><span class="sxs-lookup"><span data-stu-id="26b33-140">-IpRule</span></span>
<span data-ttu-id="26b33-141">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="26b33-141">Firewall support.</span></span> <span data-ttu-id="26b33-142">Определяет набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые должны быть включены в список разрешенных IP-адресов клиентов для определенной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="26b33-142">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="26b33-143">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="26b33-143">-KeyVaultKeyUri</span></span>
<span data-ttu-id="26b33-144">URI of the KeyVault</span><span class="sxs-lookup"><span data-stu-id="26b33-144">URI of the KeyVault</span></span>

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

### <span data-ttu-id="26b33-145">-Location</span><span class="sxs-lookup"><span data-stu-id="26b33-145">-Location</span></span>
<span data-ttu-id="26b33-146">Добавьте расположение в учетную запись базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26b33-146">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="26b33-147">Массив строк, упорядоченный по приоритету отбойного решения.</span><span class="sxs-lookup"><span data-stu-id="26b33-147">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="26b33-148">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="26b33-148">-LocationObject</span></span>
<span data-ttu-id="26b33-149">Добавьте расположение в учетную запись базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26b33-149">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="26b33-150">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="26b33-150">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="26b33-151">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="26b33-151">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="26b33-152">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших данных (в периоде времени).</span><span class="sxs-lookup"><span data-stu-id="26b33-152">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="26b33-153">Диапазон для этого значения составляет 5–86400.</span><span class="sxs-lookup"><span data-stu-id="26b33-153">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="26b33-154">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="26b33-154">-MaxStalenessPrefix</span></span>
<span data-ttu-id="26b33-155">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших запросов.</span><span class="sxs-lookup"><span data-stu-id="26b33-155">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="26b33-156">Диапазон, который можно принимать для этого значения, составляет 1–2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="26b33-156">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="26b33-157">-Name</span><span class="sxs-lookup"><span data-stu-id="26b33-157">-Name</span></span>
<span data-ttu-id="26b33-158">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="26b33-158">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="26b33-159">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="26b33-159">-PublicNetworkAccess</span></span>
<span data-ttu-id="26b33-160">Разрешен ли доступ к общедоступным конечным точкам для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="26b33-160">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="26b33-161">Возможные значения: "Включено", "Отключено"</span><span class="sxs-lookup"><span data-stu-id="26b33-161">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="26b33-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26b33-162">-ResourceGroupName</span></span>
<span data-ttu-id="26b33-163">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26b33-163">Name of resource group.</span></span>

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

### <span data-ttu-id="26b33-164">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="26b33-164">-ServerVersion</span></span>
<span data-ttu-id="26b33-165">ServerVersion, действителен только в случае учетных записей MongoDB.</span><span class="sxs-lookup"><span data-stu-id="26b33-165">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="26b33-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="26b33-166">-Tag</span></span>
<span data-ttu-id="26b33-167">Теги в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="26b33-167">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="26b33-168">Для очистки существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="26b33-168">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="26b33-169">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="26b33-169">-VirtualNetworkRule</span></span>
<span data-ttu-id="26b33-170">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="26b33-170">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="26b33-171">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="26b33-171">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="26b33-172">Массив psVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="26b33-172">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="26b33-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26b33-173">-WhatIf</span></span>
<span data-ttu-id="26b33-174">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26b33-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26b33-175">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="26b33-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26b33-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b33-176">CommonParameters</span></span>
<span data-ttu-id="26b33-177">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b33-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b33-178">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26b33-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b33-179">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26b33-179">INPUTS</span></span>

### <span data-ttu-id="26b33-180">Microsoft.Azure.Commands.Правляемые.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="26b33-180">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="26b33-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26b33-181">OUTPUTS</span></span>

### <span data-ttu-id="26b33-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="26b33-182">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="26b33-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26b33-183">NOTES</span></span>

## <span data-ttu-id="26b33-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26b33-184">RELATED LINKS</span></span>
 
