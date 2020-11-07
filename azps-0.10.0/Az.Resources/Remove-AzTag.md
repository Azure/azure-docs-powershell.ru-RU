---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66B25541-0FA5-46CF-90D8-FE9527BE11C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Remove-AzTag.md
ms.openlocfilehash: 5b7e58545b2c463c08a961758ecdb3cbce7b222c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910836"
---
# <span data-ttu-id="b20c9-101">Remove-AzTag</span><span class="sxs-lookup"><span data-stu-id="b20c9-101">Remove-AzTag</span></span>

## <span data-ttu-id="b20c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b20c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b20c9-103">Удаляет предопределенные теги или значения Azure.</span><span class="sxs-lookup"><span data-stu-id="b20c9-103">Deletes predefined Azure tags or values.</span></span>

## <span data-ttu-id="b20c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b20c9-104">SYNTAX</span></span>

```
Remove-AzTag [-Name] <String> [[-Value] <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b20c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b20c9-105">DESCRIPTION</span></span>
<span data-ttu-id="b20c9-106">Командлет **Remove-AzTag** удаляет из подписки предопределенные Теги и значения Azure.</span><span class="sxs-lookup"><span data-stu-id="b20c9-106">The **Remove-AzTag** cmdlet deletes predefined Azure tags and values from your subscription.</span></span>
<span data-ttu-id="b20c9-107">Для удаления определенных значений из предопределенного тега используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="b20c9-107">To delete particular values from a predefined tag, use the *Value* parameter.</span></span>
<span data-ttu-id="b20c9-108">По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения. Вы не можете удалить тег или значение, которые в настоящее время применены к ресурсам или группам ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b20c9-108">By default, **Remove-AzTag** deletes the specified tag and all of its values.You cannot delete a tag or value that is currently applied to a resource or resource group.</span></span>
<span data-ttu-id="b20c9-109">Перед использованием **Remove-AzTag** используйте параметр *Tag* командлета Set-AzResourceGroup для удаления тега или значений из ресурса или группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b20c9-109">Before using **Remove-AzTag** , use the *Tag* parameter of the Set-AzResourceGroup cmdlet to delete the tag or values from the resource or resource group.</span></span>
<span data-ttu-id="b20c9-110">Модуль тегов Azure, который **Remove-AzTag** является частью, может помочь вам управлять предопределенными тегами Azure.</span><span class="sxs-lookup"><span data-stu-id="b20c9-110">The Azure Tags module that **Remove-AzTag** is part of can help you manage your predefined Azure tags.</span></span>
<span data-ttu-id="b20c9-111">Тег Azure — это пара "имя-значение", которую можно использовать для классификации ресурсов и групп ресурсов Azure, таких как отдел или центр затрат, а также для отслеживания заметок и примечаний к ресурсам и группам.</span><span class="sxs-lookup"><span data-stu-id="b20c9-111">An Azure tag is a name-value pair that you can use to categorize your Azure resources and resource groups, such as by department or cost center, or to track notes or comments about the resources and groups.</span></span>
<span data-ttu-id="b20c9-112">Вы можете определять и применять теги за один шаг, но стандартные теги позволяют устанавливать стандартные, противоречивые и предсказуемые имена и значения для тегов в вашей подписке.</span><span class="sxs-lookup"><span data-stu-id="b20c9-112">You can define and apply tags in a single step, but predefined tags let you establish standard, consistent, predictable names and values for the tags in your subscription.</span></span>

## <span data-ttu-id="b20c9-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b20c9-113">EXAMPLES</span></span>

### <span data-ttu-id="b20c9-114">Пример 1: Удаление предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="b20c9-114">Example 1: Delete a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department"
```

<span data-ttu-id="b20c9-115">Эта команда удаляет предопределенный тег с именем Department и все его значения.</span><span class="sxs-lookup"><span data-stu-id="b20c9-115">This command deletes the predefined tag named Department and all of its values.</span></span>
<span data-ttu-id="b20c9-116">Если тег применен к ресурсам или группам ресурсов, команда не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b20c9-116">If the tag has been applied to any resources or resource groups, the command fails.</span></span>

