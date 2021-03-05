---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: a2acea388b34b23d4977fa65ae6e6e6d4702525b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979379"
---
# <span data-ttu-id="c0fa7-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="c0fa7-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="c0fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-102">SYNOPSIS</span></span>
<span data-ttu-id="c0fa7-103">Управляемое обновление приложения</span><span class="sxs-lookup"><span data-stu-id="c0fa7-103">Updates managed application</span></span>

## <span data-ttu-id="c0fa7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c0fa7-104">SYNTAX</span></span>

### <span data-ttu-id="c0fa7-105">SetByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0fa7-106">SetById</span><span class="sxs-lookup"><span data-stu-id="c0fa7-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0fa7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0fa7-107">DESCRIPTION</span></span>
<span data-ttu-id="c0fa7-108">**Cmdlet Set-AzManagedApplication** обновляет управляемые приложения.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="c0fa7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c0fa7-109">EXAMPLES</span></span>

### <span data-ttu-id="c0fa7-110">Пример 1. Обновление описания определения управляемого приложения</span><span class="sxs-lookup"><span data-stu-id="c0fa7-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="c0fa7-111">Эта команда обновляет описание управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-111">This command updates the managed application description</span></span>

## <span data-ttu-id="c0fa7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-112">PARAMETERS</span></span>

### <span data-ttu-id="c0fa7-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c0fa7-113">-ApiVersion</span></span>
<span data-ttu-id="c0fa7-114">В этом случае указывается используемая версия API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c0fa7-115">Если он не задан, версия API будет автоматически определена как наиболее последняя из доступных.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-115">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0fa7-116">-DefaultProfile</span></span>
<span data-ttu-id="c0fa7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0fa7-118">-Id</span><span class="sxs-lookup"><span data-stu-id="c0fa7-118">-Id</span></span>
<span data-ttu-id="c0fa7-119">Полностью управляемый ИД приложения, включая подписку.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="c0fa7-120">Например, /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0fa7-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="c0fa7-121">-Kind</span></span>
<span data-ttu-id="c0fa7-122">Тип управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-122">The managed application kind.</span></span>
<span data-ttu-id="c0fa7-123">Один из marketplace или servicecatalog</span><span class="sxs-lookup"><span data-stu-id="c0fa7-123">One of marketplace or servicecatalog</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c0fa7-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="c0fa7-125">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-125">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0fa7-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="c0fa7-127">Имя группы управляемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-127">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c0fa7-128">-Name</span></span>
<span data-ttu-id="c0fa7-129">Имя управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="c0fa7-130">-Parameter</span></span>
<span data-ttu-id="c0fa7-131">Строка параметров в формате JSON для управляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="c0fa7-132">Это может быть путь к имени файла или URI, содержащий параметры, или параметры в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-133">-Plan</span><span class="sxs-lookup"><span data-stu-id="c0fa7-133">-Plan</span></span>
<span data-ttu-id="c0fa7-134">Hash table which represents managed application plan properties.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-134">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="c0fa7-135">-Pre</span></span>
<span data-ttu-id="c0fa7-136">Указывает на то, что для автоматического определения используемой версии API следует использовать предварительные версии API.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0fa7-137">-ResourceGroupName</span></span>
<span data-ttu-id="c0fa7-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0fa7-139">-Tag</span></span>
<span data-ttu-id="c0fa7-140">Hash table which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-140">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0fa7-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0fa7-141">-Confirm</span></span>
<span data-ttu-id="c0fa7-142">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0fa7-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0fa7-143">-WhatIf</span></span>
<span data-ttu-id="c0fa7-144">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0fa7-145">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0fa7-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0fa7-146">CommonParameters</span></span>
<span data-ttu-id="c0fa7-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0fa7-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0fa7-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0fa7-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0fa7-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-149">INPUTS</span></span>

### <span data-ttu-id="c0fa7-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c0fa7-150">System.String</span></span>

### <span data-ttu-id="c0fa7-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c0fa7-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c0fa7-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c0fa7-152">OUTPUTS</span></span>

### <span data-ttu-id="c0fa7-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="c0fa7-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c0fa7-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c0fa7-154">NOTES</span></span>

## <span data-ttu-id="c0fa7-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0fa7-155">RELATED LINKS</span></span>
