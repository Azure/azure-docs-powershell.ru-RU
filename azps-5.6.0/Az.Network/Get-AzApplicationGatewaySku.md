---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: cf869a0de5847b1930879dbd610749746370791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994062"
---
# <span data-ttu-id="67751-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="67751-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="67751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67751-102">SYNOPSIS</span></span>
<span data-ttu-id="67751-103">Возвращает SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67751-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="67751-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="67751-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67751-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67751-105">DESCRIPTION</span></span>
<span data-ttu-id="67751-106">Для **шлюза приложения cmdlet Get-AzApplicationGatewaySku** получает единицу сохраняемого акций (SKU).</span><span class="sxs-lookup"><span data-stu-id="67751-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="67751-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="67751-107">EXAMPLES</span></span>

### <span data-ttu-id="67751-108">Пример 1. Получение SKU шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="67751-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="67751-109">Первая команда получает шлюз приложения ApplicationGateway01 и сохраняет результат в переменной с $AppGW.</span><span class="sxs-lookup"><span data-stu-id="67751-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="67751-110">Вторая команда получает SKU шлюза приложения ApplicationGateway01 и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="67751-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="67751-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67751-111">PARAMETERS</span></span>

### <span data-ttu-id="67751-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67751-112">-ApplicationGateway</span></span>
<span data-ttu-id="67751-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67751-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="67751-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67751-114">-DefaultProfile</span></span>
<span data-ttu-id="67751-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67751-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67751-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67751-116">CommonParameters</span></span>
<span data-ttu-id="67751-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67751-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67751-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="67751-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67751-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="67751-119">INPUTS</span></span>

### <span data-ttu-id="67751-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="67751-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="67751-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="67751-121">OUTPUTS</span></span>

### <span data-ttu-id="67751-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="67751-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="67751-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="67751-123">NOTES</span></span>

## <span data-ttu-id="67751-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67751-124">RELATED LINKS</span></span>

[<span data-ttu-id="67751-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="67751-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="67751-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="67751-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


