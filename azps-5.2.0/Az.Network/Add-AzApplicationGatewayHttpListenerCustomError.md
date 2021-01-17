---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d810afe9f5fcf2a1377f55ffe0822d3e71ee409f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410655"
---
# <span data-ttu-id="3cf74-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3cf74-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="3cf74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cf74-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf74-103">Добавляет пользовательскую ошибку в http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf74-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="3cf74-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3cf74-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3cf74-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3cf74-105">DESCRIPTION</span></span>
<span data-ttu-id="3cf74-106">С **помощью cmdlet Add-AzApplicationGatewayCustomError** пользовательская ошибка добавляется к http-слушателю шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf74-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="3cf74-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3cf74-107">EXAMPLES</span></span>

### <span data-ttu-id="3cf74-108">Пример 1. Добавляет настраиваемую ошибку на уровень http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="3cf74-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="3cf74-109">Эта команда добавляет пользовательскую ошибку http status code 502 в http listener $listener 01 и возвращает обновленного слушателя.</span><span class="sxs-lookup"><span data-stu-id="3cf74-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="3cf74-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cf74-110">PARAMETERS</span></span>

### <span data-ttu-id="3cf74-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="3cf74-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="3cf74-112">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf74-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3cf74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf74-113">-DefaultProfile</span></span>
<span data-ttu-id="3cf74-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf74-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cf74-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="3cf74-115">-HttpListener</span></span>
<span data-ttu-id="3cf74-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="3cf74-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="3cf74-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="3cf74-117">-StatusCode</span></span>
<span data-ttu-id="3cf74-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="3cf74-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="3cf74-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf74-119">CommonParameters</span></span>
<span data-ttu-id="3cf74-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf74-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf74-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf74-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf74-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3cf74-122">INPUTS</span></span>

### <span data-ttu-id="3cf74-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3cf74-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3cf74-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3cf74-124">OUTPUTS</span></span>

### <span data-ttu-id="3cf74-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="3cf74-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="3cf74-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3cf74-126">NOTES</span></span>

## <span data-ttu-id="3cf74-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3cf74-127">RELATED LINKS</span></span>

[<span data-ttu-id="3cf74-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3cf74-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="3cf74-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3cf74-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="3cf74-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="3cf74-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
