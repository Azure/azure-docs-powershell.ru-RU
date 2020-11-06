---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 790a0f0383796728b4754c4d64d98ef2ca7ed3c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561943"
---
# <span data-ttu-id="db45f-101">Start-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="db45f-101">Start-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="db45f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db45f-102">SYNOPSIS</span></span>
<span data-ttu-id="db45f-103">Компилирует конфигурацию DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="db45f-103">Compiles a DSC configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db45f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db45f-104">SYNTAX</span></span>

```
Start-AzureRmAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db45f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db45f-105">DESCRIPTION</span></span>
<span data-ttu-id="db45f-106">Командлет **Start-AzureRmAutomationDscCompilationJob** компилирует конфигурацию нужной конфигурации ТД (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="db45f-106">The **Start-AzureRmAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="db45f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db45f-107">EXAMPLES</span></span>

### <span data-ttu-id="db45f-108">Пример 1: компиляция конфигурации DSC Azure в автоматизации</span><span class="sxs-lookup"><span data-stu-id="db45f-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="db45f-109">Первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="db45f-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="db45f-110">Вторая команда компилирует конфигурацию DSC с именем Config01.</span><span class="sxs-lookup"><span data-stu-id="db45f-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="db45f-111">Команда содержит значения в $Params для параметров конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="db45f-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="db45f-112">Пример 2: компиляция конфигурации DSC Azure в автоматизации с новой версией сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="db45f-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzureRmAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="db45f-113">Как и в первом примере, первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="db45f-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>

<span data-ttu-id="db45f-114">Вторая команда компилирует конфигурацию DSC с именем Config01.</span><span class="sxs-lookup"><span data-stu-id="db45f-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="db45f-115">Команда содержит значения в $Params для параметров конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="db45f-115">The command includes the values in $Params for DSC configuration parameters.</span></span>

<span data-ttu-id="db45f-116">Она не переопределяет более раннюю конфигурацию узла, создавая новую конфигурацию узла с именем Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="db45f-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="db45f-117">Номер версии увеличивается в зависимости от уже имеющегося номера версии.</span><span class="sxs-lookup"><span data-stu-id="db45f-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="db45f-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db45f-118">PARAMETERS</span></span>

### <span data-ttu-id="db45f-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="db45f-119">-AutomationAccountName</span></span>
<span data-ttu-id="db45f-120">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="db45f-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="db45f-121">-ConfigurationData</span></span>
<span data-ttu-id="db45f-122">Задает словарь данных конфигурации для конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="db45f-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="db45f-123">-ConfigurationName</span></span>
<span data-ttu-id="db45f-124">Задает имя конфигурации DSC, которую компилирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="db45f-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db45f-125">-DefaultProfile</span></span>
<span data-ttu-id="db45f-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="db45f-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="db45f-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="db45f-128">Создает новую версию сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="db45f-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="db45f-129">-Parameters</span></span>
<span data-ttu-id="db45f-130">Указывает словарь параметров, которые используются этим командлетом для компиляции конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="db45f-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db45f-131">-ResourceGroupName</span></span>
<span data-ttu-id="db45f-132">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="db45f-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db45f-133">-Confirm</span></span>
<span data-ttu-id="db45f-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db45f-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db45f-135">-WhatIf</span></span>
<span data-ttu-id="db45f-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db45f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db45f-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db45f-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db45f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db45f-138">CommonParameters</span></span>
<span data-ttu-id="db45f-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db45f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db45f-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db45f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db45f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db45f-141">INPUTS</span></span>

### <span data-ttu-id="db45f-142">Ничего</span><span class="sxs-lookup"><span data-stu-id="db45f-142">None</span></span>
<span data-ttu-id="db45f-143">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="db45f-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db45f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db45f-144">OUTPUTS</span></span>

### <span data-ttu-id="db45f-145">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="db45f-145">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="db45f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="db45f-146">NOTES</span></span>

## <span data-ttu-id="db45f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db45f-147">RELATED LINKS</span></span>

[<span data-ttu-id="db45f-148">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="db45f-148">Get-AzureRmAutomationDscCompilationJob</span></span>](./Get-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="db45f-149">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="db45f-149">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)


