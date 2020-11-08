---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073984"
---
# <span data-ttu-id="8b00a-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8b00a-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="8b00a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8b00a-102">SYNOPSIS</span></span>
<span data-ttu-id="8b00a-103">Командлет Remove-AzVirtualHubVnetConnection удаляет подключение к виртуальной сети Azure, которое одноранговую сеть с удаленной сетью — на центральную ВИРТУАЛЬную сеть.</span><span class="sxs-lookup"><span data-stu-id="8b00a-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="8b00a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8b00a-104">SYNTAX</span></span>

### <span data-ttu-id="8b00a-105">ByHubVirtualNetworkConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b00a-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8b00a-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="8b00a-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b00a-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="8b00a-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b00a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b00a-108">DESCRIPTION</span></span>
<span data-ttu-id="8b00a-109">Командлет Remove-AzVirtualHubVnetConnection удаляет подключение к виртуальной сети Azure, которое одноранговую сеть с удаленной сетью — на центральную ВИРТУАЛЬную сеть.</span><span class="sxs-lookup"><span data-stu-id="8b00a-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="8b00a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8b00a-110">EXAMPLES</span></span>

### <span data-ttu-id="8b00a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8b00a-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="8b00a-112">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="8b00a-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="8b00a-113">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="8b00a-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="8b00a-114">После создания подключения к виртуальной сети Hub он удаляет подключение к виртуальной сети Hub, используя имя группы ресурсов, имя концентратора и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="8b00a-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="8b00a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8b00a-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="8b00a-116">В этой группе ресурсов будет создана группа ресурсов, Виртуальная глобальная сеть, Виртуальная сетевая служба, виртуальный концентратор в центре US в Azure.</span><span class="sxs-lookup"><span data-stu-id="8b00a-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="8b00a-117">После этого будет создано виртуальное сетевое подключение, которое будет использоваться для пиринга виртуальной сети с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="8b00a-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="8b00a-118">После создания подключения к виртуальной сети Hub он удаляет подключение к виртуальной сети Hub с помощью оболочки PowerShell на выходе Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="8b00a-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="8b00a-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8b00a-119">PARAMETERS</span></span>

### <span data-ttu-id="8b00a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b00a-120">-AsJob</span></span>
<span data-ttu-id="8b00a-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8b00a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b00a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b00a-122">-DefaultProfile</span></span>
<span data-ttu-id="8b00a-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b00a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b00a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="8b00a-124">-Force</span></span>
<span data-ttu-id="8b00a-125">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="8b00a-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="8b00a-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b00a-126">-InputObject</span></span>
<span data-ttu-id="8b00a-127">Ресурс hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="8b00a-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b00a-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8b00a-128">-Name</span></span>
<span data-ttu-id="8b00a-129">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b00a-129">The resource name.</span></span>

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

### <span data-ttu-id="8b00a-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8b00a-130">-ParentResourceName</span></span>
<span data-ttu-id="8b00a-131">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="8b00a-131">The parent resource name.</span></span>

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

### <span data-ttu-id="8b00a-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b00a-132">-PassThru</span></span>
<span data-ttu-id="8b00a-133">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8b00a-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8b00a-134">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8b00a-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b00a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b00a-135">-ResourceGroupName</span></span>
<span data-ttu-id="8b00a-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8b00a-136">The resource group name.</span></span>

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

### <span data-ttu-id="8b00a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b00a-137">-ResourceId</span></span>
<span data-ttu-id="8b00a-138">Идентификатор ресурса для ресурса hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="8b00a-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="8b00a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b00a-139">-Confirm</span></span>
<span data-ttu-id="8b00a-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8b00a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b00a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b00a-141">-WhatIf</span></span>
<span data-ttu-id="8b00a-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8b00a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b00a-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8b00a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b00a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b00a-144">CommonParameters</span></span>
<span data-ttu-id="8b00a-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8b00a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b00a-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b00a-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b00a-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8b00a-147">INPUTS</span></span>

### <span data-ttu-id="8b00a-148">Microsoft. Azure. Commands. Network. Models. PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="8b00a-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="8b00a-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8b00a-149">System.String</span></span>

## <span data-ttu-id="8b00a-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b00a-150">OUTPUTS</span></span>

### <span data-ttu-id="8b00a-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b00a-151">System.Boolean</span></span>

## <span data-ttu-id="8b00a-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="8b00a-152">NOTES</span></span>

## <span data-ttu-id="8b00a-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b00a-153">RELATED LINKS</span></span>

[<span data-ttu-id="8b00a-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8b00a-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="8b00a-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8b00a-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
