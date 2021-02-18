---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214737"
---
# <span data-ttu-id="2b7d2-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2b7d2-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="2b7d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b7d2-102">SYNOPSIS</span></span>
<span data-ttu-id="2b7d2-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2b7d2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2b7d2-104">SYNTAX</span></span>

### <span data-ttu-id="2b7d2-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b7d2-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7d2-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7d2-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b7d2-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="2b7d2-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b7d2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b7d2-108">DESCRIPTION</span></span>
<span data-ttu-id="2b7d2-109">Этот Set-AzEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="2b7d2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2b7d2-110">EXAMPLES</span></span>

### <span data-ttu-id="2b7d2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b7d2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="2b7d2-112">Обновляет теги пространства имен \` MyNamespaceName на \` Created.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="2b7d2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b7d2-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="2b7d2-114">Обновление состояния пространства имен \` MyNamespaceName с помощью \` autoInflate = enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="2b7d2-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="2b7d2-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2b7d2-115">Example 3</span></span>

<span data-ttu-id="2b7d2-116">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="2b7d2-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="2b7d2-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="2b7d2-118">Пример 5. Создание и обновление пространства имен с помощью управления удостоверением в кластере</span><span class="sxs-lookup"><span data-stu-id="2b7d2-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
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
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="2b7d2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b7d2-119">PARAMETERS</span></span>

### <span data-ttu-id="2b7d2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b7d2-120">-DefaultProfile</span></span>
<span data-ttu-id="2b7d2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b7d2-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="2b7d2-122">-EnableAutoInflate</span></span>
<span data-ttu-id="2b7d2-123">Указывает на то, включена ли автообъединка</span><span class="sxs-lookup"><span data-stu-id="2b7d2-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="2b7d2-124">-EnableKafka</span></span>
<span data-ttu-id="2b7d2-125">включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="2b7d2-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="2b7d2-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="2b7d2-126">-Identity</span></span>
<span data-ttu-id="2b7d2-127">включение и отключение удостоверения для пространства имен</span><span class="sxs-lookup"><span data-stu-id="2b7d2-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="2b7d2-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="2b7d2-128">-IdentityUserDefined</span></span>
<span data-ttu-id="2b7d2-129">Удостоверение пользователя или "Нет"</span><span class="sxs-lookup"><span data-stu-id="2b7d2-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="2b7d2-130">-KeyProperty</span></span>
<span data-ttu-id="2b7d2-131">Список свойств ключа, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span><span class="sxs-lookup"><span data-stu-id="2b7d2-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="2b7d2-132">-KeySource</span></span>
<span data-ttu-id="2b7d2-133">Ключевой источник</span><span class="sxs-lookup"><span data-stu-id="2b7d2-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-134">-Location</span><span class="sxs-lookup"><span data-stu-id="2b7d2-134">-Location</span></span>
<span data-ttu-id="2b7d2-135">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="2b7d2-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="2b7d2-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="2b7d2-137">Верхний предел единиц пропускной способности при включенной автообновке, значение должно быть в пределах от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-138">-Name</span><span class="sxs-lookup"><span data-stu-id="2b7d2-138">-Name</span></span>
<span data-ttu-id="2b7d2-139">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="2b7d2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b7d2-140">-ResourceGroupName</span></span>
<span data-ttu-id="2b7d2-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="2b7d2-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2b7d2-142">-SkuCapacity</span></span>
<span data-ttu-id="2b7d2-143">Единицы пропускной способности еверха.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="2b7d2-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b7d2-144">-SkuName</span></span>
<span data-ttu-id="2b7d2-145">Namespace Sku Name.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="2b7d2-146">-State</span><span class="sxs-lookup"><span data-stu-id="2b7d2-146">-State</span></span>
<span data-ttu-id="2b7d2-147">"Отключить/включить пространство имен".</span><span class="sxs-lookup"><span data-stu-id="2b7d2-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="2b7d2-148">-Tag</span></span>
<span data-ttu-id="2b7d2-149">Hashtables which represents resource Tag.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b7d2-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b7d2-150">-Confirm</span></span>
<span data-ttu-id="2b7d2-151">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b7d2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b7d2-152">-WhatIf</span></span>
<span data-ttu-id="2b7d2-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b7d2-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b7d2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b7d2-155">CommonParameters</span></span>
<span data-ttu-id="2b7d2-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b7d2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b7d2-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2b7d2-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b7d2-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7d2-158">INPUTS</span></span>

### <span data-ttu-id="2b7d2-159">System.String</span><span class="sxs-lookup"><span data-stu-id="2b7d2-159">System.String</span></span>

### <span data-ttu-id="2b7d2-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2b7d2-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2b7d2-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="2b7d2-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2b7d2-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2b7d2-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2b7d2-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2b7d2-163">OUTPUTS</span></span>

### <span data-ttu-id="2b7d2-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2b7d2-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2b7d2-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2b7d2-165">NOTES</span></span>

## <span data-ttu-id="2b7d2-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b7d2-166">RELATED LINKS</span></span>
