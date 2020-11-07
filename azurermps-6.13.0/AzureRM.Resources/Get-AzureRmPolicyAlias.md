---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRm.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicyAlias.md
ms.openlocfilehash: ee37ae0d7ed03bb760486c727df20f8579fa77c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733132"
---
# <span data-ttu-id="6b313-101">Get-AzureRmPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="6b313-101">Get-AzureRmPolicyAlias</span></span>

## <span data-ttu-id="6b313-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6b313-102">SYNOPSIS</span></span>
<span data-ttu-id="6b313-103">Get-AzureRmPolicyAlias извлекает и выводит типы ресурсов поставщика Azure, которые имеют определенные псевдонимы и соответствуют указанным значениям параметров.</span><span class="sxs-lookup"><span data-stu-id="6b313-103">Get-AzureRmPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="6b313-104">Если не указаны никакие параметры, будут выведены все типы ресурсов поставщика, которые содержат псевдоним.</span><span class="sxs-lookup"><span data-stu-id="6b313-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="6b313-105">Параметр-ListAvailable изменяет это поведение, передавая список всех соответствующих типов ресурсов, включая те, у которых нет псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="6b313-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b313-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6b313-106">SYNTAX</span></span>

```
Get-AzureRmPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b313-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b313-107">DESCRIPTION</span></span>
<span data-ttu-id="6b313-108">Командлет **Get-AzureRmPolicyAlias** получает список псевдонимов политик.</span><span class="sxs-lookup"><span data-stu-id="6b313-108">The **Get-AzureRmPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="6b313-109">Псевдонимы политик используются политикой Azure для ссылки на свойства типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="6b313-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="6b313-110">Указаны параметры, которые ограничивают элементы в списке, сопоставляя различные свойства типа ресурса или его псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="6b313-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="6b313-111">Указанное значение соответствия соответствует условию, что Целевая строка включает в себя сравнение с учетом регистра.</span><span class="sxs-lookup"><span data-stu-id="6b313-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="6b313-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6b313-112">EXAMPLES</span></span>

### <span data-ttu-id="6b313-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6b313-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="6b313-114">Список всех типов ресурсов поставщика с псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="6b313-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="6b313-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6b313-115">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="6b313-116">Список всех типов ресурсов поставщика, включая те, у которых нет псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="6b313-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="6b313-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6b313-117">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="6b313-118">Список всех типов ресурсов поставщика, для которых пространство имен совпадает с "вычисляемым" и содержит псевдоним.</span><span class="sxs-lookup"><span data-stu-id="6b313-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="6b313-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="6b313-119">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="6b313-120">Список всех типов ресурсов поставщика, тип ресурсов которых соответствует "Virtual" и содержащих псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="6b313-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="6b313-121">Пример 5</span><span class="sxs-lookup"><span data-stu-id="6b313-121">Example 5</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="6b313-122">Список всех типов ресурсов поставщика, тип ресурсов которых соответствует "Virtual", в том числе для тех, у которых нет псевдонимов.</span><span class="sxs-lookup"><span data-stu-id="6b313-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="6b313-123">Пример 6</span><span class="sxs-lookup"><span data-stu-id="6b313-123">Example 6</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="6b313-124">Список всех типов ресурсов поставщика, пространство имен которых соответствует "COMPUTE", а тип ресурса — "виртуальный" и содержит псевдоним.</span><span class="sxs-lookup"><span data-stu-id="6b313-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="6b313-125">Примечание:-NamespaceMatch и-ResourceTypeMatch предоставляют исключительные совпадения, а другие — включительно.</span><span class="sxs-lookup"><span data-stu-id="6b313-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="6b313-126">Пример 7</span><span class="sxs-lookup"><span data-stu-id="6b313-126">Example 7</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="6b313-127">Список всех типов ресурсов поставщика, которые содержат псевдоним, совпадающий с "виртуальным".</span><span class="sxs-lookup"><span data-stu-id="6b313-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="6b313-128">Пример 8</span><span class="sxs-lookup"><span data-stu-id="6b313-128">Example 8</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="6b313-129">Выводит список всех типов ресурсов поставщика, которые содержат псевдонимы, соответствующие виртуальному, или псевдоним с путем, соответствующим "Network".</span><span class="sxs-lookup"><span data-stu-id="6b313-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="6b313-130">Пример 9</span><span class="sxs-lookup"><span data-stu-id="6b313-130">Example 9</span></span>
```powershell
PS C:\> Get-AzureRmPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="6b313-131">Список всех типов ресурсов поставщика с версией Alpha API или псевдонимом с альфа-версией API.</span><span class="sxs-lookup"><span data-stu-id="6b313-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="6b313-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6b313-132">PARAMETERS</span></span>

