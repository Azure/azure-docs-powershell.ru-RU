---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 63BBDF98-75FC-4A44-9FD0-95AD21ED93A6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Export-AzureRmResourceGroup.md
ms.openlocfilehash: 3b83b18bf7a795dd8df3c93a7fd2f8b25974ce35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562215"
---
# <span data-ttu-id="725b1-101">Export-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="725b1-101">Export-AzureRmResourceGroup</span></span>

## <span data-ttu-id="725b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="725b1-102">SYNOPSIS</span></span>
<span data-ttu-id="725b1-103">Захватывает группу ресурсов в качестве шаблона и сохраняет ее в файле.</span><span class="sxs-lookup"><span data-stu-id="725b1-103">Captures a resource group as a template and saves it to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="725b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="725b1-104">SYNTAX</span></span>

```
Export-AzureRmResourceGroup -ResourceGroupName <String> [-Path <String>] [-IncludeParameterDefaultValue]
 [-IncludeComments] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="725b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="725b1-105">DESCRIPTION</span></span>
<span data-ttu-id="725b1-106">Командлет **Export-AzureRmResourceGroup** захватывает указанную группу ресурсов в качестве шаблона и сохраняет ее в JSON-файле. Это может быть полезно в сценариях, где вы уже создали некоторые ресурсы в группе ресурсов, а затем хотите использовать преимущества, предоставляемые шаблонами с резервным использованием шаблонов.</span><span class="sxs-lookup"><span data-stu-id="725b1-106">The **Export-AzureRmResourceGroup** cmdlet captures the specified resource group as a template and saves it to a JSON file.This can be useful in scenarios where you have already created some resources in your resource group, and then want to leverage the benefits of using template backed deployments.</span></span>
<span data-ttu-id="725b1-107">Этот командлет позволяет легко начать с создания шаблона для существующих ресурсов в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="725b1-107">This cmdlet gives you an easy start by generating the template for your existing resources in the resource group.</span></span>

<span data-ttu-id="725b1-108">В некоторых случаях, когда этот командлет не создает некоторые части шаблона, могут возникнуть ошибки.</span><span class="sxs-lookup"><span data-stu-id="725b1-108">There might be some cases where this cmdlet fails to generate some parts of the template.</span></span>
<span data-ttu-id="725b1-109">Предупреждающее сообщение сообщит вам о неудачных ресурсах.</span><span class="sxs-lookup"><span data-stu-id="725b1-109">Warning messages will inform you of the resources that failed.</span></span>
<span data-ttu-id="725b1-110">Шаблон будет по-прежнему создан для успешно выполненных частей.</span><span class="sxs-lookup"><span data-stu-id="725b1-110">The template will still be generated for the parts that were successful.</span></span>

## <span data-ttu-id="725b1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="725b1-111">EXAMPLES</span></span>

### <span data-ttu-id="725b1-112">Пример 1: Экспорт группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="725b1-112">Example 1: Export a resource group</span></span>
```
PS C:\>Export-AzureRmResourceGroup -ResourceGroupName "TestGroup"
```

<span data-ttu-id="725b1-113">Эта команда перехватывает группу ресурсов с именем TestGroup в качестве шаблона и сохраняет ее в JSON-файле в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="725b1-113">This command captures the resource group named TestGroup as a template, and saves it to a JSON file in the current directory.</span></span>

## <span data-ttu-id="725b1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="725b1-114">PARAMETERS</span></span>

### <span data-ttu-id="725b1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="725b1-115">-ApiVersion</span></span>
<span data-ttu-id="725b1-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="725b1-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="725b1-117">Если этот элемент не указан, используется новейшая версия API.</span><span class="sxs-lookup"><span data-stu-id="725b1-117">If not specified, the latest API version is used.</span></span>

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

### <span data-ttu-id="725b1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="725b1-118">-Force</span></span>
<span data-ttu-id="725b1-119">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="725b1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="725b1-120">-IncludeComments</span><span class="sxs-lookup"><span data-stu-id="725b1-120">-IncludeComments</span></span>
<span data-ttu-id="725b1-121">Указывает на то, что эта операция экспортирует шаблон с примечаниями.</span><span class="sxs-lookup"><span data-stu-id="725b1-121">Indicates that this operation exports the template with comments.</span></span>

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

### <span data-ttu-id="725b1-122">-IncludeParameterDefaultValue</span><span class="sxs-lookup"><span data-stu-id="725b1-122">-IncludeParameterDefaultValue</span></span>
<span data-ttu-id="725b1-123">Указывает на то, что эта операция экспортирует параметр шаблона со значением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="725b1-123">Indicates that this operation exports the template parameter with the default value.</span></span>

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

### <span data-ttu-id="725b1-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="725b1-124">-InformationAction</span></span>
<span data-ttu-id="725b1-125">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="725b1-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="725b1-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="725b1-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="725b1-127">Продолжал</span><span class="sxs-lookup"><span data-stu-id="725b1-127">Continue</span></span>
- <span data-ttu-id="725b1-128">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="725b1-128">Ignore</span></span>
- <span data-ttu-id="725b1-129">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="725b1-129">Inquire</span></span>
- <span data-ttu-id="725b1-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="725b1-130">SilentlyContinue</span></span>
- <span data-ttu-id="725b1-131">Остановить</span><span class="sxs-lookup"><span data-stu-id="725b1-131">Stop</span></span>
- <span data-ttu-id="725b1-132">Рвать</span><span class="sxs-lookup"><span data-stu-id="725b1-132">Suspend</span></span>

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

### <span data-ttu-id="725b1-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="725b1-133">-InformationVariable</span></span>
<span data-ttu-id="725b1-134">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="725b1-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="725b1-135">-Path</span><span class="sxs-lookup"><span data-stu-id="725b1-135">-Path</span></span>
<span data-ttu-id="725b1-136">Указывает путь вывода для файла шаблона.</span><span class="sxs-lookup"><span data-stu-id="725b1-136">Specifies the output path of the template file.</span></span>

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

### <span data-ttu-id="725b1-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="725b1-137">-Pre</span></span>
<span data-ttu-id="725b1-138">Указывает на то, что этот командлет использует версии API предварительного выпуска при автоматическом определении используемой версии API.</span><span class="sxs-lookup"><span data-stu-id="725b1-138">Indicates that this cmdlet use pre-release API versions when automatically determining which API version to use.</span></span>

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

### <span data-ttu-id="725b1-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="725b1-139">-ResourceGroupName</span></span>
<span data-ttu-id="725b1-140">Указывает имя группы ресурсов для экспорта.</span><span class="sxs-lookup"><span data-stu-id="725b1-140">Specifies the name of the resource group to export.</span></span>

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

### <span data-ttu-id="725b1-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="725b1-141">-Confirm</span></span>
<span data-ttu-id="725b1-142">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="725b1-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="725b1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="725b1-143">-WhatIf</span></span>
<span data-ttu-id="725b1-144">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="725b1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="725b1-145">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="725b1-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="725b1-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725b1-146">-DefaultProfile</span></span>
<span data-ttu-id="725b1-147">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="725b1-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="725b1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725b1-148">CommonParameters</span></span>
<span data-ttu-id="725b1-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="725b1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725b1-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725b1-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725b1-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="725b1-151">INPUTS</span></span>

## <span data-ttu-id="725b1-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="725b1-152">OUTPUTS</span></span>

### <span data-ttu-id="725b1-153">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="725b1-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="725b1-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="725b1-154">NOTES</span></span>

## <span data-ttu-id="725b1-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="725b1-155">RELATED LINKS</span></span>

[<span data-ttu-id="725b1-156">Find-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="725b1-156">Find-AzureRmResourceGroup</span></span>](./Find-AzureRmResourceGroup.md)


