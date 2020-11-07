---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayCustomError.md
ms.openlocfilehash: a59646c6214b3c4372eef9def61f67fe4a5bd912
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903362"
---
# <span data-ttu-id="4ba6b-101">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-101">Set-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4ba6b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ba6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba6b-103">Обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-103">Updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="4ba6b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ba6b-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ba6b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba6b-105">DESCRIPTION</span></span>
<span data-ttu-id="4ba6b-106">Командлет **Set-AzApplicationGatewayCustomError** обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-106">The **Set-AzApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="4ba6b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ba6b-107">EXAMPLES</span></span>

### <span data-ttu-id="4ba6b-108">Пример 1: обновление настраиваемой ошибки в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="4ba6b-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="4ba6b-109">Эта команда обновляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="4ba6b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ba6b-110">PARAMETERS</span></span>

### <span data-ttu-id="4ba6b-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ba6b-111">-ApplicationGateway</span></span>
<span data-ttu-id="4ba6b-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="4ba6b-112">The Application Gateway</span></span>

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

### <span data-ttu-id="4ba6b-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="4ba6b-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="4ba6b-114">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4ba6b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba6b-115">-DefaultProfile</span></span>
<span data-ttu-id="4ba6b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba6b-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="4ba6b-117">-StatusCode</span></span>
<span data-ttu-id="4ba6b-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="4ba6b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba6b-119">CommonParameters</span></span>
<span data-ttu-id="4ba6b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba6b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ba6b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba6b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ba6b-122">INPUTS</span></span>

### <span data-ttu-id="4ba6b-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4ba6b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4ba6b-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ba6b-124">OUTPUTS</span></span>

### <span data-ttu-id="4ba6b-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="4ba6b-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ba6b-126">NOTES</span></span>

## <span data-ttu-id="4ba6b-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ba6b-127">RELATED LINKS</span></span>

[<span data-ttu-id="4ba6b-128">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-128">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ba6b-129">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-129">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ba6b-130">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-130">New-AzApplicationGatewayCustomError</span></span>](./New-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="4ba6b-131">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="4ba6b-131">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)
