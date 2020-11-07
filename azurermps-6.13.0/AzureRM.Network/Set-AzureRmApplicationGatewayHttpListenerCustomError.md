---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: cb54299a1d3c06f9416ed574588a1bc77d9993a3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731964"
---
# <span data-ttu-id="7fe87-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="7fe87-101">Set-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="7fe87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7fe87-102">SYNOPSIS</span></span>
<span data-ttu-id="7fe87-103">Обновляет настраиваемое сообщение об ошибке в HTTP-прослушивателе шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7fe87-103">Updates a custom error in a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fe87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7fe87-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayHttpListenerCustomError -HttpListener <PSApplicationGatewayHttpListener>
 -StatusCode <String> -CustomErrorPageUrl <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fe87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe87-105">DESCRIPTION</span></span>
<span data-ttu-id="7fe87-106">Командлет **Set-AzureRmApplicationGatewayCustomError** обновляет настраиваемую ошибку в HTTP-прослушивателе шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7fe87-106">The **Set-AzureRmApplicationGatewayCustomError** cmdlet updates a custom error in a http listener of an application gateway.</span></span>

## <span data-ttu-id="7fe87-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7fe87-107">EXAMPLES</span></span>

### <span data-ttu-id="7fe87-108">Пример 1: обновление настраиваемой ошибки на основе прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="7fe87-108">Example 1: Updates a custom error from a http listener</span></span>
```powershell
PS C:\> $customError502Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/502.htm"
PS C:\> $updatedlistener = Set-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502 -CustomErrorPageUrl $customError502Url
```

<span data-ttu-id="7fe87-109">Эта команда обновляет настраиваемое сообщение об ошибке HTTP Code Status 502 в HTTP-прослушивателе $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="7fe87-109">This command updates the custom error of http status code 502 in the http listener $listener01, and returns the updated listener.</span></span>

## <span data-ttu-id="7fe87-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7fe87-110">PARAMETERS</span></span>

### <span data-ttu-id="7fe87-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="7fe87-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="7fe87-112">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7fe87-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fe87-113">-DefaultProfile</span></span>
<span data-ttu-id="7fe87-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7fe87-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe87-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="7fe87-115">-HttpListener</span></span>
<span data-ttu-id="7fe87-116">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="7fe87-116">The Application Gateway Http Listener</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fe87-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="7fe87-117">-StatusCode</span></span>
<span data-ttu-id="7fe87-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7fe87-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fe87-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fe87-119">CommonParameters</span></span>
<span data-ttu-id="7fe87-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7fe87-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7fe87-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fe87-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fe87-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7fe87-122">INPUTS</span></span>

### <span data-ttu-id="7fe87-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7fe87-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7fe87-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7fe87-124">OUTPUTS</span></span>

### <span data-ttu-id="7fe87-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7fe87-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7fe87-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="7fe87-126">NOTES</span></span>

## <span data-ttu-id="7fe87-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7fe87-127">RELATED LINKS</span></span>
