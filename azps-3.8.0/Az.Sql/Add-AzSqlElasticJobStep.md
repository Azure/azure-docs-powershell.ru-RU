---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 25c9845d0912374baa0e2219c234f63abe381cfc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065744"
---
# <span data-ttu-id="9a84b-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="9a84b-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="9a84b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9a84b-102">SYNOPSIS</span></span>
<span data-ttu-id="9a84b-103">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="9a84b-103">Adds a job step to a job</span></span>

## <span data-ttu-id="9a84b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9a84b-104">SYNTAX</span></span>

### <span data-ttu-id="9a84b-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9a84b-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a84b-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="9a84b-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a84b-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="9a84b-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a84b-108">Объект</span><span class="sxs-lookup"><span data-stu-id="9a84b-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a84b-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9a84b-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a84b-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="9a84b-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a84b-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9a84b-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a84b-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a84b-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a84b-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a84b-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a84b-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a84b-114">DESCRIPTION</span></span>
<span data-ttu-id="9a84b-115">Командлет Add-AzSqlElasticJobStep добавляет шаг задания в задание.</span><span class="sxs-lookup"><span data-stu-id="9a84b-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="9a84b-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9a84b-116">EXAMPLES</span></span>

### <span data-ttu-id="9a84b-117">Пример 1: Добавление шага к заданию</span><span class="sxs-lookup"><span data-stu-id="9a84b-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="9a84b-118">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="9a84b-118">Adds a job step to a job</span></span>

## <span data-ttu-id="9a84b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9a84b-119">PARAMETERS</span></span>

### <span data-ttu-id="9a84b-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="9a84b-120">-AgentName</span></span>
<span data-ttu-id="9a84b-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="9a84b-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="9a84b-122">-CommandText</span></span>
<span data-ttu-id="9a84b-123">Текст команды</span><span class="sxs-lookup"><span data-stu-id="9a84b-123">The command text</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="9a84b-124">-CredentialName</span></span>
<span data-ttu-id="9a84b-125">Имя учетных данных</span><span class="sxs-lookup"><span data-stu-id="9a84b-125">The credential name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a84b-126">-DefaultProfile</span></span>
<span data-ttu-id="9a84b-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9a84b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a84b-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="9a84b-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="9a84b-129">Начальная интервал повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="9a84b-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="9a84b-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="9a84b-130">-JobName</span></span>
<span data-ttu-id="9a84b-131">Имя задания</span><span class="sxs-lookup"><span data-stu-id="9a84b-131">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="9a84b-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="9a84b-133">Максимальное значение интервала повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="9a84b-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="9a84b-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9a84b-134">-Name</span></span>
<span data-ttu-id="9a84b-135">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="9a84b-135">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="9a84b-136">-OutputCredentialName</span></span>
<span data-ttu-id="9a84b-137">Имя учетных данных выхода</span><span class="sxs-lookup"><span data-stu-id="9a84b-137">The output credential name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="9a84b-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="9a84b-139">Объект выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="9a84b-139">The output database object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: WithOutputDb, WithOutputDbUsingParentObject, WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="9a84b-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="9a84b-141">Идентификатор ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="9a84b-141">The output database resource id</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDbId, WithOutputDbIdUsingParentObject, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="9a84b-142">-OutputSchemaName</span></span>
<span data-ttu-id="9a84b-143">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="9a84b-143">The output schema name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="9a84b-144">-OutputTableName</span></span>
<span data-ttu-id="9a84b-145">Имя выходной таблицы</span><span class="sxs-lookup"><span data-stu-id="9a84b-145">The output table name</span></span>

```yaml
Type: System.String
Parameter Sets: WithOutputDb, WithOutputDbId, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a84b-146">-ParentObject</span></span>
<span data-ttu-id="9a84b-147">Объект "задание"</span><span class="sxs-lookup"><span data-stu-id="9a84b-147">The job object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a84b-148">-ParentResourceId</span></span>
<span data-ttu-id="9a84b-149">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="9a84b-149">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, WithOutputDbUsingParentResourceId, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a84b-150">-ResourceGroupName</span></span>
<span data-ttu-id="9a84b-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9a84b-151">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="9a84b-152">-RetryAttempts</span></span>
<span data-ttu-id="9a84b-153">Повторные попытки</span><span class="sxs-lookup"><span data-stu-id="9a84b-153">The retry attempts</span></span>

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

### <span data-ttu-id="9a84b-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="9a84b-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="9a84b-155">Множитель интервала повтора</span><span class="sxs-lookup"><span data-stu-id="9a84b-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="9a84b-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="9a84b-156">-ServerName</span></span>
<span data-ttu-id="9a84b-157">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="9a84b-157">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="9a84b-158">-StepId</span></span>
<span data-ttu-id="9a84b-159">Идентификатор шага</span><span class="sxs-lookup"><span data-stu-id="9a84b-159">The step id</span></span>

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

### <span data-ttu-id="9a84b-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="9a84b-160">-TargetGroupName</span></span>
<span data-ttu-id="9a84b-161">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="9a84b-161">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, WithOutputDb, WithOutputDbId, ObjectSet, WithOutputDbUsingParentObject, WithOutputDbIdUsingParentObject, ResourceIdSet, WithOutputDbIdUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WithOutputDbUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a84b-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="9a84b-162">-TimeoutSeconds</span></span>
<span data-ttu-id="9a84b-163">Время ожидания в секундах</span><span class="sxs-lookup"><span data-stu-id="9a84b-163">The time out seconds</span></span>

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

### <span data-ttu-id="9a84b-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a84b-164">-Confirm</span></span>
<span data-ttu-id="9a84b-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9a84b-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a84b-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a84b-166">-WhatIf</span></span>
<span data-ttu-id="9a84b-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9a84b-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a84b-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9a84b-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a84b-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a84b-169">CommonParameters</span></span>
<span data-ttu-id="9a84b-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9a84b-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a84b-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a84b-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a84b-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9a84b-172">INPUTS</span></span>

### <span data-ttu-id="9a84b-173">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="9a84b-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="9a84b-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9a84b-174">OUTPUTS</span></span>

### <span data-ttu-id="9a84b-175">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="9a84b-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="9a84b-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="9a84b-176">NOTES</span></span>

## <span data-ttu-id="9a84b-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9a84b-177">RELATED LINKS</span></span>
