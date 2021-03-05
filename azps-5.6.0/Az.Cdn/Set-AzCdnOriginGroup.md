---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: c70c08ad88491d7624b078babb5e62437c22e116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985326"
---
# <span data-ttu-id="1fcfb-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1fcfb-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="1fcfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fcfb-102">SYNOPSIS</span></span>
<span data-ttu-id="1fcfb-103">Обновление группы источников CDN</span><span class="sxs-lookup"><span data-stu-id="1fcfb-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="1fcfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1fcfb-104">SYNTAX</span></span>

### <span data-ttu-id="1fcfb-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1fcfb-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fcfb-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fcfb-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fcfb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1fcfb-107">DESCRIPTION</span></span>
<span data-ttu-id="1fcfb-108">Set-AzCdnOriginGroup будет обновлять указанную группу источника в пределах указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="1fcfb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1fcfb-109">EXAMPLES</span></span>

### <span data-ttu-id="1fcfb-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1fcfb-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="1fcfb-111">Этот cmdlet обно в группе "Источник" свойство "РазномеренныйВПродажав" обновляется.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="1fcfb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fcfb-112">PARAMETERS</span></span>

### <span data-ttu-id="1fcfb-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1fcfb-113">-CdnOriginGroup</span></span>
<span data-ttu-id="1fcfb-114">Объект группы «Источник CDN».</span><span class="sxs-lookup"><span data-stu-id="1fcfb-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="1fcfb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fcfb-115">-DefaultProfile</span></span>
<span data-ttu-id="1fcfb-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fcfb-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1fcfb-117">-EndpointName</span></span>
<span data-ttu-id="1fcfb-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1fcfb-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcfb-119">-OriginGroupName</span></span>
<span data-ttu-id="1fcfb-120">Имя группы "Источник" в CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="1fcfb-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="1fcfb-121">-OriginId</span></span>
<span data-ttu-id="1fcfb-122">Azure CDN origin ids.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="1fcfb-123">-РазномероваяпровождениеInSeconds</span><span class="sxs-lookup"><span data-stu-id="1fcfb-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="1fcfb-124">Количество секунд между проверками здоровья.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="1fcfb-125">-СкайпPath</span><span class="sxs-lookup"><span data-stu-id="1fcfb-125">-ProbePath</span></span>
<span data-ttu-id="1fcfb-126">Путь относительно источника, используемого для определения его состояния.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="1fcfb-127">-РазноцветнаяПротокол</span><span class="sxs-lookup"><span data-stu-id="1fcfb-127">-ProbeProtocol</span></span>
<span data-ttu-id="1fcfb-128">Протокол для использования в медицинских организациях.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="1fcfb-129">-TypeRequestType</span><span class="sxs-lookup"><span data-stu-id="1fcfb-129">-ProbeRequestType</span></span>
<span data-ttu-id="1fcfb-130">Тип запроса на проверку состояния здоровья.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="1fcfb-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1fcfb-131">-ProfileName</span></span>
<span data-ttu-id="1fcfb-132">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1fcfb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fcfb-133">-ResourceGroupName</span></span>
<span data-ttu-id="1fcfb-134">Группа ресурсов профиля AZURE CDN.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1fcfb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fcfb-135">-Confirm</span></span>
<span data-ttu-id="1fcfb-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fcfb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fcfb-137">-WhatIf</span></span>
<span data-ttu-id="1fcfb-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fcfb-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fcfb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fcfb-140">CommonParameters</span></span>
<span data-ttu-id="1fcfb-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fcfb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fcfb-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fcfb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fcfb-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1fcfb-143">INPUTS</span></span>

### <span data-ttu-id="1fcfb-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fcfb-144">System.Object</span></span>

## <span data-ttu-id="1fcfb-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1fcfb-145">OUTPUTS</span></span>

### <span data-ttu-id="1fcfb-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="1fcfb-146">System.Object</span></span>

## <span data-ttu-id="1fcfb-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1fcfb-147">NOTES</span></span>

## <span data-ttu-id="1fcfb-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1fcfb-148">RELATED LINKS</span></span>
