---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 22a43739ec63f8287ce51c4c4f4a125b4e5b1c65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98407671"
---
# <span data-ttu-id="4c4f8-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="4c4f8-101">Remove-AzTag</span></span>

## <span data-ttu-id="4c4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="4c4f8-103">Удаление предопределеных тегов и значений Azure | Удаляет весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="4c4f8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4c4f8-104">SYNTAX</span></span>

### <span data-ttu-id="4c4f8-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c4f8-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c4f8-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4c4f8-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="4c4f8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c4f8-107">DESCRIPTION</span></span>

<span data-ttu-id="4c4f8-108">**RemovePredefinedTagSet:** командлет **Remove-AzTag** удаляет предопределные теги и значения Azure из вашей подписки.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-108">**RemovePredefinedTagSet**: The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="4c4f8-109">Чтобы удалить определенные значения из заранее определенного тега, используйте параметр *Value.*</span><span class="sxs-lookup"><span data-stu-id="4c4f8-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="4c4f8-110">По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения. Удалить тег или значение, примененные в данный момент к ресурсу или группе ресурсов, невозможно.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="4c4f8-111">Перед **использованием командлета Remove-AzTag** используйте параметр *Tag* командлета Set-AzResourceGroup, чтобы удалить тег или значения из группы ресурсов или ресурса.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-111">Before using **Remove-AzTag**, use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="4c4f8-112">Модуль "Теги Azure", который входит в **состав тега Remove-AzTag,** помогает управлять предопределными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="4c4f8-113">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="4c4f8-114">Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="4c4f8-115">**RemoveByResourceIdParameterSet:** командлет **Remove-AzTag** с **ResourceId** удаляет весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-115">**RemoveByResourceIdParameterSet**: The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="4c4f8-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4c4f8-116">EXAMPLES</span></span>

### <span data-ttu-id="4c4f8-117">Пример 1. Удаление предопределеного тега</span><span class="sxs-lookup"><span data-stu-id="4c4f8-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="4c4f8-118">Эта команда удаляет предопределный тег "Отдел" и все его значения.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="4c4f8-119">Если тег был применен к ресурсам или группам ресурсов, команда не будет применена.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="4c4f8-120">Пример 2. Удаление значения из предопределеного тега</span><span class="sxs-lookup"><span data-stu-id="4c4f8-120">Example 2: Delete a value from a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="4c4f8-121">Эта команда удаляет значение HumanResources из предопределенного тега Department.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="4c4f8-122">Тег не удаляется.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-122">It does not delete the tag.</span></span>
<span data-ttu-id="4c4f8-123">Если значение было применено к ресурсам или группам ресурсов, команда не может быть применена.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="4c4f8-124">Пример 3. Удаление всего набора тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="4c4f8-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="4c4f8-125">Эта команда удаляет весь набор тегов в подписке с {subId}.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="4c4f8-126">Он не возвращает объект, удаленный, если он не прошел через "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="4c4f8-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="4c4f8-127">Пример 4. Удаление всего набора тегов для ресурса</span><span class="sxs-lookup"><span data-stu-id="4c4f8-127">Example 4: Deletes the entire set of tags on a resource</span></span>

```powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -PassThru

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="4c4f8-128">Эта команда удаляет весь набор тегов для ресурса с помощью {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="4c4f8-129">Он возвращает удаленный проект при передаче в "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="4c4f8-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="4c4f8-130">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c4f8-130">PARAMETERS</span></span>

### <span data-ttu-id="4c4f8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c4f8-131">-DefaultProfile</span></span>
<span data-ttu-id="4c4f8-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c4f8-133">-Name</span><span class="sxs-lookup"><span data-stu-id="4c4f8-133">-Name</span></span>
<span data-ttu-id="4c4f8-134">Имя предопределяемого тега, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="4c4f8-135">По умолчанию **remove-AzTag** удаляет указанный тег и все его значения.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="4c4f8-136">Чтобы удалить выбранные значения, но не удалить тег, используйте параметр *Value.*</span><span class="sxs-lookup"><span data-stu-id="4c4f8-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f8-137">-Value</span><span class="sxs-lookup"><span data-stu-id="4c4f8-137">-Value</span></span>
<span data-ttu-id="4c4f8-138">Удаляет указанные значения из предопределяемого тега, но не удаляет его.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: RemovePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f8-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c4f8-139">-ResourceId</span></span>
<span data-ttu-id="4c4f8-140">Идентификатор ресурса для сущности с тегами.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="4c4f8-141">Ресурс, группа ресурсов или подписка могут быть помечены тегами.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-141">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f8-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c4f8-142">-PassThru</span></span>
<span data-ttu-id="4c4f8-143">Возвращает объект, который представляет удаленный тег или итоговую метку с удаленным значением.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="4c4f8-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c4f8-144">-Confirm</span></span>
<span data-ttu-id="4c4f8-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f8-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c4f8-146">-WhatIf</span></span>
<span data-ttu-id="4c4f8-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c4f8-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c4f8-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c4f8-149">CommonParameters</span></span>
<span data-ttu-id="4c4f8-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c4f8-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c4f8-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c4f8-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c4f8-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4c4f8-152">INPUTS</span></span>

### <span data-ttu-id="4c4f8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="4c4f8-153">System.String</span></span>

### <span data-ttu-id="4c4f8-154">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4c4f8-154">System.String[]</span></span>

### <span data-ttu-id="4c4f8-155">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4c4f8-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4c4f8-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4c4f8-156">OUTPUTS</span></span>

### <span data-ttu-id="4c4f8-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="4c4f8-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="4c4f8-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4c4f8-158">NOTES</span></span>

## <span data-ttu-id="4c4f8-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c4f8-159">RELATED LINKS</span></span>

[<span data-ttu-id="4c4f8-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="4c4f8-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="4c4f8-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="4c4f8-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="4c4f8-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="4c4f8-162">Update-AzTag</span></span>](./Update-AzTag.md)