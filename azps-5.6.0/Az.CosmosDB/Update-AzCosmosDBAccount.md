---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/update-azcosmosdbaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/Update-AzCosmosDBAccount.md
ms.openlocfilehash: cbee0ef9ce750dbb72af5be484106ccabec79321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010739"
---
# <span data-ttu-id="e6741-101">Update-AzCosmosDBAccount</span><span class="sxs-lookup"><span data-stu-id="e6741-101">Update-AzCosmosDBAccount</span></span>

## <span data-ttu-id="e6741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6741-102">SYNOPSIS</span></span>
<span data-ttu-id="e6741-103">Обновив атрибуты учетной записи в ПараметрахDB.</span><span class="sxs-lookup"><span data-stu-id="e6741-103">Update a CosmosDB account attributes.</span></span>

## <span data-ttu-id="e6741-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e6741-104">SYNTAX</span></span>

### <span data-ttu-id="e6741-105">ByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6741-105">ByNameParameterSet (Default)</span></span>
```
Update-AzCosmosDBAccount [-EnableAutomaticFailover <Boolean>] [-EnableMultipleWriteLocations <Boolean>]
 [-EnableVirtualNetwork <Boolean>] [-DisableKeyBasedMetadataWriteAccess <Boolean>] -ResourceGroupName <String>
 -Name <String> [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6741-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6741-106">ByResourceIdParameterSet</span></span>
```
Update-AzCosmosDBAccount -ResourceId <String> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6741-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6741-107">ByObjectParameterSet</span></span>
```
Update-AzCosmosDBAccount -InputObject <PSDatabaseAccountGetResults> [-EnableAutomaticFailover <Boolean>]
 [-EnableMultipleWriteLocations <Boolean>] [-EnableVirtualNetwork <Boolean>]
 [-DisableKeyBasedMetadataWriteAccess <Boolean>] [-DefaultConsistencyLevel <String>] [-IpRule <String[]>]
 [-MaxStalenessIntervalInSeconds <Int32>] [-MaxStalenessPrefix <Int32>] [-Tag <Hashtable>]
 [-VirtualNetworkRule <String[]>] [-VirtualNetworkRuleObject <PSVirtualNetworkRule[]>]
 [-PublicNetworkAccess <String>] [-KeyVaultKeyUri <String>] [-EnableAnalyticalStorage <Boolean>] [-AsJob]
 [-NetworkAclBypass <String>] [-NetworkAclBypassResourceId <String[]>] [-ServerVersion <String>]
 [-BackupIntervalInMinutes <Int32>] [-BackupRetentionIntervalInHours <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6741-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6741-108">DESCRIPTION</span></span>
<span data-ttu-id="e6741-109">Обновив свойства учетной записи ВайссDB.</span><span class="sxs-lookup"><span data-stu-id="e6741-109">Update the properties of a CosmosDB account.</span></span> <span data-ttu-id="e6741-110">Не удается обновить регионы учетной записи одновременно с другими свойствами.</span><span class="sxs-lookup"><span data-stu-id="e6741-110">Cannot update Account Regions simulataneously with other properties.</span></span>

## <span data-ttu-id="e6741-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e6741-111">EXAMPLES</span></span>

### <span data-ttu-id="e6741-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6741-112">Example 1</span></span>
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
NetworkAclBypass              : None
NetworkAclBypassResourceIds   : {}
```

<span data-ttu-id="e6741-113">Обновлено значение DefaultConsistencyLevel на "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations и Enabled VirtualNetwork forБ Учетная запись Скайп с именем учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e6741-113">Updated DefaultConsistencyLevel to "Strong", Enabled AutomaticFailover, Enabled MultipleWriteLocations and Enabled VirtualNetwork for CosmosDB Account with name accountName.</span></span> 

## <span data-ttu-id="e6741-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6741-114">PARAMETERS</span></span>

