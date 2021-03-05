---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/reset-azsynapsesparksessiontimeout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Reset-AzSynapseSparkSessionTimeout.md
ms.openlocfilehash: 485558c47fa8b879999777b79341fc855085b81a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973715"
---
# <span data-ttu-id="3a0fa-101">Reset-AzSynapseSparkSessionTimeout</span><span class="sxs-lookup"><span data-stu-id="3a0fa-101">Reset-AzSynapseSparkSessionTimeout</span></span>

## <span data-ttu-id="3a0fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a0fa-102">SYNOPSIS</span></span>
<span data-ttu-id="3a0fa-103">Сбрасывает время и время спарк-сеанса synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-103">Resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3a0fa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3a0fa-104">SYNTAX</span></span>

### <span data-ttu-id="3a0fa-105">ResetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3a0fa-105">ResetByNameParameterSet (Default)</span></span>
```
Reset-AzSynapseSparkSessionTimeout -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a0fa-106">ResetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a0fa-106">ResetByParentObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a0fa-107">ResetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a0fa-107">ResetByInputObjectParameterSet</span></span>
```
Reset-AzSynapseSparkSessionTimeout -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a0fa-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a0fa-108">DESCRIPTION</span></span>
<span data-ttu-id="3a0fa-109">Для сброса времени сеанса спарк-сеанса Synapse Analytics сбрасывается время сеанса **Remove-AzSynapseSparkSessionTimeout.**</span><span class="sxs-lookup"><span data-stu-id="3a0fa-109">The **Remove-AzSynapseSparkSessionTimeout** cmdlet resets timeout of a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="3a0fa-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3a0fa-110">EXAMPLES</span></span>

### <span data-ttu-id="3a0fa-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a0fa-111">Example 1</span></span>
```powershell
PS C:\> Reset-AzSynapseSparkSessionTimeout -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
```

<span data-ttu-id="3a0fa-112">Эта команда сбрасывает время сеанса спарк-аналитики Synapse с указанным livy ID.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-112">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID.</span></span>

### <span data-ttu-id="3a0fa-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3a0fa-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Reset-AzSynapseSparkSessionTimeout -LivyId 125
```

<span data-ttu-id="3a0fa-114">Эта команда сбрасывает время сеанса спарк-аналитики Synapse с указанным livy ID через канал.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-114">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

### <span data-ttu-id="3a0fa-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="3a0fa-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 125
PS C:\> $session | Reset-AzSynapseSparkSessionTimeout
```

<span data-ttu-id="3a0fa-116">Эта команда сбрасывает время сеанса спарк-аналитики Synapse с указанным livy ID через канал.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-116">This command resets timeout of the Synapse Analytics Spark session with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="3a0fa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3a0fa-117">PARAMETERS</span></span>

### <span data-ttu-id="3a0fa-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a0fa-118">-AsJob</span></span>
<span data-ttu-id="3a0fa-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3a0fa-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a0fa-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a0fa-120">-DefaultProfile</span></span>
<span data-ttu-id="3a0fa-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a0fa-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a0fa-122">-InputObject</span></span>
<span data-ttu-id="3a0fa-123">Объект ввода сеанса спарк-сеанса, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: ResetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a0fa-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="3a0fa-124">-LivyId</span></span>
<span data-ttu-id="3a0fa-125">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ResetByNameParameterSet, ResetByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a0fa-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a0fa-126">-PassThru</span></span>
<span data-ttu-id="3a0fa-127">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="3a0fa-128">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="3a0fa-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="3a0fa-129">-SparkPoolName</span></span>
<span data-ttu-id="3a0fa-130">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a0fa-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="3a0fa-131">-SparkPoolObject</span></span>
<span data-ttu-id="3a0fa-132">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: ResetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a0fa-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a0fa-133">-WorkspaceName</span></span>
<span data-ttu-id="3a0fa-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a0fa-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a0fa-135">-Confirm</span></span>
<span data-ttu-id="3a0fa-136">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a0fa-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a0fa-137">-WhatIf</span></span>
<span data-ttu-id="3a0fa-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a0fa-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a0fa-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a0fa-140">CommonParameters</span></span>
<span data-ttu-id="3a0fa-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a0fa-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a0fa-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a0fa-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a0fa-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a0fa-143">INPUTS</span></span>

### <span data-ttu-id="3a0fa-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="3a0fa-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="3a0fa-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="3a0fa-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="3a0fa-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3a0fa-146">OUTPUTS</span></span>

### <span data-ttu-id="3a0fa-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3a0fa-147">System.Boolean</span></span>

## <span data-ttu-id="3a0fa-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3a0fa-148">NOTES</span></span>

## <span data-ttu-id="3a0fa-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a0fa-149">RELATED LINKS</span></span>
