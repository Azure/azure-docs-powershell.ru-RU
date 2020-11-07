---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: de345650553771078c03d728551b4713b5696fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730185"
---
# <span data-ttu-id="5d8b6-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="5d8b6-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="5d8b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d8b6-102">SYNOPSIS</span></span>
<span data-ttu-id="5d8b6-103">Удаление делегирования служб из предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="5d8b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d8b6-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d8b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8b6-105">DESCRIPTION</span></span>
<span data-ttu-id="5d8b6-106">Командлет **Remove-AzDelegation** берет на себя подсеть с делегированием и удаляет именованное делегирование из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="5d8b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d8b6-107">EXAMPLES</span></span>

### <span data-ttu-id="5d8b6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d8b6-108">Example 1</span></span>
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

<span data-ttu-id="5d8b6-109">В этом примере первая половина (найденная в разделе _"Добавление делегирования в существующую подсеть"_ ) идентична [надстройке Add-AzDelegation](./Add-AzDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="5d8b6-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="5d8b6-110">Во второй половине первый из двух командлетов извлекает требуемую подсеть и обновляет локальную копию с учетом того, что находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="5d8b6-111">Третий командлет удаляет делегирование, созданное в первой половине от _mySubnet_ , и сохраняет обновленную подсеть в _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="5d8b6-112">Последний командлет обновляет сервер с удаленным делегированием.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="5d8b6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d8b6-113">PARAMETERS</span></span>

### <span data-ttu-id="5d8b6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d8b6-114">-DefaultProfile</span></span>
<span data-ttu-id="5d8b6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d8b6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d8b6-116">-Name</span></span>
<span data-ttu-id="5d8b6-117">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="5d8b6-117">The name of the delegation</span></span>

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

### <span data-ttu-id="5d8b6-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="5d8b6-118">-Subnet</span></span>
<span data-ttu-id="5d8b6-119">Подсеть, из которой нужно удалить делегирование.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="5d8b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d8b6-120">CommonParameters</span></span>
<span data-ttu-id="5d8b6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d8b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d8b6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d8b6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d8b6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d8b6-123">INPUTS</span></span>

### <span data-ttu-id="5d8b6-124">System. String</span><span class="sxs-lookup"><span data-stu-id="5d8b6-124">System.String</span></span>

### <span data-ttu-id="5d8b6-125">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5d8b6-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5d8b6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d8b6-126">OUTPUTS</span></span>

### <span data-ttu-id="5d8b6-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="5d8b6-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="5d8b6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d8b6-128">NOTES</span></span>

## <span data-ttu-id="5d8b6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d8b6-129">RELATED LINKS</span></span>

<span data-ttu-id="5d8b6-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5d8b6-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>