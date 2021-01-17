---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323767"
---
# <span data-ttu-id="14293-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14293-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="14293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14293-102">SYNOPSIS</span></span>
<span data-ttu-id="14293-103">Обновляет пользовательскую ошибку в http-приложении шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="14293-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="14293-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="14293-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14293-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14293-105">DESCRIPTION</span></span>
<span data-ttu-id="14293-106">С **помощью cmdlet Set-AzApplicationGateWayCustomError** пользовательская ошибка обновляется в http-приложении шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="14293-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="14293-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="14293-107">EXAMPLES</span></span>

### <span data-ttu-id="14293-108">Пример 1. Обновление пользовательской ошибки http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="14293-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="14293-109">Эта команда обновляет пользовательскую ошибку http status code 502 в http-$listener 01 и возвращает обновленного слушателя.</span><span class="sxs-lookup"><span data-stu-id="14293-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="14293-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14293-110">PARAMETERS</span></span>

### <span data-ttu-id="14293-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="14293-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="14293-112">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="14293-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="14293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14293-113">-DefaultProfile</span></span>
<span data-ttu-id="14293-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14293-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14293-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="14293-115">-HttpListener</span></span>
<span data-ttu-id="14293-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="14293-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="14293-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="14293-117">-StatusCode</span></span>
<span data-ttu-id="14293-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="14293-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="14293-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14293-119">CommonParameters</span></span>
<span data-ttu-id="14293-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14293-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14293-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14293-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14293-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="14293-122">INPUTS</span></span>

### <span data-ttu-id="14293-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="14293-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="14293-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="14293-124">OUTPUTS</span></span>

### <span data-ttu-id="14293-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="14293-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="14293-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="14293-126">NOTES</span></span>

## <span data-ttu-id="14293-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14293-127">RELATED LINKS</span></span>

[<span data-ttu-id="14293-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14293-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="14293-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14293-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="14293-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="14293-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
