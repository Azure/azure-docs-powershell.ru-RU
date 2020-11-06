---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: 89e323bd8e8dedbaa3c7716a6c10119a6fb69365
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564304"
---
# <span data-ttu-id="16f24-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span><span class="sxs-lookup"><span data-stu-id="16f24-101">Get-AzureRmApplicationGatewayHttpListenerCustomError</span></span>

## <span data-ttu-id="16f24-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="16f24-102">SYNOPSIS</span></span>
<span data-ttu-id="16f24-103">Получает пользовательские ошибки из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="16f24-103">Gets custom error(s) from a http listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16f24-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="16f24-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListenerCustomError [-StatusCode <String>]
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16f24-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f24-105">DESCRIPTION</span></span>
<span data-ttu-id="16f24-106">Командлет **Get-AzureRmApplicationGatewayCustomError** получает пользовательские ошибки из HTTP-прослушивателя шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="16f24-106">The **Get-AzureRmApplicationGatewayCustomError** cmdlet gets custom error(s) from a http listener of an application gateway.</span></span>

## <span data-ttu-id="16f24-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="16f24-107">EXAMPLES</span></span>

### <span data-ttu-id="16f24-108">Пример 1: получение настраиваемой ошибки в HTTP-прослушивателе</span><span class="sxs-lookup"><span data-stu-id="16f24-108">Example 1: Gets a custom error in a http listener</span></span>
```powershell
PS C:\> $ce = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

<span data-ttu-id="16f24-109">Эта команда возвращает и возвращает ошибку 502 кода состояния HTTP из HTTP-прослушивателя $listener 01.</span><span class="sxs-lookup"><span data-stu-id="16f24-109">This command gets and returns the custom error of http status code 502 from the http listener $listener01.</span></span>

### <span data-ttu-id="16f24-110">Пример 2: получение списка всех настраиваемых ошибок в прослушивателе HTTP</span><span class="sxs-lookup"><span data-stu-id="16f24-110">Example 2: Gets the list of all custom errors in a http listener</span></span>
```powershell
PS C:\> $ces = Get-AzureRmApplicationGatewayCustomError -HttpListener $listener01
```

<span data-ttu-id="16f24-111">Эта команда возвращает список всех настраиваемых ошибок, возникающих в HTTP-прослушивателе $listener 01.</span><span class="sxs-lookup"><span data-stu-id="16f24-111">This command gets and returns the list of all custom errors from the http listener $listener01.</span></span>

## <span data-ttu-id="16f24-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="16f24-112">PARAMETERS</span></span>

### <span data-ttu-id="16f24-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16f24-113">-DefaultProfile</span></span>
<span data-ttu-id="16f24-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16f24-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16f24-115">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="16f24-115">-HttpListener</span></span>
<span data-ttu-id="16f24-116">Прослушиватель HTTP шлюза приложений</span><span class="sxs-lookup"><span data-stu-id="16f24-116">The Application Gateway Http Listener</span></span>

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

### <span data-ttu-id="16f24-117">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="16f24-117">-StatusCode</span></span>
<span data-ttu-id="16f24-118">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="16f24-118">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16f24-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16f24-119">CommonParameters</span></span>
<span data-ttu-id="16f24-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="16f24-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="16f24-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16f24-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16f24-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="16f24-122">INPUTS</span></span>

### <span data-ttu-id="16f24-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="16f24-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="16f24-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="16f24-124">OUTPUTS</span></span>

### <span data-ttu-id="16f24-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="16f24-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="16f24-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="16f24-126">NOTES</span></span>

## <span data-ttu-id="16f24-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16f24-127">RELATED LINKS</span></span>