### <span data-ttu-id="6b313-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-133">-AliasMatch</span></span>
<span data-ttu-id="6b313-134">Включает в выходные элементы с псевдонимами, имена которых совпадают с этим значением.</span><span class="sxs-lookup"><span data-stu-id="6b313-134">Includes in the output items with aliases whose name matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b313-135">-ApiVersion</span></span>
<span data-ttu-id="6b313-136">Если этот параметр установлен, указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6b313-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="6b313-137">Если не указано, версия API автоматически определяется как самая свежая доступная.</span><span class="sxs-lookup"><span data-stu-id="6b313-137">If not specified, the API version is automatically determined as the latest available.</span></span>
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

### <span data-ttu-id="6b313-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-138">-ApiVersionMatch</span></span>
<span data-ttu-id="6b313-139">Включает в выходные элементы, для которых типы ресурсов или псевдонимы имеют соответствующую версию API.</span><span class="sxs-lookup"><span data-stu-id="6b313-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>
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

### <span data-ttu-id="6b313-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b313-140">-DefaultProfile</span></span>
<span data-ttu-id="6b313-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6b313-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="6b313-142">-ListAvailable</span></span>
<span data-ttu-id="6b313-143">Включает в себя элементы, совпадающие с псевдонимами, и без них.</span><span class="sxs-lookup"><span data-stu-id="6b313-143">Includes in the output matching items with and without aliases.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-144">-LocationMatch</span></span>
<span data-ttu-id="6b313-145">Включает в выходные элементы, для которых типы ресурсов соответствуют расположениям.</span><span class="sxs-lookup"><span data-stu-id="6b313-145">Includes in the output items whose resource types have a matching location.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-146">-NamespaceMatch</span></span>
<span data-ttu-id="6b313-147">Ограничивает вывод для элементов, пространство имен которых соответствует этому значению.</span><span class="sxs-lookup"><span data-stu-id="6b313-147">Limits the output to items whose namespace matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-148">-PathMatch</span></span>
<span data-ttu-id="6b313-149">Включает в выходные элементы с псевдонимами, которые содержат путь, совпадающий с этим значением.</span><span class="sxs-lookup"><span data-stu-id="6b313-149">Includes in the output items with aliases containing a path that matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b313-150">-Pre</span></span>
<span data-ttu-id="6b313-151">Если этот параметр установлен, при автоматическом определении версии для использования командлета необходимо использовать предварительно выпущенные версии API.</span><span class="sxs-lookup"><span data-stu-id="6b313-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>
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

### <span data-ttu-id="6b313-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="6b313-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="6b313-153">Ограничивает вывод для элементов, тип ресурсов которых соответствует этому значению.</span><span class="sxs-lookup"><span data-stu-id="6b313-153">Limits the output to items whose resource type matches this value.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b313-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b313-154">CommonParameters</span></span>
<span data-ttu-id="6b313-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6b313-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b313-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b313-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b313-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6b313-157">INPUTS</span></span>

## <span data-ttu-id="6b313-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b313-158">OUTPUTS</span></span>

### <span data-ttu-id="6b313-159">Microsoft. Azure. Commands. ResourceManager. командлеты. Реализация. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="6b313-159">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="6b313-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="6b313-160">NOTES</span></span>

* <span data-ttu-id="6b313-161">Чтобы развернуть псевдоним или любое другое свойство, переводите его в вертикальный канал `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="6b313-161">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="6b313-162">Например: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="6b313-162">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="6b313-163">Дополнительные свойства доступны в выходных данных и могут отображаться путем передачи выходных данных в поток вывода `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="6b313-163">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="6b313-164">Например: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="6b313-164">For example: `Get-AzureRmPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="6b313-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b313-165">RELATED LINKS</span></span>
