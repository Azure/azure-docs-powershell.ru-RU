---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 828b5e02b73a454a2b2023c0f084d4e1c90074fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001219"
---
# <span data-ttu-id="65887-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="65887-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="65887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65887-102">SYNOPSIS</span></span>
<span data-ttu-id="65887-103">Возвращает пользовательские ошибки http-прослушивание шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="65887-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="65887-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="65887-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="65887-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="65887-105">DESCRIPTION</span></span>
<span data-ttu-id="65887-106">С **помощью cmdlet Get-AzApplicationGateWayCustomError** пользовательская ошибка возвращается http-слушателем шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="65887-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="65887-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="65887-107">EXAMPLES</span></span>

### <span data-ttu-id="65887-108">Пример 1. Возвращает настраиваемую ошибку в http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="65887-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="65887-109">Эта команда получает и возвращает пользовательскую ошибку http-кода состояния 502 от программы http listener $listener 01.</span><span class="sxs-lookup"><span data-stu-id="65887-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="65887-110">Пример 2. Список всех пользовательских ошибок http-прослушивание</span><span class="sxs-lookup"><span data-stu-id="65887-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="65887-111">Эта команда возвращает список всех пользовательских ошибок http-$listener 01.</span><span class="sxs-lookup"><span data-stu-id="65887-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="65887-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="65887-112">PARAMETERS</span></span>

### <span data-ttu-id="65887-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65887-113">-DefaultProfile</span></span>
<span data-ttu-id="65887-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="65887-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65887-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="65887-115">-HttpListener</span></span>
<span data-ttu-id="65887-116">The Application Gateway Http Listener</span><span class="sxs-lookup"><span data-stu-id="65887-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="65887-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="65887-117">-StatusCode</span></span>
<span data-ttu-id="65887-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="65887-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65887-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65887-119">CommonParameters</span></span>
<span data-ttu-id="65887-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65887-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65887-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="65887-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65887-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="65887-122">INPUTS</span></span>

### <span data-ttu-id="65887-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="65887-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="65887-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="65887-124">OUTPUTS</span></span>

### <span data-ttu-id="65887-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="65887-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="65887-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="65887-126">NOTES</span></span>

## <span data-ttu-id="65887-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="65887-127">RELATED LINKS</span></span>

[<span data-ttu-id="65887-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="65887-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="65887-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="65887-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="65887-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="65887-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
