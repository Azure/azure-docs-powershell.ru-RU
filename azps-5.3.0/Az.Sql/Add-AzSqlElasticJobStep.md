---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: dbc27ec87be3de4c320ad60b7dc204d704fe8f2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419692"
---
# <span data-ttu-id="afd34-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="afd34-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="afd34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd34-102">SYNOPSIS</span></span>
<span data-ttu-id="afd34-103">Добавляет задание в задание</span><span class="sxs-lookup"><span data-stu-id="afd34-103">Adds a job step to a job</span></span>

## <span data-ttu-id="afd34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afd34-104">SYNTAX</span></span>

### <span data-ttu-id="afd34-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="afd34-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd34-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="afd34-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd34-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="afd34-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd34-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="afd34-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd34-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="afd34-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd34-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="afd34-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd34-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="afd34-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afd34-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="afd34-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afd34-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="afd34-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd34-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afd34-114">DESCRIPTION</span></span>
<span data-ttu-id="afd34-115">Новый Add-AzSqlElasticJobStep добавляет задание в задание с его Add-AzSqlElasticJobStep.</span><span class="sxs-lookup"><span data-stu-id="afd34-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="afd34-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afd34-116">EXAMPLES</span></span>

### <span data-ttu-id="afd34-117">Пример 1. Добавляет шаг в задание</span><span class="sxs-lookup"><span data-stu-id="afd34-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="afd34-118">Добавляет задание в задание</span><span class="sxs-lookup"><span data-stu-id="afd34-118">Adds a job step to a job</span></span>

## <span data-ttu-id="afd34-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afd34-119">PARAMETERS</span></span>

### <span data-ttu-id="afd34-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="afd34-120">-AgentName</span></span>
<span data-ttu-id="afd34-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="afd34-121">The agent name</span></span>

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

### <span data-ttu-id="afd34-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="afd34-122">-CommandText</span></span>
<span data-ttu-id="afd34-123">Текст команды</span><span class="sxs-lookup"><span data-stu-id="afd34-123">The command text</span></span>

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

### <span data-ttu-id="afd34-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="afd34-124">-CredentialName</span></span>
<span data-ttu-id="afd34-125">Имя учетной данные</span><span class="sxs-lookup"><span data-stu-id="afd34-125">The credential name</span></span>

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

### <span data-ttu-id="afd34-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd34-126">-DefaultProfile</span></span>
<span data-ttu-id="afd34-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afd34-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd34-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="afd34-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="afd34-129">Начальная retry interval seconds</span><span class="sxs-lookup"><span data-stu-id="afd34-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="afd34-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="afd34-130">-JobName</span></span>
<span data-ttu-id="afd34-131">Имя задания</span><span class="sxs-lookup"><span data-stu-id="afd34-131">The job name</span></span>

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

### <span data-ttu-id="afd34-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="afd34-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="afd34-133">Максимальное время повторного интервала</span><span class="sxs-lookup"><span data-stu-id="afd34-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="afd34-134">-Name</span><span class="sxs-lookup"><span data-stu-id="afd34-134">-Name</span></span>
<span data-ttu-id="afd34-135">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="afd34-135">The job step name</span></span>

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

### <span data-ttu-id="afd34-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="afd34-136">-OutputCredentialName</span></span>
<span data-ttu-id="afd34-137">Имя выходных учетных данных</span><span class="sxs-lookup"><span data-stu-id="afd34-137">The output credential name</span></span>

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

### <span data-ttu-id="afd34-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="afd34-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="afd34-139">Выходной объект базы данных</span><span class="sxs-lookup"><span data-stu-id="afd34-139">The output database object</span></span>

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

### <span data-ttu-id="afd34-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="afd34-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="afd34-141">ИД ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="afd34-141">The output database resource id</span></span>

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

### <span data-ttu-id="afd34-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="afd34-142">-OutputSchemaName</span></span>
<span data-ttu-id="afd34-143">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="afd34-143">The output schema name</span></span>

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

### <span data-ttu-id="afd34-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="afd34-144">-OutputTableName</span></span>
<span data-ttu-id="afd34-145">Имя выводной таблицы</span><span class="sxs-lookup"><span data-stu-id="afd34-145">The output table name</span></span>

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

### <span data-ttu-id="afd34-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="afd34-146">-ParentObject</span></span>
<span data-ttu-id="afd34-147">Объект задания</span><span class="sxs-lookup"><span data-stu-id="afd34-147">The job object</span></span>

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

### <span data-ttu-id="afd34-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="afd34-148">-ParentResourceId</span></span>
<span data-ttu-id="afd34-149">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="afd34-149">The job resource id</span></span>

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

### <span data-ttu-id="afd34-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd34-150">-ResourceGroupName</span></span>
<span data-ttu-id="afd34-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="afd34-151">The resource group name</span></span>

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

### <span data-ttu-id="afd34-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="afd34-152">-RetryAttempts</span></span>
<span data-ttu-id="afd34-153">Повторить попытку</span><span class="sxs-lookup"><span data-stu-id="afd34-153">The retry attempts</span></span>

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

### <span data-ttu-id="afd34-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="afd34-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="afd34-155">Множитель, отс множитель, возвращаясь назад</span><span class="sxs-lookup"><span data-stu-id="afd34-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="afd34-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="afd34-156">-ServerName</span></span>
<span data-ttu-id="afd34-157">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="afd34-157">The server name</span></span>

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

### <span data-ttu-id="afd34-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="afd34-158">-StepId</span></span>
<span data-ttu-id="afd34-159">Пошаговая пошаговая пошагов</span><span class="sxs-lookup"><span data-stu-id="afd34-159">The step id</span></span>

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

### <span data-ttu-id="afd34-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="afd34-160">-TargetGroupName</span></span>
<span data-ttu-id="afd34-161">Название целевой группы</span><span class="sxs-lookup"><span data-stu-id="afd34-161">The target group name</span></span>

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

### <span data-ttu-id="afd34-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="afd34-162">-TimeoutSeconds</span></span>
<span data-ttu-id="afd34-163">Время от времени отсек</span><span class="sxs-lookup"><span data-stu-id="afd34-163">The time out seconds</span></span>

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

### <span data-ttu-id="afd34-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afd34-164">-Confirm</span></span>
<span data-ttu-id="afd34-165">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd34-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd34-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd34-166">-WhatIf</span></span>
<span data-ttu-id="afd34-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd34-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd34-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="afd34-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd34-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd34-169">CommonParameters</span></span>
<span data-ttu-id="afd34-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd34-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd34-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afd34-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd34-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afd34-172">INPUTS</span></span>

### <span data-ttu-id="afd34-173">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="afd34-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="afd34-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afd34-174">OUTPUTS</span></span>

### <span data-ttu-id="afd34-175">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="afd34-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="afd34-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afd34-176">NOTES</span></span>

## <span data-ttu-id="afd34-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afd34-177">RELATED LINKS</span></span>
