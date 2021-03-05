---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993933"
---
# <span data-ttu-id="da88e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da88e-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="da88e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da88e-102">SYNOPSIS</span></span>
<span data-ttu-id="da88e-103">Получает конфигурацию WAF шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da88e-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="da88e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="da88e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="da88e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da88e-105">DESCRIPTION</span></span>
<span data-ttu-id="da88e-106">С **помощью cmdlet get-AzApplicationGatewayWebApplicationFirewallConfiguration** получает конфигурацию брандмауэра веб-приложения (WAF) шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da88e-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="da88e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="da88e-107">EXAMPLES</span></span>

### <span data-ttu-id="da88e-108">Пример 1. Настройка брандмауэра веб-приложения шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="da88e-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="da88e-109">Первая команда получает шлюз приложения ApplicationGateway01, а затем сохраняет его в $AppGW переменной.</span><span class="sxs-lookup"><span data-stu-id="da88e-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="da88e-110">Вторая команда получает конфигурацию брандмауэра шлюза приложения в $AppGW, а затем сохраняет ее в $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="da88e-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="da88e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da88e-111">PARAMETERS</span></span>

### <span data-ttu-id="da88e-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da88e-112">-ApplicationGateway</span></span>
<span data-ttu-id="da88e-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da88e-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="da88e-114">Вы можете использовать Get-AzApplicationGateway для получения объекта шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="da88e-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="da88e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da88e-115">-DefaultProfile</span></span>
<span data-ttu-id="da88e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="da88e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da88e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da88e-117">CommonParameters</span></span>
<span data-ttu-id="da88e-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da88e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da88e-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da88e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da88e-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="da88e-120">INPUTS</span></span>

### <span data-ttu-id="da88e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da88e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="da88e-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="da88e-122">OUTPUTS</span></span>

### <span data-ttu-id="da88e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da88e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="da88e-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="da88e-124">NOTES</span></span>

## <span data-ttu-id="da88e-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da88e-125">RELATED LINKS</span></span>

[<span data-ttu-id="da88e-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="da88e-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="da88e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da88e-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="da88e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="da88e-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


