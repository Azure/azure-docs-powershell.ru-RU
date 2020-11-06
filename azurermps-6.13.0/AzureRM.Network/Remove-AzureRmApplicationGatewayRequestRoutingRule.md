---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: a4c1710ebbdfad1afb428bb09cccf27865c5e56e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562855"
---
# <span data-ttu-id="01610-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="01610-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01610-102">SYNOPSIS</span></span>
<span data-ttu-id="01610-103">Удаляет правило маршрутизации запросов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="01610-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01610-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01610-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01610-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01610-105">DESCRIPTION</span></span>
<span data-ttu-id="01610-106">Командлет **Remove-AzureRmApplicationGatewayRequestRoutingRule** удаляет правило маршрутизации запросов из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="01610-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="01610-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01610-107">EXAMPLES</span></span>

### <span data-ttu-id="01610-108">Пример 1: Удаление правила маршрутизации запросов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="01610-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="01610-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01610-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="01610-110">Вторая команда удаляет правило маршрутизации запросов с именем Rule02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="01610-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="01610-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01610-111">PARAMETERS</span></span>

### <span data-ttu-id="01610-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01610-112">-ApplicationGateway</span></span>
<span data-ttu-id="01610-113">Указывает шлюз приложений, из которого нужно удалить правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="01610-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="01610-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01610-114">-DefaultProfile</span></span>
<span data-ttu-id="01610-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01610-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01610-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01610-116">-Name</span></span>
<span data-ttu-id="01610-117">Указывает имя правила маршрутизации запросов, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="01610-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="01610-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01610-118">CommonParameters</span></span>
<span data-ttu-id="01610-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01610-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01610-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01610-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01610-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01610-121">INPUTS</span></span>

### <span data-ttu-id="01610-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="01610-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="01610-123">Параметры: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01610-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="01610-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01610-124">OUTPUTS</span></span>

### <span data-ttu-id="01610-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="01610-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="01610-126">NOTES</span></span>

## <span data-ttu-id="01610-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01610-127">RELATED LINKS</span></span>

[<span data-ttu-id="01610-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-128">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01610-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-129">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01610-130">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-130">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="01610-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="01610-131">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


