---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 58cef33d6e7c05167376fe81a7c3b1e3f464f407
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902506"
---
# <span data-ttu-id="09f1e-101">Get-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="09f1e-101">Get-AzApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="09f1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="09f1e-103">Получает пользовательские ошибки из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="09f1e-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="09f1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09f1e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09f1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09f1e-105">DESCRIPTION</span></span>
<span data-ttu-id="09f1e-106">Командлет **Get-AzApplicationGatewayCustomError** получает пользовательские ошибки из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="09f1e-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="09f1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09f1e-107">EXAMPLES</span></span>

### <span data-ttu-id="09f1e-108">Пример 1: получение настраиваемой ошибки в HTTP-прослушивателе</span><span class="sxs-lookup"><span data-stu-id="09f1e-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="09f1e-109">Эта команда возвращает и возвращает ошибку 502 кода состояния HTTP из HTTP-прослушивателя $listener 01.</span><span class="sxs-lookup"><span data-stu-id="09f1e-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="09f1e-110">Пример 2: получение списка всех настраиваемых ошибок в прослушивателе HTTP</span><span class="sxs-lookup"><span data-stu-id="09f1e-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="09f1e-111">Эта команда возвращает список всех настраиваемых ошибок, возникающих в HTTP-прослушивателе $listener 01.</span><span class="sxs-lookup"><span data-stu-id="09f1e-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="09f1e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09f1e-112">PARAMETERS</span></span>

### <span data-ttu-id="09f1e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09f1e-113">-DefaultProfile</span></span>
<span data-ttu-id="09f1e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09f1e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09f1e-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="09f1e-115">-HttpListener</span></span>
<span data-ttu-id="09f1e-116">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="09f1e-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="09f1e-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="09f1e-117">-StatusCode</span></span>
<span data-ttu-id="09f1e-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="09f1e-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="09f1e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09f1e-119">CommonParameters</span></span>
<span data-ttu-id="09f1e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09f1e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09f1e-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09f1e-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09f1e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09f1e-122">INPUTS</span></span>

### <span data-ttu-id="09f1e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="09f1e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="09f1e-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09f1e-124">OUTPUTS</span></span>

### <span data-ttu-id="09f1e-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09f1e-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="09f1e-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="09f1e-126">NOTES</span></span>

## <span data-ttu-id="09f1e-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09f1e-127">RELATED LINKS</span></span>

[<span data-ttu-id="09f1e-128">Add-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="09f1e-128">Add-AzApplicationGatewayHttpListenerCustomError</span></span>](./Add-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="09f1e-129">Remove-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="09f1e-129">Remove-AzApplicationGatewayHttpListenerCustomError</span></span>](./Remove-AzApplicationGatewayHttpListenerCustomError.md)

[<span data-ttu-id="09f1e-130">Set-AzApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="09f1e-130">Set-AzApplicationGatewayHttpListenerCustomError</span></span>](./Set-AzApplicationGatewayHttpListenerCustomError.md)
