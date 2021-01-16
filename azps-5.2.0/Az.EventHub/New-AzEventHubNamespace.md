---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: a51fffe36102b05121e52054103357bd26f56d51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329311"
---
# <span data-ttu-id="e280d-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="e280d-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="e280d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e280d-102">SYNOPSIS</span></span>
<span data-ttu-id="e280d-103">Создает пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="e280d-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="e280d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e280d-104">SYNTAX</span></span>

### <span data-ttu-id="e280d-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e280d-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e280d-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="e280d-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e280d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e280d-107">DESCRIPTION</span></span>
<span data-ttu-id="e280d-108">С New-AzEventHubNamespace создается новое пространство имен концентраторов событий типа "События".</span><span class="sxs-lookup"><span data-stu-id="e280d-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="e280d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e280d-109">EXAMPLES</span></span>
### <span data-ttu-id="e280d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e280d-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="e280d-111">Создает пространство имен "Концентраторы событий" MyNamespaceName в указанном географическом расположении MyLocation в группе ресурсов \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="e280d-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e280d-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e280d-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="e280d-113">Создает пространство имен "Концентраторы событий" MyNamespaceName в указанном географическом расположении MyLocation . В группах ресурсов \` \` \` \` \` MyResourceGroupName и \` AutoInflate включены maximumThroughputUnits 10.</span><span class="sxs-lookup"><span data-stu-id="e280d-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="e280d-114">Пример 3. Область имен с поддержкой Kafka</span><span class="sxs-lookup"><span data-stu-id="e280d-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="e280d-115">Создает пространство имен Концентраторов событий MyNamespaceName в указанном географическом расположении MyLocation в группе ресурсов \` \` \` \` \` MyResourceGroupName с включенной поддержкой \` kafka и autoInflate.</span><span class="sxs-lookup"><span data-stu-id="e280d-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="e280d-116">Пример 4. Область имен с включенной поддержкой ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e280d-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="e280d-117">Создает пространство имен Концентраторов событий MyNamespaceName в указанном географическом расположении MyLocation в группе ресурсов \` \` \` \` \` MyResourceGroupName с включенной поддержкой \` kafka и autoInflate.</span><span class="sxs-lookup"><span data-stu-id="e280d-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="e280d-118">Пример 5. Создание пространства имен с помощью управления удостоверением в кластере</span><span class="sxs-lookup"><span data-stu-id="e280d-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :


# Get created namespace
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="e280d-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e280d-119">PARAMETERS</span></span>

### <span data-ttu-id="e280d-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="e280d-120">-ClusterARMId</span></span>
<span data-ttu-id="e280d-121">ARM кластера, где должно быть создано пространство имен</span><span class="sxs-lookup"><span data-stu-id="e280d-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e280d-122">-DefaultProfile</span></span>
<span data-ttu-id="e280d-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e280d-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="e280d-124">-EnableAutoInflate</span></span>
<span data-ttu-id="e280d-125">Указывает на то, включена ли автообъединка</span><span class="sxs-lookup"><span data-stu-id="e280d-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="e280d-126">-EnableKafka</span></span>
<span data-ttu-id="e280d-127">включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="e280d-127">enabling or disabling Kafka for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-128">-Identity</span><span class="sxs-lookup"><span data-stu-id="e280d-128">-Identity</span></span>
<span data-ttu-id="e280d-129">включение и отключение удостоверения для пространства имен</span><span class="sxs-lookup"><span data-stu-id="e280d-129">enabling or disabling Identity for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-130">-Location</span><span class="sxs-lookup"><span data-stu-id="e280d-130">-Location</span></span>
<span data-ttu-id="e280d-131">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="e280d-131">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="e280d-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="e280d-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="e280d-133">Верхний предел пропускной способности при включенной автообновке, значение должно быть в пределах от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="e280d-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-134">-Name</span><span class="sxs-lookup"><span data-stu-id="e280d-134">-Name</span></span>
<span data-ttu-id="e280d-135">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="e280d-135">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e280d-136">-ResourceGroupName</span></span>
<span data-ttu-id="e280d-137">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e280d-137">Resource Group Name</span></span>

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

### <span data-ttu-id="e280d-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="e280d-138">-SkuCapacity</span></span>
<span data-ttu-id="e280d-139">Единицы пропускной способности еверха.</span><span class="sxs-lookup"><span data-stu-id="e280d-139">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e280d-140">-SkuName</span></span>
<span data-ttu-id="e280d-141">Namespace Sku Name.</span><span class="sxs-lookup"><span data-stu-id="e280d-141">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="e280d-142">-Tag</span></span>
<span data-ttu-id="e280d-143">Hashtables which represents resource Tags.</span><span class="sxs-lookup"><span data-stu-id="e280d-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="e280d-144">-ZoneRedundant</span></span>
<span data-ttu-id="e280d-145">включение и отключение лишней зоны для пространства имен</span><span class="sxs-lookup"><span data-stu-id="e280d-145">enabling or disabling Zone Redundant for namespace</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e280d-146">-Confirm</span></span>
<span data-ttu-id="e280d-147">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="e280d-147">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e280d-148">-WhatIf</span></span>
<span data-ttu-id="e280d-149">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e280d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e280d-150">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e280d-150">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e280d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e280d-151">CommonParameters</span></span>
<span data-ttu-id="e280d-152">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e280d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e280d-153">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e280d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e280d-154">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e280d-154">INPUTS</span></span>

### <span data-ttu-id="e280d-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e280d-155">System.String</span></span>

### <span data-ttu-id="e280d-156">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="e280d-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="e280d-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e280d-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e280d-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e280d-158">OUTPUTS</span></span>

### <span data-ttu-id="e280d-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="e280d-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="e280d-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e280d-160">NOTES</span></span>

## <span data-ttu-id="e280d-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e280d-161">RELATED LINKS</span></span>
