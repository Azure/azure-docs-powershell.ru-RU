---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 23DB0AD2-7EB7-4373-BB8D-BB6CB651DD54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/New-AzureRmTag.md
ms.openlocfilehash: b5b7356a2cda001bb615700b38657cc0d3249ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733596"
---
# <span data-ttu-id="1f918-101">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f918-101">New-AzureRmTag</span></span>

## <span data-ttu-id="1f918-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f918-102">SYNOPSIS</span></span>
<span data-ttu-id="1f918-103">Создает предопределенный тег Azure или добавляет значения в существующий тег.</span><span class="sxs-lookup"><span data-stu-id="1f918-103">Creates a predefined Azure tag or adds values to an existing tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f918-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f918-104">SYNTAX</span></span>

```
New-AzureRmTag [-Name] <String> [[-Value] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f918-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f918-105">DESCRIPTION</span></span>
<span data-ttu-id="1f918-106">Командлет **New-AzureRmTag** создает предопределенный тег Azure с необязательным предварительно заданным значением.</span><span class="sxs-lookup"><span data-stu-id="1f918-106">The **New-AzureRmTag** cmdlet creates a predefined Azure tag with an optional predefined value.</span></span>
<span data-ttu-id="1f918-107">Кроме того, с ее помощью можно добавлять дополнительные значения для существующих предопределенных тегов.</span><span class="sxs-lookup"><span data-stu-id="1f918-107">You can also use it to add additional values to existing predefined tags.</span></span>
<span data-ttu-id="1f918-108">Чтобы создать предопределенный тег, введите уникальное имя тега.</span><span class="sxs-lookup"><span data-stu-id="1f918-108">To create a predefined tag, enter a unique tag name.</span></span>
<span data-ttu-id="1f918-109">Чтобы добавить значение в существующий предопределенный тег, укажите имя существующего тега и новое значение.</span><span class="sxs-lookup"><span data-stu-id="1f918-109">To add a value to an existing predefined tag, specify the name of the existing tag and the new value.</span></span>

<span data-ttu-id="1f918-110">Этот командлет возвращает объект, который представляет новый или измененный тег со значениями и количеством ресурсов, к которым он был применен.</span><span class="sxs-lookup"><span data-stu-id="1f918-110">This cmdlet returns an object that represents the new or modified tag with its values and the number of resources to which it has been applied.</span></span>

<span data-ttu-id="1f918-111">Модуль тегов Azure, частью которого является **New-AzureRmTag** , может помочь вам управлять стандартными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="1f918-111">The Azure Tags module that **New-AzureRmTag** is part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="1f918-112">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="1f918-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="1f918-113">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="1f918-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="1f918-114">Если подписка содержит любые предопределенные теги, вы не можете применить неопределенные теги или значения к любому ресурсу или группе ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="1f918-114">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="1f918-115">Чтобы применить предопределенный тег к ресурсу или группе ресурсов, используйте параметр *Tag* командлета New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="1f918-115">To apply a predefined tag to a resource or resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="1f918-116">Чтобы найти группы ресурсов с указанным именем тега или именем и значением, используйте параметр *Tag* для командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1f918-116">To search for resource groups with a specified tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

<span data-ttu-id="1f918-117">Каждый тег имеет имя.</span><span class="sxs-lookup"><span data-stu-id="1f918-117">Every tag has a name.</span></span>
<span data-ttu-id="1f918-118">Значения не являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="1f918-118">The values are optional.</span></span>
<span data-ttu-id="1f918-119">Предопределенный тег Azure может иметь несколько значений, но при применении тега к ресурсу или группе ресурсов следует применять имя тега и только одно из его значений.</span><span class="sxs-lookup"><span data-stu-id="1f918-119">A predefined Azure tag can have multiple values, but when you apply the tag to a resource or resource group, you apply the tag name and only one of its values.</span></span>
<span data-ttu-id="1f918-120">Например, вы можете создать готовый тег отдела со значением для каждого отдела, например "Финансы", "Отдел кадров" и т. д.</span><span class="sxs-lookup"><span data-stu-id="1f918-120">For example, you can create a predefined Department tag with a value for each department, such as Finance, Human Resources, and IT.</span></span>
<span data-ttu-id="1f918-121">Когда вы примените к ресурсу тег отдела, вы можете применить только одно предопределенное значение, например "процент".</span><span class="sxs-lookup"><span data-stu-id="1f918-121">When you apply the Department tag to a resource, you apply only one predefined value, such as Finance.</span></span>

## <span data-ttu-id="1f918-122">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f918-122">EXAMPLES</span></span>

### <span data-ttu-id="1f918-123">Пример 1: создание предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="1f918-123">Example 1: Create a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "FY2015"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====

        Finance     0
```

<span data-ttu-id="1f918-124">Эта команда создает предопределенный тег с именем FY2015.</span><span class="sxs-lookup"><span data-stu-id="1f918-124">This command creates a predefined tag named FY2015.</span></span>
<span data-ttu-id="1f918-125">У этого тега нет значений.</span><span class="sxs-lookup"><span data-stu-id="1f918-125">This tag has no values.</span></span>
<span data-ttu-id="1f918-126">Вы можете применить к ресурсу или группе ресурсов тег без значений или использовать **New-AzureRmTag** для добавления значений в тег.</span><span class="sxs-lookup"><span data-stu-id="1f918-126">You can apply a tag with no values to a resource or resource group, or use **New-AzureRmTag** to add values to the tag.</span></span>
<span data-ttu-id="1f918-127">Вы также можете указать значение при применении тега к ресурсу или группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1f918-127">You can also specify a value when you apply the tag to the resource or resource group.</span></span>

