---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 4c06b78062500ddb5c33353c00814a46e919bd8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987720"
---
# <span data-ttu-id="1ec77-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1ec77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ec77-102">SYNOPSIS</span></span>
<span data-ttu-id="1ec77-103">Обновляет пользовательскую ошибку в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="1ec77-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="1ec77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1ec77-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ec77-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ec77-105">DESCRIPTION</span></span>
<span data-ttu-id="1ec77-106">**Cmdlet Set-AzApplicationGatewayCustomError** обновляет пользовательскую ошибку в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="1ec77-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="1ec77-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1ec77-107">EXAMPLES</span></span>

### <span data-ttu-id="1ec77-108">Пример 1. Обновление настраиваемой ошибки в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="1ec77-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="1ec77-109">Эта команда обновляет пользовательскую ошибку http-кода состояния 502 в шлюзе $appgw приложения и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="1ec77-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="1ec77-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ec77-110">PARAMETERS</span></span>

### <span data-ttu-id="1ec77-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ec77-111">-ApplicationGateway</span></span>
<span data-ttu-id="1ec77-112">Шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="1ec77-112">The Application Gateway</span></span>

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

### <span data-ttu-id="1ec77-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="1ec77-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="1ec77-114">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ec77-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1ec77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ec77-115">-DefaultProfile</span></span>
<span data-ttu-id="1ec77-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1ec77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ec77-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1ec77-117">-StatusCode</span></span>
<span data-ttu-id="1ec77-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1ec77-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="1ec77-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ec77-119">CommonParameters</span></span>
<span data-ttu-id="1ec77-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ec77-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ec77-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ec77-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ec77-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec77-122">INPUTS</span></span>

### <span data-ttu-id="1ec77-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1ec77-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1ec77-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1ec77-124">OUTPUTS</span></span>

### <span data-ttu-id="1ec77-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="1ec77-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1ec77-126">NOTES</span></span>

## <span data-ttu-id="1ec77-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ec77-127">RELATED LINKS</span></span>

[<span data-ttu-id="1ec77-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ec77-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ec77-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="1ec77-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="1ec77-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
