---
external help file: Microsoft.Azure.Commands.Tags.dll-Help.xml
Module Name: AzureRM.Tags
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Tags/Commands.Tags/help/Remove-AzureRmTag.md
ms.openlocfilehash: 909781b8cd441daab8bf5f567404a5e99e88cd0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734200"
---
# <span data-ttu-id="2a0b2-101">Remove-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="2a0b2-101">Remove-AzureRmTag</span></span>

## <span data-ttu-id="2a0b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0b2-103">Удаляет предопределенные теги или значения Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-103">Deletes predefined Azure tags or values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a0b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a0b2-104">SYNTAX</span></span>

```
Remove-AzureRmTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a0b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a0b2-105">DESCRIPTION</span></span>
<span data-ttu-id="2a0b2-106">Командлет **Remove-AzureRmTag** удаляет из подписки предопределенные Теги и значения Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-106">The **Remove-AzureRmTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="2a0b2-107">Для удаления определенных значений из предопределенного тега используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="2a0b2-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="2a0b2-108">По умолчанию **Remove-AzureRmTag** удаляет указанный тег и все его значения. Вы не можете удалить тег или значение, которые в настоящее время применены к ресурсам или группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-108">By default, **Remove-AzureRmTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>

<span data-ttu-id="2a0b2-109">Перед использованием **Remove-AzureRmTag** используйте параметр *Tag* командлета Set-AzureRMResourceGroup для удаления тега или значений из ресурса или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-109">Before using **Remove-AzureRmTag** , use the *Tag* parameter of the Set-AzureRMResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>

<span data-ttu-id="2a0b2-110">Модуль тегов Azure, который **Remove-AzureRmTag** является частью, может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-110">The Azure Tags module that **Remove-AzureRmTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="2a0b2-111">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>

<span data-ttu-id="2a0b2-112">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>
<span data-ttu-id="2a0b2-113">Если подписка содержит любые предопределенные теги, вы не можете применить неопределенные теги или значения к любому ресурсу или группе ресурсов в подписке.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-113">If the subscription includes any predefined tags, you cannot apply undefined tags or values to any resource or resource group in the subscription.</span></span>

## <span data-ttu-id="2a0b2-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a0b2-114">EXAMPLES</span></span>

### <span data-ttu-id="2a0b2-115">Пример 1: Удаление предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="2a0b2-115">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department"
```

<span data-ttu-id="2a0b2-116">Эта команда удаляет предопределенный тег с именем Department и все его ресурсы.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-116">This command deletes the predefined tag named Department and all of its resources.</span></span>
<span data-ttu-id="2a0b2-117">Если тег применен к ресурсам или группам ресурсов, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-117">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="2a0b2-118">Пример 2: Удаление значения из предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="2a0b2-118">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzureRmTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="2a0b2-119">Эта команда удаляет значение HumanResources из предопределенного тега отдела.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-119">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="2a0b2-120">Тег не удаляется.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-120">It does not delete the tag.</span></span>
<span data-ttu-id="2a0b2-121">Если значение было применено к ресурсам или группам ресурсов, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-121">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="2a0b2-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a0b2-122">PARAMETERS</span></span>

### <span data-ttu-id="2a0b2-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a0b2-123">-Name</span></span>
<span data-ttu-id="2a0b2-124">Указывает имя тега, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-124">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="2a0b2-125">По умолчанию **Remove-AzureRmTag** удаляет указанный тег и все его значения.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-125">By default, **Remove-AzureRmTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="2a0b2-126">Чтобы удалить выделенные значения, но не удалять тег, используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="2a0b2-126">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="2a0b2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a0b2-127">-PassThru</span></span>
<span data-ttu-id="2a0b2-128">Возвращает объект, который представляет удаленный тег или получившийся тег с удаленным значением.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-128">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="2a0b2-129">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="2a0b2-129">-Value</span></span>
<span data-ttu-id="2a0b2-130">Удаляет указанные значения из предопределенного тега, но не удаляет тег.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-130">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0b2-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a0b2-131">-Confirm</span></span>
<span data-ttu-id="2a0b2-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a0b2-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a0b2-133">-WhatIf</span></span>
<span data-ttu-id="2a0b2-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a0b2-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a0b2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0b2-136">-DefaultProfile</span></span>
<span data-ttu-id="2a0b2-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a0b2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0b2-138">CommonParameters</span></span>
<span data-ttu-id="2a0b2-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a0b2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0b2-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0b2-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0b2-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a0b2-141">INPUTS</span></span>

### <span data-ttu-id="2a0b2-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="2a0b2-142">None</span></span>

## <span data-ttu-id="2a0b2-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a0b2-143">OUTPUTS</span></span>

### <span data-ttu-id="2a0b2-144">None или Microsoft. Azure. Commands. Tags. Model. PSTag</span><span class="sxs-lookup"><span data-stu-id="2a0b2-144">None or Microsoft.Azure.Commands.Tags.Model.PSTag</span></span>

## <span data-ttu-id="2a0b2-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a0b2-145">NOTES</span></span>

## <span data-ttu-id="2a0b2-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a0b2-146">RELATED LINKS</span></span>

[<span data-ttu-id="2a0b2-147">Get-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="2a0b2-147">Get-AzureRmTag</span></span>](./Get-AzureRmTag.md)

[<span data-ttu-id="2a0b2-148">New-AzureRmTag</span><span class="sxs-lookup"><span data-stu-id="2a0b2-148">New-AzureRmTag</span></span>](./New-AzureRmTag.md)


