---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: e2f477aa657bc4d21a650edffb7f014ae3c1ba62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730622"
---
# <span data-ttu-id="1ac38-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac38-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="1ac38-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ac38-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac38-103">Возвращает конфигурацию WAF для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ac38-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="1ac38-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ac38-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ac38-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac38-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac38-106">Командлет **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** получает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1ac38-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="1ac38-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ac38-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac38-108">Пример 1: получение конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="1ac38-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="1ac38-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="1ac38-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="1ac38-110">Вторая команда возвращает конфигурацию брандмауэра для шлюза приложения в $AppGW, а затем сохраняет его в $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="1ac38-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="1ac38-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ac38-111">PARAMETERS</span></span>

### <span data-ttu-id="1ac38-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ac38-112">-ApplicationGateway</span></span>
<span data-ttu-id="1ac38-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ac38-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="1ac38-114">Вы можете использовать командлет Get-AzApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ac38-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="1ac38-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ac38-115">-DefaultProfile</span></span>
<span data-ttu-id="1ac38-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ac38-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ac38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac38-117">CommonParameters</span></span>
<span data-ttu-id="1ac38-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ac38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac38-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ac38-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac38-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ac38-120">INPUTS</span></span>

### <span data-ttu-id="1ac38-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ac38-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ac38-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ac38-122">OUTPUTS</span></span>

### <span data-ttu-id="1ac38-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac38-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="1ac38-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ac38-124">NOTES</span></span>

## <span data-ttu-id="1ac38-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ac38-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ac38-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ac38-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="1ac38-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac38-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="1ac38-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="1ac38-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


