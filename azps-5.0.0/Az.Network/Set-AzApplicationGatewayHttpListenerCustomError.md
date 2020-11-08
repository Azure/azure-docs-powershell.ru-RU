---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 3f53bd59e85fa9dac03a99d7e192ce51325ca6a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249625"
---
# <span data-ttu-id="b0d5c-101">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b0d5c-101">Set-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="b0d5c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b0d5c-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d5c-103">Обновляет настраиваемое сообщение об ошибке в HTTP-прослушивателе шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-103">Updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="b0d5c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b0d5c-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b0d5c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0d5c-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d5c-106">Командлет **Set-AzApplicationGatewayCustomError** обновляет настраиваемую ошибку в HTTP-прослушивателе шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="b0d5c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b0d5c-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d5c-108">Пример 1: обновление настраиваемой ошибки на основе прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="b0d5c-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="b0d5c-109">Эта команда обновляет настраиваемое сообщение об ошибке HTTP Code Status 502 в HTTP-прослушивателе $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="b0d5c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b0d5c-110">PARAMETERS</span></span>

### <span data-ttu-id="b0d5c-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="b0d5c-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="b0d5c-112">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b0d5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d5c-113">-DefaultProfile</span></span>
<span data-ttu-id="b0d5c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d5c-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="b0d5c-115">-HttpListener</span></span>
<span data-ttu-id="b0d5c-116">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="b0d5c-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="b0d5c-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b0d5c-117">-StatusCode</span></span>
<span data-ttu-id="b0d5c-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b0d5c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d5c-119">CommonParameters</span></span>
<span data-ttu-id="b0d5c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b0d5c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d5c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d5c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d5c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b0d5c-122">INPUTS</span></span>

### <span data-ttu-id="b0d5c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b0d5c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b0d5c-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0d5c-124">OUTPUTS</span></span>

### <span data-ttu-id="b0d5c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b0d5c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b0d5c-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b0d5c-126">NOTES</span></span>

## <span data-ttu-id="b0d5c-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0d5c-127">RELATED LINKS</span></span>

[<span data-ttu-id="b0d5c-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b0d5c-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b0d5c-129">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b0d5c-129">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="b0d5c-130">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="b0d5c-130">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)
