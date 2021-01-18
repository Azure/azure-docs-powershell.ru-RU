---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTag.md
ms.openlocfilehash: 937ac50ac34f8b04912a0d500dedb5b490806b1a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505194"
---
# <span data-ttu-id="834aa-101">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="834aa-101">New-AzTag</span></span>

## <span data-ttu-id="834aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="834aa-102">SYNOPSIS</span></span>
<span data-ttu-id="834aa-103">Создание предопределяемой тега Azure или сужит значения к существующему тегу | Создает или обновляет весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="834aa-103">Creates a predefined Azure tag or adds values to an existing tag | Creates or updates the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="834aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="834aa-104">SYNTAX</span></span>

### <span data-ttu-id="834aa-105">CreatePredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="834aa-105">CreatePredefinedTagParameterSet</span></span>

```powershell
New-AzTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="834aa-106">CreateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="834aa-106">CreateByResourceIdParameterSet</span></span>

```powershell
New-AzTag
   -ResourceId <String>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="834aa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="834aa-107">DESCRIPTION</span></span>

<span data-ttu-id="834aa-108">**CreatePredefinedTagSet:** командлет **New-AzTag** создает готовый тег Azure с необязательным предопределительным значением.</span><span class="sxs-lookup"><span data-stu-id="834aa-108">**CreatePredefinedTagSet**: The **New-AzTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="834aa-109">С ее помощью также можно добавлять дополнительные значения к существующим предопределяемой метке.</span><span class="sxs-lookup"><span data-stu-id="834aa-109">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="834aa-110">Чтобы создать предопределный тег, введите уникальное имя тега.</span><span class="sxs-lookup"><span data-stu-id="834aa-110">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="834aa-111">Чтобы добавить значение к существующему предопределеальному тегу, укажите имя существующего и новое значение.</span><span class="sxs-lookup"><span data-stu-id="834aa-111">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>
<span data-ttu-id="834aa-112">Этот командлет возвращает объект, который представляет новый или измененный тег со значениями и количеством ресурсов, к которым он был применен.</span><span class="sxs-lookup"><span data-stu-id="834aa-112">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>
<span data-ttu-id="834aa-113">Модуль "Теги Azure", который входит в **состав тега New-AzTag,** помогает управлять предопределенами тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="834aa-113">The Azure Tags module that **New-AzTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="834aa-114">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="834aa-114">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="834aa-115">Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.</span><span class="sxs-lookup"><span data-stu-id="834aa-115">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="834aa-116">Чтобы применить предопределяный тег к ресурсу или группе ресурсов, используйте параметр *"Тег"* New-AzTag командлета.</span><span class="sxs-lookup"><span data-stu-id="834aa-116">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="834aa-117">Для поиска групп ресурсов с указанным именем или именем и значением тега используйте параметр *Tag* Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="834aa-117">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="834aa-118">У каждого тега есть имя.</span><span class="sxs-lookup"><span data-stu-id="834aa-118">Every tag has a name.</span></span>
<span data-ttu-id="834aa-119">Значения необязательны.</span><span class="sxs-lookup"><span data-stu-id="834aa-119">The values are optional.</span></span>
<span data-ttu-id="834aa-120">Предопределяемая метка Azure может иметь несколько значений, но при применении тега к ресурсу или группе ресурсов нужно применить имя тега и только одно из его значений.</span><span class="sxs-lookup"><span data-stu-id="834aa-120">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="834aa-121">Например, можно создать предопределный тег "Отдел" со значением для каждого отдела, например финансового, отдела кадров и ИТ-отдела.</span><span class="sxs-lookup"><span data-stu-id="834aa-121">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="834aa-122">При применении тега "Отдел" к ресурсу применяется только одно заранее задаированное значение, например "Финансы".</span><span class="sxs-lookup"><span data-stu-id="834aa-122">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

