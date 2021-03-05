---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBAccount.md
ms.openlocfilehash: 75085bed9c1f9b0cd0c0328b9a166c6dc08a60b7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992827"
---
# <span data-ttu-id="018bf-101">New-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="018bf-101">New-AzCosmosDBAccount</span></span>

## <span data-ttu-id="018bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018bf-102">SYNOPSIS</span></span>
<span data-ttu-id="018bf-103">Создайте учетную запись СкайпDb.</span><span class="sxs-lookup"><span data-stu-id="018bf-103">Create a new CosmosDB Account.</span></span>

## <span data-ttu-id="018bf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="018bf-104">SYNTAX</span></span>

```
New-AzCosmosDBAccount [-EnableAutomaticFailover] [-EnableMultipleWriteLocations] [-EnableVirtualNetwork]
 [-ApiKind <String>] [-DisableKeyBasedMetadataWriteAccess] [-EnableFreeTier <Boolean>] [-Location <String[]>]
 [-LocationObject <PSLocation[]>] -ResourceGroupName <String> -Name <String>
 [-DefaultConsistencyLevel <String>] [-IpRule <String[]>] [-MaxStalenessIntervalInSeconds <Int32>]
 [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>] [-VirtualNetworkRule <String[]>]
 [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>] [-PublicNetworkAccess <String>]
 [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob] [-NetworkAclBypass <String>]
 [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>] [-BackupIntervalInMinutes <Int32>]
 [-BackupRetentionIntervalInHours <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="018bf-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="018bf-105">DESCRIPTION</span></span>
<span data-ttu-id="018bf-106">Создайте новую учетную запись "ДискиDB" в данной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="018bf-106">Create a new CosmosDB Account in the given ResourceGroup.</span></span>

## <span data-ttu-id="018bf-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="018bf-107">EXAMPLES</span></span>

### <span data-ttu-id="018bf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="018bf-108">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="018bf-109">В базе данных ResourceGroup ResourceGroupName создается новая учетная запись " ССDB с именем базы данныхAccountName.</span><span class="sxs-lookup"><span data-stu-id="018bf-109">A new CosmosDB Account with name databaseAccountName is created in the ResourceGroup resourceGroupName.</span></span>

## <span data-ttu-id="018bf-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="018bf-110">PARAMETERS</span></span>

### <span data-ttu-id="018bf-111">-ApiKind</span><span class="sxs-lookup"><span data-stu-id="018bf-111">-ApiKind</span></span>
<span data-ttu-id="018bf-112">Тип учетной записи базы данных "Цы DB", который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="018bf-112">The type of Cosmos DB database account to create.</span></span>
<span data-ttu-id="018bf-113">Принятые значения: Sql, MongoDB, Гремлин, Таблица, Юлия.</span><span class="sxs-lookup"><span data-stu-id="018bf-113">Accepted values: Sql, MongoDB, Gremlin, Table, Cassandra.</span></span>
<span data-ttu-id="018bf-114">Значение по умолчанию: SQL</span><span class="sxs-lookup"><span data-stu-id="018bf-114">Default value: Sql</span></span>

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

### <span data-ttu-id="018bf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="018bf-115">-AsJob</span></span>
<span data-ttu-id="018bf-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="018bf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="018bf-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="018bf-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="018bf-118">Интервал (в минутах) резервной копии (только для учетных записей с периодическим резервным копированием).</span><span class="sxs-lookup"><span data-stu-id="018bf-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="018bf-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="018bf-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="018bf-120">Время (в часах), за которое сохраняется каждая резервная копия (только для учетных записей с периодическим резервным копированием в режиме).</span><span class="sxs-lookup"><span data-stu-id="018bf-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="018bf-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="018bf-121">-Confirm</span></span>
<span data-ttu-id="018bf-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="018bf-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="018bf-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="018bf-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="018bf-124">Стандартный уровень согласованности для учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="018bf-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="018bf-125">Принятые значения: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="018bf-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="018bf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018bf-126">-DefaultProfile</span></span>
<span data-ttu-id="018bf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="018bf-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018bf-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="018bf-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="018bf-129">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров и пропускной способности) с помощью ключей учетных записей</span><span class="sxs-lookup"><span data-stu-id="018bf-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="018bf-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="018bf-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="018bf-131">Следует указать, включена ли в учетной записи аналитическая система аналитики.</span><span class="sxs-lookup"><span data-stu-id="018bf-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="018bf-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="018bf-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="018bf-133">Включает автоматический отбой области записи в редких случаях, когда регион недоступен из-за простоя.</span><span class="sxs-lookup"><span data-stu-id="018bf-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="018bf-134">При автоматическом отписи для учетной записи будет новый регион записи, который выбирается с учетом приоритетов отключки, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="018bf-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="018bf-135">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="018bf-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="018bf-136">-EnableFreeTier</span><span class="sxs-lookup"><span data-stu-id="018bf-136">-EnableFreeTier</span></span>
<span data-ttu-id="018bf-137">Bool to indicate if FreeTier is enabled on the account.</span><span class="sxs-lookup"><span data-stu-id="018bf-137">Bool to indicate if FreeTier is enabled on the account.</span></span>

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

### <span data-ttu-id="018bf-138">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="018bf-138">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="018bf-139">Включить несколько мест записи.</span><span class="sxs-lookup"><span data-stu-id="018bf-139">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="018bf-140">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="018bf-140">Accepted values: false, true</span></span>

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

### <span data-ttu-id="018bf-141">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="018bf-141">-EnableVirtualNetwork</span></span>
<span data-ttu-id="018bf-142">Включает виртуальную сеть в учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="018bf-142">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="018bf-143">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="018bf-143">Accepted values: false, true</span></span>

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

### <span data-ttu-id="018bf-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="018bf-144">-IpRule</span></span>
<span data-ttu-id="018bf-145">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="018bf-145">Firewall support.</span></span> <span data-ttu-id="018bf-146">Набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые нужно включить в список разрешенных IP-адресов клиентов для определенной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="018bf-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="018bf-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="018bf-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="018bf-148">URI of the KeyVault</span><span class="sxs-lookup"><span data-stu-id="018bf-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="018bf-149">-Location</span><span class="sxs-lookup"><span data-stu-id="018bf-149">-Location</span></span>
<span data-ttu-id="018bf-150">Добавьте расположение в учетную запись базы данных "Диски".</span><span class="sxs-lookup"><span data-stu-id="018bf-150">Add a location to the Cosmos DB database account.</span></span>
<span data-ttu-id="018bf-151">Массив строк, упорядоченный по приоритету отбойного решения.</span><span class="sxs-lookup"><span data-stu-id="018bf-151">Array of strings, ordered by failover priority.</span></span>

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

### <span data-ttu-id="018bf-152">-LocationObject</span><span class="sxs-lookup"><span data-stu-id="018bf-152">-LocationObject</span></span>
<span data-ttu-id="018bf-153">Добавьте расположение в учетную запись базы данных "Диски".</span><span class="sxs-lookup"><span data-stu-id="018bf-153">Add a location to the Cosmos DB database account.</span></span> <span data-ttu-id="018bf-154">Массив объектов PSLocation.</span><span class="sxs-lookup"><span data-stu-id="018bf-154">Array of PSLocation objects.</span></span>

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

### <span data-ttu-id="018bf-155">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="018bf-155">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="018bf-156">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших данных (в периоде времени).</span><span class="sxs-lookup"><span data-stu-id="018bf-156">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="018bf-157">Диапазон для этого значения составляет 5–86400.</span><span class="sxs-lookup"><span data-stu-id="018bf-157">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="018bf-158">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="018bf-158">-MaxStalenessPrefix</span></span>
<span data-ttu-id="018bf-159">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших запросов.</span><span class="sxs-lookup"><span data-stu-id="018bf-159">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="018bf-160">Диапазон для этого значения составляет 1–2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="018bf-160">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="018bf-161">-Name</span><span class="sxs-lookup"><span data-stu-id="018bf-161">-Name</span></span>
<span data-ttu-id="018bf-162">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="018bf-162">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="018bf-163">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="018bf-163">-NetworkAclBypass</span></span>
<span data-ttu-id="018bf-164">Включен ли обход сетевого ACL для этой учетной записи для связи Synapse.</span><span class="sxs-lookup"><span data-stu-id="018bf-164">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="018bf-165">Возможные значения: "Нет", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="018bf-165">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="018bf-166">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="018bf-166">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="018bf-167">Список ИД ресурсов, позволяющий обойти network ACL для связи с синапсеем.</span><span class="sxs-lookup"><span data-stu-id="018bf-167">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="018bf-168">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="018bf-168">-PublicNetworkAccess</span></span>
<span data-ttu-id="018bf-169">Разрешен ли доступ к общедоступным конечным точкам для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="018bf-169">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="018bf-170">Возможные значения: "Включено", "Отключено"</span><span class="sxs-lookup"><span data-stu-id="018bf-170">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="018bf-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="018bf-171">-ResourceGroupName</span></span>
<span data-ttu-id="018bf-172">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="018bf-172">Name of resource group.</span></span>

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

### <span data-ttu-id="018bf-173">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="018bf-173">-ServerVersion</span></span>
<span data-ttu-id="018bf-174">ServerVersion, действителен только в случае учетных записей MongoDB.</span><span class="sxs-lookup"><span data-stu-id="018bf-174">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="018bf-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="018bf-175">-Tag</span></span>
<span data-ttu-id="018bf-176">Теги в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="018bf-176">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="018bf-177">Для очистки существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="018bf-177">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="018bf-178">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="018bf-178">-VirtualNetworkRule</span></span>
<span data-ttu-id="018bf-179">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="018bf-179">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="018bf-180">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="018bf-180">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="018bf-181">Массив psVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="018bf-181">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="018bf-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="018bf-182">-WhatIf</span></span>
<span data-ttu-id="018bf-183">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="018bf-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="018bf-184">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="018bf-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="018bf-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018bf-185">CommonParameters</span></span>
<span data-ttu-id="018bf-186">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018bf-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018bf-187">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="018bf-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018bf-188">INPUTS</span><span class="sxs-lookup"><span data-stu-id="018bf-188">INPUTS</span></span>

### <span data-ttu-id="018bf-189">Microsoft.Azure.Commands.Правляемые.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="018bf-189">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="018bf-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="018bf-190">OUTPUTS</span></span>

### <span data-ttu-id="018bf-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="018bf-191">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="018bf-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="018bf-192">NOTES</span></span>

## <span data-ttu-id="018bf-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="018bf-193">RELATED LINKS</span></span>
