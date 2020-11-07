---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 8718d79abef18217a727916d36c09e19de2a2de4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902585"
---
# <span data-ttu-id="67f0d-101">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="67f0d-101">Add-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="67f0d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="67f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="67f0d-103">Добавляет настраиваемое сообщение об ошибке в HTTP-прослушиватель шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67f0d-103">Adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="67f0d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="67f0d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="67f0d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="67f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="67f0d-106">Командлет **Add-AzApplicationGatewayCustomError** добавляет настраиваемую ошибку в HTTP-прослушиватель шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67f0d-106">The **Add-AzApplicationGatewayCustomError** cmdlet adds a custom error to a http listener of an application gateway.</span></span>

## <span data-ttu-id="67f0d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="67f0d-107">EXAMPLES</span></span>

### <span data-ttu-id="67f0d-108">Пример 1: Добавление настраиваемой ошибки на уровень прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="67f0d-108">Example 1: Adds custom error to http listener level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Add-AzApplicationGatewayHttpListenerCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="67f0d-109">Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в HTTP-прослушиватель $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="67f0d-109">This command adds a custom error of http status code 502 to the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="67f0d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="67f0d-110">PARAMETERS</span></span>

### <span data-ttu-id="67f0d-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="67f0d-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="67f0d-112">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67f0d-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="67f0d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67f0d-113">-DefaultProfile</span></span>
<span data-ttu-id="67f0d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="67f0d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67f0d-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="67f0d-115">-HttpListener</span></span>
<span data-ttu-id="67f0d-116">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="67f0d-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="67f0d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="67f0d-117">-StatusCode</span></span>
<span data-ttu-id="67f0d-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="67f0d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="67f0d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67f0d-119">CommonParameters</span></span>
<span data-ttu-id="67f0d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="67f0d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67f0d-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67f0d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67f0d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="67f0d-122">INPUTS</span></span>

### <span data-ttu-id="67f0d-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="67f0d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="67f0d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="67f0d-124">OUTPUTS</span></span>

### <span data-ttu-id="67f0d-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="67f0d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="67f0d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="67f0d-126">NOTES</span></span>

## <span data-ttu-id="67f0d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="67f0d-127">RELATED LINKS</span></span>

[<span data-ttu-id="67f0d-128">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="67f0d-128">Get-AzApplicationGatewayHttpListenerCustomError</span></span>](./Get-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="67f0d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="67f0d-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="67f0d-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="67f0d-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
