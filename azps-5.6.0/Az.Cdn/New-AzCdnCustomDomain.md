---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7060D3D7-B397-447E-88E3-B6F0D094770D
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdncustomdomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnCustomDomain.md
ms.openlocfilehash: 58e4d922d74f36f6f472cf3bfef8e0d0d45155d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010792"
---
# <span data-ttu-id="cc242-101">New-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc242-101">New-AzCdnCustomDomain</span></span>

## <span data-ttu-id="cc242-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc242-102">SYNOPSIS</span></span>
<span data-ttu-id="cc242-103">Создает пользовательский домен для конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="cc242-103">Creates a custom domain for a CDN endpoint.</span></span>

## <span data-ttu-id="cc242-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc242-104">SYNTAX</span></span>

### <span data-ttu-id="cc242-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc242-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -EndpointName <String>
 -ProfileName <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc242-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc242-106">ByObjectParameterSet</span></span>
```
New-AzCdnCustomDomain -HostName <String> -CustomDomainName <String> -CdnEndpoint <PSEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc242-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc242-107">DESCRIPTION</span></span>
<span data-ttu-id="cc242-108">С **его использованием** создается настраиваемый домен для конечной точки сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="cc242-108">The **New-AzCdnCustomDomain** cmdlet creates a custom domain for the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="cc242-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc242-109">EXAMPLES</span></span>

## <span data-ttu-id="cc242-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc242-110">PARAMETERS</span></span>

### <span data-ttu-id="cc242-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc242-111">-CdnEndpoint</span></span>
<span data-ttu-id="cc242-112">Определяет объект конечной точки CDN, к которому добавляется настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="cc242-112">Specifies the CDN endpoint object to which the custom domain is added.</span></span>

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

### <span data-ttu-id="cc242-113">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="cc242-113">-CustomDomainName</span></span>
<span data-ttu-id="cc242-114">Указывает имя ресурса для пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="cc242-114">Specifies the resource name of the custom domain.</span></span>

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

### <span data-ttu-id="cc242-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc242-115">-DefaultProfile</span></span>
<span data-ttu-id="cc242-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cc242-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc242-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cc242-117">-EndpointName</span></span>
<span data-ttu-id="cc242-118">Указывает имя конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cc242-118">Specifies the name of the endpoint.</span></span>

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

### <span data-ttu-id="cc242-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="cc242-119">-HostName</span></span>
<span data-ttu-id="cc242-120">Указывает имя хоста пользовательского домена.</span><span class="sxs-lookup"><span data-stu-id="cc242-120">Specifies the host name of the custom domain.</span></span>

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

### <span data-ttu-id="cc242-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cc242-121">-ProfileName</span></span>
<span data-ttu-id="cc242-122">Указывает имя профиля.</span><span class="sxs-lookup"><span data-stu-id="cc242-122">Specifies the name of the profile.</span></span>

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

### <span data-ttu-id="cc242-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc242-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc242-124">Имя группы ресурсов, к которой принадлежит настраиваемый домен.</span><span class="sxs-lookup"><span data-stu-id="cc242-124">Specifies the name of the resource group to which the custom domain belongs.</span></span>

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

### <span data-ttu-id="cc242-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc242-125">-Confirm</span></span>
<span data-ttu-id="cc242-126">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cc242-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc242-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc242-127">-WhatIf</span></span>
<span data-ttu-id="cc242-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc242-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc242-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc242-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc242-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc242-130">CommonParameters</span></span>
<span data-ttu-id="cc242-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc242-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc242-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc242-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc242-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc242-133">INPUTS</span></span>

### <span data-ttu-id="cc242-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc242-134">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

## <span data-ttu-id="cc242-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc242-135">OUTPUTS</span></span>

### <span data-ttu-id="cc242-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc242-136">Microsoft.Azure.Commands.Cdn.Models.CustomDomain.PSCustomDomain</span></span>

## <span data-ttu-id="cc242-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc242-137">NOTES</span></span>

## <span data-ttu-id="cc242-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc242-138">RELATED LINKS</span></span>

[<span data-ttu-id="cc242-139">Get-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc242-139">Get-AzCdnCustomDomain</span></span>](./Get-AzCdnCustomDomain.md)

[<span data-ttu-id="cc242-140">Remove-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc242-140">Remove-AzCdnCustomDomain</span></span>](./Remove-AzCdnCustomDomain.md)

[<span data-ttu-id="cc242-141">Test-AzCdnCustomDomain</span><span class="sxs-lookup"><span data-stu-id="cc242-141">Test-AzCdnCustomDomain</span></span>](./Test-AzCdnCustomDomain.md)


