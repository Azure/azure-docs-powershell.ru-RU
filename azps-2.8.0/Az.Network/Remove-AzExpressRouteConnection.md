---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteConnection.md
ms.openlocfilehash: 0b92f86f2a13bae6dc39ab7ffc3102be35925dd2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901974"
---
# <span data-ttu-id="e67f1-101">Remove-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e67f1-101">Remove-AzExpressRouteConnection</span></span>

## <span data-ttu-id="e67f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e67f1-102">SYNOPSIS</span></span>
<span data-ttu-id="e67f1-103">Удаление ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="e67f1-103">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="e67f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e67f1-104">SYNTAX</span></span>

### <span data-ttu-id="e67f1-105">ByExpressRouteConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e67f1-105">ByExpressRouteConnectionName (Default)</span></span>
```
Remove-AzExpressRouteConnection -ResourceGroupName <String> -ExpressRouteGatewayName <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67f1-106">ByExpressRouteConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="e67f1-106">ByExpressRouteConnectionResourceId</span></span>
```
Remove-AzExpressRouteConnection -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e67f1-107">ByExpressRouteConnectionObject</span><span class="sxs-lookup"><span data-stu-id="e67f1-107">ByExpressRouteConnectionObject</span></span>
```
Remove-AzExpressRouteConnection -InputObject <PSExpressRouteConnection> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e67f1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e67f1-108">DESCRIPTION</span></span>
<span data-ttu-id="e67f1-109">Удаление ExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="e67f1-109">Removes a ExpressRouteConnection.</span></span>

## <span data-ttu-id="e67f1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e67f1-110">EXAMPLES</span></span>

### <span data-ttu-id="e67f1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e67f1-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Remove-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection"
```

<span data-ttu-id="e67f1-112">В приведенном выше примере создается группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор — Запад US в группе ресурсов "testRG" в Azure.</span><span class="sxs-lookup"><span data-stu-id="e67f1-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="e67f1-113">Шлюз ExpressRoute будет создан на виртуальном концентраторе с двумя единицами масштабирования.</span><span class="sxs-lookup"><span data-stu-id="e67f1-113">A ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="e67f1-114">После создания шлюза он подключается к ExpressRouteSite с помощью команды New-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="e67f1-114">Once the gateway has been created, it is connected to the ExpressRouteSite using the New-AzExpressRouteConnection command.</span></span>

<span data-ttu-id="e67f1-115">После этого соединение будет удалено с помощью имени соединения.</span><span class="sxs-lookup"><span data-stu-id="e67f1-115">Then it removes the connection using the connection name.</span></span>

### <span data-ttu-id="e67f1-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e67f1-116">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> $ExpressRouteGateway = Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw"
PS C:\> $ExpressRouteCircuit = New-AzExpressRouteCircuit -ResourceGroupName "testRG" -Name "testExpressRouteCircuit" -Location "West Central US" -SkuTier Premium -SkuFamily MeteredData -ServiceProviderName "Equinix" -PeeringLocation "Silicon Valley" -BandwidthInMbps 200
PS C:\> Add-AzExpressRouteCircuitPeeringConfig -Name "AzurePrivatePeering" -ExpressRouteCircuit $ExpressRouteCircuit -PeeringType AzurePrivatePeering -PeerASN 100 -PrimaryPeerAddressPrefix "123.0.0.0/30" -SecondaryPeerAddressPrefix "123.0.0.4/30" -VlanId 300
PS C:\> $ExpressRouteCircuit = Set-AzExpressRouteCircuit -ExpressRouteCircuit $ExpressRouteCircuit
PS C:\> $ExpressRouteCircuitPeeringId = $ExpressRouteCircuit.Peerings[0].Id
PS C:\> New-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" -ExpressRouteCircuitPeeringId $ExpressRouteCircuitPeeringId -RoutingWeight 20
PS C:\> Get-AzExpressRouteConnection -ResourceGroupName $ExpressRouteGateway.ResourceGroupName -ParentResourceName $ExpressRouteGateway.Name -Name "testConnection" | Remove-AzExpressRouteConnection
```

<span data-ttu-id="e67f1-117">То же, что и в примере 1, но теперь он удаляет подключение, используя объект, переданный из командлета Get-AzExpressRouteConnection.</span><span class="sxs-lookup"><span data-stu-id="e67f1-117">Same as example 1, but it now removes the connection using the piped object from Get-AzExpressRouteConnection.</span></span>

## <span data-ttu-id="e67f1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e67f1-118">PARAMETERS</span></span>

### <span data-ttu-id="e67f1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67f1-119">-DefaultProfile</span></span>
<span data-ttu-id="e67f1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e67f1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e67f1-121">-ExpressRouteGatewayName</span><span class="sxs-lookup"><span data-stu-id="e67f1-121">-ExpressRouteGatewayName</span></span>
<span data-ttu-id="e67f1-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="e67f1-122">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67f1-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e67f1-123">-Force</span></span>
<span data-ttu-id="e67f1-124">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="e67f1-124">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="e67f1-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e67f1-125">-InputObject</span></span>
<span data-ttu-id="e67f1-126">Объект ExpressRouteConnection, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e67f1-126">The ExpressRouteConnection object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection
Parameter Sets: ByExpressRouteConnectionObject
Aliases: ExpressRouteConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e67f1-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e67f1-127">-Name</span></span>
<span data-ttu-id="e67f1-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e67f1-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases: ResourceName, ExpressRouteConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67f1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e67f1-129">-PassThru</span></span>
<span data-ttu-id="e67f1-130">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e67f1-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e67f1-131">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e67f1-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e67f1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e67f1-132">-ResourceGroupName</span></span>
<span data-ttu-id="e67f1-133">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e67f1-133">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67f1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e67f1-134">-ResourceId</span></span>
<span data-ttu-id="e67f1-135">Идентификатор ресурса объекта ExpressRouteConnection, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e67f1-135">The resource id of the ExpressRouteConnection object to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteConnectionResourceId
Aliases: ExpressRouteConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e67f1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e67f1-136">-Confirm</span></span>
<span data-ttu-id="e67f1-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e67f1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e67f1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e67f1-138">-WhatIf</span></span>
<span data-ttu-id="e67f1-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e67f1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e67f1-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e67f1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e67f1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67f1-141">CommonParameters</span></span>
<span data-ttu-id="e67f1-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e67f1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67f1-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67f1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67f1-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e67f1-144">INPUTS</span></span>

### <span data-ttu-id="e67f1-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e67f1-145">System.String</span></span>

### <span data-ttu-id="e67f1-146">Microsoft. Azure. Commands. Network. Models. PSExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="e67f1-146">Microsoft.Azure.Commands.Network.Models.PSExpressRouteConnection</span></span>

## <span data-ttu-id="e67f1-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e67f1-147">OUTPUTS</span></span>

### <span data-ttu-id="e67f1-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e67f1-148">System.Boolean</span></span>

## <span data-ttu-id="e67f1-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="e67f1-149">NOTES</span></span>

## <span data-ttu-id="e67f1-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e67f1-150">RELATED LINKS</span></span>
