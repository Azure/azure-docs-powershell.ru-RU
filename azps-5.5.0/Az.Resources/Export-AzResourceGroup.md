---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212988"
---
# <span data-ttu-id="a0f63-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0f63-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="a0f63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f63-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f63-103">Создает группу ресурсов в качестве шаблона и сохраняет ее в файл.</span><span class="sxs-lookup"><span data-stu-id="a0f63-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="a0f63-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a0f63-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0f63-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a0f63-105">DESCRIPTION</span></span>
<span data-ttu-id="a0f63-106">При **этом указанная** группа ресурсов сохраняется в файле JSON. Это может быть полезно в тех случаях, когда в вашей группе ресурсов уже созданы некоторые ресурсы, а затем вы хотите использовать преимущества использования шаблонов с задней частью развертывания.</span><span class="sxs-lookup"><span data-stu-id="a0f63-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="a0f63-107">Этот cmdlet позволяет легко начать с создания шаблона для существующих ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0f63-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="a0f63-108">В некоторых случаях этот cmdlet не может сгенерировать некоторые части шаблона.</span><span class="sxs-lookup"><span data-stu-id="a0f63-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="a0f63-109">Предупреждения о сбойных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="a0f63-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="a0f63-110">Шаблон будет по-прежнему создан для успешно созданных частей.</span><span class="sxs-lookup"><span data-stu-id="a0f63-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="a0f63-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a0f63-111">EXAMPLES</span></span>

### <span data-ttu-id="a0f63-112">Пример 1. Экспорт группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0f63-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="a0f63-113">Эта команда сохраняет группу ресурсов TestGroup в качестве шаблона и сохраняет ее в файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a0f63-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="a0f63-114">Пример 2. Экспорт отдельного ресурса из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0f63-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="a0f63-115">Эта команда сохраняет ресурс Виртуальной машины с именем TestVirtualMa в группе ресурсов TestGroup в качестве шаблона и сохраняет его в файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a0f63-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="a0f63-116">Пример 3. Экспорт части ресурсов из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a0f63-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="a0f63-117">Эта команда сохраняет два ресурса из группы ресурсов TestGroup в качестве шаблона и сохраняет их в файл JSON в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="a0f63-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="a0f63-118">Созданный шаблон не будет содержать созданных параметров.</span><span class="sxs-lookup"><span data-stu-id="a0f63-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="a0f63-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0f63-119">PARAMETERS</span></span>

### <span data-ttu-id="a0f63-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a0f63-120">-ApiVersion</span></span>
<span data-ttu-id="a0f63-121">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0f63-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a0f63-122">Если он не задан, используется последняя версия API.</span><span class="sxs-lookup"><span data-stu-id="a0f63-122">If not specified, the latest API version is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f63-123">-DefaultProfile</span></span>
<span data-ttu-id="a0f63-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a0f63-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0f63-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a0f63-125">-Force</span></span>
<span data-ttu-id="a0f63-126">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="a0f63-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="a0f63-127">-IncludeComments</span></span>
<span data-ttu-id="a0f63-128">Указывает на то, что данной операцией шаблон экспортируется с комментариями.</span><span class="sxs-lookup"><span data-stu-id="a0f63-128">Indicates that this operation exports the template with comments.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="a0f63-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="a0f63-130">Указывает на то, что в ходе этой операции экспортируется параметр шаблона со значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a0f63-130">Indicates that this operation exports the template parameter with the default value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-131">-Path</span><span class="sxs-lookup"><span data-stu-id="a0f63-131">-Path</span></span>
<span data-ttu-id="a0f63-132">Путь к выходным данным файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="a0f63-132">Specifies the output path of the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="a0f63-133">-Pre</span></span>
<span data-ttu-id="a0f63-134">Указывает на то, что этот cmdlet использует предварительные версии API при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="a0f63-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-135">-Ресурс</span><span class="sxs-lookup"><span data-stu-id="a0f63-135">-Resource</span></span>
<span data-ttu-id="a0f63-136">Список ид ресурсов для фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="a0f63-136">A list of resourceIds to filter the results by.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f63-137">-ResourceGroupName</span></span>
<span data-ttu-id="a0f63-138">Имя группы ресурсов, которая будет экспортироваться.</span><span class="sxs-lookup"><span data-stu-id="a0f63-138">Specifies the name of the resource group to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="a0f63-139">-SkipAllParameterization</span></span>
<span data-ttu-id="a0f63-140">Пропустить все параметры.</span><span class="sxs-lookup"><span data-stu-id="a0f63-140">Skip all parameterization.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="a0f63-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="a0f63-142">Пропустить параметры имен ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a0f63-142">Skip resource name parameterization.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f63-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0f63-143">-Confirm</span></span>
<span data-ttu-id="a0f63-144">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a0f63-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0f63-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0f63-145">-WhatIf</span></span>
<span data-ttu-id="a0f63-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0f63-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0f63-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a0f63-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0f63-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f63-148">CommonParameters</span></span>
<span data-ttu-id="a0f63-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0f63-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f63-150">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a0f63-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f63-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a0f63-151">INPUTS</span></span>

### <span data-ttu-id="a0f63-152">System.String</span><span class="sxs-lookup"><span data-stu-id="a0f63-152">System.String</span></span>

## <span data-ttu-id="a0f63-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a0f63-153">OUTPUTS</span></span>

### <span data-ttu-id="a0f63-154">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="a0f63-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a0f63-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a0f63-155">NOTES</span></span>

## <span data-ttu-id="a0f63-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a0f63-156">RELATED LINKS</span></span>

[<span data-ttu-id="a0f63-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0f63-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


