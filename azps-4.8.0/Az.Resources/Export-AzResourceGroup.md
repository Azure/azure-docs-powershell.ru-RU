---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 74605a57ab3f2c0898bf3eeb80950f86d4f65d94
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078058"
---
# <span data-ttu-id="6ead7-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ead7-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="6ead7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6ead7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ead7-103">Захватывает группу ресурсов в качестве шаблона и сохраняет ее в файле.</span><span class="sxs-lookup"><span data-stu-id="6ead7-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="6ead7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6ead7-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-SkipResourceNameParameterization] [-SkipAllParameterization] [-Resource <String[]>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ead7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ead7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ead7-106">Командлет **Export-AzResourceGroup** захватывает указанную группу ресурсов в качестве шаблона и сохраняет ее в JSON-файле. Это может быть полезно в сценариях, где вы уже создали некоторые ресурсы в группе ресурсов, а затем хотите использовать преимущества, предоставляемые шаблонами с резервным использованием шаблонов.</span><span class="sxs-lookup"><span data-stu-id="6ead7-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="6ead7-107">Этот командлет позволяет легко начать с создания шаблона для существующих ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ead7-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="6ead7-108">В некоторых случаях, когда этот командлет не создает некоторые части шаблона, могут возникнуть ошибки.</span><span class="sxs-lookup"><span data-stu-id="6ead7-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="6ead7-109">Предупреждающее сообщение сообщит вам о неудачных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="6ead7-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="6ead7-110">Шаблон будет по-прежнему создан для успешно выполненных частей.</span><span class="sxs-lookup"><span data-stu-id="6ead7-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="6ead7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6ead7-111">EXAMPLES</span></span>

### <span data-ttu-id="6ead7-112">Пример 1: Экспорт группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ead7-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="6ead7-113">Эта команда перехватывает группу ресурсов с именем TestGroup в качестве шаблона и сохраняет ее в JSON-файле в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="6ead7-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="6ead7-114">Пример 2: экспорт одного ресурса из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ead7-114">Example 2: Export a single resource from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -Resource "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVirtualMachine"
```

<span data-ttu-id="6ead7-115">Эта команда перехватывает ресурс виртуальной машины с именем "TestVirtualMachine" из группы ресурсов "TestGroup" в качестве шаблона и сохраняет его в JSON-файле в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="6ead7-115">This command captures the Virtual Machine resource named "TestVirtualMachine" from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span>

### <span data-ttu-id="6ead7-116">Пример 3: Экспорт выбранных ресурсов из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ead7-116">Example 3: Export a selection of resources from a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup" -SkipAllParameterization -Resource @(
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Compute/virtualMachines/TestVm",
  "/subscriptions/5f43547b-1d2d-4a3e-ace4-88d4b600d568/resourceGroups/TestGroup/providers/Microsoft.Network/networkInterfaces/TestNic"
)
```

<span data-ttu-id="6ead7-117">Эта команда захватывает два ресурса из группы ресурсов "TestGroup" в качестве шаблона и сохраняет их в JSON-файле в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="6ead7-117">This command captures two resources from the "TestGroup" resource group as a template, and saves it to a JSON file in the current directory.</span></span> <span data-ttu-id="6ead7-118">Созданный шаблон не будет содержать никаких созданных параметров.</span><span class="sxs-lookup"><span data-stu-id="6ead7-118">The generated template will not contain any generated parameters.</span></span>

## <span data-ttu-id="6ead7-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6ead7-119">PARAMETERS</span></span>

### <span data-ttu-id="6ead7-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6ead7-120">-ApiVersion</span></span>
<span data-ttu-id="6ead7-121">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ead7-121">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6ead7-122">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="6ead7-122">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="6ead7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ead7-123">-DefaultProfile</span></span>
<span data-ttu-id="6ead7-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6ead7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ead7-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6ead7-125">-Force</span></span>
<span data-ttu-id="6ead7-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6ead7-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ead7-127">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="6ead7-127">-IncludeComments</span></span>
<span data-ttu-id="6ead7-128">Указывает на то, что эта операция экспортирует шаблон с примечаниями.</span><span class="sxs-lookup"><span data-stu-id="6ead7-128">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="6ead7-129">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="6ead7-129">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="6ead7-130">Указывает на то, что эта операция экспортирует параметр шаблона со значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ead7-130">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="6ead7-131">-Path</span><span class="sxs-lookup"><span data-stu-id="6ead7-131">-Path</span></span>
<span data-ttu-id="6ead7-132">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="6ead7-132">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="6ead7-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="6ead7-133">-Pre</span></span>
<span data-ttu-id="6ead7-134">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="6ead7-134">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="6ead7-135">-Resource</span><span class="sxs-lookup"><span data-stu-id="6ead7-135">-Resource</span></span>
<span data-ttu-id="6ead7-136">Список resourceIds, по которому нужно отфильтровать результаты.</span><span class="sxs-lookup"><span data-stu-id="6ead7-136">A list of resourceIds to filter the results by.</span></span>

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

### <span data-ttu-id="6ead7-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ead7-137">-ResourceGroupName</span></span>
<span data-ttu-id="6ead7-138">Указывает имя группы ресурсов для экспорта.</span><span class="sxs-lookup"><span data-stu-id="6ead7-138">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="6ead7-139">-SkipAllParameterization</span><span class="sxs-lookup"><span data-stu-id="6ead7-139">-SkipAllParameterization</span></span>
<span data-ttu-id="6ead7-140">Пропустить все параметризации.</span><span class="sxs-lookup"><span data-stu-id="6ead7-140">Skip all parameterization.</span></span>

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

### <span data-ttu-id="6ead7-141">-SkipResourceNameParameterization</span><span class="sxs-lookup"><span data-stu-id="6ead7-141">-SkipResourceNameParameterization</span></span>
<span data-ttu-id="6ead7-142">Пропускать параметризации имен ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ead7-142">Skip resource name parameterization.</span></span>

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

### <span data-ttu-id="6ead7-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ead7-143">-Confirm</span></span>
<span data-ttu-id="6ead7-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6ead7-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ead7-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ead7-145">-WhatIf</span></span>
<span data-ttu-id="6ead7-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6ead7-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ead7-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6ead7-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ead7-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ead7-148">CommonParameters</span></span>
<span data-ttu-id="6ead7-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6ead7-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ead7-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ead7-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ead7-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6ead7-151">INPUTS</span></span>

### <span data-ttu-id="6ead7-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6ead7-152">System.String</span></span>

## <span data-ttu-id="6ead7-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ead7-153">OUTPUTS</span></span>

### <span data-ttu-id="6ead7-154">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6ead7-154">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6ead7-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="6ead7-155">NOTES</span></span>

## <span data-ttu-id="6ead7-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ead7-156">RELATED LINKS</span></span>

[<span data-ttu-id="6ead7-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6ead7-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