### <span data-ttu-id="1f918-128">Пример 2: создание предопределенного тега со значением</span><span class="sxs-lookup"><span data-stu-id="1f918-128">Example 2: Create a predefined tag with a value</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 

        Name        Count
        =========   =====
        Finance     0
```

<span data-ttu-id="1f918-129">Эта команда создает предопределенный тег с именем Department и значением Finance.</span><span class="sxs-lookup"><span data-stu-id="1f918-129">This command creates a predefined tag named Department with a value of Finance.</span></span>

### <span data-ttu-id="1f918-130">Пример 3: Добавление значения к стандартному тегу</span><span class="sxs-lookup"><span data-stu-id="1f918-130">Example 3: Add a value to a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "Department" -Value "Finance"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0 PS C:\>New-AzureRmTag -Name "Department" -Value "IT"
Name:   Department
Count:  0
Values: 
        Name        Count
        =========   =====
        Finance     0
        IT          0
```

<span data-ttu-id="1f918-131">Эти команды создают предопределенный тег отдела с двумя значениями.</span><span class="sxs-lookup"><span data-stu-id="1f918-131">These commands create a predefined tag named Department with two values.</span></span>
<span data-ttu-id="1f918-132">Если имя тега существует, **New-AzureRmTag** добавляет значение в существующий тег вместо создания нового.</span><span class="sxs-lookup"><span data-stu-id="1f918-132">If the tag name exists, **New-AzureRmTag** adds the value to the existing tag instead of creating a new one.</span></span>

### <span data-ttu-id="1f918-133">Пример 4: использование предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="1f918-133">Example 4: Use a predefined tag</span></span>
```
PS C:\>New-AzureRmTag -Name "CostCenter" -Value "0001"
Name:   CostCenter
Count:  0
Values: 
        Name        Count
        =========   =====
        0001        0 PS C:\>Set-AzureRmResourceGroup -Name "EngineerBlog" -Tag @{Name="CostCenter";Value="0001"}
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
    CostCenter   0001 PS C:\>Get-AzureRmTag -Name "CostCenter"
Name:   CostCenter
Count:  1
Values: 
        Name        Count
        =========   =====
        0001        1 PS C:\>Get-AzureRmResourceGroup -Tag @{Name="CostCenter"}
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

<span data-ttu-id="1f918-134">В этом примере команды создают и используют предопределенный тег.</span><span class="sxs-lookup"><span data-stu-id="1f918-134">The commands in this example create and use a predefined tag.</span></span>

## <span data-ttu-id="1f918-135">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f918-135">PARAMETERS</span></span>

### <span data-ttu-id="1f918-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1f918-136">-Name</span></span>
<span data-ttu-id="1f918-137">Указывает имя тега.</span><span class="sxs-lookup"><span data-stu-id="1f918-137">Specifies the tag name.</span></span>
<span data-ttu-id="1f918-138">Чтобы создать новый предопределенный тег, введите уникальное имя.</span><span class="sxs-lookup"><span data-stu-id="1f918-138">To create a new predefined tag, enter a unique name.</span></span>

<span data-ttu-id="1f918-139">Чтобы добавить значение в существующий тег, введите имя существующего тега.</span><span class="sxs-lookup"><span data-stu-id="1f918-139">To add a value to an existing tag, enter the name of the existing tag.</span></span>
<span data-ttu-id="1f918-140">Если существующий предопределенный тег имеет указанное имя, **New-AzureRmTag** добавляет указанное значение, если оно есть, в тег с этим именем вместо создания нового тега.</span><span class="sxs-lookup"><span data-stu-id="1f918-140">If an existing predefined tag has the specified name, **New-AzureRmTag** adds the specified value, if any, to the tag with that name instead of creating a new tag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f918-141">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="1f918-141">-Value</span></span>
<span data-ttu-id="1f918-142">Задает значение тега.</span><span class="sxs-lookup"><span data-stu-id="1f918-142">Specifies a tag value.</span></span>
<span data-ttu-id="1f918-143">Предопределенные Теги могут содержать несколько значений, но в каждой из них можно вводить только одно значение.</span><span class="sxs-lookup"><span data-stu-id="1f918-143">Predefined tags can have multiple values, but you can enter only one value in each command.</span></span>
<span data-ttu-id="1f918-144">Этот параметр является необязательным, поскольку теги могут иметь имена без значений.</span><span class="sxs-lookup"><span data-stu-id="1f918-144">This parameter is optional, because tags can have names without values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f918-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f918-145">-DefaultProfile</span></span>
<span data-ttu-id="1f918-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f918-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f918-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f918-147">CommonParameters</span></span>
<span data-ttu-id="1f918-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f918-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f918-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f918-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f918-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f918-150">INPUTS</span></span>

### <span data-ttu-id="1f918-151">Ничего</span><span class="sxs-lookup"><span data-stu-id="1f918-151">None</span></span>

## <span data-ttu-id="1f918-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f918-152">OUTPUTS</span></span>

### <span data-ttu-id="1f918-153">Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="1f918-153">Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="1f918-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f918-154">NOTES</span></span>

## <span data-ttu-id="1f918-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f918-155">RELATED LINKS</span></span>

[<span data-ttu-id="1f918-156">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f918-156">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="1f918-157">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="1f918-157">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


