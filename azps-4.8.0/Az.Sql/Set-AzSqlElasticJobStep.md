---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobStep.md
ms.openlocfilehash: 4f6f0471224799e818f9db29e5be5a4c49f9c45e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243878"
---
# <span data-ttu-id="8d1a3-101">Set-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="8d1a3-101">Set-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="8d1a3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="8d1a3-103">Обновляет шаг задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-103">Updates a job step</span></span>

## <span data-ttu-id="8d1a3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d1a3-104">SYNTAX</span></span>

### <span data-ttu-id="8d1a3-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d1a3-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-106">WithRemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8d1a3-106">WithRemoveOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-RemoveOutput] [-TargetGroupName <String>] [-CredentialName <String>]
 [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-107">WithAddOutput</span><span class="sxs-lookup"><span data-stu-id="8d1a3-107">WithAddOutput</span></span>
```
Set-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -OutputDatabaseResourceId <String> [-OutputCredentialName <String>]
 [-OutputTableName <String>] [-OutputSchemaName <String>] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-108">Объект</span><span class="sxs-lookup"><span data-stu-id="8d1a3-108">ObjectSet</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-OutputDatabaseObject <AzureSqlDatabaseModel>] [-OutputCredentialName <String>] [-OutputTableName <String>]
 [-OutputSchemaName <String>] [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-109">WithRemoveOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8d1a3-109">WithRemoveOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> [-RemoveOutput]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-110">WithAddOutputUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="8d1a3-110">WithAddOutputUsingParentObject</span></span>
```
Set-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8d1a3-111">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-OutputDatabaseObject <AzureSqlDatabaseModel>]
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-112">WithRemoveOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8d1a3-112">WithRemoveOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> [-RemoveOutput] [-TargetGroupName <String>]
 [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d1a3-113">WithAddOutputUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8d1a3-113">WithAddOutputUsingParentResourceId</span></span>
```
Set-AzSqlElasticJobStep [-ResourceId] <String> -OutputDatabaseResourceId <String>
 [-OutputCredentialName <String>] [-OutputTableName <String>] [-OutputSchemaName <String>]
 [-TargetGroupName <String>] [-CredentialName <String>] [-CommandText <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d1a3-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d1a3-114">DESCRIPTION</span></span>
<span data-ttu-id="8d1a3-115">Командлет Set-AzSqlElasticJobStep обновляет шаг задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-115">The Set-AzSqlElasticJobStep cmdlet updates a job step</span></span>

## <span data-ttu-id="8d1a3-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d1a3-116">EXAMPLES</span></span>

### <span data-ttu-id="8d1a3-117">Например, 1: обновляет целевую группу шага задания для задания.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-117">Example 1: Updates a job step's target group for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -TargetGroupName tg2

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg2             cred1                 (43200,10,1,120,2) SELECT 1
```

### <span data-ttu-id="8d1a3-118">Пример 2: обновление сценария T-SQL этапа задания для задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-118">Example 2: Updates a job step's T-SQL script for a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -StepName step1
$jobStep | Set-AzSqlElasticJobStep -CommandText "SELECT 2"

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 2
```

<span data-ttu-id="8d1a3-119">Обновляет шаг задания из задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-119">Updates a job step from a job</span></span>

### <span data-ttu-id="8d1a3-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8d1a3-120">Example 3</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticJobStep -AgentName agent -CommandText 'SELECT 2' -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="8d1a3-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d1a3-121">PARAMETERS</span></span>

### <span data-ttu-id="8d1a3-122">-AgentName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-122">-AgentName</span></span>
<span data-ttu-id="8d1a3-123">Имя агента</span><span class="sxs-lookup"><span data-stu-id="8d1a3-123">The agent name</span></span>

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

### <span data-ttu-id="8d1a3-124">-CommandText</span><span class="sxs-lookup"><span data-stu-id="8d1a3-124">-CommandText</span></span>
<span data-ttu-id="8d1a3-125">Текст команды</span><span class="sxs-lookup"><span data-stu-id="8d1a3-125">The command text</span></span>

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

### <span data-ttu-id="8d1a3-126">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-126">-CredentialName</span></span>
<span data-ttu-id="8d1a3-127">Имя учетных данных</span><span class="sxs-lookup"><span data-stu-id="8d1a3-127">The credential name</span></span>

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

### <span data-ttu-id="8d1a3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d1a3-128">-DefaultProfile</span></span>
<span data-ttu-id="8d1a3-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d1a3-130">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8d1a3-130">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="8d1a3-131">Начальная интервал повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="8d1a3-131">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="8d1a3-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d1a3-132">-InputObject</span></span>
<span data-ttu-id="8d1a3-133">Объект шага задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-133">The job step object</span></span>

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

### <span data-ttu-id="8d1a3-134">-JobName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-134">-JobName</span></span>
<span data-ttu-id="8d1a3-135">Имя задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-135">The job name</span></span>

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

### <span data-ttu-id="8d1a3-136">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="8d1a3-136">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="8d1a3-137">Максимальное значение интервала повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="8d1a3-137">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="8d1a3-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d1a3-138">-Name</span></span>
<span data-ttu-id="8d1a3-139">Имя шага</span><span class="sxs-lookup"><span data-stu-id="8d1a3-139">The step name</span></span>

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

### <span data-ttu-id="8d1a3-140">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-140">-OutputCredentialName</span></span>
<span data-ttu-id="8d1a3-141">Имя учетных данных выхода</span><span class="sxs-lookup"><span data-stu-id="8d1a3-141">The output credential name</span></span>

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

### <span data-ttu-id="8d1a3-142">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="8d1a3-142">-OutputDatabaseObject</span></span>
<span data-ttu-id="8d1a3-143">Объект выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="8d1a3-143">The output database object</span></span>

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

### <span data-ttu-id="8d1a3-144">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="8d1a3-144">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="8d1a3-145">Идентификатор ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="8d1a3-145">The output database resource id</span></span>

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

### <span data-ttu-id="8d1a3-146">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-146">-OutputSchemaName</span></span>
<span data-ttu-id="8d1a3-147">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="8d1a3-147">The output schema name</span></span>

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

### <span data-ttu-id="8d1a3-148">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-148">-OutputTableName</span></span>
<span data-ttu-id="8d1a3-149">Имя выходной таблицы</span><span class="sxs-lookup"><span data-stu-id="8d1a3-149">The output table name</span></span>

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

### <span data-ttu-id="8d1a3-150">-RemoveOutput</span><span class="sxs-lookup"><span data-stu-id="8d1a3-150">-RemoveOutput</span></span>
<span data-ttu-id="8d1a3-151">Флаг, указывающий, нужно ли удалять вывод</span><span class="sxs-lookup"><span data-stu-id="8d1a3-151">The flag to indicate whether to remove output</span></span>

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

### <span data-ttu-id="8d1a3-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-152">-ResourceGroupName</span></span>
<span data-ttu-id="8d1a3-153">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d1a3-153">The resource group name</span></span>

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

### <span data-ttu-id="8d1a3-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d1a3-154">-ResourceId</span></span>
<span data-ttu-id="8d1a3-155">Идентификатор ресурса шага задания</span><span class="sxs-lookup"><span data-stu-id="8d1a3-155">The job step resource id</span></span>

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

### <span data-ttu-id="8d1a3-156">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="8d1a3-156">-RetryAttempts</span></span>
<span data-ttu-id="8d1a3-157">Повторная попытка attemps</span><span class="sxs-lookup"><span data-stu-id="8d1a3-157">The retry attemps</span></span>

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

### <span data-ttu-id="8d1a3-158">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="8d1a3-158">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="8d1a3-159">Множитель для интервала повтора</span><span class="sxs-lookup"><span data-stu-id="8d1a3-159">The retry interval backoff multiplier</span></span>

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

### <span data-ttu-id="8d1a3-160">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="8d1a3-160">-ServerName</span></span>
<span data-ttu-id="8d1a3-161">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="8d1a3-161">The server name</span></span>

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

### <span data-ttu-id="8d1a3-162">-StepId</span><span class="sxs-lookup"><span data-stu-id="8d1a3-162">-StepId</span></span>
<span data-ttu-id="8d1a3-163">Текст идентификатора шага</span><span class="sxs-lookup"><span data-stu-id="8d1a3-163">The step id text</span></span>

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

### <span data-ttu-id="8d1a3-164">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="8d1a3-164">-TargetGroupName</span></span>
<span data-ttu-id="8d1a3-165">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="8d1a3-165">The target group name</span></span>

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

### <span data-ttu-id="8d1a3-166">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="8d1a3-166">-TimeoutSeconds</span></span>
<span data-ttu-id="8d1a3-167">Время ожидания в секундах</span><span class="sxs-lookup"><span data-stu-id="8d1a3-167">The timeout seconds</span></span>

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

### <span data-ttu-id="8d1a3-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d1a3-168">-Confirm</span></span>
<span data-ttu-id="8d1a3-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d1a3-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d1a3-170">-WhatIf</span></span>
<span data-ttu-id="8d1a3-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d1a3-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d1a3-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d1a3-173">CommonParameters</span></span>
<span data-ttu-id="8d1a3-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d1a3-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d1a3-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d1a3-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d1a3-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d1a3-176">INPUTS</span></span>

### <span data-ttu-id="8d1a3-177">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="8d1a3-177">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8d1a3-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d1a3-178">OUTPUTS</span></span>

### <span data-ttu-id="8d1a3-179">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="8d1a3-179">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="8d1a3-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d1a3-180">NOTES</span></span>

## <span data-ttu-id="8d1a3-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d1a3-181">RELATED LINKS</span></span>
