---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316348"
---
# <span data-ttu-id="9558d-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="9558d-101">New-AzTag</span></span>

## <span data-ttu-id="9558d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9558d-102">SYNOPSIS</span></span>
<span data-ttu-id="9558d-103">Создание предопределенного тега Azure или добавление значений в существующий тег | Создает или обновляет весь набор тегов на ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="9558d-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="9558d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9558d-104">SYNTAX</span></span>

### <span data-ttu-id="9558d-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="9558d-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9558d-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9558d-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="9558d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9558d-107">DESCRIPTION</span></span>

<span data-ttu-id="9558d-108">**CreatePredefinedTagSet** : командлет **New-AzTag** создает предопределенный тег Azure с необязательным предварительно заданным значением.</span><span class="sxs-lookup"><span data-stu-id="9558d-108">**CreatePredefinedTagSet** : The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="9558d-109">Кроме того, с ее помощью можно добавлять дополнительные значения для существующих предопределенных тегов.</span><span class="sxs-lookup"><span data-stu-id="9558d-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="9558d-110">Чтобы создать предопределенный тег, введите уникальное имя тега.</span><span class="sxs-lookup"><span data-stu-id="9558d-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="9558d-111">Чтобы добавить значение в существующий предопределенный тег, укажите имя существующего тега и новое значение.</span><span class="sxs-lookup"><span data-stu-id="9558d-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="9558d-112">Этот командлет возвращает объект, который представляет новый или измененный тег со значениями и количеством ресурсов, к которым он был применен.</span><span class="sxs-lookup"><span data-stu-id="9558d-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="9558d-113">Модуль тегов Azure, частью которого является **New-AzTag** , может помочь вам управлять стандартными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="9558d-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="9558d-114">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="9558d-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="9558d-115">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="9558d-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="9558d-116">Чтобы применить предопределенный тег к ресурсу или группе ресурсов, используйте параметр *Tag* командлета New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="9558d-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="9558d-117">Чтобы найти группы ресурсов с указанным именем тега или именем и значением, используйте параметр *Tag* для командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9558d-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="9558d-118">Каждый тег имеет имя.</span><span class="sxs-lookup"><span data-stu-id="9558d-118">Every tag has a name.</span></span>
<span data-ttu-id="9558d-119">Значения не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="9558d-119">The values are optional.</span></span>
<span data-ttu-id="9558d-120">Предопределенный тег Azure может иметь несколько значений, но при применении тега к ресурсу или группе ресурсов следует применять имя тега и только одно из его значений.</span><span class="sxs-lookup"><span data-stu-id="9558d-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="9558d-121">Например, вы можете создать готовый тег отдела со значением для каждого отдела, например "Финансы", "Отдел кадров" и т. д.</span><span class="sxs-lookup"><span data-stu-id="9558d-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="9558d-122">Когда вы примените к ресурсу тег отдела, вы можете применить только одно предопределенное значение, например "процент".</span><span class="sxs-lookup"><span data-stu-id="9558d-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="9558d-123">**CreateByResourceIdParameterSet** : командлет **New-AzTag** с **ResourceId** создает или обновляет весь набор тегов на ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="9558d-123">**CreateByResourceIdParameterSet** : The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="9558d-124">Эта операция позволяет добавить или заменить весь набор тегов в указанном ресурсе или подписке.</span><span class="sxs-lookup"><span data-stu-id="9558d-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="9558d-125">Для указанной сущности может быть не более 50 тегов.</span><span class="sxs-lookup"><span data-stu-id="9558d-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="9558d-126">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9558d-126">EXAMPLES</span></span>

### <span data-ttu-id="9558d-127">Пример 1: создание предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="9558d-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="9558d-128">Эта команда создает предопределенный тег с именем FY2015.</span><span class="sxs-lookup"><span data-stu-id="9558d-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="9558d-129">У этого тега нет значений.</span><span class="sxs-lookup"><span data-stu-id="9558d-129">This tag has no values.</span></span>
<span data-ttu-id="9558d-130">Вы можете применить к ресурсу или группе ресурсов тег без значений или использовать **New-AzTag** для добавления значений в тег.</span><span class="sxs-lookup"><span data-stu-id="9558d-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="9558d-131">Вы также можете указать значение при применении тега к ресурсу или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9558d-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="9558d-132">Пример 2: создание предопределенного тега со значением</span><span class="sxs-lookup"><span data-stu-id="9558d-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="9558d-133">Эта команда создает предопределенный тег с именем Department и значением Finance.</span><span class="sxs-lookup"><span data-stu-id="9558d-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="9558d-134">Пример 3: Добавление значения к стандартному тегу</span><span class="sxs-lookup"><span data-stu-id="9558d-134">Example 3: Add a value to a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 
PS C:\>New-AzTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="9558d-135">Эти команды создают предопределенный тег отдела с двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="9558d-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="9558d-136">Если имя тега существует, **New-AzTag** добавляет значение в существующий тег вместо создания нового.</span><span class="sxs-lookup"><span data-stu-id="9558d-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="9558d-137">Пример 4: использование предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="9558d-137">Example 4: Use a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 
PS C:\>Set-AzResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
Name:      EngineerBlog
Location:  East US
Resources: 
            
  Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US
    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001 
