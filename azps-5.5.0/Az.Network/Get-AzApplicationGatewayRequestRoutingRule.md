---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218825"
---
# <span data-ttu-id="4ed9d-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4ed9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ed9d-102">SYNOPSIS</span></span>
<span data-ttu-id="4ed9d-103">Получает правило маршрутинга запросов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="4ed9d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ed9d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ed9d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ed9d-105">DESCRIPTION</span></span>
<span data-ttu-id="4ed9d-106">Cmdlet **Get-AzApplicationGatewayRequestRoutingRule** получает правило маршрутизации запросов шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="4ed9d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ed9d-107">EXAMPLES</span></span>

### <span data-ttu-id="4ed9d-108">Пример 1. Получите определенное правило маршрутинга запросов</span><span class="sxs-lookup"><span data-stu-id="4ed9d-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="4ed9d-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4ed9d-110">Вторая команда получает правило маршрутизов запроса "Правило01" из шлюза приложения, храняного в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="4ed9d-111">Пример 2. Получить список правил маршрутки запросов</span><span class="sxs-lookup"><span data-stu-id="4ed9d-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="4ed9d-112">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="4ed9d-113">Вторая команда получает список правил маршрутизов запросов из шлюза приложения, храняного в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="4ed9d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ed9d-114">PARAMETERS</span></span>

### <span data-ttu-id="4ed9d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ed9d-115">-ApplicationGateway</span></span>
<span data-ttu-id="4ed9d-116">Определяет объект шлюза приложения, который содержит правило маршрутинга запросов.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="4ed9d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ed9d-117">-DefaultProfile</span></span>
<span data-ttu-id="4ed9d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ed9d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4ed9d-119">-Name</span></span>
<span data-ttu-id="4ed9d-120">Указывает имя правила маршрутки запроса, которое получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="4ed9d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ed9d-121">CommonParameters</span></span>
<span data-ttu-id="4ed9d-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ed9d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ed9d-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ed9d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ed9d-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed9d-124">INPUTS</span></span>

### <span data-ttu-id="4ed9d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ed9d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ed9d-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ed9d-126">OUTPUTS</span></span>

### <span data-ttu-id="4ed9d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="4ed9d-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ed9d-128">NOTES</span></span>

## <span data-ttu-id="4ed9d-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ed9d-129">RELATED LINKS</span></span>

[<span data-ttu-id="4ed9d-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ed9d-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ed9d-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="4ed9d-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="4ed9d-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


