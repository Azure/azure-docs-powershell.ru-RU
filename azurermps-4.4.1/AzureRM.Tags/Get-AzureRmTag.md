---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 726E01DD-D73C-4D4B-8FC0-52767927367C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Get-AzureRmTag.md
ms.openlocfilehash: 5e0766039a9becb65aaec13d08e46f751893b8dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566664"
---
# <span data-ttu-id="b7619-101">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b7619-101">Get-AzureRmTag</span></span>

## <span data-ttu-id="b7619-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7619-102">SYNOPSIS</span></span>
<span data-ttu-id="b7619-103">Получает предопределенные Теги Azure.</span><span class="sxs-lookup"><span data-stu-id="b7619-103">Gets predefined Azure tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7619-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7619-104">SYNTAX</span></span>

```
Get-AzureRmTag [[-Name] <String>] [-Detailed] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7619-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7619-105">DESCRIPTION</span></span>
<span data-ttu-id="b7619-106">Командлет **Get-AzureRmTag** получает предопределенные Теги Azure в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-106">The **Get-AzureRmTag** cmdlet gets predefined Azure tags in your subscription.</span></span>
<span data-ttu-id="b7619-107">Этот командлет возвращает основные сведения о тегах и подробное описание тегов и их значений.</span><span class="sxs-lookup"><span data-stu-id="b7619-107">This cmdlet returns basic information about the tags or detailed information about tags and their values.</span></span>
<span data-ttu-id="b7619-108">Все выходные объекты включают свойство Count, представляющее количество ресурсов и групп ресурсов, к которым применены теги и значения.</span><span class="sxs-lookup"><span data-stu-id="b7619-108">All output objects include a Count property that represents the number of resources and resource groups to which the tags and values have been applied.</span></span>

<span data-ttu-id="b7619-109">Модуль тегов Azure, с помощью **Get-AzureRMTag** , — это часть, которая может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="b7619-109">The Azure Tags module that **Get-AzureRMTag** is a part of can help you manage predefined Azure tags.</span></span>
<span data-ttu-id="b7619-110">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="b7619-110">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="b7619-111">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-111">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="b7619-112">Если подписка содержит любые предопределенные теги, вы не можете применить неопределенные теги или значения к любому ресурсу или группе ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-112">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

<span data-ttu-id="b7619-113">Чтобы создать предопределенный тег, используйте командлет New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="b7619-113">To create a predefined tag, use the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="b7619-114">Чтобы применить предопределенный тег к группе ресурсов, используйте параметр *Tag* командлета New-AzureRmTag.</span><span class="sxs-lookup"><span data-stu-id="b7619-114">To apply a predefined tag to a resource group, use the *Tag* parameter of the New-AzureRmTag cmdlet.</span></span>
<span data-ttu-id="b7619-115">Для поиска групп ресурсов с определенным именем тега или именем и значением используйте параметр *Tag* для командлета Get-AzureRMResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b7619-115">To search resource groups for a specific tag name or name and value, use the *Tag* parameter of the Get-AzureRMResourceGroup cmdlet.</span></span>

## <span data-ttu-id="b7619-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7619-116">EXAMPLES</span></span>

### <span data-ttu-id="b7619-117">Пример 1: получение всех стандартных тегов</span><span class="sxs-lookup"><span data-stu-id="b7619-117">Example 1: Get all predefined tags</span></span>
```
PS C:\>Get-AzureRmTag

Name      Count
========  =====

Department    5
FY2015        2
CostCenter   20
```

<span data-ttu-id="b7619-118">Эта команда получает все предопределенные теги в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-118">This command gets all predefined tags in the subscription.</span></span>
<span data-ttu-id="b7619-119">Свойство Count показывает, сколько вхождений тега применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-119">The Count property shows how many times the tag has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="b7619-120">Пример 2: получение тега по имени</span><span class="sxs-lookup"><span data-stu-id="b7619-120">Example 2: Get a tag by name</span></span>
```
PS C:\>Get-AzureRmTag -Name "Department"

