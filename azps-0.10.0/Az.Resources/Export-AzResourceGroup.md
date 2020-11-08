---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-Azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Export-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Export-AzResourceGroup.md
ms.openlocfilehash: 90ad1932a325aa79a4da2daa839a9c1d02ea72e6
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077370"
---
# <span data-ttu-id="8c27d-101">Export-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c27d-101">Export-AzResourceGroup</span></span>

## <span data-ttu-id="8c27d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8c27d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c27d-103">Захватывает группу ресурсов в качестве шаблона и сохраняет ее в файле.</span><span class="sxs-lookup"><span data-stu-id="8c27d-103">Captures a resource group as a template and saves it to a file.</span></span>

## <span data-ttu-id="8c27d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8c27d-104">SYNTAX</span></span>

```
Export-AzResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c27d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c27d-105">DESCRIPTION</span></span>
<span data-ttu-id="8c27d-106">Командлет **Export-AzResourceGroup** захватывает указанную группу ресурсов в качестве шаблона и сохраняет ее в JSON-файле. Это может быть полезно в сценариях, где вы уже создали некоторые ресурсы в группе ресурсов, а затем хотите использовать преимущества, предоставляемые шаблонами с резервным использованием шаблонов.</span><span class="sxs-lookup"><span data-stu-id="8c27d-106">The **Export-AzResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="8c27d-107">Этот командлет позволяет легко начать с создания шаблона для существующих ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c27d-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>
<span data-ttu-id="8c27d-108">В некоторых случаях, когда этот командлет не создает некоторые части шаблона, могут возникнуть ошибки.</span><span class="sxs-lookup"><span data-stu-id="8c27d-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="8c27d-109">Предупреждающее сообщение сообщит вам о неудачных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="8c27d-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="8c27d-110">Шаблон будет по-прежнему создан для успешно выполненных частей.</span><span class="sxs-lookup"><span data-stu-id="8c27d-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="8c27d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8c27d-111">EXAMPLES</span></span>

### <span data-ttu-id="8c27d-112">Пример 1: Экспорт группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8c27d-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="8c27d-113">Эта команда перехватывает группу ресурсов с именем TestGroup в качестве шаблона и сохраняет ее в JSON-файле в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="8c27d-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="8c27d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8c27d-114">PARAMETERS</span></span>

### <span data-ttu-id="8c27d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8c27d-115">-ApiVersion</span></span>
<span data-ttu-id="8c27d-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8c27d-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="8c27d-117">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="8c27d-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="8c27d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c27d-118">-DefaultProfile</span></span>
<span data-ttu-id="8c27d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8c27d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="8c27d-120">-Force</span></span>
<span data-ttu-id="8c27d-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8c27d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8c27d-122">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="8c27d-122">-IncludeComments</span></span>
<span data-ttu-id="8c27d-123">Указывает на то, что эта операция экспортирует шаблон с примечаниями.</span><span class="sxs-lookup"><span data-stu-id="8c27d-123">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="8c27d-124">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="8c27d-124">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="8c27d-125">Указывает на то, что эта операция экспортирует параметр шаблона со значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8c27d-125">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="8c27d-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8c27d-126">-InformationAction</span></span>
<span data-ttu-id="8c27d-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="8c27d-127">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="8c27d-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8c27d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8c27d-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="8c27d-129">Continue</span></span>
- <span data-ttu-id="8c27d-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="8c27d-130">Ignore</span></span>
- <span data-ttu-id="8c27d-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="8c27d-131">Inquire</span></span>
- <span data-ttu-id="8c27d-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8c27d-132">SilentlyContinue</span></span>
- <span data-ttu-id="8c27d-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="8c27d-133">Stop</span></span>
- <span data-ttu-id="8c27d-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="8c27d-134">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27d-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8c27d-135">-InformationVariable</span></span>
<span data-ttu-id="8c27d-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="8c27d-136">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8c27d-137">-Path</span><span class="sxs-lookup"><span data-stu-id="8c27d-137">-Path</span></span>
<span data-ttu-id="8c27d-138">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="8c27d-138">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="8c27d-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="8c27d-139">-Pre</span></span>
<span data-ttu-id="8c27d-140">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="8c27d-140">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="8c27d-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c27d-141">-ResourceGroupName</span></span>
<span data-ttu-id="8c27d-142">Указывает имя группы ресурсов для экспорта.</span><span class="sxs-lookup"><span data-stu-id="8c27d-142">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="8c27d-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c27d-143">-Confirm</span></span>
<span data-ttu-id="8c27d-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8c27d-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c27d-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c27d-145">-WhatIf</span></span>
<span data-ttu-id="8c27d-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8c27d-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c27d-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8c27d-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c27d-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c27d-148">CommonParameters</span></span>
<span data-ttu-id="8c27d-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8c27d-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c27d-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c27d-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c27d-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8c27d-151">INPUTS</span></span>

## <span data-ttu-id="8c27d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8c27d-152">OUTPUTS</span></span>

## <span data-ttu-id="8c27d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="8c27d-153">NOTES</span></span>

## <span data-ttu-id="8c27d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8c27d-154">RELATED LINKS</span></span>

[<span data-ttu-id="8c27d-155">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8c27d-155">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)


