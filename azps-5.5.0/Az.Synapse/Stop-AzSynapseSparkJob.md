---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkJob.md
ms.openlocfilehash: c916b5a7a7d56c241e3cd346c5b7386c0f36ddb1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229609"
---
# <span data-ttu-id="575da-101">Stop-AzSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="575da-101">Stop-AzSynapseSparkJob</span></span>

## <span data-ttu-id="575da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="575da-102">SYNOPSIS</span></span>
<span data-ttu-id="575da-103">Отменяет задание synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="575da-103">Cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="575da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="575da-104">SYNTAX</span></span>

### <span data-ttu-id="575da-105">StopSparkJobByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="575da-105">StopSparkJobByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkJob -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="575da-106">StopSparkJobByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="575da-106">StopSparkJobByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkPoolObject <PSSynapseSparkPool> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="575da-107">StopSparkJobByIdFromInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="575da-107">StopSparkJobByIdFromInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkJob -SparkJobObject <PSSynapseSparkJob> [-LivyId <Int32>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="575da-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="575da-108">DESCRIPTION</span></span>
<span data-ttu-id="575da-109">Для отмены задания synapse Analytics Spark будет отменено задание **Stop-AzSynapseSparkJob.**</span><span class="sxs-lookup"><span data-stu-id="575da-109">The **Stop-AzSynapseSparkJob** cmdlet cancels a Synapse Analytics Spark job.</span></span>

## <span data-ttu-id="575da-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="575da-110">EXAMPLES</span></span>

### <span data-ttu-id="575da-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="575da-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
```

<span data-ttu-id="575da-112">Эта команда отменяет задание synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="575da-112">This command cancels a Synapse Analytics Spark job.</span></span>

### <span data-ttu-id="575da-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="575da-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkJob -LivyId 130
```

<span data-ttu-id="575da-114">Эта команда отменяет задание спаркпарка Synapse Analytics через конвейер.</span><span class="sxs-lookup"><span data-stu-id="575da-114">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

### <span data-ttu-id="575da-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="575da-115">Example 3</span></span>
```powershell
PS C:\> $job = Get-AzSynapseSparkJob -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $job | Stop-AzSynapseSparkJob
```

<span data-ttu-id="575da-116">Эта команда отменяет задание спаркпарка Synapse Analytics через конвейер.</span><span class="sxs-lookup"><span data-stu-id="575da-116">This command cancels a Synapse Analytics Spark job through pipeline.</span></span>

## <span data-ttu-id="575da-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="575da-117">PARAMETERS</span></span>

### <span data-ttu-id="575da-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575da-118">-DefaultProfile</span></span>
<span data-ttu-id="575da-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="575da-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="575da-120">-Force</span><span class="sxs-lookup"><span data-stu-id="575da-120">-Force</span></span>
<span data-ttu-id="575da-121">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="575da-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="575da-122">-LivyId</span><span class="sxs-lookup"><span data-stu-id="575da-122">-LivyId</span></span>
<span data-ttu-id="575da-123">Идентификатор задания "Спарк".</span><span class="sxs-lookup"><span data-stu-id="575da-123">Identifier of Spark job.</span></span>

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

### <span data-ttu-id="575da-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="575da-124">-PassThru</span></span>
<span data-ttu-id="575da-125">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="575da-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="575da-126">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="575da-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="575da-127">-SparkJobObject</span><span class="sxs-lookup"><span data-stu-id="575da-127">-SparkJobObject</span></span>
<span data-ttu-id="575da-128">Объект ввода задания спарк-задания, обычно переданный по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="575da-128">Spark job input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="575da-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="575da-129">-SparkPoolName</span></span>
<span data-ttu-id="575da-130">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="575da-130">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="575da-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="575da-131">-SparkPoolObject</span></span>
<span data-ttu-id="575da-132">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="575da-132">Spark pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="575da-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="575da-133">-WorkspaceName</span></span>
<span data-ttu-id="575da-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="575da-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="575da-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="575da-135">-Confirm</span></span>
<span data-ttu-id="575da-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575da-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="575da-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="575da-137">-WhatIf</span></span>
<span data-ttu-id="575da-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="575da-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="575da-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="575da-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="575da-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575da-140">CommonParameters</span></span>
<span data-ttu-id="575da-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575da-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575da-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="575da-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575da-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="575da-143">INPUTS</span></span>

### <span data-ttu-id="575da-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="575da-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="575da-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span><span class="sxs-lookup"><span data-stu-id="575da-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkJob</span></span>

## <span data-ttu-id="575da-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="575da-146">OUTPUTS</span></span>

### <span data-ttu-id="575da-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="575da-147">System.Boolean</span></span>

## <span data-ttu-id="575da-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="575da-148">NOTES</span></span>

## <span data-ttu-id="575da-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="575da-149">RELATED LINKS</span></span>
