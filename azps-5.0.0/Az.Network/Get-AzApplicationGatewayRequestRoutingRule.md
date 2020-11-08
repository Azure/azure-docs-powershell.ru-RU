---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 57A6DB40-43EC-402C-9784-06817ECD99B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: 75666d2f897adeda4031b03309979366949a0040
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249987"
---
# <span data-ttu-id="96c25-101">Get-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-101">Get-AzApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="96c25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96c25-102">SYNOPSIS</span></span>
<span data-ttu-id="96c25-103">Возвращает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="96c25-103">Gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="96c25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96c25-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRequestRoutingRule [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96c25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96c25-105">DESCRIPTION</span></span>
<span data-ttu-id="96c25-106">Командлет **Get-AzApplicationGatewayRequestRoutingRule** получает правило маршрутизации запросов для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="96c25-106">The **Get-AzApplicationGatewayRequestRoutingRule** cmdlet gets the request routing rule of an application gateway.</span></span>

## <span data-ttu-id="96c25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96c25-107">EXAMPLES</span></span>

### <span data-ttu-id="96c25-108">Пример 1: получение определенного правила маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="96c25-108">Example 1: Get a specific request routing rule</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rule = Get-AzApplicationGatewayRequestRoutingRule -"Rule01" -ApplicationGateway $AppGW
```

<span data-ttu-id="96c25-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96c25-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="96c25-110">Вторая команда получает правило маршрутизации запросов с именем Rule01 из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96c25-110">The second command gets the request routing rule named Rule01 from the Application Gateway stored in the variable named $AppGW.</span></span>

### <span data-ttu-id="96c25-111">Пример 2: получение списка правил маршрутизации запросов</span><span class="sxs-lookup"><span data-stu-id="96c25-111">Example 2: Get a list of request routing rules</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Rules = Get-AzApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGW
```

<span data-ttu-id="96c25-112">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96c25-112">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="96c25-113">Вторая команда получает список правил маршрутизации запросов из шлюза приложения, который хранится в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96c25-113">The second command gets a list of request routing rules from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="96c25-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96c25-114">PARAMETERS</span></span>

### <span data-ttu-id="96c25-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96c25-115">-ApplicationGateway</span></span>
<span data-ttu-id="96c25-116">Указывает объект шлюза приложения, который содержит правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="96c25-116">Specifies the application gateway object that contains request routing rule.</span></span>

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

### <span data-ttu-id="96c25-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c25-117">-DefaultProfile</span></span>
<span data-ttu-id="96c25-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96c25-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96c25-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96c25-119">-Name</span></span>
<span data-ttu-id="96c25-120">Указывает имя правила маршрутизации запросов, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="96c25-120">Specifies the name of the request routing rule which this cmdlet gets.</span></span>

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

### <span data-ttu-id="96c25-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c25-121">CommonParameters</span></span>
<span data-ttu-id="96c25-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96c25-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c25-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c25-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c25-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96c25-124">INPUTS</span></span>

### <span data-ttu-id="96c25-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96c25-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96c25-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96c25-126">OUTPUTS</span></span>

### <span data-ttu-id="96c25-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="96c25-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="96c25-128">NOTES</span></span>

## <span data-ttu-id="96c25-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96c25-129">RELATED LINKS</span></span>

[<span data-ttu-id="96c25-130">Add-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-130">Add-AzApplicationGatewayRequestRoutingRule</span></span>](./Add-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="96c25-131">New-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-131">New-AzApplicationGatewayRequestRoutingRule</span></span>](./New-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="96c25-132">Remove-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-132">Remove-AzApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="96c25-133">Set-AzApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="96c25-133">Set-AzApplicationGatewayRequestRoutingRule</span></span>](./Set-AzApplicationGatewayRequestRoutingRule.md)


