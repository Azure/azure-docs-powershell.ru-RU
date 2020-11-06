---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 47FE9EF4-6000-4096-8F04-26A0C6661FDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualnetworksubnetconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualNetworkSubnetConfig.md
ms.openlocfilehash: 42765b56f0376466acb51e04d8ab6ce4a2eee1bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564735"
---
# <span data-ttu-id="a686e-101">Remove-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a686e-101">Remove-AzureRmVirtualNetworkSubnetConfig</span></span>

## <span data-ttu-id="a686e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a686e-102">SYNOPSIS</span></span>
<span data-ttu-id="a686e-103">Удаление конфигурации подсети из виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="a686e-103">Removes a subnet configuration from a virtual network.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a686e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a686e-104">SYNTAX</span></span>

```
Remove-AzureRmVirtualNetworkSubnetConfig [-Name <String>] -VirtualNetwork <PSVirtualNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a686e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a686e-105">DESCRIPTION</span></span>
<span data-ttu-id="a686e-106">Командлет **Remove-AzureRmVirtualNetworkSubnetConfig** удаляет подсеть из виртуальной сети Azure.</span><span class="sxs-lookup"><span data-stu-id="a686e-106">The **Remove-AzureRmVirtualNetworkSubnetConfig** cmdlet removes a subnet from an Azure virtual network.</span></span>

## <span data-ttu-id="a686e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a686e-107">EXAMPLES</span></span>

### <span data-ttu-id="a686e-108">1: удалите подсеть из виртуальной сети и обновите виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a686e-108">1: Remove a subnet from a virtual network and update the virtual network</span></span>
```
New-AzureRmResourceGroup -Name TestResourceGroup -Location centralus
    $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet 
    -AddressPrefix "10.0.1.0/24"

$backendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -AddressPrefix 
    "10.0.2.0/24"

$virtualNetwork = New-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName 
    TestResourceGroup -Location centralus -AddressPrefix "10.0.0.0/16" -Subnet 
    $frontendSubnet,$backendSubnet

Remove-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet -VirtualNetwork 
    $virtualNetwork
    $virtualNetwork | Set-AzureRmVirtualNetwork
```

<span data-ttu-id="a686e-109">В этом примере создается группа ресурсов и виртуальная сеть с двумя подсетями.</span><span class="sxs-lookup"><span data-stu-id="a686e-109">This example creates a resource group and a virtual network with two subnets.</span></span> <span data-ttu-id="a686e-110">Затем она использует команду Remove-AzureRmVirtualNetworkSubnetConfig для удаления подсети сервера из представления виртуальной сети в памяти.</span><span class="sxs-lookup"><span data-stu-id="a686e-110">It then uses the Remove-AzureRmVirtualNetworkSubnetConfig command to remove the backend subnet from the in-memory representation of the virtual network.</span></span> <span data-ttu-id="a686e-111">Set-AzureRmVirtualNetwork вызывается, чтобы изменить виртуальную сеть на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="a686e-111">Set-AzureRmVirtualNetwork is then called to modify the virtual network on the server side.</span></span>

## <span data-ttu-id="a686e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a686e-112">PARAMETERS</span></span>

### <span data-ttu-id="a686e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a686e-113">-DefaultProfile</span></span>
<span data-ttu-id="a686e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a686e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a686e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a686e-115">-Name</span></span>
<span data-ttu-id="a686e-116">Указывает имя конфигурации подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a686e-116">Specifies the name of the subnet configuration to remove.</span></span>

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

### <span data-ttu-id="a686e-117">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a686e-117">-VirtualNetwork</span></span>
<span data-ttu-id="a686e-118">Указывает объект **VirtualNetwork** , содержащий конфигурацию подсети, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a686e-118">Specifies the **VirtualNetwork** object that contains the subnet configuration to remove.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a686e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a686e-119">CommonParameters</span></span>
<span data-ttu-id="a686e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a686e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a686e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a686e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a686e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a686e-122">INPUTS</span></span>

### <span data-ttu-id="a686e-123">PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a686e-123">PSVirtualNetwork</span></span>
<span data-ttu-id="a686e-124">Параметр "VirtualNetwork" принимает значение типа "PSVirtualNetwork" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a686e-124">Parameter 'VirtualNetwork' accepts value of type 'PSVirtualNetwork' from the pipeline</span></span>

## <span data-ttu-id="a686e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a686e-125">OUTPUTS</span></span>

### <span data-ttu-id="a686e-126">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a686e-126">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="a686e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a686e-127">NOTES</span></span>

## <span data-ttu-id="a686e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a686e-128">RELATED LINKS</span></span>

[<span data-ttu-id="a686e-129">Add-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a686e-129">Add-AzureRmVirtualNetworkSubnetConfig</span></span>](./Add-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a686e-130">Get-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a686e-130">Get-AzureRmVirtualNetworkSubnetConfig</span></span>](./Get-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a686e-131">New-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a686e-131">New-AzureRmVirtualNetworkSubnetConfig</span></span>](./New-AzureRmVirtualNetworkSubnetConfig.md)

[<span data-ttu-id="a686e-132">Set-AzureRmVirtualNetworkSubnetConfig</span><span class="sxs-lookup"><span data-stu-id="a686e-132">Set-AzureRmVirtualNetworkSubnetConfig</span></span>](./Set-AzureRmVirtualNetworkSubnetConfig.md)


