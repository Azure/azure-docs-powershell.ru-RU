---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzTag.md
ms.openlocfilehash: 1f2289351da276a0422828c082bb51d8dc267a20
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910921"
---
# <span data-ttu-id="74a37-101">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="74a37-101">Get-AzTag</span></span>

## <span data-ttu-id="74a37-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74a37-102">SYNOPSIS</span></span>
<span data-ttu-id="74a37-103">Получает предопределенные Теги Azure.</span><span class="sxs-lookup"><span data-stu-id="74a37-103">Gets predefined Azure tags.</span></span>

## <span data-ttu-id="74a37-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74a37-104">SYNTAX</span></span>

```
Get-AzTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74a37-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74a37-105">DESCRIPTION</span></span>
<span data-ttu-id="74a37-106">Командлет **Get-AzTag** получает предопределенные Теги Azure в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-106">The **Get-AzTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="74a37-107">Этот командлет возвращает основные сведения о тегах и подробное описание тегов и их значений.</span><span class="sxs-lookup"><span data-stu-id="74a37-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="74a37-108">Все выходные объекты включают свойство Count, представляющее количество ресурсов и групп ресурсов, к которым применены теги и значения.</span><span class="sxs-lookup"><span data-stu-id="74a37-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>
<span data-ttu-id="74a37-109">Модуль тегов Azure, с помощью **Get-AzTag** , — это часть, которая может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="74a37-109">The Azure Tags module that **Get-AzTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="74a37-110">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="74a37-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="74a37-111">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="74a37-112">Чтобы создать предопределенный тег, используйте командлет New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="74a37-112">To create a predefined tag, use the New-AzTag cmdlet.</span></span>
<span data-ttu-id="74a37-113">Чтобы применить предопределенный тег к группе ресурсов, используйте параметр *Tag* командлета New-AzTag.</span><span class="sxs-lookup"><span data-stu-id="74a37-113">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzTag cmdlet.</span></span>
<span data-ttu-id="74a37-114">Для поиска групп ресурсов с определенным именем тега или именем и значением используйте параметр *Tag* для командлета Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="74a37-114">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzResourceGroup cmdlet.</span></span>

## <span data-ttu-id="74a37-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74a37-115">EXAMPLES</span></span>

### <span data-ttu-id="74a37-116">Пример 1: получение всех стандартных тегов</span><span class="sxs-lookup"><span data-stu-id="74a37-116">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="74a37-117">Эта команда получает все предопределенные теги в подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-117">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="74a37-118">Свойство Count показывает, сколько вхождений тега применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-118">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="74a37-119">Пример 2: получение тега по имени</span><span class="sxs-lookup"><span data-stu-id="74a37-119">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="74a37-120">Эта команда получает подробные сведения о теге отдела и его значениях.</span><span class="sxs-lookup"><span data-stu-id="74a37-120">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="74a37-121">Свойство Count показывает, сколько вхождений тега и каждого из его значений применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-121">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="74a37-122">Пример 3: получение значений всех тегов</span><span class="sxs-lookup"><span data-stu-id="74a37-122">Example 3: Get values of all tags</span></span>
```
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

<span data-ttu-id="74a37-123">Эта команда использует *подробный* параметр для получения подробных сведений обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-123">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="74a37-124">Параметр *Detailed* является эквивалентом использования параметра *Name* для каждого тега.</span><span class="sxs-lookup"><span data-stu-id="74a37-124">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="74a37-125">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74a37-125">PARAMETERS</span></span>

### <span data-ttu-id="74a37-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74a37-126">-DefaultProfile</span></span>
<span data-ttu-id="74a37-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74a37-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74a37-128">-Подробно</span><span class="sxs-lookup"><span data-stu-id="74a37-128">-Detailed</span></span>
<span data-ttu-id="74a37-129">Указывает на то, что при выполнении этой операции в выходных данных добавляются сведения о значениях тегов.</span><span class="sxs-lookup"><span data-stu-id="74a37-129">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="74a37-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74a37-130">-Name</span></span>
<span data-ttu-id="74a37-131">Указывает имя тега, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="74a37-131">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="74a37-132">По умолчанию **Get-AzTag** получает основные сведения обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="74a37-132">By default, **Get-AzTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="74a37-133">При указании параметра *Name* *подробный* параметр не действует.</span><span class="sxs-lookup"><span data-stu-id="74a37-133">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74a37-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74a37-134">CommonParameters</span></span>
<span data-ttu-id="74a37-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74a37-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74a37-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74a37-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74a37-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74a37-137">INPUTS</span></span>

### <span data-ttu-id="74a37-138">System. String</span><span class="sxs-lookup"><span data-stu-id="74a37-138">System.String</span></span>

### <span data-ttu-id="74a37-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="74a37-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="74a37-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74a37-140">OUTPUTS</span></span>

### <span data-ttu-id="74a37-141">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="74a37-141">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="74a37-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="74a37-142">NOTES</span></span>

## <span data-ttu-id="74a37-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74a37-143">RELATED LINKS</span></span>

[<span data-ttu-id="74a37-144">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="74a37-144">New-AzTag</span></span>](./New-AzTag.md)

[<span data-ttu-id="74a37-145">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="74a37-145">Remove-AzTag</span></span>](./Remove-AzTag.md)

