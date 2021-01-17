---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 91de215282dc05be2136237fa5fb2b244d7f0c4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98416071"
---
# <span data-ttu-id="1ecd8-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1ecd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ecd8-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecd8-103">Удаляет настраиваемую ошибку из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="1ecd8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ecd8-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecd8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecd8-105">DESCRIPTION</span></span>
<span data-ttu-id="1ecd8-106">**Cmdlet Remove-AzApplicationGatewayCustomError** удаляет настраиваемую ошибку из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="1ecd8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ecd8-107">EXAMPLES</span></span>

### <span data-ttu-id="1ecd8-108">Пример 1. Удаление настраиваемой ошибки из шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="1ecd8-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="1ecd8-109">Эта команда удаляет настраиваемую ошибку http-кода состояния 502 из $appgw приложения и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="1ecd8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ecd8-110">PARAMETERS</span></span>

### <span data-ttu-id="1ecd8-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ecd8-111">-ApplicationGateway</span></span>
<span data-ttu-id="1ecd8-112">Шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="1ecd8-112">The Application Gateway</span></span>

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

### <span data-ttu-id="1ecd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecd8-113">-DefaultProfile</span></span>
<span data-ttu-id="1ecd8-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ecd8-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1ecd8-115">-StatusCode</span></span>
<span data-ttu-id="1ecd8-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1ecd8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecd8-117">CommonParameters</span></span>
<span data-ttu-id="1ecd8-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ecd8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecd8-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecd8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecd8-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ecd8-120">INPUTS</span></span>

### <span data-ttu-id="1ecd8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ecd8-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ecd8-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ecd8-122">OUTPUTS</span></span>

### <span data-ttu-id="1ecd8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1ecd8-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ecd8-124">NOTES</span></span>

## <span data-ttu-id="1ecd8-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ecd8-125">RELATED LINKS</span></span>

[<span data-ttu-id="1ecd8-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ecd8-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ecd8-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ecd8-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ecd8-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
