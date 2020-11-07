---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8a0ce9d3e2c2a5272f6544b5c98ef763b9b288ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730212"
---
# <span data-ttu-id="9788f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9788f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="9788f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9788f-102">SYNOPSIS</span></span>
<span data-ttu-id="9788f-103">Удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9788f-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9788f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9788f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9788f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9788f-105">DESCRIPTION</span></span>
<span data-ttu-id="9788f-106">Командлет **Remove-AzApplicationGatewayCustomError** удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9788f-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="9788f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9788f-107">EXAMPLES</span></span>

### <span data-ttu-id="9788f-108">Пример 1: Удаление настраиваемой ошибки из прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="9788f-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="9788f-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 из прослушивателя HTTP $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="9788f-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="9788f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9788f-110">PARAMETERS</span></span>

### <span data-ttu-id="9788f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9788f-111">-DefaultProfile</span></span>
<span data-ttu-id="9788f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9788f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9788f-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="9788f-113">-HttpListener</span></span>
<span data-ttu-id="9788f-114">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="9788f-114">The Application Gateway Http Listener</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9788f-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="9788f-115">-StatusCode</span></span>
<span data-ttu-id="9788f-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9788f-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="9788f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9788f-117">CommonParameters</span></span>
<span data-ttu-id="9788f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9788f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9788f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9788f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9788f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9788f-120">INPUTS</span></span>

### <span data-ttu-id="9788f-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="9788f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="9788f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9788f-122">OUTPUTS</span></span>

### <span data-ttu-id="9788f-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="9788f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="9788f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="9788f-124">NOTES</span></span>

## <span data-ttu-id="9788f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9788f-125">RELATED LINKS</span></span>

[<span data-ttu-id="9788f-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9788f-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9788f-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9788f-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="9788f-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="9788f-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
