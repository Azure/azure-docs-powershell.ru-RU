---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98417028"
---
# <span data-ttu-id="bcee2-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bcee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcee2-102">SYNOPSIS</span></span>
<span data-ttu-id="bcee2-103">Обновляет пользовательскую ошибку в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="bcee2-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="bcee2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcee2-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcee2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcee2-105">DESCRIPTION</span></span>
<span data-ttu-id="bcee2-106">**Cmdlet Set-AzApplicationGatewayCustomError** обновляет пользовательскую ошибку в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="bcee2-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="bcee2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcee2-107">EXAMPLES</span></span>

### <span data-ttu-id="bcee2-108">Пример 1. Обновление настраиваемой ошибки в шлюзе приложения</span><span class="sxs-lookup"><span data-stu-id="bcee2-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="bcee2-109">Эта команда обновляет пользовательскую ошибку http-кода состояния 502 в шлюзе $appgw приложения и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="bcee2-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="bcee2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcee2-110">PARAMETERS</span></span>

### <span data-ttu-id="bcee2-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcee2-111">-ApplicationGateway</span></span>
<span data-ttu-id="bcee2-112">Шлюз приложения</span><span class="sxs-lookup"><span data-stu-id="bcee2-112">The Application Gateway</span></span>

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

### <span data-ttu-id="bcee2-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="bcee2-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="bcee2-114">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="bcee2-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bcee2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcee2-115">-DefaultProfile</span></span>
<span data-ttu-id="bcee2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcee2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcee2-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="bcee2-117">-StatusCode</span></span>
<span data-ttu-id="bcee2-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="bcee2-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="bcee2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcee2-119">CommonParameters</span></span>
<span data-ttu-id="bcee2-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcee2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcee2-121">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcee2-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcee2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcee2-122">INPUTS</span></span>

### <span data-ttu-id="bcee2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bcee2-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bcee2-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcee2-124">OUTPUTS</span></span>

### <span data-ttu-id="bcee2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="bcee2-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcee2-126">NOTES</span></span>

## <span data-ttu-id="bcee2-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcee2-127">RELATED LINKS</span></span>

[<span data-ttu-id="bcee2-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bcee2-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bcee2-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="bcee2-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="bcee2-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
