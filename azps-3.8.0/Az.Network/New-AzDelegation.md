---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074755"
---
# <span data-ttu-id="9bad4-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="9bad4-101">New-AzDelegation</span></span>

## <span data-ttu-id="9bad4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9bad4-102">SYNOPSIS</span></span>
<span data-ttu-id="9bad4-103">Создание делегирования служб.</span><span class="sxs-lookup"><span data-stu-id="9bad4-103">Creates a service delegation.</span></span>

## <span data-ttu-id="9bad4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9bad4-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9bad4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bad4-105">DESCRIPTION</span></span>
<span data-ttu-id="9bad4-106">Командлет **New-AzDelegation** создает делегирование служб, которое можно добавить в подсеть.</span><span class="sxs-lookup"><span data-stu-id="9bad4-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="9bad4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9bad4-107">EXAMPLES</span></span>

### <span data-ttu-id="9bad4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9bad4-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="9bad4-109">Первый командлет создает делегирование, которое можно добавить в подсеть, и сохраняет его в переменной $delegation.</span><span class="sxs-lookup"><span data-stu-id="9bad4-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="9bad4-110">Вторая и третья командлеты извлекают подсеть для делегирования.</span><span class="sxs-lookup"><span data-stu-id="9bad4-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="9bad4-111">Четвертый командлет добавляет созданное делегирование к нужной подсети, а последний командлет отправляет обновленную конфигурацию на сервер.</span><span class="sxs-lookup"><span data-stu-id="9bad4-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="9bad4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9bad4-112">PARAMETERS</span></span>

### <span data-ttu-id="9bad4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bad4-113">-DefaultProfile</span></span>
<span data-ttu-id="9bad4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9bad4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bad4-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9bad4-115">-Name</span></span>
<span data-ttu-id="9bad4-116">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="9bad4-116">The name of the delegation</span></span>

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

### <span data-ttu-id="9bad4-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9bad4-117">-ServiceName</span></span>
<span data-ttu-id="9bad4-118">Имя службы, которой подсеть нужно делегировать.</span><span class="sxs-lookup"><span data-stu-id="9bad4-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="9bad4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bad4-119">CommonParameters</span></span>
<span data-ttu-id="9bad4-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9bad4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bad4-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bad4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bad4-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9bad4-122">INPUTS</span></span>

### <span data-ttu-id="9bad4-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9bad4-123">System.String</span></span>

## <span data-ttu-id="9bad4-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9bad4-124">OUTPUTS</span></span>

### <span data-ttu-id="9bad4-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="9bad4-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="9bad4-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9bad4-126">NOTES</span></span>

## <span data-ttu-id="9bad4-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9bad4-127">RELATED LINKS</span></span>

<span data-ttu-id="9bad4-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="9bad4-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>