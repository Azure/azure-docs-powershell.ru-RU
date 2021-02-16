---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229228"
---
# <span data-ttu-id="115df-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="115df-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="115df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="115df-102">SYNOPSIS</span></span>
<span data-ttu-id="115df-103">Удаление группы источников CDN</span><span class="sxs-lookup"><span data-stu-id="115df-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="115df-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="115df-104">SYNTAX</span></span>

### <span data-ttu-id="115df-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="115df-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="115df-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="115df-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="115df-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="115df-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="115df-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="115df-108">DESCRIPTION</span></span>
<span data-ttu-id="115df-109">Remove-AzCdnOriginGroup удалит группу источников CDN из указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="115df-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="115df-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="115df-110">EXAMPLES</span></span>

### <span data-ttu-id="115df-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="115df-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="115df-112">Этот cmdlet удалит указанную группу источника из указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="115df-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="115df-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="115df-113">PARAMETERS</span></span>

### <span data-ttu-id="115df-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="115df-114">-CdnOriginGroup</span></span>
<span data-ttu-id="115df-115">Объект группы «Источник CDN».</span><span class="sxs-lookup"><span data-stu-id="115df-115">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="115df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115df-116">-DefaultProfile</span></span>
<span data-ttu-id="115df-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="115df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="115df-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="115df-118">-EndpointName</span></span>
<span data-ttu-id="115df-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="115df-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="115df-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="115df-120">-OriginGroupName</span></span>
<span data-ttu-id="115df-121">Имя группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="115df-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="115df-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="115df-122">-PassThru</span></span>
<span data-ttu-id="115df-123">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="115df-123">Return object if specified.</span></span>

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

### <span data-ttu-id="115df-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="115df-124">-ProfileName</span></span>
<span data-ttu-id="115df-125">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="115df-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="115df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="115df-126">-ResourceGroupName</span></span>
<span data-ttu-id="115df-127">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="115df-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="115df-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="115df-128">-ResourceId</span></span>
<span data-ttu-id="115df-129">ИД ресурса группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="115df-129">The resource id of the Azure CDN origin group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115df-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="115df-130">-Confirm</span></span>
<span data-ttu-id="115df-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="115df-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="115df-132">-WhatIf</span></span>
<span data-ttu-id="115df-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="115df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="115df-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="115df-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115df-135">CommonParameters</span></span>
<span data-ttu-id="115df-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="115df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115df-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="115df-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115df-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="115df-138">INPUTS</span></span>

### <span data-ttu-id="115df-139">Нет</span><span class="sxs-lookup"><span data-stu-id="115df-139">None</span></span>

## <span data-ttu-id="115df-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="115df-140">OUTPUTS</span></span>

### <span data-ttu-id="115df-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="115df-141">System.Boolean</span></span>

## <span data-ttu-id="115df-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="115df-142">NOTES</span></span>

## <span data-ttu-id="115df-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="115df-143">RELATED LINKS</span></span>
