---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249679"
---
# <span data-ttu-id="c24a1-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c24a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c24a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c24a1-103">Создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="c24a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c24a1-104">SYNTAX</span></span>

### <span data-ttu-id="c24a1-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="c24a1-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c24a1-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="c24a1-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c24a1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c24a1-107">DESCRIPTION</span></span>
<span data-ttu-id="c24a1-108">Командлет **New-AzApplicationGatewayIPConfiguration** создает IP-конфигурацию для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="c24a1-109">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="c24a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c24a1-110">EXAMPLES</span></span>

### <span data-ttu-id="c24a1-111">Пример 1: создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="c24a1-112">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="c24a1-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="c24a1-113">Вторая команда возвращает конфигурацию подсети для подсети, к которой принадлежит виртуальная сеть в предыдущей команде, и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c24a1-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="c24a1-114">Третья команда создает IP-конфигурацию с помощью $Subnet.</span><span class="sxs-lookup"><span data-stu-id="c24a1-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="c24a1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c24a1-115">PARAMETERS</span></span>

### <span data-ttu-id="c24a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c24a1-116">-DefaultProfile</span></span>
<span data-ttu-id="c24a1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c24a1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c24a1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c24a1-118">-Name</span></span>
<span data-ttu-id="c24a1-119">Указывает имя создаваемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c24a1-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="c24a1-120">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="c24a1-120">-Subnet</span></span>
<span data-ttu-id="c24a1-121">Указывает объект подсети.</span><span class="sxs-lookup"><span data-stu-id="c24a1-121">Specifies the subnet object.</span></span>
<span data-ttu-id="c24a1-122">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-122">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24a1-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="c24a1-123">-SubnetId</span></span>
<span data-ttu-id="c24a1-124">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="c24a1-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="c24a1-125">Это подсеть, в которой будет развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="c24a1-125">This is the subnet in which the application gateway would be deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c24a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c24a1-126">CommonParameters</span></span>
<span data-ttu-id="c24a1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c24a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c24a1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c24a1-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c24a1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c24a1-129">INPUTS</span></span>

### <span data-ttu-id="c24a1-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="c24a1-130">None</span></span>

## <span data-ttu-id="c24a1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c24a1-131">OUTPUTS</span></span>

### <span data-ttu-id="c24a1-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="c24a1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="c24a1-133">NOTES</span></span>

## <span data-ttu-id="c24a1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c24a1-134">RELATED LINKS</span></span>

[<span data-ttu-id="c24a1-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c24a1-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c24a1-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="c24a1-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c24a1-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


