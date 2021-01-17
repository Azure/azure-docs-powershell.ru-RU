---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: a6affc87ab0ace3e3808d43ac6bd9cfeb9496970
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405444"
---
# <span data-ttu-id="1b4ee-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b4ee-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="1b4ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b4ee-102">SYNOPSIS</span></span>
<span data-ttu-id="1b4ee-103">С Remove-AzVirtualHubVnetConnection-сети удаляется виртуальное сетевое подключение Azure, которое является одноранговой сетью VNET, удаленной с центром VNET.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="1b4ee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b4ee-104">SYNTAX</span></span>

### <span data-ttu-id="1b4ee-105">ByHubVirtualNetworkConnectionName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1b4ee-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1b4ee-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="1b4ee-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1b4ee-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="1b4ee-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b4ee-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b4ee-108">DESCRIPTION</span></span>
<span data-ttu-id="1b4ee-109">С Remove-AzVirtualHubVnetConnection-сети удаляется виртуальное сетевое подключение Azure, которое является одноранговой сетью VNET, удаленной с центром VNET.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="1b4ee-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b4ee-110">EXAMPLES</span></span>

### <span data-ttu-id="1b4ee-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b4ee-111">Example 1</span></span>

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

<span data-ttu-id="1b4ee-112">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора в центральной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="1b4ee-113">После этого будет создано виртуальное сетевое подключение, которое привяет виртуальную сеть к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="1b4ee-114">После создания виртуального сетевого подключения концентратора удаляется виртуальное сетевое подключение концентратора, используя имя группы ресурсов, имя концентратора и имя подключения.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="1b4ee-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1b4ee-115">Example 2</span></span>

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

<span data-ttu-id="1b4ee-116">Выше будет создание группы ресурсов, виртуальной WAN, виртуальной сети, виртуального концентратора в центральной части США в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="1b4ee-117">После этого будет создано виртуальное сетевое подключение, которое привяет виртуальную сеть к виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="1b4ee-118">После создания виртуального сетевого подключения концентратора удаляется виртуальное сетевое подключение концентратора с помощью piping powershell на выходе из Get-AzHubVirtualNetworkConnection.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="1b4ee-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b4ee-119">PARAMETERS</span></span>

### <span data-ttu-id="1b4ee-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b4ee-120">-AsJob</span></span>
<span data-ttu-id="1b4ee-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1b4ee-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b4ee-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b4ee-122">-DefaultProfile</span></span>
<span data-ttu-id="1b4ee-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b4ee-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1b4ee-124">-Force</span></span>
<span data-ttu-id="1b4ee-125">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="1b4ee-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="1b4ee-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b4ee-126">-InputObject</span></span>
<span data-ttu-id="1b4ee-127">Ресурс hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="1b4ee-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1b4ee-128">-Name</span></span>
<span data-ttu-id="1b4ee-129">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-129">The resource name.</span></span>

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

### <span data-ttu-id="1b4ee-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="1b4ee-130">-ParentResourceName</span></span>
<span data-ttu-id="1b4ee-131">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-131">The parent resource name.</span></span>

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

### <span data-ttu-id="1b4ee-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b4ee-132">-PassThru</span></span>
<span data-ttu-id="1b4ee-133">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1b4ee-134">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1b4ee-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b4ee-135">-ResourceGroupName</span></span>
<span data-ttu-id="1b4ee-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-136">The resource group name.</span></span>

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

### <span data-ttu-id="1b4ee-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b4ee-137">-ResourceId</span></span>
<span data-ttu-id="1b4ee-138">Код ресурса hubvirtualnetworkconnection, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="1b4ee-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b4ee-139">-Confirm</span></span>
<span data-ttu-id="1b4ee-140">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b4ee-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b4ee-141">-WhatIf</span></span>
<span data-ttu-id="1b4ee-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b4ee-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b4ee-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b4ee-144">CommonParameters</span></span>
<span data-ttu-id="1b4ee-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b4ee-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b4ee-146">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b4ee-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b4ee-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b4ee-147">INPUTS</span></span>

### <span data-ttu-id="1b4ee-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="1b4ee-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="1b4ee-149">System.String</span><span class="sxs-lookup"><span data-stu-id="1b4ee-149">System.String</span></span>

## <span data-ttu-id="1b4ee-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b4ee-150">OUTPUTS</span></span>

### <span data-ttu-id="1b4ee-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1b4ee-151">System.Boolean</span></span>

## <span data-ttu-id="1b4ee-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b4ee-152">NOTES</span></span>

## <span data-ttu-id="1b4ee-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b4ee-153">RELATED LINKS</span></span>

[<span data-ttu-id="1b4ee-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b4ee-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="1b4ee-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="1b4ee-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
