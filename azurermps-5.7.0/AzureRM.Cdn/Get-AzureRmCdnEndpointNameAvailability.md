---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnEndpointNameAvailability.md
ms.openlocfilehash: bf202a971497a9c43f7ed3731b7c53bc12e58d73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559263"
---
# <span data-ttu-id="01d28-101">Get-AzureRmCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="01d28-101">Get-AzureRmCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="01d28-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01d28-102">SYNOPSIS</span></span>
<span data-ttu-id="01d28-103">Получает состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="01d28-103">Gets availability status of the CDN endpoint.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01d28-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01d28-104">SYNTAX</span></span>

```
Get-AzureRmCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01d28-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01d28-105">DESCRIPTION</span></span>
<span data-ttu-id="01d28-106">Командлет **Get-AzureRmCdnEndpointNameAvailability** получает состояние доступности конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="01d28-106">The **Get-AzureRmCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="01d28-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01d28-107">EXAMPLES</span></span>

## <span data-ttu-id="01d28-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01d28-108">PARAMETERS</span></span>

### <span data-ttu-id="01d28-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01d28-109">-DefaultProfile</span></span>
<span data-ttu-id="01d28-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="01d28-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01d28-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="01d28-111">-EndpointName</span></span>
<span data-ttu-id="01d28-112">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="01d28-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="01d28-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01d28-113">CommonParameters</span></span>
<span data-ttu-id="01d28-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01d28-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01d28-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01d28-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01d28-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01d28-116">INPUTS</span></span>

### <span data-ttu-id="01d28-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="01d28-117">None</span></span>
<span data-ttu-id="01d28-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="01d28-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01d28-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01d28-119">OUTPUTS</span></span>

### <span data-ttu-id="01d28-120">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="01d28-120">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="01d28-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="01d28-121">NOTES</span></span>

## <span data-ttu-id="01d28-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01d28-122">RELATED LINKS</span></span>

