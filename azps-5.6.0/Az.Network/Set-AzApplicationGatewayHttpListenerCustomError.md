---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 63d90b646b639d7978dfbf734256976f423a3092
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953763"
---
# <span data-ttu-id="e546e-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e546e-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="e546e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e546e-102">SYNOPSIS</span></span>
<span data-ttu-id="e546e-103">Обновляет пользовательскую ошибку в http-приложении шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e546e-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="e546e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e546e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e546e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e546e-105">DESCRIPTION</span></span>
<span data-ttu-id="e546e-106">С **помощью cmdlet Set-AzApplicationGateWayCustomError** пользовательская ошибка обновляется в http-приложении шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e546e-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="e546e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e546e-107">EXAMPLES</span></span>

### <span data-ttu-id="e546e-108">Пример 1. Обновление пользовательской ошибки http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="e546e-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e546e-109">Эта команда обновляет пользовательскую ошибку http status code 502 в http listener $listener 01 и возвращает обновленного слушателя.</span><span class="sxs-lookup"><span data-stu-id="e546e-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="e546e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e546e-110">PARAMETERS</span></span>

### <span data-ttu-id="e546e-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e546e-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e546e-112">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e546e-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e546e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e546e-113">-DefaultProfile</span></span>
<span data-ttu-id="e546e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e546e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e546e-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="e546e-115">-HttpListener</span></span>
<span data-ttu-id="e546e-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="e546e-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="e546e-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e546e-117">-StatusCode</span></span>
<span data-ttu-id="e546e-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e546e-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e546e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e546e-119">CommonParameters</span></span>
<span data-ttu-id="e546e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e546e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e546e-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e546e-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e546e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e546e-122">INPUTS</span></span>

### <span data-ttu-id="e546e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="e546e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="e546e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e546e-124">OUTPUTS</span></span>

### <span data-ttu-id="e546e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e546e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e546e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e546e-126">NOTES</span></span>

## <span data-ttu-id="e546e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e546e-127">RELATED LINKS</span></span>

[<span data-ttu-id="e546e-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e546e-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e546e-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e546e-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="e546e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="e546e-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
