---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F01CB88A-49E7-41D8-B4E7-F1A4DCDC6B84
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewaySku.md
ms.openlocfilehash: c8bd4a0070aa0e5635fad7cb20a627a7d23f5922
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249982"
---
# <span data-ttu-id="84cc5-101">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="84cc5-101">Get-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="84cc5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84cc5-102">SYNOPSIS</span></span>
<span data-ttu-id="84cc5-103">Возвращает SKU шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="84cc5-103">Gets the SKU of an application gateway.</span></span>

## <span data-ttu-id="84cc5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84cc5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84cc5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84cc5-105">DESCRIPTION</span></span>
<span data-ttu-id="84cc5-106">Командлет **Get-AzApplicationGatewaySku** получает единицу хранения (SKU) шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="84cc5-106">The **Get-AzApplicationGatewaySku** cmdlet gets the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="84cc5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84cc5-107">EXAMPLES</span></span>

### <span data-ttu-id="84cc5-108">Пример 1: получение SKU шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="84cc5-108">Example 1: Get an application gateway SKU</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $SKU = Get-AzApplicationGatewaySku -ApplicationGateway $AppGW
```

<span data-ttu-id="84cc5-109">Первая команда получает шлюз приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $AppGW.</span><span class="sxs-lookup"><span data-stu-id="84cc5-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="84cc5-110">Вторая команда возвращает SKU шлюза приложения с именем ApplicationGateway01 и сохраняет результат в переменной с именем $SKU.</span><span class="sxs-lookup"><span data-stu-id="84cc5-110">The second command gets the SKU of an application gateway named ApplicationGateway01 and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="84cc5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84cc5-111">PARAMETERS</span></span>

### <span data-ttu-id="84cc5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84cc5-112">-ApplicationGateway</span></span>
<span data-ttu-id="84cc5-113">Указывает объект шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="84cc5-113">Specifies the application gateway object.</span></span>

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

### <span data-ttu-id="84cc5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84cc5-114">-DefaultProfile</span></span>
<span data-ttu-id="84cc5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84cc5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84cc5-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84cc5-116">CommonParameters</span></span>
<span data-ttu-id="84cc5-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84cc5-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84cc5-118">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="84cc5-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84cc5-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84cc5-119">INPUTS</span></span>

### <span data-ttu-id="84cc5-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="84cc5-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="84cc5-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84cc5-121">OUTPUTS</span></span>

### <span data-ttu-id="84cc5-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="84cc5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="84cc5-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="84cc5-123">NOTES</span></span>

## <span data-ttu-id="84cc5-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84cc5-124">RELATED LINKS</span></span>

[<span data-ttu-id="84cc5-125">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="84cc5-125">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)

[<span data-ttu-id="84cc5-126">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="84cc5-126">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)

