---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079452"
---
# <span data-ttu-id="7218c-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7218c-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7218c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7218c-102">SYNOPSIS</span></span>
<span data-ttu-id="7218c-103">Удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7218c-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7218c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7218c-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7218c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7218c-105">DESCRIPTION</span></span>
<span data-ttu-id="7218c-106">Командлет **Remove-AzApplicationGatewayCustomError** удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7218c-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="7218c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7218c-107">EXAMPLES</span></span>

### <span data-ttu-id="7218c-108">Пример 1: Удаление настраиваемой ошибки из прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="7218c-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="7218c-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 из прослушивателя HTTP $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="7218c-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="7218c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7218c-110">PARAMETERS</span></span>

### <span data-ttu-id="7218c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7218c-111">-DefaultProfile</span></span>
<span data-ttu-id="7218c-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7218c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7218c-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7218c-113">-HttpListener</span></span>
<span data-ttu-id="7218c-114">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="7218c-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="7218c-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7218c-115">-StatusCode</span></span>
<span data-ttu-id="7218c-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7218c-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="7218c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7218c-117">CommonParameters</span></span>
<span data-ttu-id="7218c-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7218c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7218c-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7218c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7218c-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7218c-120">INPUTS</span></span>

### <span data-ttu-id="7218c-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7218c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7218c-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7218c-122">OUTPUTS</span></span>

### <span data-ttu-id="7218c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="7218c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="7218c-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="7218c-124">NOTES</span></span>

## <span data-ttu-id="7218c-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7218c-125">RELATED LINKS</span></span>

[<span data-ttu-id="7218c-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7218c-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7218c-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7218c-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="7218c-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7218c-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)