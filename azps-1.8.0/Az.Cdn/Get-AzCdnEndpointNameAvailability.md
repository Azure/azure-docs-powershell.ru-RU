---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: ea7c714959616116ec8a0c66dbd1967a4cba73d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901466"
---
# <span data-ttu-id="56ff5-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="56ff5-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="56ff5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56ff5-102">SYNOPSIS</span></span>
<span data-ttu-id="56ff5-103">Получает состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="56ff5-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="56ff5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56ff5-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56ff5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ff5-105">DESCRIPTION</span></span>
<span data-ttu-id="56ff5-106">Командлет **Get-AzCdnEndpointNameAvailability** получает состояние доступности конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="56ff5-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="56ff5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56ff5-107">EXAMPLES</span></span>

## <span data-ttu-id="56ff5-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56ff5-108">PARAMETERS</span></span>

### <span data-ttu-id="56ff5-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ff5-109">-DefaultProfile</span></span>
<span data-ttu-id="56ff5-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56ff5-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56ff5-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="56ff5-111">-EndpointName</span></span>
<span data-ttu-id="56ff5-112">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="56ff5-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="56ff5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ff5-113">CommonParameters</span></span>
<span data-ttu-id="56ff5-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56ff5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ff5-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ff5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ff5-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56ff5-116">INPUTS</span></span>

### <span data-ttu-id="56ff5-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="56ff5-117">None</span></span>

## <span data-ttu-id="56ff5-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ff5-118">OUTPUTS</span></span>

### <span data-ttu-id="56ff5-119">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="56ff5-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="56ff5-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="56ff5-120">NOTES</span></span>

## <span data-ttu-id="56ff5-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56ff5-121">RELATED LINKS</span></span>
