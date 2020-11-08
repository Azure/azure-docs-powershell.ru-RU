---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245743"
---
# <span data-ttu-id="15ffa-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="15ffa-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="15ffa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15ffa-102">SYNOPSIS</span></span>
<span data-ttu-id="15ffa-103">Отменяет задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="15ffa-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="15ffa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15ffa-104">SYNTAX</span></span>

### <span data-ttu-id="15ffa-105">StopSparkJobByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15ffa-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ffa-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ffa-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15ffa-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15ffa-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15ffa-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15ffa-108">DESCRIPTION</span></span>
<span data-ttu-id="15ffa-109">Командлет **Stop-AzSynapseSparkJob** отменяет задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="15ffa-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="15ffa-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15ffa-110">EXAMPLES</span></span>

### <span data-ttu-id="15ffa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="15ffa-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="15ffa-112">Эта команда отменяет задание Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="15ffa-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="15ffa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="15ffa-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="15ffa-114">Эта команда отменяет задание Synapse Analytics Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="15ffa-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="15ffa-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="15ffa-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="15ffa-116">Эта команда отменяет задание Synapse Analytics Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="15ffa-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="15ffa-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15ffa-117">PARAMETERS</span></span>

### <span data-ttu-id="15ffa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15ffa-118">-DefaultProfile</span></span>
<span data-ttu-id="15ffa-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15ffa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15ffa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="15ffa-120">-Force</span></span>
<span data-ttu-id="15ffa-121">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="15ffa-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="15ffa-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="15ffa-122">-LivyId</span></span>
<span data-ttu-id="15ffa-123">Идентификатор задания Spark.</span><span class="sxs-lookup"><span data-stu-id="15ffa-123">Identifier of Spark job.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdParameterSet, StopSparkJobByIdFromParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ffa-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15ffa-124">-PassThru</span></span>
<span data-ttu-id="15ffa-125">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15ffa-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="15ffa-126">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="15ffa-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="15ffa-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="15ffa-127">-SparkJobObject</span></span>
<span data-ttu-id="15ffa-128">Объект ввода задания Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="15ffa-128">Spark job input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob
Parameter Sets: StopSparkJobByIdFromInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ffa-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="15ffa-129">-SparkPoolName</span></span>
<span data-ttu-id="15ffa-130">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="15ffa-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ffa-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="15ffa-131">-SparkPoolObject</span></span>
<span data-ttu-id="15ffa-132">Входной объект пула Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="15ffa-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: StopSparkJobByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15ffa-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="15ffa-133">-WorkspaceName</span></span>
<span data-ttu-id="15ffa-134">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="15ffa-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkJobByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15ffa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15ffa-135">-Confirm</span></span>
<span data-ttu-id="15ffa-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15ffa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15ffa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15ffa-137">-WhatIf</span></span>
<span data-ttu-id="15ffa-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15ffa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15ffa-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15ffa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15ffa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15ffa-140">CommonParameters</span></span>
<span data-ttu-id="15ffa-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15ffa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15ffa-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15ffa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15ffa-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15ffa-143">INPUTS</span></span>

### <span data-ttu-id="15ffa-144">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="15ffa-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="15ffa-145">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="15ffa-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="15ffa-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15ffa-146">OUTPUTS</span></span>

### <span data-ttu-id="15ffa-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="15ffa-147">System.Boolean</span></span>

## <span data-ttu-id="15ffa-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="15ffa-148">NOTES</span></span>

## <span data-ttu-id="15ffa-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15ffa-149">RELATED LINKS</span></span>
