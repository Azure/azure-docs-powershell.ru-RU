---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6BBD68B4-BCC6-479A-AA70-D4ED445CFB32
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointNameAvailability.md
ms.openlocfilehash: 09fd2e23cf8c91c2ffea1c10b5363011b9b189a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100215937"
---
# <span data-ttu-id="918c6-101">Get-AzCdnEndpointNameAvailability</span><span class="sxs-lookup"><span data-stu-id="918c6-101">Get-AzCdnEndpointNameAvailability</span></span>

## <span data-ttu-id="918c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="918c6-102">SYNOPSIS</span></span>
<span data-ttu-id="918c6-103">Состояние доступности конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="918c6-103">Gets availability status of the CDN endpoint.</span></span>

## <span data-ttu-id="918c6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="918c6-104">SYNTAX</span></span>

```
Get-AzCdnEndpointNameAvailability -EndpointName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="918c6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="918c6-105">DESCRIPTION</span></span>
<span data-ttu-id="918c6-106">Для получения состояния доступности конечной точки сети доставки содержимого (CDN) Azure возвращается состояние доступности для **cmdnEndpointNameAvailability.**</span><span class="sxs-lookup"><span data-stu-id="918c6-106">The **Get-AzCdnEndpointNameAvailability** cmdlet gets availability status of the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="918c6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="918c6-107">EXAMPLES</span></span>

## <span data-ttu-id="918c6-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="918c6-108">PARAMETERS</span></span>

### <span data-ttu-id="918c6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="918c6-109">-DefaultProfile</span></span>
<span data-ttu-id="918c6-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="918c6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="918c6-111">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="918c6-111">-EndpointName</span></span>
<span data-ttu-id="918c6-112">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="918c6-112">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="918c6-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="918c6-113">CommonParameters</span></span>
<span data-ttu-id="918c6-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="918c6-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="918c6-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="918c6-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="918c6-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="918c6-116">INPUTS</span></span>

### <span data-ttu-id="918c6-117">Нет</span><span class="sxs-lookup"><span data-stu-id="918c6-117">None</span></span>

## <span data-ttu-id="918c6-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="918c6-118">OUTPUTS</span></span>

### <span data-ttu-id="918c6-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="918c6-119">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="918c6-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="918c6-120">NOTES</span></span>

## <span data-ttu-id="918c6-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="918c6-121">RELATED LINKS</span></span>
