---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567266"
---
# <span data-ttu-id="07e2b-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="07e2b-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="07e2b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07e2b-102">SYNOPSIS</span></span>
<span data-ttu-id="07e2b-103">Получение делегирования (или всех делегирований) в данной подсети.</span><span class="sxs-lookup"><span data-stu-id="07e2b-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e2b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07e2b-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07e2b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e2b-105">DESCRIPTION</span></span>
<span data-ttu-id="07e2b-106">Командлет **Get-AzureRmDelegation** получает именованное делегирование из подсети.</span><span class="sxs-lookup"><span data-stu-id="07e2b-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="07e2b-107">Если не указано имя для делегирования, оно возвращает все делегирования для указанной подсети.</span><span class="sxs-lookup"><span data-stu-id="07e2b-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="07e2b-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07e2b-108">EXAMPLES</span></span>

### <span data-ttu-id="07e2b-109">1: получение определенного делегирования</span><span class="sxs-lookup"><span data-stu-id="07e2b-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="07e2b-110">Первая строка — получение нужной подсети.</span><span class="sxs-lookup"><span data-stu-id="07e2b-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="07e2b-111">Вторая строка показывает сведения о делегировании для делегирования под названием "myDelegation".</span><span class="sxs-lookup"><span data-stu-id="07e2b-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="07e2b-112">2. получение делегирования подсети</span><span class="sxs-lookup"><span data-stu-id="07e2b-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="07e2b-113">Первая строка — получение нужной подсети.</span><span class="sxs-lookup"><span data-stu-id="07e2b-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="07e2b-114">Вторая строка содержит список всех делегирований для _mySubnet_ в переменной $Delegations.</span><span class="sxs-lookup"><span data-stu-id="07e2b-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="07e2b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07e2b-115">PARAMETERS</span></span>

### <span data-ttu-id="07e2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e2b-116">-DefaultProfile</span></span>
<span data-ttu-id="07e2b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07e2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e2b-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07e2b-118">-Name</span></span>
<span data-ttu-id="07e2b-119">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="07e2b-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e2b-120">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="07e2b-120">-Subnet</span></span>
<span data-ttu-id="07e2b-121">Подсеть</span><span class="sxs-lookup"><span data-stu-id="07e2b-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e2b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e2b-122">CommonParameters</span></span>
<span data-ttu-id="07e2b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07e2b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="07e2b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e2b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e2b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07e2b-125">INPUTS</span></span>

### <span data-ttu-id="07e2b-126">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="07e2b-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="07e2b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07e2b-127">OUTPUTS</span></span>

### <span data-ttu-id="07e2b-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="07e2b-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="07e2b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="07e2b-129">NOTES</span></span>

## <span data-ttu-id="07e2b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07e2b-130">RELATED LINKS</span></span>
<span data-ttu-id="07e2b-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [New-AzureRmDelegation](./New-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="07e2b-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