<span data-ttu-id="834aa-123">**CreateByResourceIdParameterSet:** командлет **New-AzTag** с **ResourceId** создает или обновляет весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="834aa-123">**CreateByResourceIdParameterSet**: The **New-AzTag** cmdlet with a **ResourceId** creates or updates the entire set of tags on a resource or subscription.</span></span>
<span data-ttu-id="834aa-124">Эта операция позволяет добавить или заменить весь набор тегов для указанного ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="834aa-124">This operation allows adding or replacing the entire set of tags on the specified resource or subscription.</span></span> <span data-ttu-id="834aa-125">Указанное лицо может иметь не более 50 тегов.</span><span class="sxs-lookup"><span data-stu-id="834aa-125">The specified entity can have a maximum of 50 tags.</span></span>

## <span data-ttu-id="834aa-126">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="834aa-126">EXAMPLES</span></span>

### <span data-ttu-id="834aa-127">Пример 1. Создание предопределеного тега</span><span class="sxs-lookup"><span data-stu-id="834aa-127">Example 1: Create a predefined tag</span></span>
```powershell
PS C:\>New-AzTag -Name "FY2015"
                                
Name   ValuesTable Count Values 
----   ----------- ----- ------
FY2015             0     {}
```

<span data-ttu-id="834aa-128">Эта команда создает предопределен тег с именем "ФГ2015".</span><span class="sxs-lookup"><span data-stu-id="834aa-128">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="834aa-129">Этот тег не имеет значений.</span><span class="sxs-lookup"><span data-stu-id="834aa-129">This tag has no values.</span></span>
<span data-ttu-id="834aa-130">К ресурсу или группе ресурсов можно применить тег без значений или добавить к тегу значения с помощью **new-AzTag.**</span><span class="sxs-lookup"><span data-stu-id="834aa-130">You can apply a tag with no values to a resource or resource group, or use **New-AzTag** to add values to the tag.</span></span>
<span data-ttu-id="834aa-131">Вы также можете указать значение при применении тега к ресурсу или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="834aa-131">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="834aa-132">Пример 2. Создание предопределеного тега со значением</span><span class="sxs-lookup"><span data-stu-id="834aa-132">Example 2: Create a predefined tag with a value</span></span>
```powershell
PS C:\>New-AzTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="834aa-133">Эта команда создает предопределяный тег "Отдел" со значением "Финансы".</span><span class="sxs-lookup"><span data-stu-id="834aa-133">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="834aa-134">Пример 3. Добавление значения к предопределему тегу</span><span class="sxs-lookup"><span data-stu-id="834aa-134">Example 3: Add a value to a predefined tag</span></span>
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

<span data-ttu-id="834aa-135">Эти команды создают предопределяный тег "Отдел" с двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="834aa-135">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="834aa-136">Если имя тега существует, **New-AzTag** добавляет значение к существующему тегу, а не создает новый.</span><span class="sxs-lookup"><span data-stu-id="834aa-136">If the tag name exists, **New-AzTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="834aa-137">Пример 4. Использование предопределеного тега</span><span class="sxs-lookup"><span data-stu-id="834aa-137">Example 4: Use a predefined tag</span></span>
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

<span data-ttu-id="834aa-138">С помощью команд в этом примере можно создать и использовать предопределяный тег.</span><span class="sxs-lookup"><span data-stu-id="834aa-138">The commands in this example create and use a predefined tag.</span></span>

### <span data-ttu-id="834aa-139">Пример 5. Создание или обновление всего набора тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="834aa-139">Example 5: Creates or updates the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="834aa-140">Эта команда создает или обновляет весь набор тегов в подписке {subId}.</span><span class="sxs-lookup"><span data-stu-id="834aa-140">This command creates or updates the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="834aa-141">Пример 6. Создание или обновление всего набора тегов для ресурса</span><span class="sxs-lookup"><span data-stu-id="834aa-141">Example 6: Creates or updates the entire set of tags on a resource</span></span>

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

<span data-ttu-id="834aa-142">Эта команда создает или обновляет весь набор тегов на ресурсе с помощью {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="834aa-142">This command creates or updates the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="834aa-143">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="834aa-143">PARAMETERS</span></span>

### <span data-ttu-id="834aa-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="834aa-144">-DefaultProfile</span></span>
<span data-ttu-id="834aa-145">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="834aa-145">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="834aa-146">-Name</span><span class="sxs-lookup"><span data-stu-id="834aa-146">-Name</span></span>
<span data-ttu-id="834aa-147">Определяет предопределное имя тега.</span><span class="sxs-lookup"><span data-stu-id="834aa-147">Specifies the predefined tag name.</span></span>
<span data-ttu-id="834aa-148">Чтобы создать новый предопределный тег, введите уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="834aa-148">To create a new predefined tag, enter a unique name.</span></span>
<span data-ttu-id="834aa-149">Чтобы добавить значение к существующему тегу, введите его имя.</span><span class="sxs-lookup"><span data-stu-id="834aa-149">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="834aa-150">Если имя существующего предопределяемого тега задано, **New-AzTag** добавляет указанное значение (если имеется) к тегу с этим именем, а не создает новый.</span><span class="sxs-lookup"><span data-stu-id="834aa-150">If an existing predefined tag has the specified name, **New-AzTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

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

### <span data-ttu-id="834aa-151">-Value</span><span class="sxs-lookup"><span data-stu-id="834aa-151">-Value</span></span>
<span data-ttu-id="834aa-152">Определяет заранее определенное значение тега.</span><span class="sxs-lookup"><span data-stu-id="834aa-152">Specifies a predefined tag value.</span></span>
<span data-ttu-id="834aa-153">Предопределять теги могут иметь несколько значений, но в каждой команде можно ввести только одно значение.</span><span class="sxs-lookup"><span data-stu-id="834aa-153">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="834aa-154">Этот параметр необязателен, так как теги могут иметь имена без значений.</span><span class="sxs-lookup"><span data-stu-id="834aa-154">This parameter is optional, because tags can have names without values.</span></span>

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

### <span data-ttu-id="834aa-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="834aa-155">-ResourceId</span></span>
<span data-ttu-id="834aa-156">Идентификатор ресурса для сущности, помеченной тегом.</span><span class="sxs-lookup"><span data-stu-id="834aa-156">The resource identifier for the entity being tagged.</span></span> <span data-ttu-id="834aa-157">Ресурс, группа ресурсов или подписка могут быть помечены тегами.</span><span class="sxs-lookup"><span data-stu-id="834aa-157">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="834aa-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="834aa-158">-Tag</span></span>
<span data-ttu-id="834aa-159">Теги, которые нужно поместить на ресурс.</span><span class="sxs-lookup"><span data-stu-id="834aa-159">The tags to put on the resource.</span></span>

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

### <span data-ttu-id="834aa-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="834aa-160">-Confirm</span></span>
<span data-ttu-id="834aa-161">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="834aa-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="834aa-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="834aa-162">-WhatIf</span></span>
<span data-ttu-id="834aa-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="834aa-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="834aa-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="834aa-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="834aa-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="834aa-165">CommonParameters</span></span>
<span data-ttu-id="834aa-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="834aa-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="834aa-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="834aa-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="834aa-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="834aa-168">INPUTS</span></span>

### <span data-ttu-id="834aa-169">System.String</span><span class="sxs-lookup"><span data-stu-id="834aa-169">System.String</span></span>

### <span data-ttu-id="834aa-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="834aa-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="834aa-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="834aa-171">OUTPUTS</span></span>

### <span data-ttu-id="834aa-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="834aa-172">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="834aa-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="834aa-173">NOTES</span></span>

## <span data-ttu-id="834aa-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="834aa-174">RELATED LINKS</span></span>

[<span data-ttu-id="834aa-175">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="834aa-175">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="834aa-176">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="834aa-176">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="834aa-177">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="834aa-177">Update-AzTag</span></span>](./Update-AzTag.md)