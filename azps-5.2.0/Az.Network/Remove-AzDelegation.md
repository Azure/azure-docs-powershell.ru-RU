---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408908"
---
# <span data-ttu-id="b047c-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="b047c-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="b047c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b047c-102">SYNOPSIS</span></span>
<span data-ttu-id="b047c-103">Удаляет делегирования службы из предоставленной подсети.</span><span class="sxs-lookup"><span data-stu-id="b047c-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="b047c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b047c-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b047c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b047c-105">DESCRIPTION</span></span>
<span data-ttu-id="b047c-106">Для **этого с помощью cmdlet Remove-AzDelegation** передается в подсеть с делегированием.</span><span class="sxs-lookup"><span data-stu-id="b047c-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="b047c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b047c-107">EXAMPLES</span></span>

### <span data-ttu-id="b047c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b047c-108">Example 1</span></span>
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

<span data-ttu-id="b047c-109">В этом примере первая часть (в области _"Добавление_ делегирования в существующую подсеть") идентична надстройке [Add-AzDelegation.](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="b047c-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="b047c-110">Во второй половине первые два cmdlets извлекает подсеть, подсеть, обновив локализованную копию с данными на сервере.</span><span class="sxs-lookup"><span data-stu-id="b047c-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="b047c-111">Третий cmdlet удаляет делегирования, созданное в первой половине, из _mySubnet_ и сохраняет обновленную подсеть в _$subnet._</span><span class="sxs-lookup"><span data-stu-id="b047c-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="b047c-112">Последний cmdlet обновляет сервер с помощью удаленного делегирования.</span><span class="sxs-lookup"><span data-stu-id="b047c-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="b047c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b047c-113">PARAMETERS</span></span>

### <span data-ttu-id="b047c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b047c-114">-DefaultProfile</span></span>
<span data-ttu-id="b047c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b047c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b047c-116">-Name</span><span class="sxs-lookup"><span data-stu-id="b047c-116">-Name</span></span>
<span data-ttu-id="b047c-117">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="b047c-117">The name of the delegation</span></span>

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

### <span data-ttu-id="b047c-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="b047c-118">-Subnet</span></span>
<span data-ttu-id="b047c-119">Подсеть, из которой нужно удалить делегирования</span><span class="sxs-lookup"><span data-stu-id="b047c-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="b047c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b047c-120">CommonParameters</span></span>
<span data-ttu-id="b047c-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b047c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b047c-122">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b047c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b047c-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b047c-123">INPUTS</span></span>

### <span data-ttu-id="b047c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="b047c-124">System.String</span></span>

### <span data-ttu-id="b047c-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b047c-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b047c-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b047c-126">OUTPUTS</span></span>

### <span data-ttu-id="b047c-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b047c-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="b047c-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b047c-128">NOTES</span></span>

## <span data-ttu-id="b047c-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b047c-129">RELATED LINKS</span></span>

<span data-ttu-id="b047c-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="b047c-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>