PS C:\>Get-AzTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 
PS C:\>Get-AzResourceGroup -Tag @{Name="CostCenter"}
Name:      EngineerBlog
Location:  East US
Resources: 
     Name             Type                     Location
    ===============  =======================  ========
    EngineerBlog     Microsoft.Web/sites      West US

    EngSvr01         Microsoft.Sql/servers    West US
    EngDB02          Microsoft.Sql/databases  West US
Tags: 
    Name         Value
    ==========   =====
    CostCenter   0001
```

<span data-ttu-id="9558d-138">В этом примере команды создают и используют предопределенный тег.</span><span class="sxs-lookup"><span data-stu-id="9558d-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="9558d-139">Пример 5: создание или обновление всего набора тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="9558d-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

```powershell
PS C:\>$Tags = @{"tagKey1"="tagValue1"; "tagKey2"="tagValue2"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId} -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="9558d-140">Эта команда создает или обновляет весь набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="9558d-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="9558d-141">Пример 6: создание или обновление всего набора тегов на ресурсе</span><span class="sxs-lookup"><span data-stu-id="9558d-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

```powershell
PS C:\>$Tags = @{"Dept"="Finance"; "Status"="Normal"}
PS C:\>New-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1 -Tag $Tags

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="9558d-142">Эта команда создает или обновляет весь набор тегов в ресурсе с помощью {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="9558d-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="9558d-143">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9558d-143">PARAMETERS</span></span>

### <span data-ttu-id="9558d-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9558d-144">-DefaultProfile</span></span>
<span data-ttu-id="9558d-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9558d-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9558d-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9558d-146">-Name</span></span>
<span data-ttu-id="9558d-147">Задает предопределенное имя тега.</span><span class="sxs-lookup"><span data-stu-id="9558d-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="9558d-148">Чтобы создать новый предопределенный тег, введите уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="9558d-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="9558d-149">Чтобы добавить значение в существующий тег, введите имя существующего тега.</span><span class="sxs-lookup"><span data-stu-id="9558d-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="9558d-150">Если существующий предопределенный тег имеет указанное имя, **New-AzTag** добавляет указанное значение, если оно есть, в тег с этим именем вместо создания нового тега.</span><span class="sxs-lookup"><span data-stu-id="9558d-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9558d-151">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="9558d-151">-Value</span></span>
<span data-ttu-id="9558d-152">Задает предварительно определенное значение тега.</span><span class="sxs-lookup"><span data-stu-id="9558d-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="9558d-153">Предопределенные Теги могут содержать несколько значений, но в каждой из них можно вводить только одно значение.</span><span class="sxs-lookup"><span data-stu-id="9558d-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="9558d-154">Этот параметр является необязательным, поскольку теги могут иметь имена без значений.</span><span class="sxs-lookup"><span data-stu-id="9558d-154">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePredefinedTagParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9558d-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9558d-155">-ResourceId</span></span>
<span data-ttu-id="9558d-156">Идентификатор ресурса для сущности, на которую размещается тег.</span><span class="sxs-lookup"><span data-stu-id="9558d-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="9558d-157">Ресурс, Группа ресурсов или подписка может быть помечены.</span><span class="sxs-lookup"><span data-stu-id="9558d-157">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9558d-158">-Тег</span><span class="sxs-lookup"><span data-stu-id="9558d-158">-Tag</span></span>
<span data-ttu-id="9558d-159">Теги, помещаемые в ресурс.</span><span class="sxs-lookup"><span data-stu-id="9558d-159">The tags to put on the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateByResourceIdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9558d-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9558d-160">-Confirm</span></span>
<span data-ttu-id="9558d-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9558d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9558d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9558d-162">-WhatIf</span></span>
<span data-ttu-id="9558d-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9558d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9558d-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9558d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9558d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9558d-165">CommonParameters</span></span>
<span data-ttu-id="9558d-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9558d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9558d-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9558d-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9558d-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9558d-168">INPUTS</span></span>

### <span data-ttu-id="9558d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="9558d-169">System.String</span></span>

### <span data-ttu-id="9558d-170">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9558d-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9558d-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9558d-171">OUTPUTS</span></span>

### <span data-ttu-id="9558d-172">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="9558d-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="9558d-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="9558d-173">NOTES</span></span>

## <span data-ttu-id="9558d-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9558d-174">RELATED LINKS</span></span>

[<span data-ttu-id="9558d-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="9558d-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="9558d-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="9558d-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="9558d-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="9558d-177">Update-AzTag</span></span>](./Update-AzTag.md)