---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 459880d6ab771e48a9fe2d5ba69abffae35db7b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996568"
---
# <span data-ttu-id="b073d-101">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-101">Get-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b073d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b073d-102">SYNOPSIS</span></span>
<span data-ttu-id="b073d-103">Возвращает настраиваемые ошибки из шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b073d-103">Gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="b073d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b073d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayCustomError [-StatusCode <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b073d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b073d-105">DESCRIPTION</span></span>
<span data-ttu-id="b073d-106">Для получения пользовательских ошибок от шлюза приложения возвращается **cmdlet Get-AzApplicationGatewayCustomError.**</span><span class="sxs-lookup"><span data-stu-id="b073d-106">The **Get-AzApplicationGatewayCustomError** cmdlet gets custom error(s) from an application gateway.</span></span>

## <span data-ttu-id="b073d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b073d-107">EXAMPLES</span></span>

### <span data-ttu-id="b073d-108">Пример 1. Возвращает настраиваемую ошибку в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="b073d-108">Example 1: Gets a custom error in an application gateway</span></span>
```powershell
PS C:\> $ce = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="b073d-109">Эта команда возвращает пользовательскую ошибку http-кода состояния 502 из $appgw.</span><span class="sxs-lookup"><span data-stu-id="b073d-109">This command gets and returns the custom error of http status code 502 from the application gateway $appgw.</span></span>

### <span data-ttu-id="b073d-110">Пример 2. Возвращает список всех настраиваемой ошибки в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="b073d-110">Example 2: Gets the list of all custom errors in an application gateway</span></span>
```powershell
PS C:\> $ces = Get-AzApplicationGatewayCustomError -ApplicationGateway $appgw
```

<span data-ttu-id="b073d-111">Эта команда возвращает список всех настраиваемых ошибок в шлюзе $appgw.</span><span class="sxs-lookup"><span data-stu-id="b073d-111">This command gets and returns the list of all custom errors from the application gateway $appgw.</span></span>

## <span data-ttu-id="b073d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b073d-112">PARAMETERS</span></span>

### <span data-ttu-id="b073d-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b073d-113">-ApplicationGateway</span></span>
<span data-ttu-id="b073d-114">Шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="b073d-114">The Application Gateway</span></span>

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

### <span data-ttu-id="b073d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b073d-115">-DefaultProfile</span></span>
<span data-ttu-id="b073d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b073d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b073d-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="b073d-117">-StatusCode</span></span>
<span data-ttu-id="b073d-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="b073d-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="b073d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b073d-119">CommonParameters</span></span>
<span data-ttu-id="b073d-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b073d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b073d-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b073d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b073d-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b073d-122">INPUTS</span></span>

### <span data-ttu-id="b073d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b073d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b073d-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b073d-124">OUTPUTS</span></span>

### <span data-ttu-id="b073d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="b073d-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b073d-126">NOTES</span></span>

## <span data-ttu-id="b073d-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b073d-127">RELATED LINKS</span></span>

[<span data-ttu-id="b073d-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b073d-129">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-129">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b073d-130">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-130">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="b073d-131">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="b073d-131">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
