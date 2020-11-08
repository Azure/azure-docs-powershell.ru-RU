---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248347"
---
# <span data-ttu-id="09cd5-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="09cd5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="09cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="09cd5-103">Получает пользовательские ошибки из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="09cd5-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="09cd5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="09cd5-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09cd5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="09cd5-106">Командлет **Get-AzApplicationGatewayCustomError** получает пользовательские ошибки из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="09cd5-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="09cd5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="09cd5-107">EXAMPLES</span></span>

### <span data-ttu-id="09cd5-108">Пример 1: получение настраиваемой ошибки в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="09cd5-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="09cd5-109">Эта команда возвращает и возвращает ошибку 502 кода состояния HTTP из $appgw шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="09cd5-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="09cd5-110">Пример 2: получение списка всех настраиваемых ошибок в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="09cd5-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="09cd5-111">Эта команда возвращает список всех настраиваемых ошибок из $appgw шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="09cd5-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="09cd5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="09cd5-112">PARAMETERS</span></span>

### <span data-ttu-id="09cd5-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09cd5-113">-ApplicationGateway</span></span>
<span data-ttu-id="09cd5-114">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="09cd5-114">The Application Gateway</span></span>

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

### <span data-ttu-id="09cd5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09cd5-115">-DefaultProfile</span></span>
<span data-ttu-id="09cd5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="09cd5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09cd5-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="09cd5-117">-StatusCode</span></span>
<span data-ttu-id="09cd5-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="09cd5-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="09cd5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09cd5-119">CommonParameters</span></span>
<span data-ttu-id="09cd5-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="09cd5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09cd5-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09cd5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09cd5-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="09cd5-122">INPUTS</span></span>

### <span data-ttu-id="09cd5-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="09cd5-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="09cd5-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="09cd5-124">OUTPUTS</span></span>

### <span data-ttu-id="09cd5-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="09cd5-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="09cd5-126">NOTES</span></span>

## <span data-ttu-id="09cd5-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09cd5-127">RELATED LINKS</span></span>

[<span data-ttu-id="09cd5-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="09cd5-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="09cd5-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="09cd5-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="09cd5-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
