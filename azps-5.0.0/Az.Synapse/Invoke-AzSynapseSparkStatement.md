---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/invoke-azsynapsesparkstatement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Invoke-AzSynapseSparkStatement.md
ms.openlocfilehash: 64677ac73fecbaeaaaa327f21bc8e67e2a933d97
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246609"
---
# <span data-ttu-id="e86aa-101">Invoke-AzSynapseSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e86aa-101">Invoke-AzSynapseSparkStatement</span></span>

## <span data-ttu-id="e86aa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e86aa-102">SYNOPSIS</span></span>
<span data-ttu-id="e86aa-103">Вызывает оператор Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="e86aa-103">Invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e86aa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e86aa-104">SYNTAX</span></span>

### <span data-ttu-id="e86aa-105">RunSparkStatementByCodePathParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e86aa-105">RunSparkStatementByCodePathParameterSet (Default)</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86aa-106">RunSparkStatementByCodeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e86aa-106">RunSparkStatementByCodeParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -WorkspaceName <String> -SparkPoolName <String> -Language <String>
 -SessionId <Int32> -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e86aa-107">RunSparkStatementByCodeAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e86aa-107">RunSparkStatementByCodeAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -Code <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e86aa-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e86aa-108">RunSparkStatementByCodePathAndInputObjectParameterSet</span></span>
