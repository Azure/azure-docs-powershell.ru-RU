---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobehealthresponsematch
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeHealthResponseMatch.md
ms.openlocfilehash: 3306bdeb37271072b5d7e1054286f5fd9d460403
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565475"
---
# <span data-ttu-id="1cb28-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1cb28-101">New-AzureRmApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1cb28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1cb28-102">SYNOPSIS</span></span>
<span data-ttu-id="1cb28-103">Создание ответа на запрос проверки работоспособности, который используется зондом проверки работоспособности для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="1cb28-103">Creates a health probe response match used by Health Probe for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cb28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1cb28-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeHealthResponseMatch [-Body <String>]
 [-StatusCode <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cb28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb28-105">DESCRIPTION</span></span>
<span data-ttu-id="1cb28-106">Командлет **Add-AzureRmApplicationGatewayProbeHealthResponseMatch** создает ответ на проверку работоспособности, который используется зондом проверки работоспособности для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="1cb28-106">**The Add-AzureRmApplicationGatewayProbeHealthResponseMatch** cmdlet creates a health probe response match used by Health Probe for an application gateway.</span></span>

## <span data-ttu-id="1cb28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1cb28-107">EXAMPLES</span></span>

### <span data-ttu-id="1cb28-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1cb28-108">Example 1</span></span>
```
PS C:\>$responsematch = New-AzureRmApplicationGatewayProbeHealthResponseMatch -Body "helloworld" -StatusCode "200-399","503"
```

<span data-ttu-id="1cb28-109">Эта команда создает ответ на запрос о работоспособности, который можно передать в ProbeConfig в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="1cb28-109">This command creates a health response match which can be passed to ProbeConfig as a parameter.</span></span>

## <span data-ttu-id="1cb28-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1cb28-110">PARAMETERS</span></span>

### <span data-ttu-id="1cb28-111">-Body</span><span class="sxs-lookup"><span data-stu-id="1cb28-111">-Body</span></span>
<span data-ttu-id="1cb28-112">Текст, который должен содержаться в ответе работоспособности.</span><span class="sxs-lookup"><span data-stu-id="1cb28-112">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1cb28-113">Пустое значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1cb28-113">Default value is empty</span></span>

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

### <span data-ttu-id="1cb28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cb28-114">-DefaultProfile</span></span>
<span data-ttu-id="1cb28-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1cb28-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cb28-116">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="1cb28-116">-StatusCode</span></span>
<span data-ttu-id="1cb28-117">Допустимые диапазоны работоспособных кодов состояния. Диапазон работоспособных кодов состояния по умолчанию составляет 200-399</span><span class="sxs-lookup"><span data-stu-id="1cb28-117">Allowed ranges of healthy status codes.Default range of healthy status codes is 200 - 399</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cb28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cb28-118">CommonParameters</span></span>
<span data-ttu-id="1cb28-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1cb28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cb28-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cb28-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cb28-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1cb28-121">INPUTS</span></span>

### <span data-ttu-id="1cb28-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="1cb28-122">None</span></span>

## <span data-ttu-id="1cb28-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1cb28-123">OUTPUTS</span></span>

### <span data-ttu-id="1cb28-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbeHealthResponseMatch</span><span class="sxs-lookup"><span data-stu-id="1cb28-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch</span></span>

## <span data-ttu-id="1cb28-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="1cb28-125">NOTES</span></span>

## <span data-ttu-id="1cb28-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1cb28-126">RELATED LINKS</span></span>

