---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CC033DA8-FACC-44E2-82F9-E30FADBF8926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 859ef684424069bb5fc4c5b45de3e722f0921705
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913601"
---
# <span data-ttu-id="37b16-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-101">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="37b16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37b16-102">SYNOPSIS</span></span>
<span data-ttu-id="37b16-103">Удаляет правило маршрутизации запросов из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="37b16-103">Removes a request routing rule from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37b16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37b16-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b16-105">DESCRIPTION</span></span>
<span data-ttu-id="37b16-106">Командлет **Remove-AzureRmApplicationGatewayRequestRoutingRule** удаляет правило маршрутизации запросов из шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="37b16-106">The **Remove-AzureRmApplicationGatewayRequestRoutingRule** cmdlet removes a request routing rule from an Azure application gateway.</span></span>

## <span data-ttu-id="37b16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37b16-107">EXAMPLES</span></span>

### <span data-ttu-id="37b16-108">Пример 1: Удаление правила маршрутизации запросов из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="37b16-108">Example 1: Remove a request routing rule from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayRequestRoutingRule -ApplicationGateway $AppGw -Name "Rule02"
```

<span data-ttu-id="37b16-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="37b16-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="37b16-110">Вторая команда удаляет правило маршрутизации запросов с именем Rule02 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="37b16-110">The second command removes the request routing rule named Rule02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="37b16-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37b16-111">PARAMETERS</span></span>

### <span data-ttu-id="37b16-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="37b16-112">-ApplicationGateway</span></span>
<span data-ttu-id="37b16-113">Указывает шлюз приложений, из которого нужно удалить правило маршрутизации запросов.</span><span class="sxs-lookup"><span data-stu-id="37b16-113">Specifies the application gateway from which to remove a request routing rule.</span></span>

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

### <span data-ttu-id="37b16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b16-114">-DefaultProfile</span></span>
<span data-ttu-id="37b16-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37b16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b16-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="37b16-116">-Name</span></span>
<span data-ttu-id="37b16-117">Указывает имя правила маршрутизации запросов, для которого удаляется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="37b16-117">Specifies the name of the request routing rule for which this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b16-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b16-118">CommonParameters</span></span>
<span data-ttu-id="37b16-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37b16-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b16-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b16-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b16-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37b16-121">INPUTS</span></span>

### <span data-ttu-id="37b16-122">System. String</span><span class="sxs-lookup"><span data-stu-id="37b16-122">System.String</span></span>

## <span data-ttu-id="37b16-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37b16-123">OUTPUTS</span></span>

### <span data-ttu-id="37b16-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="37b16-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="37b16-125">NOTES</span></span>

## <span data-ttu-id="37b16-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37b16-126">RELATED LINKS</span></span>

[<span data-ttu-id="37b16-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-127">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="37b16-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-128">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="37b16-129">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-129">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./New-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="37b16-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="37b16-130">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


