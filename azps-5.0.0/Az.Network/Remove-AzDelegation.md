---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249646"
---
# <span data-ttu-id="aa306-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="aa306-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="aa306-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa306-102">SYNOPSIS</span></span>
<span data-ttu-id="aa306-103">Удаление делегирования служб из предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="aa306-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="aa306-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa306-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="aa306-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa306-105">DESCRIPTION</span></span>
<span data-ttu-id="aa306-106">Командлет **Remove-AzDelegation** берет на себя подсеть с делегированием и удаляет именованное делегирование из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="aa306-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="aa306-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa306-107">EXAMPLES</span></span>

### <span data-ttu-id="aa306-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aa306-108">Example 1</span></span>
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

<span data-ttu-id="aa306-109">В этом примере первая половина (найденная в разделе _"Добавление делегирования в существующую подсеть"_ ) идентична [надстройке Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="aa306-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="aa306-110">Во второй половине первый из двух командлетов извлекает требуемую подсеть и обновляет локальную копию с учетом того, что находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="aa306-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="aa306-111">Третий командлет удаляет делегирование, созданное в первой половине от _mySubnet_ , и сохраняет обновленную подсеть в _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="aa306-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="aa306-112">Последний командлет обновляет сервер с удаленным делегированием.</span><span class="sxs-lookup"><span data-stu-id="aa306-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="aa306-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa306-113">PARAMETERS</span></span>

### <span data-ttu-id="aa306-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa306-114">-DefaultProfile</span></span>
<span data-ttu-id="aa306-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa306-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa306-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aa306-116">-Name</span></span>
<span data-ttu-id="aa306-117">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="aa306-117">The name of the delegation</span></span>

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

### <span data-ttu-id="aa306-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="aa306-118">-Subnet</span></span>
<span data-ttu-id="aa306-119">Подсеть, из которой нужно удалить делегирование.</span><span class="sxs-lookup"><span data-stu-id="aa306-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="aa306-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa306-120">CommonParameters</span></span>
<span data-ttu-id="aa306-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa306-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa306-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa306-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa306-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa306-123">INPUTS</span></span>

### <span data-ttu-id="aa306-124">System. String</span><span class="sxs-lookup"><span data-stu-id="aa306-124">System.String</span></span>

### <span data-ttu-id="aa306-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="aa306-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="aa306-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa306-126">OUTPUTS</span></span>

### <span data-ttu-id="aa306-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="aa306-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="aa306-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa306-128">NOTES</span></span>

## <span data-ttu-id="aa306-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa306-129">RELATED LINKS</span></span>

<span data-ttu-id="aa306-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="aa306-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>