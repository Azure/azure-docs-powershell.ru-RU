---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733148"
---
# <span data-ttu-id="3a9ff-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="3a9ff-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="3a9ff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a9ff-102">SYNOPSIS</span></span>
<span data-ttu-id="3a9ff-103">Командлет New-AzureRmVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a9ff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a9ff-104">SYNTAX</span></span>

### <span data-ttu-id="3a9ff-105">ByVirtualHubNameByRemoteVirtualNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a9ff-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9ff-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3a9ff-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a9ff-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3a9ff-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9ff-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3a9ff-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a9ff-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="3a9ff-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a9ff-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3a9ff-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a9ff-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a9ff-111">DESCRIPTION</span></span>
<span data-ttu-id="3a9ff-112">Командлет New-AzureRmVirtualHubVnetConnection создает ресурс HubVirtualNetworkConnection, который является одноранговым узлом виртуальной сети для виртуального концентратора Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="3a9ff-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a9ff-113">EXAMPLES</span></span>

### <span data-ttu-id="3a9ff-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a9ff-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="3a9ff-115">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="3a9ff-116">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="3a9ff-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a9ff-117">PARAMETERS</span></span>

### <span data-ttu-id="3a9ff-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a9ff-118">-AsJob</span></span>
<span data-ttu-id="3a9ff-119">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a9ff-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a9ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a9ff-120">-DefaultProfile</span></span>
<span data-ttu-id="3a9ff-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a9ff-122">-Name</span></span>
<span data-ttu-id="3a9ff-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3a9ff-124">-ParentObject</span></span>
<span data-ttu-id="3a9ff-125">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a9ff-126">-ParentResourceId</span></span>
<span data-ttu-id="3a9ff-127">Родительский ресурс.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="3a9ff-128">-ParentResourceName</span></span>
<span data-ttu-id="3a9ff-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3a9ff-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="3a9ff-131">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3a9ff-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="3a9ff-133">Удаленная виртуальная сеть, к которой подключено это подключение к виртуальному сетевому концентратору.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a9ff-134">-ResourceGroupName</span></span>
<span data-ttu-id="3a9ff-135">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a9ff-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a9ff-136">-Confirm</span></span>
<span data-ttu-id="3a9ff-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a9ff-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a9ff-138">-WhatIf</span></span>
<span data-ttu-id="3a9ff-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a9ff-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a9ff-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a9ff-141">CommonParameters</span></span>
<span data-ttu-id="3a9ff-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a9ff-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a9ff-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a9ff-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a9ff-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a9ff-144">INPUTS</span></span>

### <span data-ttu-id="3a9ff-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3a9ff-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3a9ff-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3a9ff-146">System.String</span></span>

## <span data-ttu-id="3a9ff-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a9ff-147">OUTPUTS</span></span>

### <span data-ttu-id="3a9ff-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="3a9ff-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="3a9ff-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a9ff-149">NOTES</span></span>

## <span data-ttu-id="3a9ff-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a9ff-150">RELATED LINKS</span></span>
