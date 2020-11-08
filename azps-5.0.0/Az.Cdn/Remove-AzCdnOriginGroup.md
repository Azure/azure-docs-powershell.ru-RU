---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249095"
---
# <span data-ttu-id="0568c-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0568c-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="0568c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0568c-102">SYNOPSIS</span></span>
<span data-ttu-id="0568c-103">Удаление группы происхождения сети CDN</span><span class="sxs-lookup"><span data-stu-id="0568c-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="0568c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0568c-104">SYNTAX</span></span>

### <span data-ttu-id="0568c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0568c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0568c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0568c-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0568c-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0568c-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0568c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0568c-108">DESCRIPTION</span></span>
<span data-ttu-id="0568c-109">Remove-AzCdnOriginGroup удалит группу источников CDN из указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0568c-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="0568c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0568c-110">EXAMPLES</span></span>

### <span data-ttu-id="0568c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0568c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="0568c-112">Этот командлет удалит указанную группу начала из данной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0568c-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="0568c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0568c-113">PARAMETERS</span></span>

### <span data-ttu-id="0568c-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="0568c-114">-CdnOriginGroup</span></span>
<span data-ttu-id="0568c-115">Объект группы источника CDN.</span><span class="sxs-lookup"><span data-stu-id="0568c-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="0568c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0568c-116">-DefaultProfile</span></span>
<span data-ttu-id="0568c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0568c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0568c-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="0568c-118">-EndpointName</span></span>
<span data-ttu-id="0568c-119">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="0568c-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="0568c-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="0568c-120">-OriginGroupName</span></span>
<span data-ttu-id="0568c-121">Имя группы источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="0568c-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="0568c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0568c-122">-PassThru</span></span>
<span data-ttu-id="0568c-123">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="0568c-123">Return object if specified.</span></span>

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

### <span data-ttu-id="0568c-124">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="0568c-124">-ProfileName</span></span>
<span data-ttu-id="0568c-125">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="0568c-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="0568c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0568c-126">-ResourceGroupName</span></span>
<span data-ttu-id="0568c-127">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="0568c-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="0568c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0568c-128">-ResourceId</span></span>
<span data-ttu-id="0568c-129">Идентификатор ресурса группы происхождения Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="0568c-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="0568c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0568c-130">-Confirm</span></span>
<span data-ttu-id="0568c-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0568c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0568c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0568c-132">-WhatIf</span></span>
<span data-ttu-id="0568c-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0568c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0568c-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0568c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0568c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0568c-135">CommonParameters</span></span>
<span data-ttu-id="0568c-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0568c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0568c-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0568c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0568c-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0568c-138">INPUTS</span></span>

### <span data-ttu-id="0568c-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="0568c-139">None</span></span>

## <span data-ttu-id="0568c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0568c-140">OUTPUTS</span></span>

### <span data-ttu-id="0568c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0568c-141">System.Boolean</span></span>

## <span data-ttu-id="0568c-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0568c-142">NOTES</span></span>

## <span data-ttu-id="0568c-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0568c-143">RELATED LINKS</span></span>
