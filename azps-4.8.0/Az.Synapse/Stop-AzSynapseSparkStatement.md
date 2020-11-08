---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/stop-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Stop-AzSynapseSparkStatement.md
ms.openlocfilehash: 84d3f73735c3606813d769d9b0daf0f9716fc1a3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077465"
---
# <span data-ttu-id="eed4c-101">Stop-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="eed4c-101">Stop-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="eed4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eed4c-102">SYNOPSIS</span></span>
<span data-ttu-id="eed4c-103">Отменяет Synapse аналитическую инструкцию Spark.</span><span class="sxs-lookup"><span data-stu-id="eed4c-103">Cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="eed4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eed4c-104">SYNTAX</span></span>

### <span data-ttu-id="eed4c-105">StopSparkStatementByIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eed4c-105">StopSparkStatementByIdParameterSet (Default)</span></span>
```
Stop-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -LivyId <Int32> -SessionId <Int32>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eed4c-106">StopSparkStatementByIdFromParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed4c-106">StopSparkStatementByIdFromParentObjectParameterSet</span></span>
```
Stop-AzSynapseSparkStatement -SessionObject <PSSynapseSparkSession> -LivyId <Int32> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eed4c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed4c-107">DESCRIPTION</span></span>
<span data-ttu-id="eed4c-108">Командлет **Stop-AzSynapseSparkStatement** Отменяет инструкцию Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="eed4c-108">The **Stop-AzSynapseSparkStatement** cmdlet cancels a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="eed4c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eed4c-109">EXAMPLES</span></span>

### <span data-ttu-id="eed4c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eed4c-110">Example 1</span></span>
```powershell
PS C:\> Stop-AzSynapseStatement -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -SessionId 130 -LivyId 1
```

<span data-ttu-id="eed4c-111">Эта команда отменяет инструкцию Spark с указанным ИДЕНТИФИКАТОРом Livy.</span><span class="sxs-lookup"><span data-stu-id="eed4c-111">This command cancels the Spark statement with the specified livy ID.</span></span>

### <span data-ttu-id="eed4c-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="eed4c-112">Example 2</span></span>
```powershell
PS C:\> $session = Get-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -LivyId 130
PS C:\> $session | Stop-AzSynapseStatement -LivyId 3
```

<span data-ttu-id="eed4c-113">Эта команда отменяет инструкцию Spark с указанным ИД Livy в конвейере.</span><span class="sxs-lookup"><span data-stu-id="eed4c-113">This command cancels the Spark statement with the specified livy ID through pipeline.</span></span>

## <span data-ttu-id="eed4c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eed4c-114">PARAMETERS</span></span>

### <span data-ttu-id="eed4c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed4c-115">-DefaultProfile</span></span>
<span data-ttu-id="eed4c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed4c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed4c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="eed4c-117">-Force</span></span>
<span data-ttu-id="eed4c-118">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="eed4c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eed4c-119">-LivyId</span><span class="sxs-lookup"><span data-stu-id="eed4c-119">-LivyId</span></span>
<span data-ttu-id="eed4c-120">Идентификатор инструкции Spark.</span><span class="sxs-lookup"><span data-stu-id="eed4c-120">Identifier of Spark statement.</span></span>

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

### <span data-ttu-id="eed4c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eed4c-121">-PassThru</span></span>
<span data-ttu-id="eed4c-122">Этот командлет не возвращает объект по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="eed4c-122">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="eed4c-123">Если этот параметр указан, функция возвращает значение истина, если операция завершилась успешно.</span><span class="sxs-lookup"><span data-stu-id="eed4c-123">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eed4c-124">-SessionId</span><span class="sxs-lookup"><span data-stu-id="eed4c-124">-SessionId</span></span>
<span data-ttu-id="eed4c-125">Идентификатор сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="eed4c-125">Identifier of Spark session.</span></span>

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

### <span data-ttu-id="eed4c-126">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="eed4c-126">-SessionObject</span></span>
<span data-ttu-id="eed4c-127">Входной объект сеанса Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="eed4c-127">Spark session input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="eed4c-128">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="eed4c-128">-SparkPoolName</span></span>
<span data-ttu-id="eed4c-129">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="eed4c-129">Name of Synapse Spark pool.</span></span>

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

### <span data-ttu-id="eed4c-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="eed4c-130">-WorkspaceName</span></span>
<span data-ttu-id="eed4c-131">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="eed4c-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="eed4c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eed4c-132">-Confirm</span></span>
<span data-ttu-id="eed4c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eed4c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed4c-134">-WhatIf</span></span>
<span data-ttu-id="eed4c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eed4c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed4c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eed4c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed4c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed4c-137">CommonParameters</span></span>
<span data-ttu-id="eed4c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eed4c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed4c-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eed4c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed4c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eed4c-140">INPUTS</span></span>

### <span data-ttu-id="eed4c-141">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="eed4c-141">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="eed4c-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed4c-142">OUTPUTS</span></span>

### <span data-ttu-id="eed4c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eed4c-143">System.Boolean</span></span>

## <span data-ttu-id="eed4c-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="eed4c-144">NOTES</span></span>

## <span data-ttu-id="eed4c-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed4c-145">RELATED LINKS</span></span>
