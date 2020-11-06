---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: cc1f6b487d0faf58999a0326a77e01bea74d8c91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560072"
---
# <span data-ttu-id="85a61-101">Remove-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="85a61-101">Remove-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="85a61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85a61-102">SYNOPSIS</span></span>
<span data-ttu-id="85a61-103">Удаляет настраиваемое сообщение об ошибке из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="85a61-103">Removes a custom error from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85a61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85a61-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayCustomError -StatusCode <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85a61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a61-105">DESCRIPTION</span></span>
<span data-ttu-id="85a61-106">Командлет **Remove-AzureRmApplicationGatewayCustomError** удаляет настраиваемую ошибку из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="85a61-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from an application gateway.</span></span>

## <span data-ttu-id="85a61-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85a61-107">EXAMPLES</span></span>

### <span data-ttu-id="85a61-108">Пример 1: Удаление настраиваемой ошибки из шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="85a61-108">Example 1: Removes custom error from an application gateway</span></span>
```
PS C:\> $updatedgateway = Remove-AzureRmApplicationGatewayCustomError -ApplicationGateway $appgw -StatusCode HttpStatus502
```

<span data-ttu-id="85a61-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 с $appgw шлюза приложений и возвращает обновленный шлюз.</span><span class="sxs-lookup"><span data-stu-id="85a61-109">This command removes the custom error of http status code 502 from the application gateway $appgw, and return the updated gateway.</span></span>

## <span data-ttu-id="85a61-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85a61-110">PARAMETERS</span></span>

### <span data-ttu-id="85a61-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85a61-111">-ApplicationGateway</span></span>
<span data-ttu-id="85a61-112">Шлюз приложений</span><span class="sxs-lookup"><span data-stu-id="85a61-112">The Application Gateway</span></span>

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

### <span data-ttu-id="85a61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85a61-113">-DefaultProfile</span></span>
<span data-ttu-id="85a61-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85a61-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85a61-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="85a61-115">-StatusCode</span></span>
<span data-ttu-id="85a61-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="85a61-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="85a61-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85a61-117">CommonParameters</span></span>
<span data-ttu-id="85a61-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85a61-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85a61-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85a61-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85a61-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85a61-120">INPUTS</span></span>

### <span data-ttu-id="85a61-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85a61-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85a61-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85a61-122">OUTPUTS</span></span>

### <span data-ttu-id="85a61-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="85a61-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="85a61-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="85a61-124">NOTES</span></span>

## <span data-ttu-id="85a61-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85a61-125">RELATED LINKS</span></span>
