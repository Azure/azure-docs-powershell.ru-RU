---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560064"
---
# <span data-ttu-id="8a4fe-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="8a4fe-101">Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="8a4fe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a4fe-102">SYNOPSIS</span></span>
<span data-ttu-id="8a4fe-103">Удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-103">Removes a custom error from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a4fe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a4fe-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a4fe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a4fe-105">DESCRIPTION</span></span>
<span data-ttu-id="8a4fe-106">Командлет **Remove-AzureRmApplicationGatewayCustomError** удаляет настраиваемую ошибку из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-106">The **Remove-AzureRmApplicationGatewayCustomError** cmdlet removes a custom error from a http listener of an application gateway.</span></span>

## <span data-ttu-id="8a4fe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a4fe-107">EXAMPLES</span></span>

### <span data-ttu-id="8a4fe-108">Пример 1: Удаление настраиваемой ошибки из прослушивателя HTTP</span><span class="sxs-lookup"><span data-stu-id="8a4fe-108">Example 1: Removes custom error from a http listener</span></span>
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="8a4fe-109">Эта команда удаляет настраиваемую ошибку кода состояния HTTP 502 из прослушивателя HTTP $listener 01 и возвращает обновленный прослушиватель.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-109">This command removes the custom error of http status code 502 from the http listener $listener01, and return the updated listener.</span></span>

## <span data-ttu-id="8a4fe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a4fe-110">PARAMETERS</span></span>

### <span data-ttu-id="8a4fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a4fe-111">-DefaultProfile</span></span>
<span data-ttu-id="8a4fe-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a4fe-113">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="8a4fe-113">-HttpListener</span></span>
<span data-ttu-id="8a4fe-114">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="8a4fe-114">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="8a4fe-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="8a4fe-115">-StatusCode</span></span>
<span data-ttu-id="8a4fe-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="8a4fe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a4fe-117">CommonParameters</span></span>
<span data-ttu-id="8a4fe-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a4fe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8a4fe-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a4fe-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a4fe-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a4fe-120">INPUTS</span></span>

### <span data-ttu-id="8a4fe-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8a4fe-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="8a4fe-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a4fe-122">OUTPUTS</span></span>

### <span data-ttu-id="8a4fe-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="8a4fe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="8a4fe-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a4fe-124">NOTES</span></span>

## <span data-ttu-id="8a4fe-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a4fe-125">RELATED LINKS</span></span>
