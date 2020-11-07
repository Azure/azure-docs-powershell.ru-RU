---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDelegation.md
ms.openlocfilehash: 1daa68e021646d91a2ab1b45382b137771411325
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734338"
---
# <span data-ttu-id="3e249-101">Remove-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="3e249-101">Remove-AzureRmDelegation</span></span>

## <span data-ttu-id="3e249-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e249-102">SYNOPSIS</span></span>
<span data-ttu-id="3e249-103">Удаление делегирования служб из предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="3e249-103">Removes a service delegation from the provided subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e249-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e249-104">SYNTAX</span></span>

```
Remove-AzureRmDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e249-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e249-105">DESCRIPTION</span></span>
<span data-ttu-id="3e249-106">Командлет **Remove-AzureRmDelegation** берет на себя подсеть с делегированием и удаляет именованное делегирование из этой подсети.</span><span class="sxs-lookup"><span data-stu-id="3e249-106">The **Remove-AzureRmDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="3e249-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e249-107">EXAMPLES</span></span>

### <span data-ttu-id="3e249-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3e249-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzureRmDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="3e249-109">В этом примере первая половина (найденная в разделе _"Добавление делегирования в существующую подсеть"_ ) идентична [надстройке Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span><span class="sxs-lookup"><span data-stu-id="3e249-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_ ) is identical to [Add-AzureRmDelegation](./Add-AzureRmDelegation.md).</span></span> <span data-ttu-id="3e249-110">Во второй половине первый из двух командлетов извлекает требуемую подсеть и обновляет локальную копию с учетом того, что находится на сервере.</span><span class="sxs-lookup"><span data-stu-id="3e249-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="3e249-111">Третий командлет удаляет делегирование, созданное в первой половине от _mySubnet_ , и сохраняет обновленную подсеть в _$Subnet_.</span><span class="sxs-lookup"><span data-stu-id="3e249-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="3e249-112">Последний командлет обновляет сервер с удаленным делегированием.</span><span class="sxs-lookup"><span data-stu-id="3e249-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="3e249-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e249-113">PARAMETERS</span></span>

### <span data-ttu-id="3e249-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e249-114">-DefaultProfile</span></span>
<span data-ttu-id="3e249-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e249-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e249-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e249-116">-Name</span></span>
<span data-ttu-id="3e249-117">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="3e249-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e249-118">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3e249-118">-ServiceName</span></span>
<span data-ttu-id="3e249-119">Имя службы, которой подсеть нужно делегировать.</span><span class="sxs-lookup"><span data-stu-id="3e249-119">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="3e249-120">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="3e249-120">-Subnet</span></span>
<span data-ttu-id="3e249-121">Подсеть, из которой нужно удалить делегирование.</span><span class="sxs-lookup"><span data-stu-id="3e249-121">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="3e249-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e249-122">CommonParameters</span></span>
<span data-ttu-id="3e249-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e249-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e249-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e249-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e249-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e249-125">INPUTS</span></span>

### <span data-ttu-id="3e249-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3e249-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
### <span data-ttu-id="3e249-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3e249-127">System.String</span></span>
## <span data-ttu-id="3e249-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e249-128">OUTPUTS</span></span>

### <span data-ttu-id="3e249-129">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="3e249-129">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>
## <span data-ttu-id="3e249-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e249-130">NOTES</span></span>

## <span data-ttu-id="3e249-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e249-131">RELATED LINKS</span></span>

<span data-ttu-id="3e249-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="3e249-132">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
