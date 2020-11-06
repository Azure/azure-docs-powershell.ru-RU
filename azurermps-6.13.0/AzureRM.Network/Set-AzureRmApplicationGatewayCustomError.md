---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 94a4b4dc41aa1ae7c2a7bb2596018382296f5f87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564204"
---
# <span data-ttu-id="13e90-101">Set-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13e90-101">Set-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="13e90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13e90-102">SYNOPSIS</span></span>
<span data-ttu-id="13e90-103">Обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="13e90-103">Updates a custom error in an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="13e90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13e90-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13e90-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e90-105">DESCRIPTION</span></span>
<span data-ttu-id="13e90-106">Командлет **Set-AzureRmApplicationGatewayCustomError** обновляет настраиваемое сообщение об ошибке в шлюзе приложений.</span><span class="sxs-lookup"><span data-stu-id="13e90-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in an application gateway.</span></span>

## <span data-ttu-id="13e90-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13e90-107">EXAMPLES</span></span>

### <span data-ttu-id="13e90-108">Пример 1: обновление настраиваемой ошибки в шлюзе приложений</span><span class="sxs-lookup"><span data-stu-id="13e90-108">Example 1: Updates custom error in an application gateway</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Set-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="13e90-109">Эта команда обновляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="13e90-109">This command updates the custom error of http status code 502 in the application gateway $appgw, and returns the updated gateway.</span></span>

## <span data-ttu-id="13e90-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13e90-110">PARAMETERS</span></span>

### <span data-ttu-id="13e90-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13e90-111">-ApplicationGateway</span></span>
<span data-ttu-id="13e90-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="13e90-112">The Application Gateway</span></span>

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

### <span data-ttu-id="13e90-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="13e90-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="13e90-114">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="13e90-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="13e90-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13e90-115">-DefaultProfile</span></span>
<span data-ttu-id="13e90-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13e90-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13e90-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="13e90-117">-StatusCode</span></span>
<span data-ttu-id="13e90-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="13e90-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="13e90-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13e90-119">CommonParameters</span></span>
<span data-ttu-id="13e90-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13e90-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13e90-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13e90-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13e90-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13e90-122">INPUTS</span></span>

### <span data-ttu-id="13e90-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13e90-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13e90-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13e90-124">OUTPUTS</span></span>

### <span data-ttu-id="13e90-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="13e90-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="13e90-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="13e90-126">NOTES</span></span>

## <span data-ttu-id="13e90-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13e90-127">RELATED LINKS</span></span>
