---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234884"
---
# <span data-ttu-id="ebb2f-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ebb2f-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="ebb2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb2f-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb2f-103">Создание группы источников CDN</span><span class="sxs-lookup"><span data-stu-id="ebb2f-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="ebb2f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ebb2f-104">SYNTAX</span></span>

### <span data-ttu-id="ebb2f-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ebb2f-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ebb2f-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ebb2f-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebb2f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ebb2f-107">DESCRIPTION</span></span>
<span data-ttu-id="ebb2f-108">Новая New-AzCdnOriginGroup будет создаваться в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="ebb2f-109">Если это первая группа источника для конечной точки, необходимо также настроить свойство DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="ebb2f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ebb2f-110">EXAMPLES</span></span>

### <span data-ttu-id="ebb2f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ebb2f-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="ebb2f-112">Этот cmdlet создаст новую группу источника в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="ebb2f-113">Он будет использовать заданный источник в качестве набора.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="ebb2f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebb2f-114">PARAMETERS</span></span>

### <span data-ttu-id="ebb2f-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ebb2f-115">-CdnOriginGroup</span></span>
<span data-ttu-id="ebb2f-116">Объект группы «Источник CDN».</span><span class="sxs-lookup"><span data-stu-id="ebb2f-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="ebb2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb2f-117">-DefaultProfile</span></span>
<span data-ttu-id="ebb2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebb2f-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ebb2f-119">-EndpointName</span></span>
<span data-ttu-id="ebb2f-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ebb2f-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb2f-121">-OriginGroupName</span></span>
<span data-ttu-id="ebb2f-122">Имя группы "Источник" в CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="ebb2f-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="ebb2f-123">-OriginId</span></span>
<span data-ttu-id="ebb2f-124">Azure CDN origin ids.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb2f-125">-РазномероваяпровождениеInSeconds</span><span class="sxs-lookup"><span data-stu-id="ebb2f-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="ebb2f-126">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb2f-127">-СкайпPath</span><span class="sxs-lookup"><span data-stu-id="ebb2f-127">-ProbePath</span></span>
<span data-ttu-id="ebb2f-128">Путь относительно источника, используемого для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb2f-129">-Разноцветнаяпротокол</span><span class="sxs-lookup"><span data-stu-id="ebb2f-129">-ProbeProtocol</span></span>
<span data-ttu-id="ebb2f-130">Протокол для использования в медицинских организациях.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb2f-131">-TypeRequestType</span><span class="sxs-lookup"><span data-stu-id="ebb2f-131">-ProbeRequestType</span></span>
<span data-ttu-id="ebb2f-132">Тип запроса на проверку состояния здоровья.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebb2f-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ebb2f-133">-ProfileName</span></span>
<span data-ttu-id="ebb2f-134">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ebb2f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb2f-135">-ResourceGroupName</span></span>
<span data-ttu-id="ebb2f-136">Группа ресурсов профиля Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="ebb2f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebb2f-137">-Confirm</span></span>
<span data-ttu-id="ebb2f-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ebb2f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebb2f-139">-WhatIf</span></span>
<span data-ttu-id="ebb2f-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ebb2f-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ebb2f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb2f-142">CommonParameters</span></span>
<span data-ttu-id="ebb2f-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebb2f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb2f-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebb2f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb2f-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebb2f-145">INPUTS</span></span>

### <span data-ttu-id="ebb2f-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="ebb2f-146">System.Object</span></span>

## <span data-ttu-id="ebb2f-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ebb2f-147">OUTPUTS</span></span>

### <span data-ttu-id="ebb2f-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="ebb2f-148">System.Object</span></span>

## <span data-ttu-id="ebb2f-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ebb2f-149">NOTES</span></span>

## <span data-ttu-id="ebb2f-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ebb2f-150">RELATED LINKS</span></span>
