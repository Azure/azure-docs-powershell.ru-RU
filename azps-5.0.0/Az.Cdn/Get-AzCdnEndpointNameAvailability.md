---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249545"
---
# <span data-ttu-id="2087a-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2087a-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="2087a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2087a-102">SYNOPSIS</span></span>
<span data-ttu-id="2087a-103">Получает состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="2087a-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="2087a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2087a-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2087a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2087a-105">DESCRIPTION</span></span>
<span data-ttu-id="2087a-106">Командлет **Get-AzCdnEndpointNameAvailability** получает состояние доступности конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="2087a-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="2087a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2087a-107">EXAMPLES</span></span>

## <span data-ttu-id="2087a-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2087a-108">PARAMETERS</span></span>

### <span data-ttu-id="2087a-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2087a-109">-DefaultProfile</span></span>
<span data-ttu-id="2087a-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2087a-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2087a-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2087a-111">-EndpointName</span></span>
<span data-ttu-id="2087a-112">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2087a-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="2087a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2087a-113">CommonParameters</span></span>
<span data-ttu-id="2087a-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2087a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2087a-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2087a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2087a-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2087a-116">INPUTS</span></span>

### <span data-ttu-id="2087a-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="2087a-117">None</span></span>

## <span data-ttu-id="2087a-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2087a-118">OUTPUTS</span></span>

### <span data-ttu-id="2087a-119">Microsoft. Azure. Commands. CDN. Models. Endpoint. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="2087a-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="2087a-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="2087a-120">NOTES</span></span>

## <span data-ttu-id="2087a-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2087a-121">RELATED LINKS</span></span>
