---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 367d4efc8332b862a8db276934acfa971d7c0d9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001208"
---
# <span data-ttu-id="b8837-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b8837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8837-102">SYNOPSIS</span></span>
<span data-ttu-id="b8837-103">Получает конфигурацию IP-адреса шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b8837-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="b8837-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b8837-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8837-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b8837-105">DESCRIPTION</span></span>
<span data-ttu-id="b8837-106">Для получения конфигурации IP-адреса шлюза приложения возвращается **cmdlet Get-AzApplicationGatewayIPConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="b8837-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="b8837-107">Конфигурация IP-адреса содержит подсеть, в которой развернут шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="b8837-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="b8837-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b8837-108">EXAMPLES</span></span>

### <span data-ttu-id="b8837-109">Пример 1. Настройка определенных IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b8837-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="b8837-110">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда получает конфигурацию IP-адреса GateSubnet01 из шлюза, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b8837-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="b8837-111">Пример 2. Получить список конфигураций IP-адресов</span><span class="sxs-lookup"><span data-stu-id="b8837-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="b8837-112">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw. Вторая команда получает список всех конфигураций IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="b8837-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="b8837-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8837-113">PARAMETERS</span></span>

### <span data-ttu-id="b8837-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8837-114">-ApplicationGateway</span></span>
<span data-ttu-id="b8837-115">Определяет объект шлюза приложения, который содержит конфигурацию IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="b8837-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="b8837-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8837-116">-DefaultProfile</span></span>
<span data-ttu-id="b8837-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b8837-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8837-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b8837-118">-Name</span></span>
<span data-ttu-id="b8837-119">Указывает имя конфигурации IP-адреса, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8837-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="b8837-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8837-120">CommonParameters</span></span>
<span data-ttu-id="b8837-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8837-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8837-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8837-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8837-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8837-123">INPUTS</span></span>

### <span data-ttu-id="b8837-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8837-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b8837-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b8837-125">OUTPUTS</span></span>

### <span data-ttu-id="b8837-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="b8837-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b8837-127">NOTES</span></span>

## <span data-ttu-id="b8837-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b8837-128">RELATED LINKS</span></span>

[<span data-ttu-id="b8837-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8837-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8837-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="b8837-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="b8837-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


