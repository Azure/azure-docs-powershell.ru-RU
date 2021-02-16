---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100229593"
---
# <span data-ttu-id="c811a-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="c811a-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="c811a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c811a-102">SYNOPSIS</span></span>
<span data-ttu-id="c811a-103">Отменяет спарк-заявление Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c811a-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c811a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c811a-104">SYNTAX</span></span>

### <span data-ttu-id="c811a-105">StopSparkStatementByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c811a-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c811a-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c811a-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c811a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c811a-107">DESCRIPTION</span></span>
<span data-ttu-id="c811a-108">Для отмены спарк-выписки по Synapse Analytics будет отменена **cmdlet Stop-AzSynapseSparkStatement.**</span><span class="sxs-lookup"><span data-stu-id="c811a-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="c811a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c811a-109">EXAMPLES</span></span>

### <span data-ttu-id="c811a-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c811a-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="c811a-111">Эта команда отменяет команду спарка с указанным livy ID.</span><span class="sxs-lookup"><span data-stu-id="c811a-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="c811a-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c811a-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="c811a-113">Эта команда отменяет команду спарка с указанным livy ID через канал.</span><span class="sxs-lookup"><span data-stu-id="c811a-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="c811a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c811a-114">PARAMETERS</span></span>

### <span data-ttu-id="c811a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c811a-115">-DefaultProfile</span></span>
<span data-ttu-id="c811a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c811a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c811a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c811a-117">-Force</span></span>
<span data-ttu-id="c811a-118">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c811a-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c811a-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="c811a-119">-LivyId</span></span>
<span data-ttu-id="c811a-120">Идентификатор спарк-идентификатора.</span><span class="sxs-lookup"><span data-stu-id="c811a-120">Identifier of Spark statement.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c811a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c811a-121">-PassThru</span></span>
<span data-ttu-id="c811a-122">Этот cmdlet не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c811a-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c811a-123">Если этот переключатель задан, возвращается истина, если он успешен.</span><span class="sxs-lookup"><span data-stu-id="c811a-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c811a-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="c811a-124">-SessionId</span></span>
<span data-ttu-id="c811a-125">Идентификатор спарк-сеанса.</span><span class="sxs-lookup"><span data-stu-id="c811a-125">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c811a-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="c811a-126">-SessionObject</span></span>
<span data-ttu-id="c811a-127">Объект ввода сеанса спарк-сеанса, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c811a-127">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: StopSparkStatementByIdFromParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c811a-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="c811a-128">-SparkPoolName</span></span>
<span data-ttu-id="c811a-129">Имя пула спарков Synapse.</span><span class="sxs-lookup"><span data-stu-id="c811a-129">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c811a-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c811a-130">-WorkspaceName</span></span>
<span data-ttu-id="c811a-131">Имя рабочей области Synapse.</span><span class="sxs-lookup"><span data-stu-id="c811a-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: StopSparkStatementByIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c811a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c811a-132">-Confirm</span></span>
<span data-ttu-id="c811a-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c811a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c811a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c811a-134">-WhatIf</span></span>
<span data-ttu-id="c811a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c811a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c811a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c811a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c811a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c811a-137">CommonParameters</span></span>
<span data-ttu-id="c811a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c811a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c811a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c811a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c811a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c811a-140">INPUTS</span></span>

### <span data-ttu-id="c811a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="c811a-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="c811a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c811a-142">OUTPUTS</span></span>

### <span data-ttu-id="c811a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c811a-143">System.Boolean</span></span>

## <span data-ttu-id="c811a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c811a-144">NOTES</span></span>

## <span data-ttu-id="c811a-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c811a-145">RELATED LINKS</span></span>
