---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: f21c8303f1ec156132653a5d05c1149ef10a9ee7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727610"
---
# <span data-ttu-id="e0aff-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="e0aff-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="e0aff-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0aff-102">SYNOPSIS</span></span>
<span data-ttu-id="e0aff-103">Получает состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="e0aff-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="e0aff-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0aff-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0aff-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0aff-105">DESCRIPTION</span></span>
<span data-ttu-id="e0aff-106">Командлет **Get-AzCdnEndpointNameAvailability** получает состояние доступности конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="e0aff-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e0aff-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0aff-107">EXAMPLES</span></span>

## <span data-ttu-id="e0aff-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0aff-108">PARAMETERS</span></span>

### <span data-ttu-id="e0aff-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0aff-109">-DefaultProfile</span></span>
<span data-ttu-id="e0aff-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0aff-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0aff-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e0aff-111">-EndpointName</span></span>
<span data-ttu-id="e0aff-112">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="e0aff-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="e0aff-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0aff-113">CommonParameters</span></span>
<span data-ttu-id="e0aff-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0aff-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0aff-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0aff-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0aff-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0aff-116">INPUTS</span></span>

### <span data-ttu-id="e0aff-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0aff-117">None</span></span>

## <span data-ttu-id="e0aff-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0aff-118">OUTPUTS</span></span>

### <span data-ttu-id="e0aff-119">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="e0aff-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="e0aff-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0aff-120">NOTES</span></span>

## <span data-ttu-id="e0aff-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0aff-121">RELATED LINKS</span></span>
