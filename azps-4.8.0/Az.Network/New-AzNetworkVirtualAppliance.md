---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkVirtualAppliance.md
ms.openlocfilehash: 9b3991a24430afa74853f742bffa12b772dbeaf2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244824"
---
# <span data-ttu-id="097d5-101">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="097d5-101">New-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="097d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="097d5-102">SYNOPSIS</span></span>
<span data-ttu-id="097d5-103">Создайте ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="097d5-103">Create a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="097d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="097d5-104">SYNTAX</span></span>

### <span data-ttu-id="097d5-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="097d5-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> -Location <String>
 -VirtualHubId <String> -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32>
 [-Identity <PSManagedServiceIdentity>] [-BootStrapConfigurationBlob <String[]>]
 [-CloudInitConfigurationBlob <String[]>] [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="097d5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="097d5-106">ResourceIdParameterSet</span></span>
```
New-AzNetworkVirtualAppliance -ResourceId <String> -Location <String> -VirtualHubId <String>
 -Sku <PSVirtualApplianceSkuProperties> -VirtualApplianceAsn <Int32> [-Identity <PSManagedServiceIdentity>]
 [-BootStrapConfigurationBlob <String[]>] [-CloudInitConfigurationBlob <String[]>]
 [-CloudInitConfiguration <String>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="097d5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="097d5-107">DESCRIPTION</span></span>
<span data-ttu-id="097d5-108">Команда New-AzNetworkVirtualAppliance создает ресурс сетевого виртуального устройства в Azure.</span><span class="sxs-lookup"><span data-stu-id="097d5-108">The New-AzNetworkVirtualAppliance command creates a Network Virtual Appliance resource in Azure.</span></span>

## <span data-ttu-id="097d5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="097d5-109">EXAMPLES</span></span>

### <span data-ttu-id="097d5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="097d5-110">Example 1</span></span>
```powershell
PS C:\> $sku=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
PS C:\> $hub=Get-AzVirtualHub -ResourceGroupName testrg -Name hub
PS C:\> $nva=New-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva -Location eastus2 -VirtualApplianceAsn 1270 -VirtualHubId $hub.Id -Sku $sku -CloudInitConfiguration "echo Hello World!"

```

<span data-ttu-id="097d5-111">Создание нового ресурса виртуального сетевого устройства в группе ресурсов: testrg.</span><span class="sxs-lookup"><span data-stu-id="097d5-111">Creates a new Network Virtual Appliance resource in resource group: testrg.</span></span>

## <span data-ttu-id="097d5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="097d5-112">PARAMETERS</span></span>

### <span data-ttu-id="097d5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="097d5-113">-AsJob</span></span>
<span data-ttu-id="097d5-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="097d5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="097d5-115">-BootStrapConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="097d5-115">-BootStrapConfigurationBlob</span></span>
<span data-ttu-id="097d5-116">URL-адрес блоба конфигурации начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="097d5-116">The Bootstrap configuration blob URL.</span></span>

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

### <span data-ttu-id="097d5-117">-CloudInitConfiguration</span><span class="sxs-lookup"><span data-stu-id="097d5-117">-CloudInitConfiguration</span></span>
<span data-ttu-id="097d5-118">Конфигурация Cloudinit в виде обычного текста.</span><span class="sxs-lookup"><span data-stu-id="097d5-118">The Cloudinit configuration as plain text.</span></span>

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

### <span data-ttu-id="097d5-119">-CloudInitConfigurationBlob</span><span class="sxs-lookup"><span data-stu-id="097d5-119">-CloudInitConfigurationBlob</span></span>
<span data-ttu-id="097d5-120">URL-адрес хранилища больших двоичных объектов конфигурации Cloudinit.</span><span class="sxs-lookup"><span data-stu-id="097d5-120">The Cloudinit configuration blob storage URL.</span></span>

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

### <span data-ttu-id="097d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="097d5-121">-DefaultProfile</span></span>
<span data-ttu-id="097d5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="097d5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="097d5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="097d5-123">-Force</span></span>
<span data-ttu-id="097d5-124">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="097d5-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="097d5-125">-Identity</span><span class="sxs-lookup"><span data-stu-id="097d5-125">-Identity</span></span>
<span data-ttu-id="097d5-126">Управляемое удостоверение.</span><span class="sxs-lookup"><span data-stu-id="097d5-126">The Managed identity.</span></span>

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

### <span data-ttu-id="097d5-127">-Location</span><span class="sxs-lookup"><span data-stu-id="097d5-127">-Location</span></span>
<span data-ttu-id="097d5-128">Расположение общедоступного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="097d5-128">The public IP address location.</span></span>

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

### <span data-ttu-id="097d5-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="097d5-129">-Name</span></span>
<span data-ttu-id="097d5-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="097d5-130">The resource name.</span></span>

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

### <span data-ttu-id="097d5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="097d5-131">-ResourceGroupName</span></span>
<span data-ttu-id="097d5-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="097d5-132">The resource group name.</span></span>

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

### <span data-ttu-id="097d5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="097d5-133">-ResourceId</span></span>
<span data-ttu-id="097d5-134">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="097d5-134">The resource Id.</span></span>

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

### <span data-ttu-id="097d5-135">-SKU</span><span class="sxs-lookup"><span data-stu-id="097d5-135">-Sku</span></span>
<span data-ttu-id="097d5-136">SKU виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="097d5-136">The Sku of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="097d5-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="097d5-137">-Tag</span></span>
<span data-ttu-id="097d5-138">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="097d5-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="097d5-139">-VirtualApplianceAsn</span><span class="sxs-lookup"><span data-stu-id="097d5-139">-VirtualApplianceAsn</span></span>
<span data-ttu-id="097d5-140">Номер ASN виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="097d5-140">The ASN number of the Virtual Appliance.</span></span>

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

### <span data-ttu-id="097d5-141">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="097d5-141">-VirtualHubId</span></span>
<span data-ttu-id="097d5-142">Идентификатор ресурса виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="097d5-142">The Resource Id of the Virtual Hub.</span></span>

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

### <span data-ttu-id="097d5-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="097d5-143">-Confirm</span></span>
<span data-ttu-id="097d5-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="097d5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="097d5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="097d5-145">-WhatIf</span></span>
<span data-ttu-id="097d5-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="097d5-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="097d5-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="097d5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="097d5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097d5-148">CommonParameters</span></span>
<span data-ttu-id="097d5-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="097d5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097d5-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="097d5-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097d5-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="097d5-151">INPUTS</span></span>

### <span data-ttu-id="097d5-152">System. String</span><span class="sxs-lookup"><span data-stu-id="097d5-152">System.String</span></span>

### <span data-ttu-id="097d5-153">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="097d5-153">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

### <span data-ttu-id="097d5-154">System. Int32</span><span class="sxs-lookup"><span data-stu-id="097d5-154">System.Int32</span></span>

### <span data-ttu-id="097d5-155">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="097d5-155">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

### <span data-ttu-id="097d5-156">System. String []</span><span class="sxs-lookup"><span data-stu-id="097d5-156">System.String[]</span></span>

### <span data-ttu-id="097d5-157">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="097d5-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="097d5-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="097d5-158">OUTPUTS</span></span>

### <span data-ttu-id="097d5-159">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="097d5-159">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="097d5-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="097d5-160">NOTES</span></span>

## <span data-ttu-id="097d5-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="097d5-161">RELATED LINKS</span></span>
