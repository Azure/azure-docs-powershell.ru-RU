---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
ms.openlocfilehash: 7b83e7f8ca372faf8158e248d326595a0d162d6a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913458"
---
# <span data-ttu-id="e83c0-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83c0-101">Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e83c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e83c0-102">SYNOPSIS</span></span>
<span data-ttu-id="e83c0-103">Возвращает конфигурацию WAF для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e83c0-103">Gets the WAF configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e83c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e83c0-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e83c0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e83c0-105">DESCRIPTION</span></span>
<span data-ttu-id="e83c0-106">Командлет **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** получает конфигурацию брандмауэра веб-приложения (WAF) для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e83c0-106">The **Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="e83c0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e83c0-107">EXAMPLES</span></span>

### <span data-ttu-id="e83c0-108">Пример 1: получение конфигурации брандмауэра для веб-приложения "шлюз приложений"</span><span class="sxs-lookup"><span data-stu-id="e83c0-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzureRmApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="e83c0-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет его в переменной $AppGW.</span><span class="sxs-lookup"><span data-stu-id="e83c0-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>

<span data-ttu-id="e83c0-110">Вторая команда возвращает конфигурацию брандмауэра для шлюза приложения в $AppGW, а затем сохраняет его в $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="e83c0-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="e83c0-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e83c0-111">PARAMETERS</span></span>

### <span data-ttu-id="e83c0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e83c0-112">-ApplicationGateway</span></span>
<span data-ttu-id="e83c0-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e83c0-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="e83c0-114">Вы можете использовать командлет Get-AzureRmApplicationGateway, чтобы получить объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e83c0-114">You can use the Get-AzureRmApplicationGateway cmdlet to get an application gateway object.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e83c0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e83c0-115">-DefaultProfile</span></span>
<span data-ttu-id="e83c0-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e83c0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e83c0-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e83c0-117">CommonParameters</span></span>
<span data-ttu-id="e83c0-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e83c0-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e83c0-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e83c0-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e83c0-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e83c0-120">INPUTS</span></span>

### <span data-ttu-id="e83c0-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e83c0-121">PSApplicationGateway</span></span>
<span data-ttu-id="e83c0-122">Параметр "ApplicationGateway" принимает значение типа "PSApplicationGateway" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e83c0-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="e83c0-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e83c0-123">OUTPUTS</span></span>

### <span data-ttu-id="e83c0-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83c0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="e83c0-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e83c0-125">NOTES</span></span>

## <span data-ttu-id="e83c0-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e83c0-126">RELATED LINKS</span></span>

[<span data-ttu-id="e83c0-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e83c0-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="e83c0-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83c0-128">New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="e83c0-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="e83c0-129">Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzureRmApplicationGatewayWebApplicationFirewallConfiguration.md)


