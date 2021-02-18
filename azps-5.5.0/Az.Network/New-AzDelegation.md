---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240840"
---
# <span data-ttu-id="659aa-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="659aa-101">New-AzDelegation</span></span>

## <span data-ttu-id="659aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="659aa-102">SYNOPSIS</span></span>
<span data-ttu-id="659aa-103">Создает делегирования службы.</span><span class="sxs-lookup"><span data-stu-id="659aa-103">Creates a service delegation.</span></span>

## <span data-ttu-id="659aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="659aa-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="659aa-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="659aa-105">DESCRIPTION</span></span>
<span data-ttu-id="659aa-106">Для **этого создается делегирование** службы, которое можно добавить в подсеть.</span><span class="sxs-lookup"><span data-stu-id="659aa-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="659aa-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="659aa-107">EXAMPLES</span></span>

### <span data-ttu-id="659aa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="659aa-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="659aa-109">Первый cmdlet создает делегирования, которое можно добавить в подсеть, и сохраняет его в переменной $delegation.</span><span class="sxs-lookup"><span data-stu-id="659aa-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="659aa-110">Второй и третий cmdlets извлекает подсеть для делегирования.</span><span class="sxs-lookup"><span data-stu-id="659aa-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="659aa-111">Четвертый cmdlet добавляет созданное делегирования в подсеть интересов, а последний из них отправляет обновленную конфигурацию на сервер.</span><span class="sxs-lookup"><span data-stu-id="659aa-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="659aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="659aa-112">PARAMETERS</span></span>

### <span data-ttu-id="659aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="659aa-113">-DefaultProfile</span></span>
<span data-ttu-id="659aa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="659aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="659aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="659aa-115">-Name</span></span>
<span data-ttu-id="659aa-116">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="659aa-116">The name of the delegation</span></span>

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

### <span data-ttu-id="659aa-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="659aa-117">-ServiceName</span></span>
<span data-ttu-id="659aa-118">Имя службы, которой должна быть делегирована подсеть.</span><span class="sxs-lookup"><span data-stu-id="659aa-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="659aa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="659aa-119">CommonParameters</span></span>
<span data-ttu-id="659aa-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="659aa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="659aa-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="659aa-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="659aa-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="659aa-122">INPUTS</span></span>

### <span data-ttu-id="659aa-123">System.String</span><span class="sxs-lookup"><span data-stu-id="659aa-123">System.String</span></span>

## <span data-ttu-id="659aa-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="659aa-124">OUTPUTS</span></span>

### <span data-ttu-id="659aa-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="659aa-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="659aa-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="659aa-126">NOTES</span></span>

## <span data-ttu-id="659aa-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="659aa-127">RELATED LINKS</span></span>

<span data-ttu-id="659aa-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="659aa-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>