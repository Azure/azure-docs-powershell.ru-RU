---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 34f09ca41326b2f6686a41cdeba0910317bc7a2c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242628"
---
# <span data-ttu-id="6414c-101">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6414c-101">Start-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="6414c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6414c-102">SYNOPSIS</span></span>
<span data-ttu-id="6414c-103">Компилирует конфигурацию DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6414c-103">Compiles a DSC configuration in Automation.</span></span>

## <span data-ttu-id="6414c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6414c-104">SYNTAX</span></span>

```
Start-AzAutomationDscCompilationJob [-ConfigurationName] <String> [-Parameters <IDictionary>]
 [-ConfigurationData <IDictionary>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6414c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6414c-105">DESCRIPTION</span></span>
<span data-ttu-id="6414c-106">Командлет **Start-AzAutomationDscCompilationJob** компилирует конфигурацию нужной конфигурации ТД (DSC) в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6414c-106">The **Start-AzAutomationDscCompilationJob** cmdlet compiles an APS Desired State Configuration (DSC) configuration in Azure Automation.</span></span>

## <span data-ttu-id="6414c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6414c-107">EXAMPLES</span></span>

### <span data-ttu-id="6414c-108">Пример 1: компиляция конфигурации DSC Azure в автоматизации</span><span class="sxs-lookup"><span data-stu-id="6414c-108">Example 1: Compile an Azure DSC configuration in Automation</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6414c-109">Первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="6414c-109">The first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="6414c-110">Вторая команда компилирует конфигурацию DSC с именем Config01.</span><span class="sxs-lookup"><span data-stu-id="6414c-110">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="6414c-111">Команда содержит значения в $Params для параметров конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="6414c-111">The command includes the values in $Params for DSC configuration parameters.</span></span>

### <span data-ttu-id="6414c-112">Пример 2: компиляция конфигурации DSC Azure в автоматизации с новой версией сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="6414c-112">Example 2: Compile an Azure DSC configuration in Automation with a new Node Configuration build version.</span></span>
```
PS C:\>$Params = @{"StringParam"="Hello World";"IntegerParam"=32}
PS C:\> Start-AzAutomationDscCompilationJob -ConfigurationName "Config01" -Parameters $Params -ResourceGroupName "ResourceGroup01" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="6414c-113">Как и в первом примере, первая команда создает словарь параметров и сохраняет их в переменной $Params.</span><span class="sxs-lookup"><span data-stu-id="6414c-113">Similar to the first example, the first command creates a dictionary of parameters, and stores them in the $Params variable.</span></span>
<span data-ttu-id="6414c-114">Вторая команда компилирует конфигурацию DSC с именем Config01.</span><span class="sxs-lookup"><span data-stu-id="6414c-114">The second command compiles the DSC configuration named Config01.</span></span>
<span data-ttu-id="6414c-115">Команда содержит значения в $Params для параметров конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="6414c-115">The command includes the values in $Params for DSC configuration parameters.</span></span>
<span data-ttu-id="6414c-116">Она не переопределяет более раннюю конфигурацию узла, создавая новую конфигурацию узла с именем Config01 [<2>]. <NodeName> .</span><span class="sxs-lookup"><span data-stu-id="6414c-116">It does not override the earlier existing Node Configuration by creating a new Node Configuration with the name Config01[<2>].<NodeName>.</span></span> <span data-ttu-id="6414c-117">Номер версии увеличивается в зависимости от уже имеющегося номера версии.</span><span class="sxs-lookup"><span data-stu-id="6414c-117">The version number is incremented based on the existing version number already present.</span></span>

## <span data-ttu-id="6414c-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6414c-118">PARAMETERS</span></span>

### <span data-ttu-id="6414c-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6414c-119">-AutomationAccountName</span></span>
<span data-ttu-id="6414c-120">Указывает имя учетной записи автоматизации, содержащей конфигурацию DSC, которая компилируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="6414c-120">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-121">-ConfigurationData</span><span class="sxs-lookup"><span data-stu-id="6414c-121">-ConfigurationData</span></span>
<span data-ttu-id="6414c-122">Задает словарь данных конфигурации для конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="6414c-122">Specifies a dictionary of configuration data for DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-123">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="6414c-123">-ConfigurationName</span></span>
<span data-ttu-id="6414c-124">Задает имя конфигурации DSC, которую компилирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6414c-124">Specifies the name of the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6414c-125">-DefaultProfile</span></span>
<span data-ttu-id="6414c-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6414c-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6414c-127">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="6414c-127">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="6414c-128">Создает новую версию сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="6414c-128">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-129">-Parameters</span><span class="sxs-lookup"><span data-stu-id="6414c-129">-Parameters</span></span>
<span data-ttu-id="6414c-130">Указывает словарь параметров, которые используются этим командлетом для компиляции конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="6414c-130">Specifies a dictionary of parameters that this cmdlet uses to compile the DSC configuration.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6414c-131">-ResourceGroupName</span></span>
<span data-ttu-id="6414c-132">Указывает имя группы ресурсов, в которой этот командлет компилирует конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="6414c-132">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="6414c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6414c-133">-Confirm</span></span>
<span data-ttu-id="6414c-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6414c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6414c-135">-WhatIf</span></span>
<span data-ttu-id="6414c-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6414c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6414c-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6414c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6414c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6414c-138">CommonParameters</span></span>
<span data-ttu-id="6414c-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6414c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6414c-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6414c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6414c-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6414c-141">INPUTS</span></span>

### <span data-ttu-id="6414c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="6414c-142">System.String</span></span>

## <span data-ttu-id="6414c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6414c-143">OUTPUTS</span></span>

### <span data-ttu-id="6414c-144">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="6414c-144">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="6414c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="6414c-145">NOTES</span></span>

## <span data-ttu-id="6414c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6414c-146">RELATED LINKS</span></span>

[<span data-ttu-id="6414c-147">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="6414c-147">Get-AzAutomationDscCompilationJob</span></span>](./Get-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="6414c-148">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="6414c-148">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)


