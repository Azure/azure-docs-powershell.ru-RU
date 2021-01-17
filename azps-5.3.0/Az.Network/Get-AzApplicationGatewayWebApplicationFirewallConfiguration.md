---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98422335"
---
# <span data-ttu-id="6afa0-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afa0-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6afa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6afa0-102">SYNOPSIS</span></span>
<span data-ttu-id="6afa0-103">Получает конфигурацию WAF шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6afa0-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="6afa0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6afa0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6afa0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6afa0-105">DESCRIPTION</span></span>
<span data-ttu-id="6afa0-106">Для шлюза приложения с помощью **cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration** получает конфигурацию брандмауэра веб-приложения (WAF).</span><span class="sxs-lookup"><span data-stu-id="6afa0-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="6afa0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6afa0-107">EXAMPLES</span></span>

### <span data-ttu-id="6afa0-108">Пример 1. Настройка брандмауэра веб-приложения шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="6afa0-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="6afa0-109">Первая команда получает шлюз приложения ApplicationGateway01, а затем сохраняет его в $AppGW переменной.</span><span class="sxs-lookup"><span data-stu-id="6afa0-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="6afa0-110">Вторая команда получает конфигурацию брандмауэра шлюза приложения в $AppGW, а затем сохраняет ее в $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="6afa0-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="6afa0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6afa0-111">PARAMETERS</span></span>

### <span data-ttu-id="6afa0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afa0-112">-ApplicationGateway</span></span>
<span data-ttu-id="6afa0-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="6afa0-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="6afa0-114">Для получения объекта шлюза Get-AzApplicationGateway можно использовать Get-AzApplicationGateway приложения.</span><span class="sxs-lookup"><span data-stu-id="6afa0-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="6afa0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6afa0-115">-DefaultProfile</span></span>
<span data-ttu-id="6afa0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6afa0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6afa0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6afa0-117">CommonParameters</span></span>
<span data-ttu-id="6afa0-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6afa0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6afa0-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6afa0-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6afa0-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6afa0-120">INPUTS</span></span>

### <span data-ttu-id="6afa0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afa0-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6afa0-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6afa0-122">OUTPUTS</span></span>

### <span data-ttu-id="6afa0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afa0-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="6afa0-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6afa0-124">NOTES</span></span>

## <span data-ttu-id="6afa0-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6afa0-125">RELATED LINKS</span></span>

[<span data-ttu-id="6afa0-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6afa0-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="6afa0-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afa0-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="6afa0-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="6afa0-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


