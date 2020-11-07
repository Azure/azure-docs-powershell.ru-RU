---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 312AA609-7362-42A5-A889-C0784D5A2943
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c0dad1f63f8a203a9f1b8aaeb75a2be13bfc61f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902769"
---
# <span data-ttu-id="af7db-101">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-101">New-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="af7db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="af7db-102">SYNOPSIS</span></span>
<span data-ttu-id="af7db-103">Создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-103">Creates an IP configuration for an application gateway.</span></span>

## <span data-ttu-id="af7db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="af7db-104">SYNTAX</span></span>

### <span data-ttu-id="af7db-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="af7db-105">SetByResourceId</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af7db-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="af7db-106">SetByResource</span></span>
```
New-AzApplicationGatewayIPConfiguration -Name <String> [-Subnet <PSSubnet>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af7db-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7db-107">DESCRIPTION</span></span>
<span data-ttu-id="af7db-108">Командлет **New-AzApplicationGatewayIPConfiguration** создает IP-конфигурацию для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-108">The **New-AzApplicationGatewayIPConfiguration** cmdlet creates an IP configuration for an application gateway.</span></span>
<span data-ttu-id="af7db-109">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-109">The IP configuration contains the subnet in which application gateway is deployed.</span></span>

## <span data-ttu-id="af7db-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="af7db-110">EXAMPLES</span></span>

### <span data-ttu-id="af7db-111">Пример 1: создание IP-конфигурации для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-111">Example 1: Create an IP configuration for an application gateway.</span></span>
```
PS C:\>$VNet = Get-AzVirtualNetwork -Name "VNet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $VNet 
PS C:\ $GatewayIpConfig = New-AzApplicationGatewayIPConfiguration -Name "AppGwSubnet01" -Subnet $Subnet
```

<span data-ttu-id="af7db-112">Первая команда возвращает виртуальную сеть с именем VNet01, которая относится к группе ресурсов с именем ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="af7db-112">The first command gets a virtual network named VNet01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="af7db-113">Вторая команда возвращает конфигурацию подсети для подсети, к которой принадлежит виртуальная сеть в предыдущей команде, и сохраняет ее в переменной $Subnet.</span><span class="sxs-lookup"><span data-stu-id="af7db-113">The second command gets the subnet configuration for the subnet that the virtual network in the previous command belongs to, and stores it in the $Subnet variable.</span></span>
<span data-ttu-id="af7db-114">Третья команда создает IP-конфигурацию с помощью $Subnet.</span><span class="sxs-lookup"><span data-stu-id="af7db-114">The third command creates the IP configuration using $Subnet.</span></span>

## <span data-ttu-id="af7db-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="af7db-115">PARAMETERS</span></span>

### <span data-ttu-id="af7db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af7db-116">-DefaultProfile</span></span>
<span data-ttu-id="af7db-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="af7db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af7db-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="af7db-118">-Name</span></span>
<span data-ttu-id="af7db-119">Указывает имя создаваемой IP-конфигурации.</span><span class="sxs-lookup"><span data-stu-id="af7db-119">Specifies the name of the IP configuration to create.</span></span>

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

### <span data-ttu-id="af7db-120">-Подсеть</span><span class="sxs-lookup"><span data-stu-id="af7db-120">-Subnet</span></span>
<span data-ttu-id="af7db-121">Указывает объект подсети.</span><span class="sxs-lookup"><span data-stu-id="af7db-121">Specifies the subnet object.</span></span>
<span data-ttu-id="af7db-122">Это подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-122">This is the subnet in which the application gateway is deployed.</span></span>

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

### <span data-ttu-id="af7db-123">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="af7db-123">-SubnetId</span></span>
<span data-ttu-id="af7db-124">Указывает идентификатор подсети.</span><span class="sxs-lookup"><span data-stu-id="af7db-124">Specifies the subnet ID.</span></span>
<span data-ttu-id="af7db-125">Это подсеть, в которой будет развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="af7db-125">This is the subnet in which the application gateway would be deployed.</span></span>

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

### <span data-ttu-id="af7db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af7db-126">CommonParameters</span></span>
<span data-ttu-id="af7db-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="af7db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af7db-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af7db-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af7db-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="af7db-129">INPUTS</span></span>

### <span data-ttu-id="af7db-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="af7db-130">None</span></span>

## <span data-ttu-id="af7db-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="af7db-131">OUTPUTS</span></span>

### <span data-ttu-id="af7db-132">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-132">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="af7db-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="af7db-133">NOTES</span></span>

## <span data-ttu-id="af7db-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="af7db-134">RELATED LINKS</span></span>

[<span data-ttu-id="af7db-135">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-135">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="af7db-136">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-136">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="af7db-137">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-137">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="af7db-138">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="af7db-138">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


