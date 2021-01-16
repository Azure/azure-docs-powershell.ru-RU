---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509354"
---
# <span data-ttu-id="1bbd0-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1bbd0-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="1bbd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bbd0-102">SYNOPSIS</span></span>
<span data-ttu-id="1bbd0-103">Удаление источника CDN</span><span class="sxs-lookup"><span data-stu-id="1bbd0-103">Removes a CDN origin</span></span>

## <span data-ttu-id="1bbd0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1bbd0-104">SYNTAX</span></span>

### <span data-ttu-id="1bbd0-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1bbd0-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1bbd0-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bbd0-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bbd0-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1bbd0-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bbd0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1bbd0-108">DESCRIPTION</span></span>
<span data-ttu-id="1bbd0-109">Remove-AzCdnOrigin будет удалено из данной конечной точки источник CDN.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="1bbd0-110">Если источник является единственным в пределах указанной конечной точки, удаление завершится сбой, так как требуется хотя бы один источник.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="1bbd0-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1bbd0-111">EXAMPLES</span></span>

### <span data-ttu-id="1bbd0-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1bbd0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="1bbd0-113">Этот cmdlet удалит указанный источник из указанной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="1bbd0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bbd0-114">PARAMETERS</span></span>

### <span data-ttu-id="1bbd0-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="1bbd0-115">-CdnOrigin</span></span>
<span data-ttu-id="1bbd0-116">Источник CDN.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="1bbd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bbd0-117">-DefaultProfile</span></span>
<span data-ttu-id="1bbd0-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1bbd0-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1bbd0-119">-EndpointName</span></span>
<span data-ttu-id="1bbd0-120">Имя конечной точки CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1bbd0-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="1bbd0-121">-OriginName</span></span>
<span data-ttu-id="1bbd0-122">Имя источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="1bbd0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1bbd0-123">-PassThru</span></span>
<span data-ttu-id="1bbd0-124">Возврат объекта, если он задан.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-124">Return object if specified.</span></span>

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

### <span data-ttu-id="1bbd0-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1bbd0-125">-ProfileName</span></span>
<span data-ttu-id="1bbd0-126">Имя профиля CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1bbd0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bbd0-127">-ResourceGroupName</span></span>
<span data-ttu-id="1bbd0-128">Группа ресурсов профиля Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1bbd0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bbd0-129">-ResourceId</span></span>
<span data-ttu-id="1bbd0-130">ИД ресурса источника CDN Azure.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="1bbd0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bbd0-131">-Confirm</span></span>
<span data-ttu-id="1bbd0-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bbd0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bbd0-133">-WhatIf</span></span>
<span data-ttu-id="1bbd0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bbd0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bbd0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bbd0-136">CommonParameters</span></span>
<span data-ttu-id="1bbd0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bbd0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bbd0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1bbd0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bbd0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1bbd0-139">INPUTS</span></span>

### <span data-ttu-id="1bbd0-140">Нет</span><span class="sxs-lookup"><span data-stu-id="1bbd0-140">None</span></span>

## <span data-ttu-id="1bbd0-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1bbd0-141">OUTPUTS</span></span>

### <span data-ttu-id="1bbd0-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1bbd0-142">System.Boolean</span></span>

## <span data-ttu-id="1bbd0-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1bbd0-143">NOTES</span></span>

## <span data-ttu-id="1bbd0-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1bbd0-144">RELATED LINKS</span></span>