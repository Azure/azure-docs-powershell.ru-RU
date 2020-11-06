---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmDelegation.md
ms.openlocfilehash: 0306d327bf7e93eedd040979912622b2dcbc09d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567722"
---
# <span data-ttu-id="e26a6-101">Add-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="e26a6-101">Add-AzureRmDelegation</span></span>

## <span data-ttu-id="e26a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e26a6-102">SYNOPSIS</span></span>
<span data-ttu-id="e26a6-103">Добавляет делегирование в подсеть.</span><span class="sxs-lookup"><span data-stu-id="e26a6-103">Adds a delegation to a subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e26a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e26a6-104">SYNTAX</span></span>

```
Add-AzureRmDelegation -Name <String> -ServiceName <String> -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e26a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e26a6-105">DESCRIPTION</span></span>
<span data-ttu-id="e26a6-106">Командлет **Add-AzureRmDelegation** добавляет делегирование служб в подсеть Azure.</span><span class="sxs-lookup"><span data-stu-id="e26a6-106">The **Add-AzureRmDelegation** cmdlet adds a service delegation to an Azure subnet.</span></span>

## <span data-ttu-id="e26a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e26a6-107">EXAMPLES</span></span>

### <span data-ttu-id="e26a6-108">1: Добавление делегирования</span><span class="sxs-lookup"><span data-stu-id="e26a6-108">1: Adding a delegation</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="e26a6-109">Первая команда извлекает виртуальную сеть, в которой находится подсеть.</span><span class="sxs-lookup"><span data-stu-id="e26a6-109">The first command retrieves the virtual network on which the subnet lies.</span></span> <span data-ttu-id="e26a6-110">Вторая команда изолирует подсеть, которой вы хотите делегировать.</span><span class="sxs-lookup"><span data-stu-id="e26a6-110">The second command isolates out the subnet of interest - the one which you want to delegate.</span></span> <span data-ttu-id="e26a6-111">Третья команда добавляет делегирование в подсеть.</span><span class="sxs-lookup"><span data-stu-id="e26a6-111">The third command adds a delegation to the subnet.</span></span> <span data-ttu-id="e26a6-112">Этот конкретный пример полезен, если вы хотите включить SQL для создания конечных точек интерфейса в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="e26a6-112">This particular example would be useful when you want to enable SQL to create interface endpoints in this subnet.</span></span> <span data-ttu-id="e26a6-113">Последняя команда отправляет обновленную подсеть на сервер для фактического обновления вашей подсети.</span><span class="sxs-lookup"><span data-stu-id="e26a6-113">The final command sends the updated subnet to the server to actually update your subnet.</span></span>

## <span data-ttu-id="e26a6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e26a6-114">PARAMETERS</span></span>

### <span data-ttu-id="e26a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e26a6-115">-DefaultProfile</span></span>
<span data-ttu-id="e26a6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e26a6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e26a6-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e26a6-117">-Name</span></span>
<span data-ttu-id="e26a6-118">Имя делегирования</span><span class="sxs-lookup"><span data-stu-id="e26a6-118">The name of the delegation</span></span>

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

### <span data-ttu-id="e26a6-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e26a6-119">-ServiceName</span></span>
<span data-ttu-id="e26a6-120">Имя службы, которой подсеть нужно делегировать.</span><span class="sxs-lookup"><span data-stu-id="e26a6-120">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="e26a6-121">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="e26a6-121">-Subnet</span></span>
<span data-ttu-id="e26a6-122">Подсеть</span><span class="sxs-lookup"><span data-stu-id="e26a6-122">The subnet</span></span>

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

### <span data-ttu-id="e26a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e26a6-123">CommonParameters</span></span>
<span data-ttu-id="e26a6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e26a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e26a6-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e26a6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e26a6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e26a6-126">INPUTS</span></span>

### <span data-ttu-id="e26a6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="e26a6-127">System.String</span></span>

### <span data-ttu-id="e26a6-128">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e26a6-128">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e26a6-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e26a6-129">OUTPUTS</span></span>

### <span data-ttu-id="e26a6-130">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="e26a6-130">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="e26a6-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e26a6-131">NOTES</span></span>

## <span data-ttu-id="e26a6-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e26a6-132">RELATED LINKS</span></span>
<span data-ttu-id="e26a6-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="e26a6-133">[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
