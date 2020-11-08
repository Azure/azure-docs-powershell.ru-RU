---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 058f4a61f1e7ff2fe7f416ea0e4ada098c9efe51
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078765"
---
# <span data-ttu-id="ec0b5-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec0b5-101">Get-AzTag</span></span>

## <span data-ttu-id="ec0b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ec0b5-102">SYNOPSIS</span></span>
<span data-ttu-id="ec0b5-103">Получает предопределенные Теги Azure | Возвращает весь набор тегов на ресурсе или в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-103">Gets predefined Azure tags | Gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="ec0b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ec0b5-104">SYNTAX</span></span>

### <span data-ttu-id="ec0b5-105">GetPredefinedTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0b5-105">GetPredefinedTagParameterSet</span></span>
```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ec0b5-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec0b5-106">GetByResourceIdParameterSet</span></span>
```
Get-AzTag -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec0b5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec0b5-107">DESCRIPTION</span></span>

<span data-ttu-id="ec0b5-108">**GetPredefinedTagSet** : командлет **Get-AzTag** получает предопределенные Теги Azure в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-108">**GetPredefinedTagSet** : The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="ec0b5-109">Этот командлет возвращает основные сведения о тегах и подробное описание тегов и их значений.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-109">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="ec0b5-110">Все выходные объекты включают свойство Count, представляющее количество ресурсов и групп ресурсов, к которым применены теги и значения.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-110">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="ec0b5-111">Модуль тегов Azure, с помощью **Get-AzTag** , — это часть, которая может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-111">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="ec0b5-112">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-112">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="ec0b5-113">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-113">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="ec0b5-114">Чтобы создать предопределенный тег, используйте командлет New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-114">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="ec0b5-115">Чтобы применить предопределенный тег к группе ресурсов, используйте параметр *Tag* командлета New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-115">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="ec0b5-116">Для поиска групп ресурсов с определенным именем тега или именем и значением используйте параметр *Tag* для командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-116">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

<span data-ttu-id="ec0b5-117">**GetByResourceIdParameterSet** : командлет **Get-AzTag** с **ResourceId** получает полный набор тегов для ресурса или подписки.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-117">**GetByResourceIdParameterSet** : The **Get-AzTag** cmdlet with a **ResourceId** gets the entire set of tags on a resource or subscription.</span></span>

## <span data-ttu-id="ec0b5-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ec0b5-118">EXAMPLES</span></span>

### <span data-ttu-id="ec0b5-119">Пример 1: получение всех стандартных тегов</span><span class="sxs-lookup"><span data-stu-id="ec0b5-119">Example 1: Get all predefined tags</span></span>
```powershell
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="ec0b5-120">Эта команда получает все предопределенные теги в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-120">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec0b5-121">Свойство Count показывает, сколько вхождений тега применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-121">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="ec0b5-122">Пример 2: получение тега по имени</span><span class="sxs-lookup"><span data-stu-id="ec0b5-122">Example 2: Get a tag by name</span></span>
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

<span data-ttu-id="ec0b5-123">Эта команда получает подробные сведения о теге отдела и его значениях.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-123">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="ec0b5-124">Свойство Count показывает, сколько вхождений тега и каждого из его значений применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-124">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="ec0b5-125">Пример 3: получение значений всех тегов</span><span class="sxs-lookup"><span data-stu-id="ec0b5-125">Example 3: Get values of all tags</span></span>
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

<span data-ttu-id="ec0b5-126">Эта команда использует *подробный* параметр для получения подробных сведений обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-126">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec0b5-127">Параметр *Detailed* является эквивалентом использования параметра *Name* для каждого тега.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-127">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

### <span data-ttu-id="ec0b5-128">Пример 4: получение всего набора тегов в подписке</span><span class="sxs-lookup"><span data-stu-id="ec0b5-128">Example 4: Get the entire set of tags on a subscription</span></span>

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

<span data-ttu-id="ec0b5-129">Эта команда возвращает весь набор тегов в подписке с помощью {subId}.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-129">This command gets the entire set of tags on the subscription with {subId}.</span></span>

### <span data-ttu-id="ec0b5-130">Пример 5: получение всего набора тегов на ресурсе</span><span class="sxs-lookup"><span data-stu-id="ec0b5-130">Example 5: Get the entire set of tags on a resource</span></span>

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

<span data-ttu-id="ec0b5-131">Эта команда возвращает весь набор тегов для ресурса с {resourceId}.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-131">This command gets the entire set of tags on the resource with {resourceId}.</span></span>

## <span data-ttu-id="ec0b5-132">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ec0b5-132">PARAMETERS</span></span>

### <span data-ttu-id="ec0b5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec0b5-133">-DefaultProfile</span></span>
<span data-ttu-id="ec0b5-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec0b5-135">-Подробно</span><span class="sxs-lookup"><span data-stu-id="ec0b5-135">-Detailed</span></span>
<span data-ttu-id="ec0b5-136">Указывает на то, что при выполнении этой операции в выходных данных добавляются сведения о значениях тегов.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-136">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="ec0b5-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ec0b5-137">-Name</span></span>
<span data-ttu-id="ec0b5-138">Имя предопределенного тега.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-138">Name of the predefined tag.</span></span>
<span data-ttu-id="ec0b5-139">По умолчанию **Get-AzTag** получает основные сведения обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-139">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="ec0b5-140">При указании параметра *Name* *подробный* параметр не действует.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-140">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="ec0b5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ec0b5-141">-ResourceId</span></span>
<span data-ttu-id="ec0b5-142">Идентификатор ресурса для помеченной сущности.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-142">The resource identifier for the tagged entity.</span></span> <span data-ttu-id="ec0b5-143">Ресурс, Группа ресурсов или подписка может быть помечены.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-143">A resource, a resource group or a subscription may be tagged.</span></span>

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

### <span data-ttu-id="ec0b5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec0b5-144">CommonParameters</span></span>
<span data-ttu-id="ec0b5-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ec0b5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec0b5-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec0b5-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec0b5-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ec0b5-147">INPUTS</span></span>

### <span data-ttu-id="ec0b5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ec0b5-148">System.String</span></span>

### <span data-ttu-id="ec0b5-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec0b5-149">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec0b5-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ec0b5-150">OUTPUTS</span></span>

### <span data-ttu-id="ec0b5-151">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag | Microsoft. Azure. Commands. Tags. Model. PSTagResource</span><span class="sxs-lookup"><span data-stu-id="ec0b5-151">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag | Microsoft.Azure.Commands.Tags.Model.PSTagResource</span></span>

## <span data-ttu-id="ec0b5-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="ec0b5-152">NOTES</span></span>

## <span data-ttu-id="ec0b5-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ec0b5-153">RELATED LINKS</span></span>

[<span data-ttu-id="ec0b5-154">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec0b5-154">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="ec0b5-155">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec0b5-155">Remove-AzTag</span></span>](./Remove-AzTag.md)

[<span data-ttu-id="ec0b5-156">Update-AzTag</span><span class="sxs-lookup"><span data-stu-id="ec0b5-156">Update-AzTag</span></span>](./Update-AzTag.md)
