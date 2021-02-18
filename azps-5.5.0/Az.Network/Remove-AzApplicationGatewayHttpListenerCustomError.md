---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 82675befb6a900bacdead036f323959e1e7a72a9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223692"
---
# <span data-ttu-id="d7f0f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d7f0f-101">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="d7f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d7f0f-103">Удаляет пользовательскую ошибку http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-103">Removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="d7f0f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d7f0f-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d7f0f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d7f0f-106">С **помощью cmdlet Remove-AzApplicationGateWayCustomError** пользовательская ошибка удаляется из http-слушателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-106">The **Remove-AzApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="d7f0f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d7f0f-107">EXAMPLES</span></span>

### <span data-ttu-id="d7f0f-108">Пример 1. Удаление настраиваемой ошибки http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="d7f0f-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="d7f0f-109">Эта команда удаляет пользовательскую ошибку http status code 502 из программы http listener $listener 01 и возвращает обновленного слушателя.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="d7f0f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-110">PARAMETERS</span></span>

### <span data-ttu-id="d7f0f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7f0f-111">-DefaultProfile</span></span>
<span data-ttu-id="d7f0f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7f0f-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="d7f0f-113">-HttpListener</span></span>
<span data-ttu-id="d7f0f-114">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="d7f0f-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="d7f0f-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="d7f0f-115">-StatusCode</span></span>
<span data-ttu-id="d7f0f-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="d7f0f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7f0f-117">CommonParameters</span></span>
<span data-ttu-id="d7f0f-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7f0f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7f0f-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7f0f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7f0f-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-120">INPUTS</span></span>

### <span data-ttu-id="d7f0f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="d7f0f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="d7f0f-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d7f0f-122">OUTPUTS</span></span>

### <span data-ttu-id="d7f0f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="d7f0f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="d7f0f-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d7f0f-124">NOTES</span></span>

## <span data-ttu-id="d7f0f-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7f0f-125">RELATED LINKS</span></span>

[<span data-ttu-id="d7f0f-126">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d7f0f-126">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d7f0f-127">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d7f0f-127">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="d7f0f-128">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="d7f0f-128">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
