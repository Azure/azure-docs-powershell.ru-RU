---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 424dd1c13dbc6d860bec05da84704caba96735af
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066330"
---
# <span data-ttu-id="e88d0-101">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-101">Add-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e88d0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e88d0-102">SYNOPSIS</span></span>
<span data-ttu-id="e88d0-103">Добавляет настраиваемое сообщение об ошибке в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="e88d0-103">Adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e88d0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e88d0-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e88d0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88d0-105">DESCRIPTION</span></span>
<span data-ttu-id="e88d0-106">Командлет **Add-AzApplicationGatewayCustomError** Добавляет настраиваемое сообщение об ошибке в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="e88d0-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="e88d0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e88d0-107">EXAMPLES</span></span>

### <span data-ttu-id="e88d0-108">Пример 1: Добавление настраиваемой ошибки на уровне шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="e88d0-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="e88d0-109">Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="e88d0-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

### <span data-ttu-id="e88d0-110">Пример 2: Добавление настраиваемой ошибки на уровень прослушивателя шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="e88d0-110">Example 2: Adds custom error to application gateway listener level</span></span>
```powershell
PS C:\> $resourceGroup = "resourceGroupName"
PS C:\> $AppGWName = "applicationGatewayName"
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $listenerName = "listenerName"
PS C:\> $AppGw = Get-AzApplicationGateway -Name $AppGWName -ResourceGroupName $rg
PS C:\> $listener = Get-AzApplicationGatewayHttpListener -ApplicationGateway $AppGW -Name $listenerName
PS C:\> $updatedListener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url 
PS C:\> Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="e88d0-111">Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений на уровне прослушивателя и возвращают обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="e88d0-111">This command adds a custom error of http status code 502 to the application gateway $appgw at the listener level, and return the updated gateway.</span></span>

## <span data-ttu-id="e88d0-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e88d0-112">PARAMETERS</span></span>

### <span data-ttu-id="e88d0-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e88d0-113">-ApplicationGateway</span></span>
<span data-ttu-id="e88d0-114">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="e88d0-114">The Application Gateway</span></span>

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

### <span data-ttu-id="e88d0-115">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="e88d0-115">-CustomErrorPageUrl</span></span>
<span data-ttu-id="e88d0-116">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e88d0-116">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e88d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e88d0-117">-DefaultProfile</span></span>
<span data-ttu-id="e88d0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e88d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e88d0-119">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="e88d0-119">-StatusCode</span></span>
<span data-ttu-id="e88d0-120">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="e88d0-120">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="e88d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e88d0-121">CommonParameters</span></span>
<span data-ttu-id="e88d0-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e88d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e88d0-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e88d0-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e88d0-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e88d0-124">INPUTS</span></span>

### <span data-ttu-id="e88d0-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e88d0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e88d0-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e88d0-126">OUTPUTS</span></span>

### <span data-ttu-id="e88d0-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="e88d0-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="e88d0-128">NOTES</span></span>

## <span data-ttu-id="e88d0-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e88d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="e88d0-130">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-130">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e88d0-131">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-131">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e88d0-132">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-132">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="e88d0-133">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="e88d0-133">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
