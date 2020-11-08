---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 1bbb2494ddbe6d355f38a719e3eaf08622b80169
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066258"
---
# <span data-ttu-id="fbb52-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="fbb52-101">Remove-AzTag</span></span>

## <span data-ttu-id="fbb52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbb52-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb52-103">Удаление предопределенных тегов или значений Azure | Удаляет весь набор тегов на ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="fbb52-103">Deletes predefined Azure tags or values | Deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="fbb52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbb52-104">SYNTAX</span></span>

### <span data-ttu-id="fbb52-105">RemovePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb52-105">RemovePredefinedTagParameterSet</span></span>

```powershell
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbb52-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fbb52-106">RemoveByResourceIdParameterSet</span></span>

```powershell
Remove-AzTag
   -ResourceId <String>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="fbb52-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb52-107">DESCRIPTION</span></span>

<span data-ttu-id="fbb52-108">**RemovePredefinedTagSet** : командлет **Remove-AzTag** удаляет из подписки предопределенные Теги и значения Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb52-108">**RemovePredefinedTagSet** : The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="fbb52-109">Для удаления определенных значений из предопределенного тега используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="fbb52-109">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="fbb52-110">По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения. Вы не можете удалить тег или значение, которые в настоящее время применены к ресурсам или группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbb52-110">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="fbb52-111">Перед использованием **Remove-AzTag** используйте параметр *Tag* командлета Set-AzResourceGroup для удаления тега или значений из ресурса или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fbb52-111">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="fbb52-112">Модуль тегов Azure, который **Remove-AzTag** является частью, может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb52-112">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="fbb52-113">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="fbb52-113">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="fbb52-114">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="fbb52-114">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

<span data-ttu-id="fbb52-115">**RemoveByResourceIdParameterSet** : командлет **Remove-AzTag** с **ResourceId** удаляет весь набор тегов на ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="fbb52-115">**RemoveByResourceIdParameterSet** : The **Remove-AzTag** cmdlet with a **ResourceId** deletes the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="fbb52-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbb52-116">EXAMPLES</span></span>

### <span data-ttu-id="fbb52-117">Пример 1: Удаление предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="fbb52-117">Example 1: Delete a predefined tag</span></span>
```powershell
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="fbb52-118">Эта команда удаляет предопределенный тег с именем Department и все его значения.</span><span class="sxs-lookup"><span data-stu-id="fbb52-118">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="fbb52-119">Если тег применен к ресурсам или группам ресурсов, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbb52-119">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="fbb52-120">Пример 2: Удаление значения из предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="fbb52-120">Example 2: Delete a value from a predefined tag</span></span>
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

<span data-ttu-id="fbb52-121">Эта команда удаляет значение HumanResources из предопределенного тега отдела.</span><span class="sxs-lookup"><span data-stu-id="fbb52-121">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="fbb52-122">Тег не удаляется.</span><span class="sxs-lookup"><span data-stu-id="fbb52-122">It does not delete the tag.</span></span>
<span data-ttu-id="fbb52-123">Если значение было применено к ресурсам или группам ресурсов, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="fbb52-123">If the value has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="fbb52-124">Пример 3: удаление всего набора тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="fbb52-124">Example 3: Deletes the entire set of tags on a subscription</span></span>

``` powershell
PS C:\>Remove-AzTag -ResourceId /subscriptions/{subId}
```

<span data-ttu-id="fbb52-125">Эта команда удаляет весь набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="fbb52-125">This command deletes the entire set of tags on the subscription with {subId}.</span></span> <span data-ttu-id="fbb52-126">Он не будет возвращать объект, который удаляется, если не передается значение "-пропустить".</span><span class="sxs-lookup"><span data-stu-id="fbb52-126">It will not return the object deleted if not passing in "-PassThru".</span></span>

### <span data-ttu-id="fbb52-127">Пример 4: удаление всего набора тегов на ресурсе</span><span class="sxs-lookup"><span data-stu-id="fbb52-127">Example 4: Deletes the entire set of tags on a resource</span></span>

``` powershell
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

<span data-ttu-id="fbb52-128">Эта команда удаляет весь набор тегов в ресурсе с помощью {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="fbb52-128">This command deletes the entire set of tags on the resource with {resourceId}.</span></span> <span data-ttu-id="fbb52-129">Функция возвращает удаленную oject при передаче в "-PassThru".</span><span class="sxs-lookup"><span data-stu-id="fbb52-129">It returns the deleted oject when passing in "-PassThru".</span></span>

## <span data-ttu-id="fbb52-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbb52-130">PARAMETERS</span></span>

### <span data-ttu-id="fbb52-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb52-131">-DefaultProfile</span></span>
<span data-ttu-id="fbb52-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fbb52-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbb52-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fbb52-133">-Name</span></span>
<span data-ttu-id="fbb52-134">Указывает имя предопределенного тега, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fbb52-134">Specifies the Name of the predefined tag to remove.</span></span>
<span data-ttu-id="fbb52-135">По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения.</span><span class="sxs-lookup"><span data-stu-id="fbb52-135">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="fbb52-136">Чтобы удалить выделенные значения, но не удалять тег, используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="fbb52-136">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="fbb52-137">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="fbb52-137">-Value</span></span>
<span data-ttu-id="fbb52-138">Удаляет указанные значения из предопределенного тега, но не удаляет тег.</span><span class="sxs-lookup"><span data-stu-id="fbb52-138">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="fbb52-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbb52-139">-ResourceId</span></span>
<span data-ttu-id="fbb52-140">Идентификатор ресурса для помеченной сущности.</span><span class="sxs-lookup"><span data-stu-id="fbb52-140">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="fbb52-141">Ресурс, Группа ресурсов или подписка может быть помечены.</span><span class="sxs-lookup"><span data-stu-id="fbb52-141">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="fbb52-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbb52-142">-PassThru</span></span>
<span data-ttu-id="fbb52-143">Возвращает объект, который представляет удаленный тег или получившийся тег с удаленным значением.</span><span class="sxs-lookup"><span data-stu-id="fbb52-143">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="fbb52-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbb52-144">-Confirm</span></span>
<span data-ttu-id="fbb52-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb52-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbb52-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbb52-146">-WhatIf</span></span>
<span data-ttu-id="fbb52-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fbb52-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbb52-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fbb52-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbb52-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb52-149">CommonParameters</span></span>
<span data-ttu-id="fbb52-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbb52-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb52-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbb52-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb52-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbb52-152">INPUTS</span></span>

### <span data-ttu-id="fbb52-153">System. String</span><span class="sxs-lookup"><span data-stu-id="fbb52-153">System.String</span></span>

### <span data-ttu-id="fbb52-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="fbb52-154">System.String[]</span></span>

### <span data-ttu-id="fbb52-155">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fbb52-155">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbb52-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbb52-156">OUTPUTS</span></span>

### <span data-ttu-id="fbb52-157">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="fbb52-157">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="fbb52-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbb52-158">NOTES</span></span>

## <span data-ttu-id="fbb52-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbb52-159">RELATED LINKS</span></span>

[<span data-ttu-id="fbb52-160">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="fbb52-160">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="fbb52-161">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="fbb52-161">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="fbb52-162">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="fbb52-162">Update-AzTag</span></span>](./Update-AzTag.md)
