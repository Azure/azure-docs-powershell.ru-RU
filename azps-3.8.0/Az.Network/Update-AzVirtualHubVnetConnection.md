---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualHubVnetConnection.md
ms.openlocfilehash: e3ba40bf4527571ed6b3396a9208a9a0931a7be7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912955"
---
# <span data-ttu-id="c5dd8-101">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="c5dd8-101">Update-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="c5dd8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c5dd8-103">Обновление существующего HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-103">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="c5dd8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5dd8-104">SYNTAX</span></span>

### <span data-ttu-id="c5dd8-105">ByHubVirtualNetworkConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c5dd8-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5dd8-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="c5dd8-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Update-AzVirtualHubVnetConnection -InputObject <PSHubVirtualNetworkConnection>
 -EnableInternetSecurity <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c5dd8-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="c5dd8-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Update-AzVirtualHubVnetConnection -ResourceId <String> -EnableInternetSecurity <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5dd8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="c5dd8-109">Обновление существующего HubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-109">Updates an existing HubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="c5dd8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="c5dd8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c5dd8-111">Example 1</span></span>
```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Update-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -EnableInternetSecurity $true
Name                   : testvnetconnection
Id                     : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : True
ProvisioningState      : Succeeded
```

<span data-ttu-id="c5dd8-112">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="c5dd8-113">Кроме того, будет создано виртуальное сетевое подключение, которое является одноранговым виртуальным окружением для виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-113">A Virtual Network Connection is also created which is peer the Virtual Network to the Virtual Hub.</span></span> <span data-ttu-id="c5dd8-114">После этого виртуальное сетевое подключение обновится, чтобы обеспечить безопасность в Интернете.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-114">This Virtual Network Connection is then updated to enable internet security.</span></span>

## <span data-ttu-id="c5dd8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5dd8-115">PARAMETERS</span></span>

### <span data-ttu-id="c5dd8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5dd8-116">-AsJob</span></span>
<span data-ttu-id="c5dd8-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c5dd8-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5dd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5dd8-118">-DefaultProfile</span></span>
<span data-ttu-id="c5dd8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-120">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="c5dd8-120">-EnableInternetSecurity</span></span>
<span data-ttu-id="c5dd8-121">Включите Интернет-безопасность для этого подключения.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-121">Enable internet security for this connection.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c5dd8-122">-InputObject</span></span>
<span data-ttu-id="c5dd8-123">Ресурс hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-123">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5dd8-124">-Name</span></span>
<span data-ttu-id="c5dd8-125">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-125">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="c5dd8-126">-ParentResourceName</span></span>
<span data-ttu-id="c5dd8-127">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-127">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5dd8-128">-ResourceGroupName</span></span>
<span data-ttu-id="c5dd8-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c5dd8-130">-ResourceId</span></span>
<span data-ttu-id="c5dd8-131">Идентификатор ресурса для ресурса hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-131">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5dd8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5dd8-132">-Confirm</span></span>
<span data-ttu-id="c5dd8-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5dd8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5dd8-134">-WhatIf</span></span>
<span data-ttu-id="c5dd8-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5dd8-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5dd8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5dd8-137">CommonParameters</span></span>
<span data-ttu-id="c5dd8-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5dd8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5dd8-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5dd8-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5dd8-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5dd8-140">INPUTS</span></span>

### <span data-ttu-id="c5dd8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c5dd8-141">System.String</span></span>

### <span data-ttu-id="c5dd8-142">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="c5dd8-142">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="c5dd8-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5dd8-143">OUTPUTS</span></span>

### <span data-ttu-id="c5dd8-144">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="c5dd8-144">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="c5dd8-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5dd8-145">NOTES</span></span>

## <span data-ttu-id="c5dd8-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5dd8-146">RELATED LINKS</span></span>