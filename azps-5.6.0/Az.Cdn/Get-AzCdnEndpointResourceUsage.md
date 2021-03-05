---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: d39bd2d3a10f1ff8512b54cdf45902fb10f6810d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015411"
---
# <span data-ttu-id="35d96-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="35d96-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="35d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35d96-102">SYNOPSIS</span></span>
<span data-ttu-id="35d96-103">Возвращает использование ресурсов конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="35d96-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="35d96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35d96-104">SYNTAX</span></span>

### <span data-ttu-id="35d96-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35d96-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35d96-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35d96-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35d96-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35d96-107">DESCRIPTION</span></span>
<span data-ttu-id="35d96-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="35d96-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="35d96-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35d96-109">EXAMPLES</span></span>

### <span data-ttu-id="35d96-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="35d96-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="35d96-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="35d96-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="35d96-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35d96-112">PARAMETERS</span></span>

### <span data-ttu-id="35d96-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d96-113">-CdnEndpoint</span></span>
<span data-ttu-id="35d96-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="35d96-114">The CDN endpoint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35d96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d96-115">-DefaultProfile</span></span>
<span data-ttu-id="35d96-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="35d96-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35d96-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="35d96-117">-EndpointName</span></span>
<span data-ttu-id="35d96-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="35d96-118">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d96-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="35d96-119">-ProfileName</span></span>
<span data-ttu-id="35d96-120">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="35d96-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d96-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d96-121">-ResourceGroupName</span></span>
<span data-ttu-id="35d96-122">Группа ресурсов профиля СЕТИ CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="35d96-122">The resource group of the Azure CDN Profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35d96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d96-123">CommonParameters</span></span>
<span data-ttu-id="35d96-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d96-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35d96-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d96-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35d96-126">INPUTS</span></span>

### <span data-ttu-id="35d96-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="35d96-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="35d96-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35d96-128">OUTPUTS</span></span>

### <span data-ttu-id="35d96-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="35d96-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="35d96-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35d96-130">NOTES</span></span>

## <span data-ttu-id="35d96-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35d96-131">RELATED LINKS</span></span>
