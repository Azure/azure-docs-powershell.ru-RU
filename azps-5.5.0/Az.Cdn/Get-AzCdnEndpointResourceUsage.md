---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnendpointresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnEndpointResourceUsage.md
ms.openlocfilehash: 7b8773f4e8e0f63404d81c56703181124f6f8ad0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239143"
---
# <span data-ttu-id="c823d-101">Get-AzCdnEndpointResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c823d-101">Get-AzCdnEndpointResourceUsage</span></span>

## <span data-ttu-id="c823d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c823d-102">SYNOPSIS</span></span>
<span data-ttu-id="c823d-103">Возвращает использование ресурсов конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="c823d-103">Gets the resource usage of a CDN endpoint.</span></span>

## <span data-ttu-id="c823d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c823d-104">SYNTAX</span></span>

### <span data-ttu-id="c823d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c823d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c823d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c823d-106">ByObjectParameterSet</span></span>
```
Get-AzCdnEndpointResourceUsage [-EndpointName <String>] -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c823d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c823d-107">DESCRIPTION</span></span>
<span data-ttu-id="c823d-108">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="c823d-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c823d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c823d-109">EXAMPLES</span></span>

### <span data-ttu-id="c823d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c823d-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="c823d-111">{{ Добавьте здесь описание примера }}</span><span class="sxs-lookup"><span data-stu-id="c823d-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="c823d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c823d-112">PARAMETERS</span></span>

### <span data-ttu-id="c823d-113">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="c823d-113">-CdnEndpoint</span></span>
<span data-ttu-id="c823d-114">Объект конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="c823d-114">The CDN endpoint object.</span></span>

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

### <span data-ttu-id="c823d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c823d-115">-DefaultProfile</span></span>
<span data-ttu-id="c823d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c823d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c823d-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c823d-117">-EndpointName</span></span>
<span data-ttu-id="c823d-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c823d-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="c823d-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="c823d-119">-ProfileName</span></span>
<span data-ttu-id="c823d-120">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="c823d-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="c823d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c823d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c823d-122">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="c823d-122">The resource group of the Azure CDN Profile.</span></span>

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

### <span data-ttu-id="c823d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c823d-123">CommonParameters</span></span>
<span data-ttu-id="c823d-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c823d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c823d-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c823d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c823d-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c823d-126">INPUTS</span></span>

### <span data-ttu-id="c823d-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="c823d-127">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="c823d-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c823d-128">OUTPUTS</span></span>

### <span data-ttu-id="c823d-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="c823d-129">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="c823d-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c823d-130">NOTES</span></span>

## <span data-ttu-id="c823d-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c823d-131">RELATED LINKS</span></span>
