---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247639"
---
# <span data-ttu-id="64315-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="64315-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="64315-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64315-102">SYNOPSIS</span></span>
<span data-ttu-id="64315-103">Обновляет группу источников CDN</span><span class="sxs-lookup"><span data-stu-id="64315-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="64315-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64315-104">SYNTAX</span></span>

### <span data-ttu-id="64315-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64315-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64315-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="64315-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64315-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64315-107">DESCRIPTION</span></span>
<span data-ttu-id="64315-108">Set-AzCdnOriginGroup обновит указанную группу начала в пределах данной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="64315-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="64315-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64315-109">EXAMPLES</span></span>

### <span data-ttu-id="64315-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="64315-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="64315-111">Этот командлет обновит свойство ProbeIntervalInSeconds в группе "источник".</span><span class="sxs-lookup"><span data-stu-id="64315-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="64315-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64315-112">PARAMETERS</span></span>

### <span data-ttu-id="64315-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="64315-113">-CdnOriginGroup</span></span>
<span data-ttu-id="64315-114">Объект группы источника CDN.</span><span class="sxs-lookup"><span data-stu-id="64315-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="64315-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64315-115">-DefaultProfile</span></span>
<span data-ttu-id="64315-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64315-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64315-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="64315-117">-EndpointName</span></span>
<span data-ttu-id="64315-118">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="64315-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="64315-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="64315-119">-OriginGroupName</span></span>
<span data-ttu-id="64315-120">Имя группы источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="64315-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="64315-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="64315-121">-OriginId</span></span>
<span data-ttu-id="64315-122">Идентификаторы группы источников Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="64315-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="64315-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="64315-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="64315-124">Количество секунд между зондами проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="64315-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="64315-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="64315-125">-ProbePath</span></span>
<span data-ttu-id="64315-126">Относительный путь к источнику, который используется для определения работоспособности источника.</span><span class="sxs-lookup"><span data-stu-id="64315-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="64315-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="64315-127">-ProbeProtocol</span></span>
<span data-ttu-id="64315-128">Протокол, используемый для проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="64315-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="64315-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="64315-129">-ProbeRequestType</span></span>
<span data-ttu-id="64315-130">Тип выполняемого запроса проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="64315-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="64315-131">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="64315-131">-ProfileName</span></span>
<span data-ttu-id="64315-132">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="64315-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="64315-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64315-133">-ResourceGroupName</span></span>
<span data-ttu-id="64315-134">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="64315-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="64315-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64315-135">-Confirm</span></span>
<span data-ttu-id="64315-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64315-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64315-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64315-137">-WhatIf</span></span>
<span data-ttu-id="64315-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64315-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64315-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64315-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64315-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64315-140">CommonParameters</span></span>
<span data-ttu-id="64315-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64315-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64315-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64315-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64315-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64315-143">INPUTS</span></span>

### <span data-ttu-id="64315-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="64315-144">System.Object</span></span>

## <span data-ttu-id="64315-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64315-145">OUTPUTS</span></span>

### <span data-ttu-id="64315-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="64315-146">System.Object</span></span>

## <span data-ttu-id="64315-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="64315-147">NOTES</span></span>

## <span data-ttu-id="64315-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64315-148">RELATED LINKS</span></span>
