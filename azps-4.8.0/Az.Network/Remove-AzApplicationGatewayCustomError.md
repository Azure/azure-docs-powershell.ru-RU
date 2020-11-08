---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079454"
---
# <span data-ttu-id="48d18-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="48d18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48d18-102">SYNOPSIS</span></span>
<span data-ttu-id="48d18-103">Удаляет настраиваемое сообщение об ошибке из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="48d18-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="48d18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48d18-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48d18-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d18-105">DESCRIPTION</span></span>
<span data-ttu-id="48d18-106">Командлет **Remove-AzApplicationGatewayCustomError** удаляет настраиваемую ошибку из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="48d18-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="48d18-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48d18-107">EXAMPLES</span></span>

### <span data-ttu-id="48d18-108">Пример 1: Удаление настраиваемой ошибки из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="48d18-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="48d18-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 с $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="48d18-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="48d18-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48d18-110">PARAMETERS</span></span>

### <span data-ttu-id="48d18-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48d18-111">-ApplicationGateway</span></span>
<span data-ttu-id="48d18-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="48d18-112">The Application Gateway</span></span>

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

### <span data-ttu-id="48d18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48d18-113">-DefaultProfile</span></span>
<span data-ttu-id="48d18-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="48d18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48d18-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="48d18-115">-StatusCode</span></span>
<span data-ttu-id="48d18-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="48d18-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="48d18-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48d18-117">CommonParameters</span></span>
<span data-ttu-id="48d18-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48d18-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48d18-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48d18-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48d18-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48d18-120">INPUTS</span></span>

### <span data-ttu-id="48d18-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="48d18-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="48d18-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48d18-122">OUTPUTS</span></span>

### <span data-ttu-id="48d18-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="48d18-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="48d18-124">NOTES</span></span>

## <span data-ttu-id="48d18-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48d18-125">RELATED LINKS</span></span>

[<span data-ttu-id="48d18-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48d18-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48d18-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="48d18-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="48d18-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
