---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparksession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkSession.md
ms.openlocfilehash: c13fef9b8d0dbf34b3b31ca4a9a1e405a2583ac7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229604"
---
# <span data-ttu-id="c836c-101">Stop-AzSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c836c-101">Stop-AzSynapseSparkSession</span></span>

## <span data-ttu-id="c836c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c836c-102">SYNOPSIS</span></span>
<span data-ttu-id="c836c-103">Остановка сеанса спарк-аналитики Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c836c-103">Stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c836c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c836c-104">SYNTAX</span></span>

### <span data-ttu-id="c836c-105">DeleteByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c836c-105">DeleteByNameParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkSession -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c836c-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c836c-106">DeleteByParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -LivyId <Int32> -SparkPoolObject <PSSynapseSparkPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c836c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c836c-107">DeleteByInputObjectParameterSet</span></span>
```
Stop-AzSynapseSparkSession -InputObject <PSSynapseSparkSession> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c836c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c836c-108">DESCRIPTION</span></span>
<span data-ttu-id="c836c-109">**Спарклет Stop-AzSynapseSparkSession** останавливает сеанс спаркпарков Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c836c-109">The **Stop-AzSynapseSparkSession** cmdlet stops a Synapse Analytics Spark session.</span></span>

## <span data-ttu-id="c836c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c836c-110">EXAMPLES</span></span>

### <span data-ttu-id="c836c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c836c-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
```

<span data-ttu-id="c836c-112">Эта команда останавливает сеанс спарк-сеанса Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c836c-112">This command stops a Synapse Analytics Spark session.</span></span>

### <span data-ttu-id="c836c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c836c-113">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool
PS C:\> $pool | Stop-AzSynapseSparkSession -LivyId 324
```

<span data-ttu-id="c836c-114">Эта команда останавливает сеанс спаркпарков Synapse Analytics через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c836c-114">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

### <span data-ttu-id="c836c-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c836c-115">Example 3</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 324
PS C:\> $session | Stop-AzSynapseSparkSession
```

<span data-ttu-id="c836c-116">Эта команда останавливает сеанс спаркпарков Synapse Analytics через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c836c-116">This command stops a Synapse Analytics Spark session through pipeline.</span></span>

## <span data-ttu-id="c836c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c836c-117">PARAMETERS</span></span>

### <span data-ttu-id="c836c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c836c-118">-AsJob</span></span>
<span data-ttu-id="c836c-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c836c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c836c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c836c-120">-DefaultProfile</span></span>
<span data-ttu-id="c836c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c836c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c836c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c836c-122">-InputObject</span></span>
<span data-ttu-id="c836c-123">Объект ввода сеанса спарк-сеанса, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c836c-123">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c836c-124">-LivyId</span><span class="sxs-lookup"><span data-stu-id="c836c-124">-LivyId</span></span>
<span data-ttu-id="c836c-125">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="c836c-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c836c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c836c-126">-PassThru</span></span>
<span data-ttu-id="c836c-127">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c836c-127">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c836c-128">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="c836c-128">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c836c-129">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c836c-129">-SparkPoolName</span></span>
<span data-ttu-id="c836c-130">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="c836c-130">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c836c-131">-SparkPoolObject</span><span class="sxs-lookup"><span data-stu-id="c836c-131">-SparkPoolObject</span></span>
<span data-ttu-id="c836c-132">Входной объект пула спаркпарков, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c836c-132">Spark pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c836c-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c836c-133">-WorkspaceName</span></span>
<span data-ttu-id="c836c-134">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c836c-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c836c-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c836c-135">-Confirm</span></span>
<span data-ttu-id="c836c-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c836c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c836c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c836c-137">-WhatIf</span></span>
<span data-ttu-id="c836c-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c836c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c836c-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c836c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c836c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c836c-140">CommonParameters</span></span>
<span data-ttu-id="c836c-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c836c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c836c-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c836c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c836c-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c836c-143">INPUTS</span></span>

### <span data-ttu-id="c836c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="c836c-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkPool</span></span>

### <span data-ttu-id="c836c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c836c-145">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c836c-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c836c-146">OUTPUTS</span></span>

### <span data-ttu-id="c836c-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c836c-147">System.Boolean</span></span>

## <span data-ttu-id="c836c-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c836c-148">NOTES</span></span>

## <span data-ttu-id="c836c-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c836c-149">RELATED LINKS</span></span>
