---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: e9e10eb151c6908e05047d80c5aed4aff3b9f613
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405700"
---
# <span data-ttu-id="89a8d-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="89a8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="89a8d-103">Создает конфигурацию IP-адреса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="89a8d-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="89a8d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89a8d-104">SYNTAX</span></span>

### <span data-ttu-id="89a8d-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="89a8d-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89a8d-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="89a8d-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89a8d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89a8d-107">DESCRIPTION</span></span>
<span data-ttu-id="89a8d-108">Для шлюза приложения создается конфигурация **IP-адреса.**</span><span class="sxs-lookup"><span data-stu-id="89a8d-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="89a8d-109">Конфигурация IP-адреса содержит подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="89a8d-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="89a8d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89a8d-110">EXAMPLES</span></span>

### <span data-ttu-id="89a8d-111">Пример 1. Создание конфигурации IP-адреса для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="89a8d-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="89a8d-112">Первая команда получает виртуальную сеть VNet01, которая принадлежит к группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="89a8d-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="89a8d-113">Вторая команда получает конфигурацию подсети для подсети, к которой относится виртуальная сеть в предыдущей команде, и сохраняет ее в переменной $Subnet сети.</span><span class="sxs-lookup"><span data-stu-id="89a8d-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="89a8d-114">Третья команда создает конфигурацию IP-адреса с помощью $Subnet.</span><span class="sxs-lookup"><span data-stu-id="89a8d-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="89a8d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89a8d-115">PARAMETERS</span></span>

### <span data-ttu-id="89a8d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89a8d-116">-DefaultProfile</span></span>
<span data-ttu-id="89a8d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89a8d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89a8d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="89a8d-118">-Name</span></span>
<span data-ttu-id="89a8d-119">Указывает имя создаемой конфигурации IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="89a8d-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="89a8d-120">-Subnet</span><span class="sxs-lookup"><span data-stu-id="89a8d-120">-Subnet</span></span>
<span data-ttu-id="89a8d-121">Указывает объект подсети.</span><span class="sxs-lookup"><span data-stu-id="89a8d-121">Specifies the subnet object.</span></span>
<span data-ttu-id="89a8d-122">Это подсеть, в которой развертывается шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="89a8d-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="89a8d-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="89a8d-123">-SubnetId</span></span>
<span data-ttu-id="89a8d-124">Определяет ИД подсети.</span><span class="sxs-lookup"><span data-stu-id="89a8d-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="89a8d-125">Это подсеть, в которой будет развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="89a8d-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="89a8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89a8d-126">CommonParameters</span></span>
<span data-ttu-id="89a8d-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89a8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89a8d-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89a8d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89a8d-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89a8d-129">INPUTS</span></span>

### <span data-ttu-id="89a8d-130">Нет</span><span class="sxs-lookup"><span data-stu-id="89a8d-130">None</span></span>

## <span data-ttu-id="89a8d-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89a8d-131">OUTPUTS</span></span>

### <span data-ttu-id="89a8d-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="89a8d-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89a8d-133">NOTES</span></span>

## <span data-ttu-id="89a8d-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89a8d-134">RELATED LINKS</span></span>

[<span data-ttu-id="89a8d-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89a8d-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89a8d-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="89a8d-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="89a8d-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


