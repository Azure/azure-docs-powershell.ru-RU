---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/invoke-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Invoke-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: 91eb23f3af613cf349219f82d133d08dd6e65b5c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975016"
---
# <span data-ttu-id="fee46-101">Invoke-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="fee46-101">Invoke-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="fee46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee46-102">SYNOPSIS</span></span>
 <span data-ttu-id="fee46-103">Вызывает другой экземпляр запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="fee46-103">Invokes another instance of a trigger run.</span></span>

## <span data-ttu-id="fee46-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fee46-104">SYNTAX</span></span>

### <span data-ttu-id="fee46-105">ByFactoryNameByParameterFile (Default)</span><span class="sxs-lookup"><span data-stu-id="fee46-105">ByFactoryNameByParameterFile (Default)</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fee46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fee46-106">ByInputObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee46-107">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="fee46-107">ByFactoryName</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee46-108">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fee46-108">ByFactoryObject</span></span>
```
Invoke-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fee46-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fee46-109">DESCRIPTION</span></span>
<span data-ttu-id="fee46-110">Команда **Invoke-AzDataFactoryV2TriggerRun** запускает другой экземпляр запуска триггера с новым идом запуска.</span><span class="sxs-lookup"><span data-stu-id="fee46-110">The **Invoke-AzDataFactoryV2TriggerRun** command starts another instance of a trigger run with a new trigger run id.</span></span>

## <span data-ttu-id="fee46-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fee46-111">EXAMPLES</span></span>

### <span data-ttu-id="fee46-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fee46-112">Example 1</span></span>
```powershell
PS C:\> Invoke-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```
<span data-ttu-id="fee46-113">Запуск другого экземпляра триггера с новым идом запуска, сохраняя те же windowStartTime и windowEndTime, что и исходный запуск.</span><span class="sxs-lookup"><span data-stu-id="fee46-113">Starts another instance of a trigger run with a new trigger run id, keeping the same windowStartTime and windowEndTime as the original trigger run.</span></span>

## <span data-ttu-id="fee46-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fee46-114">PARAMETERS</span></span>

### <span data-ttu-id="fee46-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fee46-115">-DataFactory</span></span>
<span data-ttu-id="fee46-116">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="fee46-116">The data factory object.</span></span>

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

### <span data-ttu-id="fee46-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="fee46-117">-DataFactoryName</span></span>
<span data-ttu-id="fee46-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="fee46-118">The data factory name.</span></span>

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

### <span data-ttu-id="fee46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee46-119">-DefaultProfile</span></span>
<span data-ttu-id="fee46-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fee46-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fee46-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee46-121">-InputObject</span></span>
<span data-ttu-id="fee46-122">Сведения о запуске триггера.</span><span class="sxs-lookup"><span data-stu-id="fee46-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="fee46-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fee46-123">-PassThru</span></span>
<span data-ttu-id="fee46-124">Если для указанного cmdlet задано написание истина в случае успешной операции.</span><span class="sxs-lookup"><span data-stu-id="fee46-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="fee46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee46-125">-ResourceGroupName</span></span>
<span data-ttu-id="fee46-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fee46-126">The resource group name.</span></span>

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

### <span data-ttu-id="fee46-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="fee46-127">-TriggerName</span></span>
<span data-ttu-id="fee46-128">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="fee46-128">The trigger name.</span></span>

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

### <span data-ttu-id="fee46-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="fee46-129">-TriggerRunId</span></span>
<span data-ttu-id="fee46-130">ИД запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="fee46-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="fee46-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fee46-131">-Confirm</span></span>
<span data-ttu-id="fee46-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="fee46-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee46-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee46-133">-WhatIf</span></span>
<span data-ttu-id="fee46-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fee46-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee46-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fee46-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee46-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee46-136">CommonParameters</span></span>
<span data-ttu-id="fee46-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fee46-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee46-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fee46-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee46-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fee46-139">INPUTS</span></span>

### <span data-ttu-id="fee46-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="fee46-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="fee46-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fee46-141">System.String</span></span>

### <span data-ttu-id="fee46-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="fee46-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="fee46-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fee46-143">OUTPUTS</span></span>

### <span data-ttu-id="fee46-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span><span class="sxs-lookup"><span data-stu-id="fee46-144">Microsoft.Azure.Commands.DataFactoryV2.Models.PSPipeline</span></span>

## <span data-ttu-id="fee46-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fee46-145">NOTES</span></span>

## <span data-ttu-id="fee46-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fee46-146">RELATED LINKS</span></span>
