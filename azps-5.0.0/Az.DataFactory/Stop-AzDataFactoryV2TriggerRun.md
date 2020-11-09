---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2triggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2TriggerRun.md
ms.openlocfilehash: e2800614e414a041073ae5396fb4b0e1e5833b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313685"
---
# <span data-ttu-id="0e4c4-101">Stop-AzDataFactoryV2TriggerRun</span><span class="sxs-lookup"><span data-stu-id="0e4c4-101">Stop-AzDataFactoryV2TriggerRun</span></span>

## <span data-ttu-id="0e4c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e4c4-102">SYNOPSIS</span></span>
<span data-ttu-id="0e4c4-103">Остановка запуска триггера в фабрике данных.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-103">Stops a trigger run in a data factory.</span></span>

## <span data-ttu-id="0e4c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e4c4-104">SYNTAX</span></span>

### <span data-ttu-id="0e4c4-105">ByFactoryName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0e4c4-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4c4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0e4c4-106">ByInputObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-InputObject] <PSTriggerRun> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e4c4-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0e4c4-107">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2TriggerRun [-TriggerName] <String> [-TriggerRunId] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0e4c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e4c4-108">DESCRIPTION</span></span>
<span data-ttu-id="0e4c4-109">Командлет **Stop-AzDataFactoryV2TriggerRun** останавливает выполнение триггера в фабрике данных, указанной с именем триггера и идентификатором запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-109">The **Stop-AzDataFactoryV2TriggerRun** cmdlet stops a trigger run in a data factory specified with the trigger name and trigger run ID.</span></span>
<span data-ttu-id="0e4c4-110">В настоящее время поддерживается только для TumblingWindowTriggers в WaitingOnDependency состоянии.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-110">Currently only supported for TumblingWindowTriggers in WaitingOnDependency State.</span></span>

## <span data-ttu-id="0e4c4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e4c4-111">EXAMPLES</span></span>

### <span data-ttu-id="0e4c4-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0e4c4-112">Example 1</span></span>
```powershell
PS C:\> Stop-AzDataFactoryV2TriggerRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -TriggerName "testTumblingWindowTrigger" -TriggerRunId 08586002468005888497807248799CU16
```

<span data-ttu-id="0e4c4-113">Эта команда останавливает запуск триггера с идентификатором "08586002468005888497807248799CU16" в WikiADF Factory.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-113">This command stops the trigger run with id '08586002468005888497807248799CU16' in the factory WikiADF.</span></span>

## <span data-ttu-id="0e4c4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e4c4-114">PARAMETERS</span></span>

### <span data-ttu-id="0e4c4-115">— Фактическое.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-115">-DataFactory</span></span>
<span data-ttu-id="0e4c4-116">Объект фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-116">The data factory object.</span></span>

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

### <span data-ttu-id="0e4c4-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0e4c4-117">-DataFactoryName</span></span>
<span data-ttu-id="0e4c4-118">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-118">The data factory name.</span></span>

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

### <span data-ttu-id="0e4c4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e4c4-119">-DefaultProfile</span></span>
<span data-ttu-id="0e4c4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e4c4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e4c4-121">-InputObject</span></span>
<span data-ttu-id="0e4c4-122">Сведения о запуске триггера.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-122">The information about the trigger run.</span></span>

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

### <span data-ttu-id="0e4c4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0e4c4-123">-PassThru</span></span>
<span data-ttu-id="0e4c4-124">При успешном указании командлета записать истинную операцию в case.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-124">If specified the cmdlet write true in case operation succeeds.</span></span>

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

### <span data-ttu-id="0e4c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e4c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e4c4-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-126">The resource group name.</span></span>

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

### <span data-ttu-id="0e4c4-127">-TriggerName</span><span class="sxs-lookup"><span data-stu-id="0e4c4-127">-TriggerName</span></span>
<span data-ttu-id="0e4c4-128">Имя триггера.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-128">The trigger name.</span></span>

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

### <span data-ttu-id="0e4c4-129">-TriggerRunId</span><span class="sxs-lookup"><span data-stu-id="0e4c4-129">-TriggerRunId</span></span>
<span data-ttu-id="0e4c4-130">КОД запуска триггера.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-130">The Run ID of the trigger.</span></span>

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

### <span data-ttu-id="0e4c4-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0e4c4-131">-Confirm</span></span>
<span data-ttu-id="0e4c4-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e4c4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e4c4-133">-WhatIf</span></span>
<span data-ttu-id="0e4c4-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e4c4-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e4c4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e4c4-136">CommonParameters</span></span>
<span data-ttu-id="0e4c4-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e4c4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e4c4-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e4c4-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e4c4-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e4c4-139">INPUTS</span></span>

### <span data-ttu-id="0e4c4-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="0e4c4-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerRun</span></span>

### <span data-ttu-id="0e4c4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0e4c4-141">System.String</span></span>

### <span data-ttu-id="0e4c4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0e4c4-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="0e4c4-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e4c4-143">OUTPUTS</span></span>

### <span data-ttu-id="0e4c4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e4c4-144">System.Boolean</span></span>

## <span data-ttu-id="0e4c4-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e4c4-145">NOTES</span></span>

## <span data-ttu-id="0e4c4-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e4c4-146">RELATED LINKS</span></span>
