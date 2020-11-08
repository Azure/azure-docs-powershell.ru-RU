---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078881"
---
# <span data-ttu-id="48215-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="48215-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48215-102">SYNOPSIS</span></span>
<span data-ttu-id="48215-103">Удаляет правило маршрутизации запросов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="48215-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="48215-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48215-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48215-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48215-105">DESCRIPTION</span></span>
<span data-ttu-id="48215-106">Командлет **Remove-AzApplicationGatewayRequestRoutingRule** удаляет правило маршрутизации запросов из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="48215-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="48215-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48215-107">EXAMPLES</span></span>

### <span data-ttu-id="48215-108">Пример 1: Удаление правила маршрутизации запросов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="48215-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="48215-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48215-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="48215-110">Вторая команда удаляет правило маршрутизации запросов с именем Rule02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="48215-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="48215-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48215-111">PARAMETERS</span></span>

### <span data-ttu-id="48215-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48215-112">-ApplicationGateway</span></span>
<span data-ttu-id="48215-113">Указывает шлюз приложений, из которого нужно удалить правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="48215-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="48215-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48215-114">-DefaultProfile</span></span>
<span data-ttu-id="48215-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48215-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48215-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48215-116">-Name</span></span>
<span data-ttu-id="48215-117">Указывает имя правила маршрутизации запросов, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="48215-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="48215-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48215-118">CommonParameters</span></span>
<span data-ttu-id="48215-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48215-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48215-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48215-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48215-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48215-121">INPUTS</span></span>

### <span data-ttu-id="48215-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48215-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48215-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48215-123">OUTPUTS</span></span>

### <span data-ttu-id="48215-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="48215-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="48215-125">NOTES</span></span>

## <span data-ttu-id="48215-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48215-126">RELATED LINKS</span></span>

[<span data-ttu-id="48215-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="48215-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="48215-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="48215-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="48215-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