### <span data-ttu-id="b20c9-117">Пример 2: Удаление значения из предопределенного тега</span><span class="sxs-lookup"><span data-stu-id="b20c9-117">Example 2: Delete a value from a predefined tag</span></span>
```
PS C:\>Remove-AzTag -Name "Department" -Value "HumanResources" -PassThru
Name:   Department
Count:  14
Values: 

        Name        Count
        =========   =====

        Finance        2
        IT            12
```

<span data-ttu-id="b20c9-118">Эта команда удаляет значение HumanResources из предопределенного тега отдела.</span><span class="sxs-lookup"><span data-stu-id="b20c9-118">This command deletes the HumanResources value from the predefined Department tag.</span></span>
<span data-ttu-id="b20c9-119">Тег не удаляется.</span><span class="sxs-lookup"><span data-stu-id="b20c9-119">It does not delete the tag.</span></span>
<span data-ttu-id="b20c9-120">Если значение было применено к ресурсам или группам ресурсов, команда завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="b20c9-120">If the value has been applied to any resources or resource groups, the command fails.</span></span>

## <span data-ttu-id="b20c9-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b20c9-121">PARAMETERS</span></span>

### <span data-ttu-id="b20c9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b20c9-122">-DefaultProfile</span></span>
<span data-ttu-id="b20c9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b20c9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b20c9-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b20c9-124">-Name</span></span>
<span data-ttu-id="b20c9-125">Указывает имя тега, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="b20c9-125">Specifies the name of the tag to be deleted.</span></span>
<span data-ttu-id="b20c9-126">По умолчанию **Remove-AzTag** удаляет указанный тег и все его значения.</span><span class="sxs-lookup"><span data-stu-id="b20c9-126">By default, **Remove-AzTag** removes the specified tag and all of its values.</span></span>
<span data-ttu-id="b20c9-127">Чтобы удалить выделенные значения, но не удалять тег, используйте параметр *value* .</span><span class="sxs-lookup"><span data-stu-id="b20c9-127">To delete selected values, but not delete the tag, use the *Value* parameter.</span></span>

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

### <span data-ttu-id="b20c9-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b20c9-128">-PassThru</span></span>
<span data-ttu-id="b20c9-129">Возвращает объект, который представляет удаленный тег или получившийся тег с удаленным значением.</span><span class="sxs-lookup"><span data-stu-id="b20c9-129">Returns an object that represents the deleted tag or the resulting tag with deleted valued.</span></span>

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

### <span data-ttu-id="b20c9-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="b20c9-130">-Value</span></span>
<span data-ttu-id="b20c9-131">Удаляет указанные значения из предопределенного тега, но не удаляет тег.</span><span class="sxs-lookup"><span data-stu-id="b20c9-131">Deletes the specified values from the predefined tag, but does not delete the tag.</span></span>

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

### <span data-ttu-id="b20c9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b20c9-132">-Confirm</span></span>
<span data-ttu-id="b20c9-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b20c9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b20c9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b20c9-134">-WhatIf</span></span>
<span data-ttu-id="b20c9-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b20c9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b20c9-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b20c9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b20c9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20c9-137">CommonParameters</span></span>
<span data-ttu-id="b20c9-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b20c9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20c9-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b20c9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20c9-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b20c9-140">INPUTS</span></span>

### <span data-ttu-id="b20c9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b20c9-141">System.String</span></span>

### <span data-ttu-id="b20c9-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="b20c9-142">System.String[]</span></span>

### <span data-ttu-id="b20c9-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b20c9-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b20c9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b20c9-144">OUTPUTS</span></span>

### <span data-ttu-id="b20c9-145">Microsoft. Azure. Commands. ResourceManager. Common. Tags. PSTag</span><span class="sxs-lookup"><span data-stu-id="b20c9-145">Microsoft.Azure.Commands.ResourceManager.Common.Tags.PSTag</span></span>

## <span data-ttu-id="b20c9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b20c9-146">NOTES</span></span>

## <span data-ttu-id="b20c9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b20c9-147">RELATED LINKS</span></span>

[<span data-ttu-id="b20c9-148">Get-AzTag</span><span class="sxs-lookup"><span data-stu-id="b20c9-148">Get-AzTag</span></span>](./Get-AzTag.md)

[<span data-ttu-id="b20c9-149">New-AzTag</span><span class="sxs-lookup"><span data-stu-id="b20c9-149">New-AzTag</span></span>](./New-AzTag.md)

