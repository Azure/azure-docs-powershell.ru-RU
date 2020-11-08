---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246263"
---
# <span data-ttu-id="71851-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="71851-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="71851-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71851-102">SYNOPSIS</span></span>
<span data-ttu-id="71851-103">Создание новой группы происхождения сети CDN</span><span class="sxs-lookup"><span data-stu-id="71851-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="71851-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71851-104">SYNTAX</span></span>

### <span data-ttu-id="71851-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71851-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71851-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71851-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71851-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71851-107">DESCRIPTION</span></span>
<span data-ttu-id="71851-108">New-AzCdnOriginGroup создаст новую группу начала в пределах указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="71851-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="71851-109">Если это первая группа источника для конечной точки, необходимо также задать свойство DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="71851-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="71851-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71851-110">EXAMPLES</span></span>

### <span data-ttu-id="71851-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="71851-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="71851-112">Этот командлет создаст новую группу начала в указанной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="71851-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="71851-113">Он будет использовать заданные идентификаторы происхождения в качестве набора источников.</span><span class="sxs-lookup"><span data-stu-id="71851-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="71851-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71851-114">PARAMETERS</span></span>

### <span data-ttu-id="71851-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="71851-115">-CdnOriginGroup</span></span>
<span data-ttu-id="71851-116">Объект группы источника CDN.</span><span class="sxs-lookup"><span data-stu-id="71851-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="71851-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71851-117">-DefaultProfile</span></span>
<span data-ttu-id="71851-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="71851-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71851-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="71851-119">-EndpointName</span></span>
<span data-ttu-id="71851-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="71851-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="71851-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="71851-121">-OriginGroupName</span></span>
<span data-ttu-id="71851-122">Имя группы источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="71851-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="71851-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="71851-123">-OriginId</span></span>
<span data-ttu-id="71851-124">Идентификаторы группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="71851-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="71851-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="71851-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="71851-126">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="71851-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="71851-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="71851-127">-ProbePath</span></span>
<span data-ttu-id="71851-128">Относительный путь к источнику, который используется для определения работоспособности источника.</span><span class="sxs-lookup"><span data-stu-id="71851-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="71851-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="71851-129">-ProbeProtocol</span></span>
<span data-ttu-id="71851-130">Протокол, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="71851-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="71851-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="71851-131">-ProbeRequestType</span></span>
<span data-ttu-id="71851-132">Тип выполняемого запроса проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="71851-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="71851-133">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="71851-133">-ProfileName</span></span>
<span data-ttu-id="71851-134">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="71851-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="71851-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71851-135">-ResourceGroupName</span></span>
<span data-ttu-id="71851-136">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="71851-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="71851-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71851-137">-Confirm</span></span>
<span data-ttu-id="71851-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71851-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71851-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71851-139">-WhatIf</span></span>
<span data-ttu-id="71851-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71851-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71851-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71851-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71851-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71851-142">CommonParameters</span></span>
<span data-ttu-id="71851-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71851-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71851-144">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71851-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71851-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71851-145">INPUTS</span></span>

### <span data-ttu-id="71851-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="71851-146">System.Object</span></span>

## <span data-ttu-id="71851-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71851-147">OUTPUTS</span></span>

### <span data-ttu-id="71851-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="71851-148">System.Object</span></span>

## <span data-ttu-id="71851-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="71851-149">NOTES</span></span>

## <span data-ttu-id="71851-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71851-150">RELATED LINKS</span></span>
