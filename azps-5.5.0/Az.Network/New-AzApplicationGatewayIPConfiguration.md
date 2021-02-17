---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213796"
---
# <span data-ttu-id="84862-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="84862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84862-102">SYNOPSIS</span></span>
<span data-ttu-id="84862-103">Создает конфигурацию IP-адреса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="84862-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="84862-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84862-104">SYNTAX</span></span>

### <span data-ttu-id="84862-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="84862-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84862-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="84862-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84862-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84862-107">DESCRIPTION</span></span>
<span data-ttu-id="84862-108">Для шлюза приложения создается конфигурация **IP-адреса.**</span><span class="sxs-lookup"><span data-stu-id="84862-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="84862-109">Конфигурация IP-адреса содержит подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="84862-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="84862-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84862-110">EXAMPLES</span></span>

### <span data-ttu-id="84862-111">Пример 1. Создание конфигурации IP-адреса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="84862-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="84862-112">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="84862-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="84862-113">Вторая команда получает конфигурацию подсети, к которой относится виртуальная сеть в предыдущей команде, и сохраняет ее в переменной $Subnet сети.</span><span class="sxs-lookup"><span data-stu-id="84862-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="84862-114">Третья команда создает конфигурацию IP-адреса с помощью $Subnet.</span><span class="sxs-lookup"><span data-stu-id="84862-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="84862-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84862-115">PARAMETERS</span></span>

### <span data-ttu-id="84862-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84862-116">-DefaultProfile</span></span>
<span data-ttu-id="84862-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84862-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84862-118">-Name</span><span class="sxs-lookup"><span data-stu-id="84862-118">-Name</span></span>
<span data-ttu-id="84862-119">Указывает имя создаемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="84862-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="84862-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="84862-120">-Subnet</span></span>
<span data-ttu-id="84862-121">Указывает объект подсети.</span><span class="sxs-lookup"><span data-stu-id="84862-121">Specifies the subnet object.</span></span>
<span data-ttu-id="84862-122">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="84862-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="84862-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="84862-123">-SubnetId</span></span>
<span data-ttu-id="84862-124">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="84862-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="84862-125">Это подсеть, в которой будет развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="84862-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="84862-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84862-126">CommonParameters</span></span>
<span data-ttu-id="84862-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84862-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84862-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84862-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84862-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84862-129">INPUTS</span></span>

### <span data-ttu-id="84862-130">Нет</span><span class="sxs-lookup"><span data-stu-id="84862-130">None</span></span>

## <span data-ttu-id="84862-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84862-131">OUTPUTS</span></span>

### <span data-ttu-id="84862-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="84862-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84862-133">NOTES</span></span>

## <span data-ttu-id="84862-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84862-134">RELATED LINKS</span></span>

[<span data-ttu-id="84862-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="84862-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="84862-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="84862-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="84862-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


