---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 84c80ba4469d8003344d99b7dfbb89ff7d6660b2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326329"
---
# <span data-ttu-id="73d15-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="73d15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73d15-102">SYNOPSIS</span></span>
<span data-ttu-id="73d15-103">Возвращает настраиваемые ошибки из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="73d15-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="73d15-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73d15-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d15-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73d15-105">DESCRIPTION</span></span>
<span data-ttu-id="73d15-106">Для получения пользовательских ошибок от шлюза приложения возвращается **cmdlet Get-AzApplicationGatewayCustomError.**</span><span class="sxs-lookup"><span data-stu-id="73d15-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="73d15-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73d15-107">EXAMPLES</span></span>

### <span data-ttu-id="73d15-108">Пример 1. Возвращает настраиваемую ошибку в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="73d15-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="73d15-109">Эта команда возвращает пользовательскую ошибку http-кода состояния 502 из $appgw.</span><span class="sxs-lookup"><span data-stu-id="73d15-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="73d15-110">Пример 2. Возвращает список всех настраиваемой ошибки в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="73d15-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="73d15-111">Эта команда возвращает список всех настраиваемых ошибок в шлюзе $appgw.</span><span class="sxs-lookup"><span data-stu-id="73d15-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="73d15-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73d15-112">PARAMETERS</span></span>

### <span data-ttu-id="73d15-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73d15-113">-ApplicationGateway</span></span>
<span data-ttu-id="73d15-114">Шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="73d15-114">The Application Gateway</span></span>

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

### <span data-ttu-id="73d15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d15-115">-DefaultProfile</span></span>
<span data-ttu-id="73d15-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73d15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73d15-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="73d15-117">-StatusCode</span></span>
<span data-ttu-id="73d15-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="73d15-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="73d15-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d15-119">CommonParameters</span></span>
<span data-ttu-id="73d15-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d15-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d15-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73d15-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d15-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73d15-122">INPUTS</span></span>

### <span data-ttu-id="73d15-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="73d15-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="73d15-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73d15-124">OUTPUTS</span></span>

### <span data-ttu-id="73d15-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="73d15-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73d15-126">NOTES</span></span>

## <span data-ttu-id="73d15-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73d15-127">RELATED LINKS</span></span>

[<span data-ttu-id="73d15-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="73d15-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="73d15-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="73d15-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="73d15-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
