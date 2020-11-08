---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 213c6616a143f7be64454f6538fac5d5c89afd54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074868"
---
# <span data-ttu-id="8a561-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="8a561-101">Get-AzDelegation</span></span>

## <span data-ttu-id="8a561-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a561-102">SYNOPSIS</span></span>
<span data-ttu-id="8a561-103">Получение делегирования (или всех делегирований) в данной подсети.</span><span class="sxs-lookup"><span data-stu-id="8a561-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="8a561-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a561-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a561-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a561-105">DESCRIPTION</span></span>
<span data-ttu-id="8a561-106">Командлет **Get-AzDelegation** получает именованное делегирование из подсети.</span><span class="sxs-lookup"><span data-stu-id="8a561-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="8a561-107">Если не указано имя для делегирования, оно возвращает все делегирования для указанной подсети.</span><span class="sxs-lookup"><span data-stu-id="8a561-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="8a561-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a561-108">EXAMPLES</span></span>

### <span data-ttu-id="8a561-109">1: получение определенного делегирования</span><span class="sxs-lookup"><span data-stu-id="8a561-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="8a561-110">Первая строка — получение нужной подсети.</span><span class="sxs-lookup"><span data-stu-id="8a561-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="8a561-111">Вторая строка показывает сведения о делегировании для делегирования под названием "myDelegation".</span><span class="sxs-lookup"><span data-stu-id="8a561-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="8a561-112">2. получение делегирования подсети</span><span class="sxs-lookup"><span data-stu-id="8a561-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="8a561-113">Первая строка — получение нужной подсети.</span><span class="sxs-lookup"><span data-stu-id="8a561-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="8a561-114">Вторая строка содержит список всех делегирований для _mySubnet_ в переменной $Delegations.</span><span class="sxs-lookup"><span data-stu-id="8a561-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="8a561-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a561-115">PARAMETERS</span></span>

### <span data-ttu-id="8a561-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a561-116">-DefaultProfile</span></span>
<span data-ttu-id="8a561-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a561-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a561-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a561-118">-Name</span></span>
<span data-ttu-id="8a561-119">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="8a561-119">The name of the delegation</span></span>

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

### <span data-ttu-id="8a561-120">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="8a561-120">-Subnet</span></span>
<span data-ttu-id="8a561-121">Подсеть</span><span class="sxs-lookup"><span data-stu-id="8a561-121">The subnet</span></span>

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

### <span data-ttu-id="8a561-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a561-122">CommonParameters</span></span>
<span data-ttu-id="8a561-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a561-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a561-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a561-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a561-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a561-125">INPUTS</span></span>

### <span data-ttu-id="8a561-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a561-126">System.String</span></span>

### <span data-ttu-id="8a561-127">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="8a561-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="8a561-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a561-128">OUTPUTS</span></span>

### <span data-ttu-id="8a561-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="8a561-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="8a561-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a561-130">NOTES</span></span>

## <span data-ttu-id="8a561-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a561-131">RELATED LINKS</span></span>

<span data-ttu-id="8a561-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="8a561-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>