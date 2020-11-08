---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 08447949836af59223572bac1b8fec54f3704d9d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244328"
---
# <span data-ttu-id="906cd-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="906cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="906cd-102">SYNOPSIS</span></span>
<span data-ttu-id="906cd-103">Обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="906cd-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="906cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="906cd-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="906cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="906cd-105">DESCRIPTION</span></span>
<span data-ttu-id="906cd-106">Командлет **Set-AzApplicationGatewayCustomError** обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="906cd-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="906cd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="906cd-107">EXAMPLES</span></span>

### <span data-ttu-id="906cd-108">Пример 1: обновление настраиваемой ошибки в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="906cd-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="906cd-109">Эта команда обновляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="906cd-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="906cd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="906cd-110">PARAMETERS</span></span>

### <span data-ttu-id="906cd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="906cd-111">-ApplicationGateway</span></span>
<span data-ttu-id="906cd-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="906cd-112">The Application Gateway</span></span>

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

### <span data-ttu-id="906cd-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="906cd-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="906cd-114">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="906cd-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="906cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="906cd-115">-DefaultProfile</span></span>
<span data-ttu-id="906cd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="906cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="906cd-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="906cd-117">-StatusCode</span></span>
<span data-ttu-id="906cd-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="906cd-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="906cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="906cd-119">CommonParameters</span></span>
<span data-ttu-id="906cd-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="906cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="906cd-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="906cd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="906cd-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="906cd-122">INPUTS</span></span>

### <span data-ttu-id="906cd-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="906cd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="906cd-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="906cd-124">OUTPUTS</span></span>

### <span data-ttu-id="906cd-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="906cd-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="906cd-126">NOTES</span></span>

## <span data-ttu-id="906cd-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="906cd-127">RELATED LINKS</span></span>

[<span data-ttu-id="906cd-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="906cd-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="906cd-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="906cd-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="906cd-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
