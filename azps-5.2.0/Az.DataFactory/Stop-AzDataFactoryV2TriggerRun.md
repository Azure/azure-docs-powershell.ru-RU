---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391351"
---
# <span data-ttu-id="5050c-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="5050c-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="5050c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5050c-102">SYNOPSIS</span></span>
<span data-ttu-id="5050c-103">Остановка запуска триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="5050c-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="5050c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5050c-104">SYNTAX</span></span>

### <span data-ttu-id="5050c-105">ByFactoryName (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5050c-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5050c-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5050c-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="5050c-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5050c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5050c-108">DESCRIPTION</span></span>
<span data-ttu-id="5050c-109">**Cmdlet Stop-AzDataFactoryV2TriggerRun** останавливает запуск триггера в фабрике данных, заданном с именем триггера и именем триггера.</span><span class="sxs-lookup"><span data-stu-id="5050c-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="5050c-110">В настоящее время поддерживается только для TumblingWindowTriggers в области WaitingOnDependency.</span><span class="sxs-lookup"><span data-stu-id="5050c-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="5050c-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5050c-111">EXAMPLES</span></span>

### <span data-ttu-id="5050c-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5050c-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="5050c-113">Эта команда останавливает запуск триггера вместе с идом '08586002468005888497807248799CU16' на заводском wikiADF.</span><span class="sxs-lookup"><span data-stu-id="5050c-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="5050c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5050c-114">PARAMETERS</span></span>

### <span data-ttu-id="5050c-115">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="5050c-115">-DataFactory</span></span>
<span data-ttu-id="5050c-116">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5050c-116">The data factory object.</span></span>

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

### <span data-ttu-id="5050c-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="5050c-117">-DataFactoryName</span></span>
<span data-ttu-id="5050c-118">Название фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="5050c-118">The data factory name.</span></span>

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

### <span data-ttu-id="5050c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5050c-119">-DefaultProfile</span></span>
<span data-ttu-id="5050c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5050c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5050c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5050c-121">-InputObject</span></span>
<span data-ttu-id="5050c-122">Сведения о запуске триггера.</span><span class="sxs-lookup"><span data-stu-id="5050c-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="5050c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5050c-123">-PassThru</span></span>
<span data-ttu-id="5050c-124">Если для указанного cmdlet задано написание истина в случае успешного написания.</span><span class="sxs-lookup"><span data-stu-id="5050c-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="5050c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5050c-125">-ResourceGroupName</span></span>
<span data-ttu-id="5050c-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5050c-126">The resource group name.</span></span>

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

### <span data-ttu-id="5050c-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="5050c-127">-TriggerName</span></span>
<span data-ttu-id="5050c-128">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="5050c-128">The trigger name.</span></span>

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

### <span data-ttu-id="5050c-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="5050c-129">-TriggerRunId</span></span>
<span data-ttu-id="5050c-130">ИД запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="5050c-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="5050c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5050c-131">-Confirm</span></span>
<span data-ttu-id="5050c-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="5050c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5050c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5050c-133">-WhatIf</span></span>
<span data-ttu-id="5050c-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5050c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5050c-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5050c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5050c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5050c-136">CommonParameters</span></span>
<span data-ttu-id="5050c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5050c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5050c-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5050c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5050c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5050c-139">INPUTS</span></span>

### <span data-ttu-id="5050c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="5050c-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="5050c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="5050c-141">System.String</span></span>

### <span data-ttu-id="5050c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="5050c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="5050c-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5050c-143">OUTPUTS</span></span>

### <span data-ttu-id="5050c-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5050c-144">System.Boolean</span></span>

## <span data-ttu-id="5050c-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5050c-145">NOTES</span></span>

## <span data-ttu-id="5050c-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5050c-146">RELATED LINKS</span></span>
