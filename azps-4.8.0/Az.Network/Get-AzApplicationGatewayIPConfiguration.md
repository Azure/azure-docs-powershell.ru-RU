---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236980"
---
# <span data-ttu-id="356e5-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="356e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="356e5-102">SYNOPSIS</span></span>
<span data-ttu-id="356e5-103">Возвращает конфигурацию IP для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="356e5-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="356e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="356e5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="356e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="356e5-105">DESCRIPTION</span></span>
<span data-ttu-id="356e5-106">Командлет **Get-AzApplicationGatewayIPConfiguration** получает IP-конфигурацию шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="356e5-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="356e5-107">Конфигурация IP содержит подсеть, в которой развернут шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="356e5-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="356e5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="356e5-108">EXAMPLES</span></span>

### <span data-ttu-id="356e5-109">Пример 1: получение определенной конфигурации IP</span><span class="sxs-lookup"><span data-stu-id="356e5-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="356e5-110">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда получает IP-конфигурацию с именем GateSubnet01 из шлюза, хранящегося в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="356e5-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="356e5-111">Пример 2: получение списка конфигураций IP</span><span class="sxs-lookup"><span data-stu-id="356e5-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="356e5-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда возвращает список всех конфигураций IP.</span><span class="sxs-lookup"><span data-stu-id="356e5-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="356e5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="356e5-113">PARAMETERS</span></span>

### <span data-ttu-id="356e5-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356e5-114">-ApplicationGateway</span></span>
<span data-ttu-id="356e5-115">Указывает объект шлюза приложения, который содержит IP-конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="356e5-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="356e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="356e5-116">-DefaultProfile</span></span>
<span data-ttu-id="356e5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="356e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="356e5-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="356e5-118">-Name</span></span>
<span data-ttu-id="356e5-119">Указывает имя конфигурации IP, которую этот командлет получает.</span><span class="sxs-lookup"><span data-stu-id="356e5-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="356e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="356e5-120">CommonParameters</span></span>
<span data-ttu-id="356e5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="356e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="356e5-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="356e5-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="356e5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="356e5-123">INPUTS</span></span>

### <span data-ttu-id="356e5-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="356e5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="356e5-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="356e5-125">OUTPUTS</span></span>

### <span data-ttu-id="356e5-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="356e5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="356e5-127">NOTES</span></span>

## <span data-ttu-id="356e5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="356e5-128">RELATED LINKS</span></span>

[<span data-ttu-id="356e5-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="356e5-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="356e5-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="356e5-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="356e5-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


