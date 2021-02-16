---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233513"
---
# <span data-ttu-id="bd4fd-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bd4fd-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="bd4fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd4fd-102">SYNOPSIS</span></span>
<span data-ttu-id="bd4fd-103">Обновление группы источников CDN</span><span class="sxs-lookup"><span data-stu-id="bd4fd-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="bd4fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bd4fd-104">SYNTAX</span></span>

### <span data-ttu-id="bd4fd-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bd4fd-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bd4fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bd4fd-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bd4fd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bd4fd-107">DESCRIPTION</span></span>
<span data-ttu-id="bd4fd-108">Set-AzCdnOriginGroup будет обновлять указанную группу источника в пределах указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="bd4fd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bd4fd-109">EXAMPLES</span></span>

### <span data-ttu-id="bd4fd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bd4fd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="bd4fd-111">Этот cmdlet обно в группе "Источник" свойство "РазномеренныеВПродажахInSeconds" обновляется.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="bd4fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd4fd-112">PARAMETERS</span></span>

### <span data-ttu-id="bd4fd-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bd4fd-113">-CdnOriginGroup</span></span>
<span data-ttu-id="bd4fd-114">Объект группы «Источник CDN».</span><span class="sxs-lookup"><span data-stu-id="bd4fd-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="bd4fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd4fd-115">-DefaultProfile</span></span>
<span data-ttu-id="bd4fd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd4fd-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bd4fd-117">-EndpointName</span></span>
<span data-ttu-id="bd4fd-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bd4fd-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4fd-119">-OriginGroupName</span></span>
<span data-ttu-id="bd4fd-120">Имя группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="bd4fd-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="bd4fd-121">-OriginId</span></span>
<span data-ttu-id="bd4fd-122">Azure CDN origin ids.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="bd4fd-123">-В этом же окте.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="bd4fd-124">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="bd4fd-125">-СкайпPath</span><span class="sxs-lookup"><span data-stu-id="bd4fd-125">-ProbePath</span></span>
<span data-ttu-id="bd4fd-126">Путь относительно источника, используемого для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="bd4fd-127">-Разноцветнаяпротокол</span><span class="sxs-lookup"><span data-stu-id="bd4fd-127">-ProbeProtocol</span></span>
<span data-ttu-id="bd4fd-128">Протокол для использования в медицинских организациях.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="bd4fd-129">-TypeRequestType</span><span class="sxs-lookup"><span data-stu-id="bd4fd-129">-ProbeRequestType</span></span>
<span data-ttu-id="bd4fd-130">Тип запроса на проверку состояния здоровья.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="bd4fd-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bd4fd-131">-ProfileName</span></span>
<span data-ttu-id="bd4fd-132">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bd4fd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd4fd-133">-ResourceGroupName</span></span>
<span data-ttu-id="bd4fd-134">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="bd4fd-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bd4fd-135">-Confirm</span></span>
<span data-ttu-id="bd4fd-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd4fd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd4fd-137">-WhatIf</span></span>
<span data-ttu-id="bd4fd-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd4fd-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd4fd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd4fd-140">CommonParameters</span></span>
<span data-ttu-id="bd4fd-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd4fd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd4fd-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd4fd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd4fd-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bd4fd-143">INPUTS</span></span>

### <span data-ttu-id="bd4fd-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="bd4fd-144">System.Object</span></span>

## <span data-ttu-id="bd4fd-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bd4fd-145">OUTPUTS</span></span>

### <span data-ttu-id="bd4fd-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="bd4fd-146">System.Object</span></span>

## <span data-ttu-id="bd4fd-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bd4fd-147">NOTES</span></span>

## <span data-ttu-id="bd4fd-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bd4fd-148">RELATED LINKS</span></span>
