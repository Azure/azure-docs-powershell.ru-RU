---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 21E9F441-A00B-4F79-8FF1-968D92982471
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/unpublish-azcdnendpointcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Unpublish-AzCdnEndpointContent.md
ms.openlocfilehash: eb108e665bce54d2b94fc4ab4a56c9573248289a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399396"
---
# <span data-ttu-id="19dda-101">Unpublish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="19dda-101">Unpublish-AzCdnEndpointContent</span></span>

## <span data-ttu-id="19dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19dda-102">SYNOPSIS</span></span>
<span data-ttu-id="19dda-103">Очистка конечной точки CDN.</span><span class="sxs-lookup"><span data-stu-id="19dda-103">Purges a CDN endpoint.</span></span>

## <span data-ttu-id="19dda-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19dda-104">SYNTAX</span></span>

### <span data-ttu-id="19dda-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19dda-105">ByFieldsParameterSet (Default)</span></span>
```
Unpublish-AzCdnEndpointContent -EndpointName <String> -ProfileName <String> -ResourceGroupName <String>
 -PurgeContent <String[]> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-106">ByObjectParameterSet</span></span>
```
Unpublish-AzCdnEndpointContent -CdnEndpoint <PSEndpoint> -PurgeContent <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dda-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19dda-107">DESCRIPTION</span></span>
<span data-ttu-id="19dda-108">Для очистки содержимого из конечной точки СЕТИ доставки содержимого (CDN) Azure очищается проектлет **Unpublish-AzCdnEndpointContent.**</span><span class="sxs-lookup"><span data-stu-id="19dda-108">The **Unpublish-AzCdnEndpointContent** cmdlet purges the content from an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="19dda-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19dda-109">EXAMPLES</span></span>

## <span data-ttu-id="19dda-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19dda-110">PARAMETERS</span></span>

### <span data-ttu-id="19dda-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="19dda-111">-CdnEndpoint</span></span>
<span data-ttu-id="19dda-112">Указывает конечную точку, которую очищает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dda-112">Specifies the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="19dda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dda-113">-DefaultProfile</span></span>
<span data-ttu-id="19dda-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19dda-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19dda-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="19dda-115">-EndpointName</span></span>
<span data-ttu-id="19dda-116">Указывает имя конечной точки, которую очищает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dda-116">Specifies name of the endpoint that this cmdlet purges.</span></span>

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

### <span data-ttu-id="19dda-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19dda-117">-PassThru</span></span>
<span data-ttu-id="19dda-118">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="19dda-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="19dda-119">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="19dda-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="19dda-120">-ProfileName</span></span>
<span data-ttu-id="19dda-121">Имя профиля, к которому относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="19dda-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="19dda-122">-PurgeContent</span><span class="sxs-lookup"><span data-stu-id="19dda-122">-PurgeContent</span></span>
<span data-ttu-id="19dda-123">Определяет массив относительных путей для содержимого на сервере-источнике, который очищает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dda-123">Specifies an array of relative paths for the content on the origin server that this cmdlet purges.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dda-124">-ResourceGroupName</span></span>
<span data-ttu-id="19dda-125">Имя группы ресурсов, к которой относится конечная точка.</span><span class="sxs-lookup"><span data-stu-id="19dda-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="19dda-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19dda-126">-Confirm</span></span>
<span data-ttu-id="19dda-127">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="19dda-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19dda-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dda-128">-WhatIf</span></span>
<span data-ttu-id="19dda-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19dda-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19dda-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19dda-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19dda-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dda-131">CommonParameters</span></span>
<span data-ttu-id="19dda-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dda-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dda-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19dda-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dda-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19dda-134">INPUTS</span></span>

### <span data-ttu-id="19dda-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="19dda-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="19dda-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19dda-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19dda-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19dda-137">OUTPUTS</span></span>

### <span data-ttu-id="19dda-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19dda-138">System.Boolean</span></span>

## <span data-ttu-id="19dda-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19dda-139">NOTES</span></span>

## <span data-ttu-id="19dda-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19dda-140">RELATED LINKS</span></span>

[<span data-ttu-id="19dda-141">Publish-AzCdnEndpointContent</span><span class="sxs-lookup"><span data-stu-id="19dda-141">Publish-AzCdnEndpointContent</span></span>](./Publish-AzCdnEndpointContent.md)


