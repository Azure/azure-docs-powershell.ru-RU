---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249096"
---
# <span data-ttu-id="85eda-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="85eda-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="85eda-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="85eda-102">SYNOPSIS</span></span>
<span data-ttu-id="85eda-103">Удаление происхождения сети CDN</span><span class="sxs-lookup"><span data-stu-id="85eda-103">Removes a CDN origin</span></span>

## <span data-ttu-id="85eda-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="85eda-104">SYNTAX</span></span>

### <span data-ttu-id="85eda-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85eda-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85eda-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85eda-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85eda-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85eda-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85eda-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85eda-108">DESCRIPTION</span></span>
<span data-ttu-id="85eda-109">Remove-AzCdnOrigin удалит источник CDN из данной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="85eda-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="85eda-110">Если источником является единственный источник в пределах указанной конечной точки, удаление завершится сбоем, так как требуется по крайней мере 1 источник.</span><span class="sxs-lookup"><span data-stu-id="85eda-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="85eda-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="85eda-111">EXAMPLES</span></span>

### <span data-ttu-id="85eda-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="85eda-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="85eda-113">Этот командлет удалит указанный источник из данной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="85eda-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="85eda-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="85eda-114">PARAMETERS</span></span>

### <span data-ttu-id="85eda-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="85eda-115">-CdnOrigin</span></span>
<span data-ttu-id="85eda-116">Объект источника CDN.</span><span class="sxs-lookup"><span data-stu-id="85eda-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85eda-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85eda-117">-DefaultProfile</span></span>
<span data-ttu-id="85eda-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85eda-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85eda-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="85eda-119">-EndpointName</span></span>
<span data-ttu-id="85eda-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="85eda-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="85eda-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="85eda-121">-OriginName</span></span>
<span data-ttu-id="85eda-122">Имя источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="85eda-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="85eda-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85eda-123">-PassThru</span></span>
<span data-ttu-id="85eda-124">Возвращаемый объект, если он указан.</span><span class="sxs-lookup"><span data-stu-id="85eda-124">Return object if specified.</span></span>

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

### <span data-ttu-id="85eda-125">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="85eda-125">-ProfileName</span></span>
<span data-ttu-id="85eda-126">Имя профиля CDN в службе Azure.</span><span class="sxs-lookup"><span data-stu-id="85eda-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="85eda-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85eda-127">-ResourceGroupName</span></span>
<span data-ttu-id="85eda-128">Группа ресурсов в профиле CDN для Azure.</span><span class="sxs-lookup"><span data-stu-id="85eda-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="85eda-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85eda-129">-ResourceId</span></span>
<span data-ttu-id="85eda-130">Идентификатор ресурса источника Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="85eda-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="85eda-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85eda-131">-Confirm</span></span>
<span data-ttu-id="85eda-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="85eda-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85eda-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85eda-133">-WhatIf</span></span>
<span data-ttu-id="85eda-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="85eda-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85eda-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="85eda-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85eda-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85eda-136">CommonParameters</span></span>
<span data-ttu-id="85eda-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="85eda-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85eda-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85eda-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85eda-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="85eda-139">INPUTS</span></span>

### <span data-ttu-id="85eda-140">Ничего</span><span class="sxs-lookup"><span data-stu-id="85eda-140">None</span></span>

## <span data-ttu-id="85eda-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="85eda-141">OUTPUTS</span></span>

### <span data-ttu-id="85eda-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85eda-142">System.Boolean</span></span>

## <span data-ttu-id="85eda-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="85eda-143">NOTES</span></span>

## <span data-ttu-id="85eda-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85eda-144">RELATED LINKS</span></span>
