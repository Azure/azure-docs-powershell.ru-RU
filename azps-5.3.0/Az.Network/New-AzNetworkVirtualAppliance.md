---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505533"
---
# <span data-ttu-id="a7c08-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a7c08-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="a7c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7c08-102">SYNOPSIS</span></span>
<span data-ttu-id="a7c08-103">Создайте ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="a7c08-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="a7c08-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7c08-104">SYNTAX</span></span>

### <span data-ttu-id="a7c08-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7c08-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7c08-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7c08-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7c08-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7c08-107">DESCRIPTION</span></span>
<span data-ttu-id="a7c08-108">Команда New-AzNetworkVirtualAppliance создает ресурс сетевого виртуального устройства в Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c08-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="a7c08-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7c08-109">EXAMPLES</span></span>

### <span data-ttu-id="a7c08-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7c08-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="a7c08-111">Создание ресурса сетевого виртуального устройства в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="a7c08-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="a7c08-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7c08-112">PARAMETERS</span></span>

### <span data-ttu-id="a7c08-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a7c08-113">-AsJob</span></span>
<span data-ttu-id="a7c08-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a7c08-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a7c08-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="a7c08-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="a7c08-116">URL-адрес BLOB-сайта конфигурации Bootstrap.</span><span class="sxs-lookup"><span data-stu-id="a7c08-116">The Bootstrap configuration blob URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="a7c08-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="a7c08-118">Конфигурация Cloudinit как обычный текст.</span><span class="sxs-lookup"><span data-stu-id="a7c08-118">The Cloudinit configuration as plain text.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="a7c08-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="a7c08-120">URL-адрес хранилища BLOB-то конфигурации Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="a7c08-120">The Cloudinit configuration blob storage URL.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7c08-121">-DefaultProfile</span></span>
<span data-ttu-id="a7c08-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7c08-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7c08-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a7c08-123">-Force</span></span>
<span data-ttu-id="a7c08-124">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="a7c08-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a7c08-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="a7c08-125">-Identity</span></span>
<span data-ttu-id="a7c08-126">Управляемое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="a7c08-126">The Managed identity.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-127">-Location</span><span class="sxs-lookup"><span data-stu-id="a7c08-127">-Location</span></span>
<span data-ttu-id="a7c08-128">Расположение общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a7c08-128">The public IP address location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-129">-Name</span><span class="sxs-lookup"><span data-stu-id="a7c08-129">-Name</span></span>
<span data-ttu-id="a7c08-130">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7c08-130">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7c08-131">-ResourceGroupName</span></span>
<span data-ttu-id="a7c08-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7c08-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7c08-133">-ResourceId</span></span>
<span data-ttu-id="a7c08-134">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="a7c08-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="a7c08-135">-Sku</span></span>
<span data-ttu-id="a7c08-136">SKU виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="a7c08-136">The Sku of the Virtual Appliance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="a7c08-137">-Tag</span></span>
<span data-ttu-id="a7c08-138">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="a7c08-138">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="a7c08-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="a7c08-140">AsN-номер виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="a7c08-140">The ASN number of the Virtual Appliance.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="a7c08-141">-VirtualHubId</span></span>
<span data-ttu-id="a7c08-142">ИД ресурса виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="a7c08-142">The Resource Id of the Virtual Hub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7c08-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7c08-143">-Confirm</span></span>
<span data-ttu-id="a7c08-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7c08-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7c08-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7c08-145">-WhatIf</span></span>
<span data-ttu-id="a7c08-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7c08-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7c08-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7c08-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7c08-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7c08-148">CommonParameters</span></span>
<span data-ttu-id="a7c08-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7c08-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7c08-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7c08-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7c08-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7c08-151">INPUTS</span></span>

### <span data-ttu-id="a7c08-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a7c08-152">System.String</span></span>

### <span data-ttu-id="a7c08-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="a7c08-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="a7c08-154">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a7c08-154">System.Int32</span></span>

### <span data-ttu-id="a7c08-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="a7c08-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="a7c08-156">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a7c08-156">System.String[]</span></span>

### <span data-ttu-id="a7c08-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a7c08-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a7c08-158">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7c08-158">OUTPUTS</span></span>

### <span data-ttu-id="a7c08-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="a7c08-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="a7c08-160">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7c08-160">NOTES</span></span>

## <span data-ttu-id="a7c08-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7c08-161">RELATED LINKS</span></span>