```
Invoke-AzSynapseSparkStatement -Language <String> -SessionObject <PSSynapseSparkSession> [-SessionId <Int32>]
 -FilePath <String> [-Response] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e86aa-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e86aa-109">DESCRIPTION</span></span>
<span data-ttu-id="e86aa-110">Командлет **Invoke-AzSynapseSparkStatement** вызывает инструкцию Synapse Analytics Spark.</span><span class="sxs-lookup"><span data-stu-id="e86aa-110">The **Invoke-AzSynapseSparkStatement** cmdlet invokes a Synapse Analytics Spark statement.</span></span>

## <span data-ttu-id="e86aa-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e86aa-111">EXAMPLES</span></span>

### <span data-ttu-id="e86aa-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e86aa-112">Example 1</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="e86aa-113">Эти команды применяют сеанс Spark, а затем вызывают встроенную инструкцию Spark с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="e86aa-113">These commands start a Spark session then invoke an inline Spark statement through pipeline.</span></span>

### <span data-ttu-id="e86aa-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e86aa-114">Example 2</span></span>
```powershell
PS C:\> Invoke-AzSynapseSparkStatement -SessionId 324 -Language 'Spark' -Code '
>> print("Hello world\n")
>> '
```

<span data-ttu-id="e86aa-115">Эти команды запускают сеанс Spark и вызывают встроенную инструкцию Spark.</span><span class="sxs-lookup"><span data-stu-id="e86aa-115">These commands start a Spark session then invoke an inline Spark statement.</span></span>

### <span data-ttu-id="e86aa-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e86aa-116">Example 3</span></span>
```powershell
PS C:\> $session = Start-AzSynapseSparkSession -WorkspaceName ContosoWorkspace -SparkPoolName ContosoSparkPool -Name ContosoSessionName -ExecutorCount 3 -ExecutorSize Small
PS C:\> $session.Language = 'Spark' 
PS C:\> $session | Invoke-AzSynapseSparkStatement -FilePath C:\path\to\code.sc
```

<span data-ttu-id="e86aa-117">Эти команды запускают сеанс Spark и вызывают в файле инструкции Spark.</span><span class="sxs-lookup"><span data-stu-id="e86aa-117">These commands start a Spark session then invoke Spark statements in a file.</span></span>

## <span data-ttu-id="e86aa-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e86aa-118">PARAMETERS</span></span>

### <span data-ttu-id="e86aa-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e86aa-119">-AsJob</span></span>
<span data-ttu-id="e86aa-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e86aa-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e86aa-121">-Code (код)</span><span class="sxs-lookup"><span data-stu-id="e86aa-121">-Code</span></span>
<span data-ttu-id="e86aa-122">Код выполнения.</span><span class="sxs-lookup"><span data-stu-id="e86aa-122">The execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeParameterSet, RunSparkStatementByCodeAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e86aa-123">-DefaultProfile</span></span>
<span data-ttu-id="e86aa-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e86aa-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e86aa-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="e86aa-125">-FilePath</span></span>
<span data-ttu-id="e86aa-126">Указывает локальный путь к файлу, который содержит код выполнения.</span><span class="sxs-lookup"><span data-stu-id="e86aa-126">Specifies a local file path that contains the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-127">-Language</span><span class="sxs-lookup"><span data-stu-id="e86aa-127">-Language</span></span>
<span data-ttu-id="e86aa-128">Язык кода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e86aa-128">Language of the execution code.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:
Accepted values: Spark, Scala, PySpark, Python, SparkDotNet, CSharp, SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-129">-Ответ</span><span class="sxs-lookup"><span data-stu-id="e86aa-129">-Response</span></span>
<span data-ttu-id="e86aa-130">Указывает на то, что должен возвращаться весь ответ.</span><span class="sxs-lookup"><span data-stu-id="e86aa-130">Indicates full response should be return.</span></span>

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

### <span data-ttu-id="e86aa-131">-SessionId</span><span class="sxs-lookup"><span data-stu-id="e86aa-131">-SessionId</span></span>
<span data-ttu-id="e86aa-132">Идентификатор сеанса Spark.</span><span class="sxs-lookup"><span data-stu-id="e86aa-132">Identifier of Spark session.</span></span>

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Int32
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-133">-SessionObject</span><span class="sxs-lookup"><span data-stu-id="e86aa-133">-SessionObject</span></span>
<span data-ttu-id="e86aa-134">Входной объект сеанса Spark, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e86aa-134">Spark session input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession
Parameter Sets: RunSparkStatementByCodeAndInputObjectParameterSet, RunSparkStatementByCodePathAndInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-135">-SparkPoolName</span><span class="sxs-lookup"><span data-stu-id="e86aa-135">-SparkPoolName</span></span>
<span data-ttu-id="e86aa-136">Название пула Spark Synapse.</span><span class="sxs-lookup"><span data-stu-id="e86aa-136">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-137">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="e86aa-137">-WorkspaceName</span></span>
<span data-ttu-id="e86aa-138">Имя Synapse рабочей области.</span><span class="sxs-lookup"><span data-stu-id="e86aa-138">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RunSparkStatementByCodePathParameterSet, RunSparkStatementByCodeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e86aa-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e86aa-139">-Confirm</span></span>
<span data-ttu-id="e86aa-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e86aa-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e86aa-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e86aa-141">-WhatIf</span></span>
<span data-ttu-id="e86aa-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e86aa-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e86aa-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e86aa-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e86aa-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e86aa-144">CommonParameters</span></span>
<span data-ttu-id="e86aa-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e86aa-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e86aa-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e86aa-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e86aa-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e86aa-147">INPUTS</span></span>

### <span data-ttu-id="e86aa-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e86aa-148">System.String</span></span>

### <span data-ttu-id="e86aa-149">Microsoft. Azure. Commands. Synapse. Models. PSSynapseSparkSession</span><span class="sxs-lookup"><span data-stu-id="e86aa-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSparkSession</span></span>

## <span data-ttu-id="e86aa-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e86aa-150">OUTPUTS</span></span>

### <span data-ttu-id="e86aa-151">Microsoft. Azure. Commands. Synapse. Models. PSSynapseExtendedSparkStatement</span><span class="sxs-lookup"><span data-stu-id="e86aa-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseExtendedSparkStatement</span></span>

## <span data-ttu-id="e86aa-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="e86aa-152">NOTES</span></span>

## <span data-ttu-id="e86aa-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e86aa-153">RELATED LINKS</span></span>