Name:   Department
Count:  5
Values: 

        Name        Count
        ==========  =====

        Finance       2
        IT            3
```

<span data-ttu-id="b7619-121">Эта команда получает подробные сведения о теге отдела и его значениях.</span><span class="sxs-lookup"><span data-stu-id="b7619-121">This command gets detailed information about the Department tag and its values.</span></span>
<span data-ttu-id="b7619-122">Свойство Count показывает, сколько вхождений тега и каждого из его значений применено к ресурсам и группам ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-122">The Count property shows how many times the tag and each of its values has been applied to resources and resource groups in the subscription.</span></span>

### <span data-ttu-id="b7619-123">Пример 3: получение значений всех тегов</span><span class="sxs-lookup"><span data-stu-id="b7619-123">Example 3: Get values of all tags</span></span>
```
PS C:\>Get-AzureRmTag -Detailed

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

<span data-ttu-id="b7619-124">Эта команда использует *подробный* параметр для получения подробных сведений обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-124">This command uses the *Detailed* parameter to get detailed information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="b7619-125">Параметр *Detailed* является эквивалентом использования параметра *Name* для каждого тега.</span><span class="sxs-lookup"><span data-stu-id="b7619-125">Using the *Detailed* parameter is the equivalent of using the *Name* parameter for every tag.</span></span>

## <span data-ttu-id="b7619-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7619-126">PARAMETERS</span></span>

### <span data-ttu-id="b7619-127">-Подробно</span><span class="sxs-lookup"><span data-stu-id="b7619-127">-Detailed</span></span>
<span data-ttu-id="b7619-128">Указывает на то, что при выполнении этой операции в выходных данных добавляются сведения о значениях тегов.</span><span class="sxs-lookup"><span data-stu-id="b7619-128">Indicates that this operation adds information about tag values to the output.</span></span>

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

### <span data-ttu-id="b7619-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b7619-129">-Name</span></span>
<span data-ttu-id="b7619-130">Указывает имя тега, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="b7619-130">Specifies the name of the tag to get.</span></span>
<span data-ttu-id="b7619-131">По умолчанию **Get-AzureRmTag** получает основные сведения обо всех предопределенных тегах в подписке.</span><span class="sxs-lookup"><span data-stu-id="b7619-131">By default, **Get-AzureRmTag** gets basic information about all predefined tags in the subscription.</span></span>
<span data-ttu-id="b7619-132">При указании параметра *Name* *подробный* параметр не действует.</span><span class="sxs-lookup"><span data-stu-id="b7619-132">When you specify the *Name* parameter, the *Detailed* parameter has no effect.</span></span>

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

### <span data-ttu-id="b7619-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7619-133">-DefaultProfile</span></span>
<span data-ttu-id="b7619-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7619-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7619-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7619-135">CommonParameters</span></span>
<span data-ttu-id="b7619-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7619-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7619-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7619-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7619-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7619-138">INPUTS</span></span>

### <span data-ttu-id="b7619-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="b7619-139">None</span></span>

## <span data-ttu-id="b7619-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7619-140">OUTPUTS</span></span>

### <span data-ttu-id="b7619-141">Microsoft. Azure. Commands. Tags. Model. PSTag, Microsoft. Azure. Commands. Tags</span><span class="sxs-lookup"><span data-stu-id="b7619-141">Microsoft.Azure.Commands.Tags.Model.PSTag, Microsoft.Azure.Commands.Tags</span></span>

## <span data-ttu-id="b7619-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7619-142">NOTES</span></span>

## <span data-ttu-id="b7619-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7619-143">RELATED LINKS</span></span>

[<span data-ttu-id="b7619-144">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b7619-144">New-AzureRmTag</span></span>](./New-AzureRmTag.md)

[<span data-ttu-id="b7619-145">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="b7619-145">Remove-AzureRmTag</span></span>](./Remove-AzureRmTag.md)


