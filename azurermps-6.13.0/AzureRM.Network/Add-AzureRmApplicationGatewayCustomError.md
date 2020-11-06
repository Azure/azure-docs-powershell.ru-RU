---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: b56c358a208683e513844e36e561efa9e76cbede
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560119"
---
# <span data-ttu-id="106d6-101">Add-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="106d6-101">Add-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="106d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="106d6-102">SYNOPSIS</span></span>
<span data-ttu-id="106d6-103">Добавляет настраиваемое сообщение об ошибке в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="106d6-103">Adds a custom error to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="106d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="106d6-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayCustomError -ApplicationGateway <PSApplicationGateway> -StatusCode <String>
 -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="106d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="106d6-105">DESCRIPTION</span></span>
<span data-ttu-id="106d6-106">Командлет **Add-AzureRmApplicationGatewayCustomError** Добавляет настраиваемое сообщение об ошибке в шлюз приложений.</span><span class="sxs-lookup"><span data-stu-id="106d6-106">The **Add-AzureRmApplicationGatewayCustomError** cmdlet adds a custom error to an application gateway.</span></span>

## <span data-ttu-id="106d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="106d6-107">EXAMPLES</span></span>

### <span data-ttu-id="106d6-108">Пример 1: Добавление настраиваемой ошибки на уровне шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="106d6-108">Example 1: Adds custom error to application gateway level</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedgateway = Add-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="106d6-109">Эта команда добавляет настраиваемую ошибку кода состояния HTTP 502 в $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="106d6-109">This command adds a custom error of http status code 502 to the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="106d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="106d6-110">PARAMETERS</span></span>

### <span data-ttu-id="106d6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="106d6-111">-ApplicationGateway</span></span>
<span data-ttu-id="106d6-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="106d6-112">The Application Gateway</span></span>

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

### <span data-ttu-id="106d6-113">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="106d6-113">-CustomErrorPageUrl</span></span>
<span data-ttu-id="106d6-114">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="106d6-114">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="106d6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106d6-115">-DefaultProfile</span></span>
<span data-ttu-id="106d6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="106d6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106d6-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="106d6-117">-StatusCode</span></span>
<span data-ttu-id="106d6-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="106d6-118">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="106d6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106d6-119">CommonParameters</span></span>
<span data-ttu-id="106d6-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="106d6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106d6-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="106d6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106d6-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="106d6-122">INPUTS</span></span>

### <span data-ttu-id="106d6-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="106d6-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="106d6-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="106d6-124">OUTPUTS</span></span>

### <span data-ttu-id="106d6-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="106d6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="106d6-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="106d6-126">NOTES</span></span>

## <span data-ttu-id="106d6-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="106d6-127">RELATED LINKS</span></span>
