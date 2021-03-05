---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 65149a0a52bc1bbb696b78033ec38670db97da48
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993796"
---
# <span data-ttu-id="25bb2-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="25bb2-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="25bb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25bb2-102">SYNOPSIS</span></span>
<span data-ttu-id="25bb2-103">Удаляет делегирования службы из предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="25bb2-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="25bb2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25bb2-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="25bb2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25bb2-105">DESCRIPTION</span></span>
<span data-ttu-id="25bb2-106">Для **этого с помощью cmdlet Remove-AzDelegation** передается в подсеть с делегированием.</span><span class="sxs-lookup"><span data-stu-id="25bb2-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="25bb2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25bb2-107">EXAMPLES</span></span>

### <span data-ttu-id="25bb2-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25bb2-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="25bb2-109">В этом примере первая часть (в области _"Добавление_ делегирования в существующую подсеть") идентична надстройке [Add-AzDelegation.](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="25bb2-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="25bb2-110">Во второй половине первые два cmdlets извлекает подсеть, подсеть, обновив локализованную копию с данными на сервере.</span><span class="sxs-lookup"><span data-stu-id="25bb2-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="25bb2-111">Третий cmdlet удаляет делегирования, созданное в первой половине, из _mySubnet_ и сохраняет обновленную подсеть в _$subnet._</span><span class="sxs-lookup"><span data-stu-id="25bb2-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="25bb2-112">Последний cmdlet обновляет сервер с помощью удаленного делегирования.</span><span class="sxs-lookup"><span data-stu-id="25bb2-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="25bb2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25bb2-113">PARAMETERS</span></span>

### <span data-ttu-id="25bb2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25bb2-114">-DefaultProfile</span></span>
<span data-ttu-id="25bb2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25bb2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25bb2-116">-Name</span><span class="sxs-lookup"><span data-stu-id="25bb2-116">-Name</span></span>
<span data-ttu-id="25bb2-117">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="25bb2-117">The name of the delegation</span></span>

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

### <span data-ttu-id="25bb2-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="25bb2-118">-Subnet</span></span>
<span data-ttu-id="25bb2-119">Подсеть, из которой нужно удалить делегирования</span><span class="sxs-lookup"><span data-stu-id="25bb2-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="25bb2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25bb2-120">CommonParameters</span></span>
<span data-ttu-id="25bb2-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25bb2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25bb2-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25bb2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25bb2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25bb2-123">INPUTS</span></span>

### <span data-ttu-id="25bb2-124">System.String</span><span class="sxs-lookup"><span data-stu-id="25bb2-124">System.String</span></span>

### <span data-ttu-id="25bb2-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="25bb2-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="25bb2-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25bb2-126">OUTPUTS</span></span>

### <span data-ttu-id="25bb2-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="25bb2-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="25bb2-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25bb2-128">NOTES</span></span>

## <span data-ttu-id="25bb2-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25bb2-129">RELATED LINKS</span></span>

<span data-ttu-id="25bb2-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="25bb2-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>