---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080261"
---
# <span data-ttu-id="93077-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="93077-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="93077-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93077-102">SYNOPSIS</span></span>
<span data-ttu-id="93077-103">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="93077-103">Adds a job step to a job</span></span>

## <span data-ttu-id="93077-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93077-104">SYNTAX</span></span>

### <span data-ttu-id="93077-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93077-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93077-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="93077-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93077-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="93077-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93077-108">Объект</span><span class="sxs-lookup"><span data-stu-id="93077-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93077-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="93077-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93077-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="93077-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93077-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="93077-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="93077-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="93077-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93077-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="93077-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93077-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93077-114">DESCRIPTION</span></span>
<span data-ttu-id="93077-115">Командлет Add-AzSqlElasticJobStep добавляет шаг задания в задание.</span><span class="sxs-lookup"><span data-stu-id="93077-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="93077-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93077-116">EXAMPLES</span></span>

### <span data-ttu-id="93077-117">Пример 1: Добавление шага к заданию</span><span class="sxs-lookup"><span data-stu-id="93077-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="93077-118">Добавляет шаг задания к заданию</span><span class="sxs-lookup"><span data-stu-id="93077-118">Adds a job step to a job</span></span>

## <span data-ttu-id="93077-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93077-119">PARAMETERS</span></span>

### <span data-ttu-id="93077-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="93077-120">-AgentName</span></span>
<span data-ttu-id="93077-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="93077-121">The agent name</span></span>

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

### <span data-ttu-id="93077-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="93077-122">-CommandText</span></span>
<span data-ttu-id="93077-123">Текст команды</span><span class="sxs-lookup"><span data-stu-id="93077-123">The command text</span></span>

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

### <span data-ttu-id="93077-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="93077-124">-CredentialName</span></span>
<span data-ttu-id="93077-125">Имя учетных данных</span><span class="sxs-lookup"><span data-stu-id="93077-125">The credential name</span></span>

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

### <span data-ttu-id="93077-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93077-126">-DefaultProfile</span></span>
<span data-ttu-id="93077-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93077-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93077-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="93077-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="93077-129">Начальная интервал повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="93077-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="93077-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="93077-130">-JobName</span></span>
<span data-ttu-id="93077-131">Имя задания</span><span class="sxs-lookup"><span data-stu-id="93077-131">The job name</span></span>

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

### <span data-ttu-id="93077-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="93077-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="93077-133">Максимальное значение интервала повтора (в секундах)</span><span class="sxs-lookup"><span data-stu-id="93077-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="93077-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93077-134">-Name</span></span>
<span data-ttu-id="93077-135">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="93077-135">The job step name</span></span>

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

### <span data-ttu-id="93077-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="93077-136">-OutputCredentialName</span></span>
<span data-ttu-id="93077-137">Имя учетных данных выхода</span><span class="sxs-lookup"><span data-stu-id="93077-137">The output credential name</span></span>

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

### <span data-ttu-id="93077-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="93077-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="93077-139">Объект выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="93077-139">The output database object</span></span>

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

### <span data-ttu-id="93077-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="93077-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="93077-141">Идентификатор ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="93077-141">The output database resource id</span></span>

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

### <span data-ttu-id="93077-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="93077-142">-OutputSchemaName</span></span>
<span data-ttu-id="93077-143">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="93077-143">The output schema name</span></span>

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

### <span data-ttu-id="93077-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="93077-144">-OutputTableName</span></span>
<span data-ttu-id="93077-145">Имя выходной таблицы</span><span class="sxs-lookup"><span data-stu-id="93077-145">The output table name</span></span>

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

### <span data-ttu-id="93077-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="93077-146">-ParentObject</span></span>
<span data-ttu-id="93077-147">Объект "задание"</span><span class="sxs-lookup"><span data-stu-id="93077-147">The job object</span></span>

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

### <span data-ttu-id="93077-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="93077-148">-ParentResourceId</span></span>
<span data-ttu-id="93077-149">Идентификатор ресурса задания</span><span class="sxs-lookup"><span data-stu-id="93077-149">The job resource id</span></span>

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

### <span data-ttu-id="93077-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93077-150">-ResourceGroupName</span></span>
<span data-ttu-id="93077-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93077-151">The resource group name</span></span>

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

### <span data-ttu-id="93077-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="93077-152">-RetryAttempts</span></span>
<span data-ttu-id="93077-153">Повторные попытки</span><span class="sxs-lookup"><span data-stu-id="93077-153">The retry attempts</span></span>

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

### <span data-ttu-id="93077-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="93077-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="93077-155">Множитель интервала повтора</span><span class="sxs-lookup"><span data-stu-id="93077-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="93077-156">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="93077-156">-ServerName</span></span>
<span data-ttu-id="93077-157">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="93077-157">The server name</span></span>

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

### <span data-ttu-id="93077-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="93077-158">-StepId</span></span>
<span data-ttu-id="93077-159">Идентификатор шага</span><span class="sxs-lookup"><span data-stu-id="93077-159">The step id</span></span>

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

### <span data-ttu-id="93077-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="93077-160">-TargetGroupName</span></span>
<span data-ttu-id="93077-161">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="93077-161">The target group name</span></span>

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

### <span data-ttu-id="93077-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="93077-162">-TimeoutSeconds</span></span>
<span data-ttu-id="93077-163">Время ожидания в секундах</span><span class="sxs-lookup"><span data-stu-id="93077-163">The time out seconds</span></span>

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

### <span data-ttu-id="93077-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93077-164">-Confirm</span></span>
<span data-ttu-id="93077-165">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93077-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93077-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93077-166">-WhatIf</span></span>
<span data-ttu-id="93077-167">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93077-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93077-168">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93077-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93077-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93077-169">CommonParameters</span></span>
<span data-ttu-id="93077-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93077-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93077-171">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93077-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93077-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93077-172">INPUTS</span></span>

### <span data-ttu-id="93077-173">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="93077-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="93077-174">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93077-174">OUTPUTS</span></span>

### <span data-ttu-id="93077-175">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="93077-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="93077-176">Пуск</span><span class="sxs-lookup"><span data-stu-id="93077-176">NOTES</span></span>

## <span data-ttu-id="93077-177">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93077-177">RELATED LINKS</span></span>