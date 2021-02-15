---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: f32b06e9b162a4d142d6d6fff9b7cdca34e0b30b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223860"
---
# <span data-ttu-id="a703e-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="a703e-101">Get-AzDelegation</span></span>

## <span data-ttu-id="a703e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a703e-102">SYNOPSIS</span></span>
<span data-ttu-id="a703e-103">Получите делегирования (или все делегирования) в данной подсети.</span><span class="sxs-lookup"><span data-stu-id="a703e-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="a703e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a703e-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a703e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a703e-105">DESCRIPTION</span></span>
<span data-ttu-id="a703e-106">Для **именоваемого делегирования** из подсети возвращается имя делегирования.</span><span class="sxs-lookup"><span data-stu-id="a703e-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="a703e-107">Если делегирования не назначено, возвращаются все делегирования в предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="a703e-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="a703e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a703e-108">EXAMPLES</span></span>

### <span data-ttu-id="a703e-109">1. Просмотр определенного делегирования</span><span class="sxs-lookup"><span data-stu-id="a703e-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="a703e-110">Первая строка извлекает подсеть интересов.</span><span class="sxs-lookup"><span data-stu-id="a703e-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a703e-111">Во второй строке показаны сведения о делегирования для делегирования под названием "myDelegation".</span><span class="sxs-lookup"><span data-stu-id="a703e-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="a703e-112">2. Просмотр всех делегирования подсети</span><span class="sxs-lookup"><span data-stu-id="a703e-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="a703e-113">Первая строка извлекает подсеть интересов.</span><span class="sxs-lookup"><span data-stu-id="a703e-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a703e-114">Во второй строке список всех делегирования в _mySubnet_ хранится в переменной $delegations.</span><span class="sxs-lookup"><span data-stu-id="a703e-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="a703e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a703e-115">PARAMETERS</span></span>

### <span data-ttu-id="a703e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a703e-116">-DefaultProfile</span></span>
<span data-ttu-id="a703e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a703e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a703e-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a703e-118">-Name</span></span>
<span data-ttu-id="a703e-119">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="a703e-119">The name of the delegation</span></span>

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

### <span data-ttu-id="a703e-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="a703e-120">-Subnet</span></span>
<span data-ttu-id="a703e-121">Подсеть</span><span class="sxs-lookup"><span data-stu-id="a703e-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a703e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a703e-122">CommonParameters</span></span>
<span data-ttu-id="a703e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a703e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a703e-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a703e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a703e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a703e-125">INPUTS</span></span>

### <span data-ttu-id="a703e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="a703e-126">System.String</span></span>

### <span data-ttu-id="a703e-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a703e-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a703e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a703e-128">OUTPUTS</span></span>

### <span data-ttu-id="a703e-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a703e-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a703e-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a703e-130">NOTES</span></span>

## <span data-ttu-id="a703e-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a703e-131">RELATED LINKS</span></span>

<span data-ttu-id="a703e-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a703e-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
