---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566800"
---
# <span data-ttu-id="ae6f9-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="ae6f9-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="ae6f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae6f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6f9-103">Создание делегирования служб.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae6f9-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ae6f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae6f9-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6f9-106">Командлет **New-AzureRmDelegation** создает делегирование служб, которое можно добавить в подсеть.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="ae6f9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae6f9-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6f9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ae6f9-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="ae6f9-109">Первый командлет создает делегирование, которое можно добавить в подсеть, и сохраняет его в переменной $delegation.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="ae6f9-110">Вторая и третья командлеты извлекают подсеть для делегирования.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="ae6f9-111">Четвертый командлет добавляет созданное делегирование к нужной подсети, а последний командлет отправляет обновленную конфигурацию на сервер.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="ae6f9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae6f9-112">PARAMETERS</span></span>

### <span data-ttu-id="ae6f9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6f9-113">-DefaultProfile</span></span>
<span data-ttu-id="ae6f9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6f9-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae6f9-115">-Name</span></span>
<span data-ttu-id="ae6f9-116">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="ae6f9-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae6f9-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae6f9-117">-ServiceName</span></span>
<span data-ttu-id="ae6f9-118">Имя службы, которой подсеть нужно делегировать.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6f9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6f9-119">CommonParameters</span></span>
<span data-ttu-id="ae6f9-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae6f9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae6f9-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6f9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6f9-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae6f9-122">INPUTS</span></span>

### <span data-ttu-id="ae6f9-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6f9-123">System.String</span></span>

## <span data-ttu-id="ae6f9-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae6f9-124">OUTPUTS</span></span>

### <span data-ttu-id="ae6f9-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="ae6f9-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="ae6f9-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae6f9-126">NOTES</span></span>

## <span data-ttu-id="ae6f9-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae6f9-127">RELATED LINKS</span></span>
<span data-ttu-id="ae6f9-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="ae6f9-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
