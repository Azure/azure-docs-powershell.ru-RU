---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 6afbd081eca842e2185428f90a18932e05c3bbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984651"
---
# <span data-ttu-id="acd6c-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="acd6c-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="acd6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd6c-102">SYNOPSIS</span></span>
<span data-ttu-id="acd6c-103">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="acd6c-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="acd6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="acd6c-104">SYNTAX</span></span>

### <span data-ttu-id="acd6c-105">NamespaceParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="acd6c-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd6c-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd6c-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="acd6c-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="acd6c-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acd6c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="acd6c-108">DESCRIPTION</span></span>
<span data-ttu-id="acd6c-109">Этот Set-AzEventHubNamespace обновляет свойства указанного пространства имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="acd6c-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="acd6c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="acd6c-110">EXAMPLES</span></span>

### <span data-ttu-id="acd6c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="acd6c-111">Example 1</span></span>
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

<span data-ttu-id="acd6c-112">Обновляет теги пространства имен \` MyNamespaceName на \` Created.</span><span class="sxs-lookup"><span data-stu-id="acd6c-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="acd6c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="acd6c-113">Example 2</span></span>
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

<span data-ttu-id="acd6c-114">Обновление состояния пространства имен \` MyNamespaceName с помощью \` autoInflate = enabled и MaximumThroughputUnits = 10</span><span class="sxs-lookup"><span data-stu-id="acd6c-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="acd6c-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="acd6c-115">Example 3</span></span>

<span data-ttu-id="acd6c-116">Обновляет указанное пространство имен концентраторов событий.</span><span class="sxs-lookup"><span data-stu-id="acd6c-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="acd6c-117">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="acd6c-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="acd6c-118">Пример 5. Создание и обновление пространства имен с помощью управления удостоверением в кластере</span><span class="sxs-lookup"><span data-stu-id="acd6c-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="acd6c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acd6c-119">PARAMETERS</span></span>

### <span data-ttu-id="acd6c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd6c-120">-DefaultProfile</span></span>
<span data-ttu-id="acd6c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="acd6c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="acd6c-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="acd6c-122">-EnableAutoInflate</span></span>
<span data-ttu-id="acd6c-123">Указывает на то, включена ли автообъединка</span><span class="sxs-lookup"><span data-stu-id="acd6c-123">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="acd6c-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="acd6c-124">-EnableKafka</span></span>
<span data-ttu-id="acd6c-125">включение и отключение Kafka для пространства имен</span><span class="sxs-lookup"><span data-stu-id="acd6c-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="acd6c-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="acd6c-126">-Identity</span></span>
<span data-ttu-id="acd6c-127">включение и отключение удостоверения для пространства имен</span><span class="sxs-lookup"><span data-stu-id="acd6c-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="acd6c-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="acd6c-128">-IdentityUserDefined</span></span>
<span data-ttu-id="acd6c-129">Удостоверение пользователя или "Нет"</span><span class="sxs-lookup"><span data-stu-id="acd6c-129">User defined Identity or None</span></span>

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

### <span data-ttu-id="acd6c-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="acd6c-130">-KeyProperty</span></span>
<span data-ttu-id="acd6c-131">Список свойств ключа, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span><span class="sxs-lookup"><span data-stu-id="acd6c-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

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

### <span data-ttu-id="acd6c-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="acd6c-132">-KeySource</span></span>
<span data-ttu-id="acd6c-133">Ключевой источник</span><span class="sxs-lookup"><span data-stu-id="acd6c-133">Key Source</span></span>

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

### <span data-ttu-id="acd6c-134">-Location</span><span class="sxs-lookup"><span data-stu-id="acd6c-134">-Location</span></span>
<span data-ttu-id="acd6c-135">Расположение пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="acd6c-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="acd6c-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="acd6c-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="acd6c-137">Верхний предел единиц пропускной способности при включенной автообновке, значение должно быть в пределах от 0 до 20 единиц пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="acd6c-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="acd6c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="acd6c-138">-Name</span></span>
<span data-ttu-id="acd6c-139">Имя пространства имен EventHub.</span><span class="sxs-lookup"><span data-stu-id="acd6c-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="acd6c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd6c-140">-ResourceGroupName</span></span>
<span data-ttu-id="acd6c-141">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acd6c-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="acd6c-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="acd6c-142">-SkuCapacity</span></span>
<span data-ttu-id="acd6c-143">Единицы пропускной способности еверха.</span><span class="sxs-lookup"><span data-stu-id="acd6c-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="acd6c-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="acd6c-144">-SkuName</span></span>
<span data-ttu-id="acd6c-145">Namespace Sku Name.</span><span class="sxs-lookup"><span data-stu-id="acd6c-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="acd6c-146">-State</span><span class="sxs-lookup"><span data-stu-id="acd6c-146">-State</span></span>
<span data-ttu-id="acd6c-147">"Отключить/включить пространство имен".</span><span class="sxs-lookup"><span data-stu-id="acd6c-147">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="acd6c-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="acd6c-148">-Tag</span></span>
<span data-ttu-id="acd6c-149">Hashtables which represents resource Tag.</span><span class="sxs-lookup"><span data-stu-id="acd6c-149">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="acd6c-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="acd6c-150">-Confirm</span></span>
<span data-ttu-id="acd6c-151">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd6c-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd6c-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd6c-152">-WhatIf</span></span>
<span data-ttu-id="acd6c-153">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acd6c-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd6c-154">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="acd6c-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd6c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd6c-155">CommonParameters</span></span>
<span data-ttu-id="acd6c-156">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acd6c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd6c-157">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acd6c-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd6c-158">INPUTS</span><span class="sxs-lookup"><span data-stu-id="acd6c-158">INPUTS</span></span>

### <span data-ttu-id="acd6c-159">System.String</span><span class="sxs-lookup"><span data-stu-id="acd6c-159">System.String</span></span>

### <span data-ttu-id="acd6c-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="acd6c-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="acd6c-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="acd6c-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="acd6c-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="acd6c-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="acd6c-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acd6c-163">OUTPUTS</span></span>

### <span data-ttu-id="acd6c-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="acd6c-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="acd6c-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="acd6c-165">NOTES</span></span>

## <span data-ttu-id="acd6c-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="acd6c-166">RELATED LINKS</span></span>
