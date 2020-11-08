---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235586"
---
# <span data-ttu-id="6ab29-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab29-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6ab29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ab29-102">SYNOPSIS</span></span>
<span data-ttu-id="6ab29-103">Возвращает конфигурацию WAF для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6ab29-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="6ab29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ab29-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ab29-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ab29-105">DESCRIPTION</span></span>
<span data-ttu-id="6ab29-106">Командлет **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** получает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6ab29-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="6ab29-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ab29-107">EXAMPLES</span></span>

### <span data-ttu-id="6ab29-108">Пример 1: получение конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="6ab29-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="6ab29-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="6ab29-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="6ab29-110">Вторая команда возвращает конфигурацию брандмауэра для шлюза приложения в $AppGW, а затем сохраняет его в $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="6ab29-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="6ab29-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ab29-111">PARAMETERS</span></span>

### <span data-ttu-id="6ab29-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ab29-112">-ApplicationGateway</span></span>
<span data-ttu-id="6ab29-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6ab29-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="6ab29-114">Вы можете использовать командлет Get-AzApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6ab29-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="6ab29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ab29-115">-DefaultProfile</span></span>
<span data-ttu-id="6ab29-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ab29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ab29-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab29-117">CommonParameters</span></span>
<span data-ttu-id="6ab29-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ab29-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab29-119">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ab29-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab29-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ab29-120">INPUTS</span></span>

### <span data-ttu-id="6ab29-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ab29-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6ab29-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ab29-122">OUTPUTS</span></span>

### <span data-ttu-id="6ab29-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab29-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6ab29-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ab29-124">NOTES</span></span>

## <span data-ttu-id="6ab29-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ab29-125">RELATED LINKS</span></span>

[<span data-ttu-id="6ab29-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6ab29-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="6ab29-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab29-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="6ab29-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6ab29-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

