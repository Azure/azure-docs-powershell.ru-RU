---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: d383ddc5c7e0cf1b4ddb618fa11089883049d327
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958563"
---
# <span data-ttu-id="9721a-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="9721a-101">New-AzDelegation</span></span>

## <span data-ttu-id="9721a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9721a-102">SYNOPSIS</span></span>
<span data-ttu-id="9721a-103">Создается делегирования службы.</span><span class="sxs-lookup"><span data-stu-id="9721a-103">Creates a service delegation.</span></span>

## <span data-ttu-id="9721a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9721a-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9721a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9721a-105">DESCRIPTION</span></span>
<span data-ttu-id="9721a-106">Для **этого создается делегирование** службы, которое можно добавить в подсеть.</span><span class="sxs-lookup"><span data-stu-id="9721a-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="9721a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9721a-107">EXAMPLES</span></span>

### <span data-ttu-id="9721a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9721a-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="9721a-109">Первый cmdlet создает делегирования, которое можно добавить в подсеть, и сохраняет его в переменной $delegation.</span><span class="sxs-lookup"><span data-stu-id="9721a-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="9721a-110">Второй и третий cmdlets извлекает подсеть для делегирования.</span><span class="sxs-lookup"><span data-stu-id="9721a-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="9721a-111">Четвертый cmdlet добавляет созданное делегирования в подсеть интересов, а последний из них отправляет обновленную конфигурацию на сервер.</span><span class="sxs-lookup"><span data-stu-id="9721a-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="9721a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9721a-112">PARAMETERS</span></span>

### <span data-ttu-id="9721a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9721a-113">-DefaultProfile</span></span>
<span data-ttu-id="9721a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9721a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9721a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="9721a-115">-Name</span></span>
<span data-ttu-id="9721a-116">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="9721a-116">The name of the delegation</span></span>

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

### <span data-ttu-id="9721a-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9721a-117">-ServiceName</span></span>
<span data-ttu-id="9721a-118">Имя службы, которой должна быть делегирована подсеть.</span><span class="sxs-lookup"><span data-stu-id="9721a-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="9721a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9721a-119">CommonParameters</span></span>
<span data-ttu-id="9721a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9721a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9721a-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9721a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9721a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9721a-122">INPUTS</span></span>

### <span data-ttu-id="9721a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9721a-123">System.String</span></span>

## <span data-ttu-id="9721a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9721a-124">OUTPUTS</span></span>

### <span data-ttu-id="9721a-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="9721a-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="9721a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9721a-126">NOTES</span></span>

## <span data-ttu-id="9721a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9721a-127">RELATED LINKS</span></span>

<span data-ttu-id="9721a-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="9721a-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>