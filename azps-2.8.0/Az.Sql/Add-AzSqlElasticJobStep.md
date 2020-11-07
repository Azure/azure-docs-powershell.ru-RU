---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 79b26156ae99bfcdd94671649b403b495377af30
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93905242"
---
# <span data-ttu-id="f20ca-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="f20ca-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="f20ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f20ca-102">SYNOPSIS</span></span>
<span data-ttu-id="f20ca-103">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="f20ca-103">Adds a job step to a job</span></span>

## <span data-ttu-id="f20ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f20ca-104">SYNTAX</span></span>

### <span data-ttu-id="f20ca-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f20ca-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20ca-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="f20ca-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20ca-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="f20ca-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20ca-108">Объект</span><span class="sxs-lookup"><span data-stu-id="f20ca-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20ca-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f20ca-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20ca-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="f20ca-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20ca-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f20ca-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f20ca-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f20ca-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f20ca-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f20ca-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f20ca-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f20ca-114">DESCRIPTION</span></span>
<span data-ttu-id="f20ca-115">Командлет Add-AzSqlElasticJobStep добавляет шаг задания в задание.</span><span class="sxs-lookup"><span data-stu-id="f20ca-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="f20ca-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f20ca-116">EXAMPLES</span></span>

### <span data-ttu-id="f20ca-117">Пример 1: Добавление шага к заданию</span><span class="sxs-lookup"><span data-stu-id="f20ca-117">Example 1 - Adds a step to a job</span></span>
```
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="f20ca-118">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="f20ca-118">Adds a job step to a job</span></span>

## <span data-ttu-id="f20ca-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f20ca-119">PARAMETERS</span></span>

### <span data-ttu-id="f20ca-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="f20ca-120">-AgentName</span></span>
<span data-ttu-id="f20ca-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="f20ca-121">The agent name</span></span>

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

### <span data-ttu-id="f20ca-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="f20ca-122">-CommandText</span></span>
<span data-ttu-id="f20ca-123">Текст команды</span><span class="sxs-lookup"><span data-stu-id="f20ca-123">The command text</span></span>

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

### <span data-ttu-id="f20ca-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="f20ca-124">-CredentialName</span></span>
<span data-ttu-id="f20ca-125">Имя учетных данных</span><span class="sxs-lookup"><span data-stu-id="f20ca-125">The credential name</span></span>

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

### <span data-ttu-id="f20ca-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f20ca-126">-DefaultProfile</span></span>
<span data-ttu-id="f20ca-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f20ca-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f20ca-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f20ca-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="f20ca-129">Начальная интервал повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="f20ca-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="f20ca-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="f20ca-130">-JobName</span></span>
<span data-ttu-id="f20ca-131">Имя задания</span><span class="sxs-lookup"><span data-stu-id="f20ca-131">The job name</span></span>

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

### <span data-ttu-id="f20ca-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="f20ca-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="f20ca-133">Максимальное значение интервала повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="f20ca-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="f20ca-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f20ca-134">-Name</span></span>
<span data-ttu-id="f20ca-135">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="f20ca-135">The job step name</span></span>

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

### <span data-ttu-id="f20ca-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="f20ca-136">-OutputCredentialName</span></span>
<span data-ttu-id="f20ca-137">Имя учетных данных выхода</span><span class="sxs-lookup"><span data-stu-id="f20ca-137">The output credential name</span></span>

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

### <span data-ttu-id="f20ca-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f20ca-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="f20ca-139">Объект выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="f20ca-139">The output database object</span></span>

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

### <span data-ttu-id="f20ca-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="f20ca-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="f20ca-141">Идентификатор ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="f20ca-141">The output database resource id</span></span>

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

### <span data-ttu-id="f20ca-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="f20ca-142">-OutputSchemaName</span></span>
<span data-ttu-id="f20ca-143">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="f20ca-143">The output schema name</span></span>

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

### <span data-ttu-id="f20ca-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="f20ca-144">-OutputTableName</span></span>
<span data-ttu-id="f20ca-145">Имя выходной таблицы</span><span class="sxs-lookup"><span data-stu-id="f20ca-145">The output table name</span></span>

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

### <span data-ttu-id="f20ca-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f20ca-146">-ParentObject</span></span>
<span data-ttu-id="f20ca-147">Объект "задание"</span><span class="sxs-lookup"><span data-stu-id="f20ca-147">The job object</span></span>

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

### <span data-ttu-id="f20ca-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f20ca-148">-ParentResourceId</span></span>
<span data-ttu-id="f20ca-149">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="f20ca-149">The job resource id</span></span>

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

### <span data-ttu-id="f20ca-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f20ca-150">-ResourceGroupName</span></span>
<span data-ttu-id="f20ca-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f20ca-151">The resource group name</span></span>

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

### <span data-ttu-id="f20ca-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="f20ca-152">-RetryAttempts</span></span>
<span data-ttu-id="f20ca-153">Повторные попытки</span><span class="sxs-lookup"><span data-stu-id="f20ca-153">The retry attempts</span></span>

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

### <span data-ttu-id="f20ca-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="f20ca-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="f20ca-155">Множитель интервала повтора</span><span class="sxs-lookup"><span data-stu-id="f20ca-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="f20ca-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="f20ca-156">-ServerName</span></span>
<span data-ttu-id="f20ca-157">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="f20ca-157">The server name</span></span>

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

### <span data-ttu-id="f20ca-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="f20ca-158">-StepId</span></span>
<span data-ttu-id="f20ca-159">Идентификатор шага</span><span class="sxs-lookup"><span data-stu-id="f20ca-159">The step id</span></span>

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

### <span data-ttu-id="f20ca-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="f20ca-160">-TargetGroupName</span></span>
<span data-ttu-id="f20ca-161">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="f20ca-161">The target group name</span></span>

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

### <span data-ttu-id="f20ca-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="f20ca-162">-TimeoutSeconds</span></span>
<span data-ttu-id="f20ca-163">Время ожидания в секундах</span><span class="sxs-lookup"><span data-stu-id="f20ca-163">The time out seconds</span></span>

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

### <span data-ttu-id="f20ca-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f20ca-164">-Confirm</span></span>
<span data-ttu-id="f20ca-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f20ca-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f20ca-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f20ca-166">-WhatIf</span></span>
<span data-ttu-id="f20ca-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f20ca-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f20ca-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f20ca-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f20ca-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f20ca-169">CommonParameters</span></span>
<span data-ttu-id="f20ca-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f20ca-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f20ca-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f20ca-171">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f20ca-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f20ca-172">INPUTS</span></span>

### <span data-ttu-id="f20ca-173">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="f20ca-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="f20ca-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f20ca-174">OUTPUTS</span></span>

### <span data-ttu-id="f20ca-175">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="f20ca-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="f20ca-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="f20ca-176">NOTES</span></span>

## <span data-ttu-id="f20ca-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f20ca-177">RELATED LINKS</span></span>
