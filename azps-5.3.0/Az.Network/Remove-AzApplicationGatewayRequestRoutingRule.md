---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: c1c630c39039d39b1957ccab78bb96d8f085176c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506909"
---
# <span data-ttu-id="7dde8-101">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-101">Remove-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7dde8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dde8-102">SYNOPSIS</span></span>
<span data-ttu-id="7dde8-103">Удаляет правило маршрутки запроса из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7dde8-103">Removes a request routing rule from an application gateway.</span></span>

## <span data-ttu-id="7dde8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7dde8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7dde8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7dde8-105">DESCRIPTION</span></span>
<span data-ttu-id="7dde8-106">Cmdlet **Remove-AzApplicationGatewayRequestRoutingRule** удаляет правило маршрутизации запросов из шлюза приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7dde8-106">The **Remove-AzApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="7dde8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7dde8-107">EXAMPLES</span></span>

### <span data-ttu-id="7dde8-108">Пример 1. Удаление правила маршрутки запроса из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="7dde8-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="7dde8-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7dde8-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7dde8-110">Вторая команда удаляет правило маршрутизов запроса "Правило02" из шлюза приложения, $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7dde8-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7dde8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7dde8-111">PARAMETERS</span></span>

### <span data-ttu-id="7dde8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dde8-112">-ApplicationGateway</span></span>
<span data-ttu-id="7dde8-113">Указывает шлюз приложения, из которого нужно удалить правило маршрутки запросов.</span><span class="sxs-lookup"><span data-stu-id="7dde8-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="7dde8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dde8-114">-DefaultProfile</span></span>
<span data-ttu-id="7dde8-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7dde8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7dde8-116">-Name</span><span class="sxs-lookup"><span data-stu-id="7dde8-116">-Name</span></span>
<span data-ttu-id="7dde8-117">Указывает имя правила маршрутки запроса, для которого этот cmdlet удаляется.</span><span class="sxs-lookup"><span data-stu-id="7dde8-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="7dde8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dde8-118">CommonParameters</span></span>
<span data-ttu-id="7dde8-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7dde8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dde8-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dde8-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dde8-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7dde8-121">INPUTS</span></span>

### <span data-ttu-id="7dde8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7dde8-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7dde8-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7dde8-123">OUTPUTS</span></span>

### <span data-ttu-id="7dde8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="7dde8-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7dde8-125">NOTES</span></span>

## <span data-ttu-id="7dde8-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7dde8-126">RELATED LINKS</span></span>

[<span data-ttu-id="7dde8-127">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-127">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dde8-128">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-128">Get-AzApplicationGatewayRequestRoutingRule</span></span>](./Get-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dde8-129">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-129">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="7dde8-130">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7dde8-130">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)

