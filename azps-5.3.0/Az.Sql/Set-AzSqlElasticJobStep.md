---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506469"
---
# <span data-ttu-id="726a6-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="726a6-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="726a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="726a6-102">SYNOPSIS</span></span>
<span data-ttu-id="726a6-103">Обновление шага задания</span><span class="sxs-lookup"><span data-stu-id="726a6-103">Updates a job step</span></span>

## <span data-ttu-id="726a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="726a6-104">SYNTAX</span></span>

### <span data-ttu-id="726a6-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="726a6-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726a6-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="726a6-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="726a6-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="726a6-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="726a6-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="726a6-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726a6-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="726a6-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726a6-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="726a6-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726a6-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="726a6-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="726a6-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="726a6-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="726a6-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="726a6-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="726a6-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="726a6-114">DESCRIPTION</span></span>
<span data-ttu-id="726a6-115">Новый Set-AzSqlElasticJobStep обновляет шаг задания</span><span class="sxs-lookup"><span data-stu-id="726a6-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="726a6-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="726a6-116">EXAMPLES</span></span>

### <span data-ttu-id="726a6-117">Пример 1. Обновление целевой группы шага задания</span><span class="sxs-lookup"><span data-stu-id="726a6-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="726a6-118">Пример 2. Обновление сценария T-SQL задания</span><span class="sxs-lookup"><span data-stu-id="726a6-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="726a6-119">Обновление шага задания</span><span class="sxs-lookup"><span data-stu-id="726a6-119">Updates a job step from a job</span></span>

### <span data-ttu-id="726a6-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="726a6-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="726a6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="726a6-121">PARAMETERS</span></span>

### <span data-ttu-id="726a6-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="726a6-122">-AgentName</span></span>
<span data-ttu-id="726a6-123">Имя агента</span><span class="sxs-lookup"><span data-stu-id="726a6-123">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="726a6-124">-CommandText</span></span>
<span data-ttu-id="726a6-125">Текст команды</span><span class="sxs-lookup"><span data-stu-id="726a6-125">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="726a6-126">-CredentialName</span></span>
<span data-ttu-id="726a6-127">Имя учетной данные</span><span class="sxs-lookup"><span data-stu-id="726a6-127">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="726a6-128">-DefaultProfile</span></span>
<span data-ttu-id="726a6-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="726a6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="726a6-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="726a6-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="726a6-131">Начальная retry interval seconds</span><span class="sxs-lookup"><span data-stu-id="726a6-131">The initial retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="726a6-132">-InputObject</span></span>
<span data-ttu-id="726a6-133">Объект шага задания</span><span class="sxs-lookup"><span data-stu-id="726a6-133">The job step object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet, WithRemoveOutputUsingParentObject, WithAddOutputUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="726a6-134">-JobName</span></span>
<span data-ttu-id="726a6-135">Имя задания</span><span class="sxs-lookup"><span data-stu-id="726a6-135">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="726a6-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="726a6-137">Максимальное значение интервала повторного интервала</span><span class="sxs-lookup"><span data-stu-id="726a6-137">The maximum retry interval seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-138">-Name</span><span class="sxs-lookup"><span data-stu-id="726a6-138">-Name</span></span>
<span data-ttu-id="726a6-139">Имя шага</span><span class="sxs-lookup"><span data-stu-id="726a6-139">The step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="726a6-140">-OutputCredentialName</span></span>
<span data-ttu-id="726a6-141">Имя выходных учетных данных</span><span class="sxs-lookup"><span data-stu-id="726a6-141">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="726a6-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="726a6-143">Выходной объект базы данных</span><span class="sxs-lookup"><span data-stu-id="726a6-143">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="726a6-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="726a6-145">ИД ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="726a6-145">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithAddOutput, WithAddOutputUsingParentObject, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="726a6-146">-OutputSchemaName</span></span>
<span data-ttu-id="726a6-147">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="726a6-147">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="726a6-148">-OutputTableName</span></span>
<span data-ttu-id="726a6-149">Имя выводной таблицы</span><span class="sxs-lookup"><span data-stu-id="726a6-149">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithAddOutput, ObjectSet, WithAddOutputUsingParentObject, ResourceIdSet, WithAddOutputUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="726a6-150">-RemoveOutput</span></span>
<span data-ttu-id="726a6-151">Флажок, который показывает, нужно ли удалять выходные данные</span><span class="sxs-lookup"><span data-stu-id="726a6-151">The flag to indicate whether to remove output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WithRemoveOutput, WithRemoveOutputUsingParentObject, WithRemoveOutputUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="726a6-152">-ResourceGroupName</span></span>
<span data-ttu-id="726a6-153">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="726a6-153">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="726a6-154">-ResourceId</span></span>
<span data-ttu-id="726a6-155">ИД ресурса шага задания</span><span class="sxs-lookup"><span data-stu-id="726a6-155">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithRemoveOutputUsingParentResourceId, WithAddOutputUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="726a6-156">-RetryAttempts</span></span>
<span data-ttu-id="726a6-157">Повторить атемпуты</span><span class="sxs-lookup"><span data-stu-id="726a6-157">The retry attemps</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="726a6-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="726a6-159">Множитель backoff интервала повторно</span><span class="sxs-lookup"><span data-stu-id="726a6-159">The retry interval backoff multiplier</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="726a6-160">-ServerName</span></span>
<span data-ttu-id="726a6-161">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="726a6-161">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithRemoveOutput, WithAddOutput
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="726a6-162">-StepId</span></span>
<span data-ttu-id="726a6-163">Текст пошаговая пошаговая пошаговая по</span><span class="sxs-lookup"><span data-stu-id="726a6-163">The step id text</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="726a6-164">-TargetGroupName</span></span>
<span data-ttu-id="726a6-165">Название целевой группы</span><span class="sxs-lookup"><span data-stu-id="726a6-165">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="726a6-166">-TimeoutSeconds</span></span>
<span data-ttu-id="726a6-167">Время времени и времени.</span><span class="sxs-lookup"><span data-stu-id="726a6-167">The timeout seconds</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="726a6-168">-Confirm</span></span>
<span data-ttu-id="726a6-169">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726a6-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="726a6-170">-WhatIf</span></span>
<span data-ttu-id="726a6-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="726a6-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="726a6-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="726a6-172">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="726a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="726a6-173">CommonParameters</span></span>
<span data-ttu-id="726a6-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="726a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="726a6-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="726a6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="726a6-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="726a6-176">INPUTS</span></span>

### <span data-ttu-id="726a6-177">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="726a6-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="726a6-178">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="726a6-178">OUTPUTS</span></span>

### <span data-ttu-id="726a6-179">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="726a6-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="726a6-180">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="726a6-180">NOTES</span></span>

## <span data-ttu-id="726a6-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="726a6-181">RELATED LINKS</span></span>
