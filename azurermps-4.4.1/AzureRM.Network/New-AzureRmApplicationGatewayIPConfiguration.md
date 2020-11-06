---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 076965d0f63a8c28742cf9853068b9e020403a66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568039"
---
# <span data-ttu-id="2b1ab-101">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-101">New-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2b1ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b1ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2b1ab-103">Создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-103">Creates an IP configuration for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b1ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b1ab-104">SYNTAX</span></span>

### <span data-ttu-id="2b1ab-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2b1ab-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2b1ab-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="2b1ab-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b1ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b1ab-107">DESCRIPTION</span></span>
<span data-ttu-id="2b1ab-108">Командлет **New-AzureRmApplicationGatewayIPConfiguration** создает IP-конфигурацию для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-108">The **New-AzureRmApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="2b1ab-109">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="2b1ab-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b1ab-110">EXAMPLES</span></span>

### <span data-ttu-id="2b1ab-111">Пример 1: создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzureRmvirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzureRmApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="2b1ab-112">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>

<span data-ttu-id="2b1ab-113">Вторая команда возвращает конфигурацию подсети для подсети, к которой принадлежит виртуальная сеть в предыдущей команде, и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>

<span data-ttu-id="2b1ab-114">Третья команда создает IP-конфигурацию с помощью $Subnet.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="2b1ab-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b1ab-115">PARAMETERS</span></span>

### <span data-ttu-id="2b1ab-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b1ab-116">-Name</span></span>
<span data-ttu-id="2b1ab-117">Указывает имя создаваемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-117">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="2b1ab-118">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="2b1ab-118">-Subnet</span></span>
<span data-ttu-id="2b1ab-119">Указывает объект подсети.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-119">Specifies the subnet object.</span></span>
<span data-ttu-id="2b1ab-120">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-120">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="2b1ab-121">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2b1ab-121">-SubnetId</span></span>
<span data-ttu-id="2b1ab-122">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-122">Specifies the subnet ID.</span></span>
<span data-ttu-id="2b1ab-123">Это подсеть, в которой будет развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-123">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="2b1ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b1ab-124">-DefaultProfile</span></span>
<span data-ttu-id="2b1ab-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b1ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b1ab-126">CommonParameters</span></span>
<span data-ttu-id="2b1ab-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b1ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b1ab-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b1ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b1ab-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b1ab-129">INPUTS</span></span>

### <span data-ttu-id="2b1ab-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2b1ab-130">System.String</span></span>

## <span data-ttu-id="2b1ab-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b1ab-131">OUTPUTS</span></span>

### <span data-ttu-id="2b1ab-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="2b1ab-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b1ab-133">NOTES</span></span>

## <span data-ttu-id="2b1ab-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b1ab-134">RELATED LINKS</span></span>

[<span data-ttu-id="2b1ab-135">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-135">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2b1ab-136">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-136">Get-AzureRmApplicationGatewayIPConfiguration</span></span>](./Get-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2b1ab-137">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-137">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="2b1ab-138">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b1ab-138">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


