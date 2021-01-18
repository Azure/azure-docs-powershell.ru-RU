---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: af0fcf4e96d919c2c52a2ab30e583f288d20fc4e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518969"
---
# <span data-ttu-id="ac648-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="ac648-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="ac648-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac648-102">SYNOPSIS</span></span>
 <span data-ttu-id="ac648-103">Вызывает другой экземпляр запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="ac648-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="ac648-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ac648-104">SYNTAX</span></span>

### <span data-ttu-id="ac648-105">ByFactoryNameByParameterFile (Default)</span><span class="sxs-lookup"><span data-stu-id="ac648-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac648-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac648-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac648-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac648-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac648-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ac648-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac648-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac648-109">DESCRIPTION</span></span>
<span data-ttu-id="ac648-110">Команда **Invoke-AzDataFactoryV2TriggerRun** запускает другой экземпляр запуска триггера с новым идом запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="ac648-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="ac648-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ac648-111">EXAMPLES</span></span>

### <span data-ttu-id="ac648-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ac648-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="ac648-113">Запуск другого экземпляра триггера с новым идом запуска, сохраняя те же windowStartTime и windowEndTime, что и исходный триггер.</span><span class="sxs-lookup"><span data-stu-id="ac648-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="ac648-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac648-114">PARAMETERS</span></span>

### <span data-ttu-id="ac648-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ac648-115">-DataFactory</span></span>
<span data-ttu-id="ac648-116">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ac648-116">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac648-117">-DataFactoryName</span></span>
<span data-ttu-id="ac648-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="ac648-118">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac648-119">-DefaultProfile</span></span>
<span data-ttu-id="ac648-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac648-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac648-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac648-121">-InputObject</span></span>
<span data-ttu-id="ac648-122">Сведения о запуске триггера.</span><span class="sxs-lookup"><span data-stu-id="ac648-122">The information about the trigger run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac648-123">-PassThru</span></span>
<span data-ttu-id="ac648-124">Если для указанного cmdlet задано написание истина в случае успешного написания.</span><span class="sxs-lookup"><span data-stu-id="ac648-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="ac648-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac648-125">-ResourceGroupName</span></span>
<span data-ttu-id="ac648-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ac648-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="ac648-127">-TriggerName</span></span>
<span data-ttu-id="ac648-128">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="ac648-128">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="ac648-129">-TriggerRunId</span></span>
<span data-ttu-id="ac648-130">ИД запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="ac648-130">The Run ID of the trigger.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryObject
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac648-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac648-131">-Confirm</span></span>
<span data-ttu-id="ac648-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ac648-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac648-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac648-133">-WhatIf</span></span>
<span data-ttu-id="ac648-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac648-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac648-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ac648-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac648-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac648-136">CommonParameters</span></span>
<span data-ttu-id="ac648-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac648-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac648-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ac648-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac648-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ac648-139">INPUTS</span></span>

### <span data-ttu-id="ac648-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="ac648-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="ac648-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ac648-141">System.String</span></span>

### <span data-ttu-id="ac648-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac648-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="ac648-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ac648-143">OUTPUTS</span></span>

### <span data-ttu-id="ac648-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="ac648-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="ac648-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ac648-145">NOTES</span></span>

## <span data-ttu-id="ac648-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac648-146">RELATED LINKS</span></span>