### <span data-ttu-id="e6741-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6741-115">-AsJob</span></span>
<span data-ttu-id="e6741-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e6741-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e6741-117">-BackupIntervalInMinutes</span><span class="sxs-lookup"><span data-stu-id="e6741-117">-BackupIntervalInMinutes</span></span>
<span data-ttu-id="e6741-118">Интервал (в минутах) резервного копирования (только для учетных записей с периодическим резервным копированием).</span><span class="sxs-lookup"><span data-stu-id="e6741-118">The interval(in minutes) with which backup are taken (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="e6741-119">-BackupRetentionIntervalInHours</span><span class="sxs-lookup"><span data-stu-id="e6741-119">-BackupRetentionIntervalInHours</span></span>
<span data-ttu-id="e6741-120">Время (в часах), за которое сохраняется каждая резервная копия (только для учетных записей с периодическим резервным копированием в режиме).</span><span class="sxs-lookup"><span data-stu-id="e6741-120">The time(in hours) for which each backup is retained (only for accounts with periodic mode backups)</span></span>

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

### <span data-ttu-id="e6741-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6741-121">-Confirm</span></span>
<span data-ttu-id="e6741-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6741-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6741-123">-DefaultConsistencyLevel</span><span class="sxs-lookup"><span data-stu-id="e6741-123">-DefaultConsistencyLevel</span></span>
<span data-ttu-id="e6741-124">Стандартный уровень согласованности для учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="e6741-124">Default consistency level of the Cosmos DB database account.</span></span>
<span data-ttu-id="e6741-125">Принятые значения: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span><span class="sxs-lookup"><span data-stu-id="e6741-125">Accepted values: BoundedStaleness, ConsistentPrefix, Eventual, Session, Strong</span></span>

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

### <span data-ttu-id="e6741-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6741-126">-DefaultProfile</span></span>
<span data-ttu-id="e6741-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6741-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6741-128">-DisableKeyBasedMetadataWriteAccess</span><span class="sxs-lookup"><span data-stu-id="e6741-128">-DisableKeyBasedMetadataWriteAccess</span></span>
<span data-ttu-id="e6741-129">Отключение операций записи для ресурсов метаданных (баз данных, контейнеров и пропускной способности) с помощью ключей учетных записей</span><span class="sxs-lookup"><span data-stu-id="e6741-129">Disable write operations on metadata resources (databases, containers, throughput) via account keys</span></span>

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

### <span data-ttu-id="e6741-130">-EnableAnalyticalStorage</span><span class="sxs-lookup"><span data-stu-id="e6741-130">-EnableAnalyticalStorage</span></span>
<span data-ttu-id="e6741-131">Следует указать, включена ли в учетной записи аналитическая система аналитики.</span><span class="sxs-lookup"><span data-stu-id="e6741-131">Bool to indicate if AnalyticalStorage is enabled on the account.</span></span>

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

### <span data-ttu-id="e6741-132">-EnableAutomaticFailover</span><span class="sxs-lookup"><span data-stu-id="e6741-132">-EnableAutomaticFailover</span></span>
<span data-ttu-id="e6741-133">Включает автоматический отбой области записи в редких случаях, когда регион недоступен из-за простоя.</span><span class="sxs-lookup"><span data-stu-id="e6741-133">Enables automatic failover of the write region in the rare event that the region is unavailable due to an outage.</span></span>
<span data-ttu-id="e6741-134">При автоматическом отписи для учетной записи будет новый регион записи, который выбирается с учетом приоритетов отключки, настроенных для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e6741-134">Automatic failover will result in a new write region for the account and is chosen based on the failover priorities configured for the account.</span></span>
<span data-ttu-id="e6741-135">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="e6741-135">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e6741-136">-EnableMultipleWriteLocations</span><span class="sxs-lookup"><span data-stu-id="e6741-136">-EnableMultipleWriteLocations</span></span>
<span data-ttu-id="e6741-137">Включить несколько мест записи.</span><span class="sxs-lookup"><span data-stu-id="e6741-137">Enable Multiple Write Locations.</span></span>
<span data-ttu-id="e6741-138">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="e6741-138">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e6741-139">-EnableVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e6741-139">-EnableVirtualNetwork</span></span>
<span data-ttu-id="e6741-140">Включает виртуальную сеть в учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="e6741-140">Enables virtual network on the Cosmos DB database account.</span></span>
<span data-ttu-id="e6741-141">Принятые значения: ЛОЖЬ, ИСТИНА</span><span class="sxs-lookup"><span data-stu-id="e6741-141">Accepted values: false, true</span></span>

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

### <span data-ttu-id="e6741-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6741-142">-InputObject</span></span>
<span data-ttu-id="e6741-143">Объект учетной записи ВайсDB</span><span class="sxs-lookup"><span data-stu-id="e6741-143">CosmosDB Account object</span></span>

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

### <span data-ttu-id="e6741-144">-IpRule</span><span class="sxs-lookup"><span data-stu-id="e6741-144">-IpRule</span></span>
<span data-ttu-id="e6741-145">Поддержка брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="e6741-145">Firewall support.</span></span> <span data-ttu-id="e6741-146">Набор IP-адресов или диапазонов IP-адресов в форме CIDR, которые нужно включить в список разрешенных IP-адресов клиентов для определенной учетной записи базы данных.</span><span class="sxs-lookup"><span data-stu-id="e6741-146">Specifies the set of IP addresses or IP address ranges in CIDR form to be included as the allowed list of client IPs for a given database account.</span></span>

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

### <span data-ttu-id="e6741-147">-KeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="e6741-147">-KeyVaultKeyUri</span></span>
<span data-ttu-id="e6741-148">URI of the KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6741-148">URI of the KeyVault</span></span>

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

### <span data-ttu-id="e6741-149">-MaxStalenessIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="e6741-149">-MaxStalenessIntervalInSeconds</span></span>
<span data-ttu-id="e6741-150">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших данных (в периоде времени).</span><span class="sxs-lookup"><span data-stu-id="e6741-150">When used with Bounded Staleness consistency, this value represents the time amount of staleness (in timespan) tolerated.</span></span>
<span data-ttu-id="e6741-151">Диапазон для этого значения составляет 5–86400.</span><span class="sxs-lookup"><span data-stu-id="e6741-151">Accepted range for this value is 5-86400.</span></span>

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

### <span data-ttu-id="e6741-152">-MaxStalenessPrefix</span><span class="sxs-lookup"><span data-stu-id="e6741-152">-MaxStalenessPrefix</span></span>
<span data-ttu-id="e6741-153">Если используется согласованность связанных устаревших данных, это значение представляет количество устаревших запросов.</span><span class="sxs-lookup"><span data-stu-id="e6741-153">When used with Bounded Staleness consistency, this value represents the number of stale requests tolerated.</span></span>
<span data-ttu-id="e6741-154">Диапазон для этого значения составляет 1–2 147 483 647.</span><span class="sxs-lookup"><span data-stu-id="e6741-154">Accepted range for this value is 1 - 2,147,483,647.</span></span>

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

### <span data-ttu-id="e6741-155">-Name</span><span class="sxs-lookup"><span data-stu-id="e6741-155">-Name</span></span>
<span data-ttu-id="e6741-156">Имя учетной записи базы данных "Цы DB".</span><span class="sxs-lookup"><span data-stu-id="e6741-156">Name of the Cosmos DB database account.</span></span>

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

### <span data-ttu-id="e6741-157">-NetworkAclBypass</span><span class="sxs-lookup"><span data-stu-id="e6741-157">-NetworkAclBypass</span></span>
<span data-ttu-id="e6741-158">Включен ли обход сетевого ACL для этой учетной записи для связи Synapse.</span><span class="sxs-lookup"><span data-stu-id="e6741-158">Whether or not Network Acl Bypass is enabled for this account for Synapse Link.</span></span> <span data-ttu-id="e6741-159">Возможные значения: "Нет", "AzureServices".</span><span class="sxs-lookup"><span data-stu-id="e6741-159">Possible values include: 'None', 'AzureServices'.</span></span>

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

### <span data-ttu-id="e6741-160">-NetworkAclBypassResourceId</span><span class="sxs-lookup"><span data-stu-id="e6741-160">-NetworkAclBypassResourceId</span></span>
<span data-ttu-id="e6741-161">Список ИД ресурсов, позволяющий обойти network ACL для связи с синапсеем.</span><span class="sxs-lookup"><span data-stu-id="e6741-161">List of Resource Ids to allow Network Acl Bypass for Synapse Link.</span></span>

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

### <span data-ttu-id="e6741-162">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e6741-162">-PublicNetworkAccess</span></span>
<span data-ttu-id="e6741-163">Разрешен ли доступ к общедоступным конечным точкам для этого сервера.</span><span class="sxs-lookup"><span data-stu-id="e6741-163">Whether or not public endpoint access is allowed for this server.</span></span> <span data-ttu-id="e6741-164">Возможные значения: "Включено", "Отключено"</span><span class="sxs-lookup"><span data-stu-id="e6741-164">Possible values include: 'Enabled', 'Disabled'</span></span>

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

### <span data-ttu-id="e6741-165">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6741-165">-ResourceGroupName</span></span>
<span data-ttu-id="e6741-166">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6741-166">Name of resource group.</span></span>

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

### <span data-ttu-id="e6741-167">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6741-167">-ResourceId</span></span>
<span data-ttu-id="e6741-168">ResourceId ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6741-168">ResourceId of the resource.</span></span>

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

### <span data-ttu-id="e6741-169">-ServerVersion</span><span class="sxs-lookup"><span data-stu-id="e6741-169">-ServerVersion</span></span>
<span data-ttu-id="e6741-170">ServerVersion, действителен только в случае учетных записей MongoDB.</span><span class="sxs-lookup"><span data-stu-id="e6741-170">ServerVersion, valid only in case of MongoDB Accounts.</span></span>

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

### <span data-ttu-id="e6741-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="e6741-171">-Tag</span></span>
<span data-ttu-id="e6741-172">Теги в качестве пар ключа и значения.</span><span class="sxs-lookup"><span data-stu-id="e6741-172">Hashtable of tags as key-value pairs.</span></span>
<span data-ttu-id="e6741-173">Для очистки существующего тега используйте пустую строку.</span><span class="sxs-lookup"><span data-stu-id="e6741-173">Use empty string to clear existing tag.</span></span>

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

### <span data-ttu-id="e6741-174">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="e6741-174">-VirtualNetworkRule</span></span>
<span data-ttu-id="e6741-175">Массив строковых значений ACL для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e6741-175">Array of string values of ACL's for virtual network.</span></span>

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

### <span data-ttu-id="e6741-176">-VirtualNetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="e6741-176">-VirtualNetworkRuleObject</span></span>
<span data-ttu-id="e6741-177">Массив psVirtualNetworkRuleObjects для виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="e6741-177">Array of PSVirtualNetworkRuleObjects for virtual network.</span></span>

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

### <span data-ttu-id="e6741-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6741-178">-WhatIf</span></span>
<span data-ttu-id="e6741-179">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6741-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6741-180">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e6741-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6741-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6741-181">CommonParameters</span></span>
<span data-ttu-id="e6741-182">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6741-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6741-183">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e6741-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6741-184">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e6741-184">INPUTS</span></span>

### <span data-ttu-id="e6741-185">Microsoft.Azure.Commands.ВацыDB.Models.PSCorsRule[]</span><span class="sxs-lookup"><span data-stu-id="e6741-185">Microsoft.Azure.Commands.CosmosDB.Models.PSCorsRule[]</span></span>

## <span data-ttu-id="e6741-186">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e6741-186">OUTPUTS</span></span>

### <span data-ttu-id="e6741-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span><span class="sxs-lookup"><span data-stu-id="e6741-187">Microsoft.Azure.Commands.CosmosDB.Models.PSDatabaseAccount</span></span>

## <span data-ttu-id="e6741-188">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e6741-188">NOTES</span></span>

## <span data-ttu-id="e6741-189">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6741-189">RELATED LINKS</span></span>
