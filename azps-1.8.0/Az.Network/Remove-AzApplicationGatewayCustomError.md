---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c92c3c6b66e1b1208c7a0425b27a7e966bf6689
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730221"
---
# <span data-ttu-id="0bec7-101">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-101">Remove-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0bec7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bec7-102">SYNOPSIS</span></span>
<span data-ttu-id="0bec7-103">Удаляет настраиваемое сообщение об ошибке из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0bec7-103">Removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="0bec7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bec7-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bec7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bec7-105">DESCRIPTION</span></span>
<span data-ttu-id="0bec7-106">Командлет **Remove-AzApplicationGatewayCustomError** удаляет настраиваемую ошибку из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="0bec7-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="0bec7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bec7-107">EXAMPLES</span></span>

### <span data-ttu-id="0bec7-108">Пример 1: Удаление настраиваемой ошибки из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="0bec7-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="0bec7-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 с $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="0bec7-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="0bec7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bec7-110">PARAMETERS</span></span>

### <span data-ttu-id="0bec7-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bec7-111">-ApplicationGateway</span></span>
<span data-ttu-id="0bec7-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="0bec7-112">The Application Gateway</span></span>

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

### <span data-ttu-id="0bec7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bec7-113">-DefaultProfile</span></span>
<span data-ttu-id="0bec7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bec7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bec7-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="0bec7-115">-StatusCode</span></span>
<span data-ttu-id="0bec7-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="0bec7-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="0bec7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bec7-117">CommonParameters</span></span>
<span data-ttu-id="0bec7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bec7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bec7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bec7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bec7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bec7-120">INPUTS</span></span>

### <span data-ttu-id="0bec7-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0bec7-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0bec7-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bec7-122">OUTPUTS</span></span>

### <span data-ttu-id="0bec7-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="0bec7-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bec7-124">NOTES</span></span>

## <span data-ttu-id="0bec7-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bec7-125">RELATED LINKS</span></span>

[<span data-ttu-id="0bec7-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0bec7-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0bec7-128">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-128">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="0bec7-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="0bec7-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
