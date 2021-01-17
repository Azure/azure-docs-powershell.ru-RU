---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413791"
---
# <span data-ttu-id="63d40-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="63d40-101">Get-AzTag</span></span>

## <span data-ttu-id="63d40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d40-102">SYNOPSIS</span></span>
<span data-ttu-id="63d40-103">Предопределяются теги Azure | Возвращает весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="63d40-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="63d40-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63d40-104">SYNTAX</span></span>

### <span data-ttu-id="63d40-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="63d40-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63d40-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="63d40-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d40-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d40-107">DESCRIPTION</span></span>

<span data-ttu-id="63d40-108">**GetPredefinedTagSet:** командлет **Get-AzTag** получает предопределять теги Azure в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-108">**GetPredefinedTagSet**: The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="63d40-109">Этот командлет возвращает основные сведения о тегах или подробные сведения о тегах и их значениях.</span><span class="sxs-lookup"><span data-stu-id="63d40-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="63d40-110">Все выходные объекты содержат свойство Count, которое представляет количество ресурсов и групп ресурсов, к которым были применены теги и значения.</span><span class="sxs-lookup"><span data-stu-id="63d40-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="63d40-111">Модуль "Теги Azure", который входит в **состав тега Get-AzTag,** помогает управлять предопределенами тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="63d40-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="63d40-112">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, например по отделам или центрам затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="63d40-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="63d40-113">Теги можно определять и применять в одном шаге, но предопределяемые теги помечают стандартные, согласованные, предсказуемые имена и значения для тегов в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="63d40-114">Чтобы создать предопределный тег, воспользуйтесь New-AzTag командлетом.</span><span class="sxs-lookup"><span data-stu-id="63d40-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="63d40-115">Чтобы применить предопределяный тег к группе ресурсов, используйте параметр *"Тег"* New-AzTag командлета.</span><span class="sxs-lookup"><span data-stu-id="63d40-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="63d40-116">Для поиска в группах ресурсов определенного имени или имени тега и значения используйте параметр *Tag* Get-AzResourceGroup командлета.</span><span class="sxs-lookup"><span data-stu-id="63d40-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="63d40-117">**GetByResourceIdParameterSet:** командлет **Get-AzTag** с **ResourceId** получает весь набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="63d40-117">**GetByResourceIdParameterSet**: The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="63d40-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63d40-118">EXAMPLES</span></span>

### <span data-ttu-id="63d40-119">Пример 1. Получить все предопределные теги</span><span class="sxs-lookup"><span data-stu-id="63d40-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="63d40-120">Эта команда получает все заранее задав теги в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="63d40-121">Свойство Count показывает, сколько раз тег применялся к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="63d40-122">Пример 2. Пометка тега по имени</span><span class="sxs-lookup"><span data-stu-id="63d40-122">Example 2: Get a tag by name</span></span>
```powershell
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="63d40-123">Эта команда получает подробные сведения о теге Department и его значениях.</span><span class="sxs-lookup"><span data-stu-id="63d40-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="63d40-124">Свойство Count показывает, сколько раз тег и каждое из его значений применялось к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="63d40-125">Пример 3. Получить значения всех тегов</span><span class="sxs-lookup"><span data-stu-id="63d40-125">Example 3: Get values of all tags</span></span>
```powershell
PS C:\>Get-AzTag -Detailed

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3


Name:   FY2015
Count:  2


Name:   CostCenter
Count:  20
Values: 

        Name        Count
        ==========  =====

        0001          5
        0002         10
        0003          5
```

<span data-ttu-id="63d40-126">Эта команда использует параметр *Detailed* для получения подробных сведений обо всех предопределеных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="63d40-127">Использование *параметра Detailed* эквивалентно использованию *параметра Name* для каждого тега.</span><span class="sxs-lookup"><span data-stu-id="63d40-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="63d40-128">Пример 4. Получите весь набор тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="63d40-128">Example 4: Get the entire set of tags on a subscription</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             tagKey1  tagValue1
             tagKey2  tagValue2
```

<span data-ttu-id="63d40-129">Эта команда получает весь набор тегов для подписки {subId}.</span><span class="sxs-lookup"><span data-stu-id="63d40-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="63d40-130">Пример 5. Получите весь набор тегов для ресурса</span><span class="sxs-lookup"><span data-stu-id="63d40-130">Example 5: Get the entire set of tags on a resource</span></span>

```powershell
PS C:\>Get-AzTag -ResourceId /subscriptions/{subId}/resourcegroups/{rg}/providers/Microsoft.Sql/servers/Server1

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             Dept     Finance
             Status   Normal
```

<span data-ttu-id="63d40-131">Эта команда получает весь набор тегов для ресурса с помощью {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="63d40-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="63d40-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63d40-132">PARAMETERS</span></span>

### <span data-ttu-id="63d40-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d40-133">-DefaultProfile</span></span>
<span data-ttu-id="63d40-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63d40-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d40-135">-Подробный</span><span class="sxs-lookup"><span data-stu-id="63d40-135">-Detailed</span></span>
<span data-ttu-id="63d40-136">Указывает на то, что эта операция добавляет к выходным данным сведения о значениях тегов.</span><span class="sxs-lookup"><span data-stu-id="63d40-136">Indicates that this operation adds information about tag values to the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d40-137">-Name</span><span class="sxs-lookup"><span data-stu-id="63d40-137">-Name</span></span>
<span data-ttu-id="63d40-138">Имя предопределяемого тега.</span><span class="sxs-lookup"><span data-stu-id="63d40-138">Name of the predefined tag.</span></span>
<span data-ttu-id="63d40-139">По умолчанию **Get-AzTag** получает основные сведения обо всех предопределеных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="63d40-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="63d40-140">Если задать параметр *Name,* подробный *параметр* не будет действовать.</span><span class="sxs-lookup"><span data-stu-id="63d40-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: GetPredefinedTagParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d40-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63d40-141">-ResourceId</span></span>
<span data-ttu-id="63d40-142">Идентификатор ресурса для сущности с тегами.</span><span class="sxs-lookup"><span data-stu-id="63d40-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="63d40-143">Ресурс, группа ресурсов или подписка могут быть помечены тегами.</span><span class="sxs-lookup"><span data-stu-id="63d40-143">A resource, a resource group or a subscription may be tagged.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63d40-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d40-144">CommonParameters</span></span>
<span data-ttu-id="63d40-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d40-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d40-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63d40-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d40-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63d40-147">INPUTS</span></span>

### <span data-ttu-id="63d40-148">System.String</span><span class="sxs-lookup"><span data-stu-id="63d40-148">System.String</span></span>

### <span data-ttu-id="63d40-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="63d40-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="63d40-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63d40-150">OUTPUTS</span></span>

### <span data-ttu-id="63d40-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span><span class="sxs-lookup"><span data-stu-id="63d40-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="63d40-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63d40-152">NOTES</span></span>

## <span data-ttu-id="63d40-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63d40-153">RELATED LINKS</span></span>

[<span data-ttu-id="63d40-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="63d40-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="63d40-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="63d40-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="63d40-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="63d40-156">Update-AzTag</span></span>](./Update-AzTag.md)
