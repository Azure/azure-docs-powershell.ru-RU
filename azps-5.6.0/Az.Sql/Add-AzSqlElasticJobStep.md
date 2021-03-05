---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/add-azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobStep.md
ms.openlocfilehash: 41314cb2a65912e2973e91b27036fc099d2cbca6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961539"
---
# <span data-ttu-id="b4e38-101">Add-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="b4e38-101">Add-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="b4e38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4e38-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e38-103">Добавляет задание в задание</span><span class="sxs-lookup"><span data-stu-id="b4e38-103">Adds a job step to a job</span></span>

## <span data-ttu-id="b4e38-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4e38-104">SYNTAX</span></span>

### <span data-ttu-id="b4e38-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b4e38-105">DefaultSet (Default)</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String> -Name <String>
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e38-106">WithOutputDb</span><span class="sxs-lookup"><span data-stu-id="b4e38-106">WithOutputDb</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String> -OutputTableName <String>
 -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e38-107">WithOutputDbId</span><span class="sxs-lookup"><span data-stu-id="b4e38-107">WithOutputDbId</span></span>
```
Add-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -TargetGroupName <String> -CredentialName <String> -CommandText <String>
 -OutputDatabaseResourceId <String> -OutputCredentialName <String> -OutputTableName <String> -Name <String>
 [-OutputSchemaName <String>] [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e38-108">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b4e38-108">ObjectSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>]
 [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e38-109">WithOutputDbUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b4e38-109">WithOutputDbUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e38-110">WithOutputDbIdUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b4e38-110">WithOutputDbIdUsingParentObject</span></span>
```
Add-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -TargetGroupName <String>
 -CredentialName <String> -CommandText <String> -OutputDatabaseResourceId <String>
 -OutputCredentialName <String> -OutputTableName <String> -Name <String> [-OutputSchemaName <String>]
 [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e38-111">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b4e38-111">ResourceIdSet</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -Name <String> [-StepId <Int32>] [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>]
 [-InitialRetryIntervalSeconds <Int32>] [-MaximumRetryIntervalSeconds <Int32>]
 [-RetryIntervalBackoffMultiplier <Double>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e38-112">WithOutputDbUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e38-112">WithOutputDbUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseObject <AzureSqlDatabaseModel> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4e38-113">WithOutputDbIdUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e38-113">WithOutputDbIdUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobStep [-ParentResourceId] <String> -TargetGroupName <String> -CredentialName <String>
 -CommandText <String> -OutputDatabaseResourceId <String> -OutputCredentialName <String>
 -OutputTableName <String> -Name <String> [-OutputSchemaName <String>] [-StepId <Int32>]
 [-TimeoutSeconds <Int32>] [-RetryAttempts <Int32>] [-InitialRetryIntervalSeconds <Int32>]
 [-MaximumRetryIntervalSeconds <Int32>] [-RetryIntervalBackoffMultiplier <Double>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4e38-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4e38-114">DESCRIPTION</span></span>
<span data-ttu-id="b4e38-115">Новый Add-AzSqlElasticJobStep добавляет шаг задания в задание</span><span class="sxs-lookup"><span data-stu-id="b4e38-115">The Add-AzSqlElasticJobStep cmdlet adds a job step to a job</span></span>

## <span data-ttu-id="b4e38-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4e38-116">EXAMPLES</span></span>

### <span data-ttu-id="b4e38-117">Пример 1. Добавляет шаг в задание</span><span class="sxs-lookup"><span data-stu-id="b4e38-117">Example 1: Adds a step to a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -Name job1
$job | Add-AzSqlElasticJobStep -Name step1 -TargetGroupName tg1 -CredentialName cred1 -CommandText "SELECT 1"

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="b4e38-118">Добавляет задание в задание</span><span class="sxs-lookup"><span data-stu-id="b4e38-118">Adds a job step to a job</span></span>

## <span data-ttu-id="b4e38-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4e38-119">PARAMETERS</span></span>

### <span data-ttu-id="b4e38-120">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b4e38-120">-AgentName</span></span>
<span data-ttu-id="b4e38-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="b4e38-121">The agent name</span></span>

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

### <span data-ttu-id="b4e38-122">-CommandText</span><span class="sxs-lookup"><span data-stu-id="b4e38-122">-CommandText</span></span>
<span data-ttu-id="b4e38-123">Текст команды</span><span class="sxs-lookup"><span data-stu-id="b4e38-123">The command text</span></span>

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

### <span data-ttu-id="b4e38-124">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="b4e38-124">-CredentialName</span></span>
<span data-ttu-id="b4e38-125">Имя учетной данные</span><span class="sxs-lookup"><span data-stu-id="b4e38-125">The credential name</span></span>

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

### <span data-ttu-id="b4e38-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e38-126">-DefaultProfile</span></span>
<span data-ttu-id="b4e38-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e38-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4e38-128">-InitialRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b4e38-128">-InitialRetryIntervalSeconds</span></span>
<span data-ttu-id="b4e38-129">Начальная retry interval seconds</span><span class="sxs-lookup"><span data-stu-id="b4e38-129">The initial retry interval seconds</span></span>

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

### <span data-ttu-id="b4e38-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="b4e38-130">-JobName</span></span>
<span data-ttu-id="b4e38-131">Имя задания</span><span class="sxs-lookup"><span data-stu-id="b4e38-131">The job name</span></span>

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

### <span data-ttu-id="b4e38-132">-MaximumRetryIntervalSeconds</span><span class="sxs-lookup"><span data-stu-id="b4e38-132">-MaximumRetryIntervalSeconds</span></span>
<span data-ttu-id="b4e38-133">Максимальное время повторного интервала</span><span class="sxs-lookup"><span data-stu-id="b4e38-133">The maximum retry interval seconds</span></span>

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

### <span data-ttu-id="b4e38-134">-Name</span><span class="sxs-lookup"><span data-stu-id="b4e38-134">-Name</span></span>
<span data-ttu-id="b4e38-135">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="b4e38-135">The job step name</span></span>

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

### <span data-ttu-id="b4e38-136">-OutputCredentialName</span><span class="sxs-lookup"><span data-stu-id="b4e38-136">-OutputCredentialName</span></span>
<span data-ttu-id="b4e38-137">Имя выходных учетных данных</span><span class="sxs-lookup"><span data-stu-id="b4e38-137">The output credential name</span></span>

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

### <span data-ttu-id="b4e38-138">-OutputDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="b4e38-138">-OutputDatabaseObject</span></span>
<span data-ttu-id="b4e38-139">Выходной объект базы данных</span><span class="sxs-lookup"><span data-stu-id="b4e38-139">The output database object</span></span>

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

### <span data-ttu-id="b4e38-140">-OutputDatabaseResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e38-140">-OutputDatabaseResourceId</span></span>
<span data-ttu-id="b4e38-141">ИД ресурса выходной базы данных</span><span class="sxs-lookup"><span data-stu-id="b4e38-141">The output database resource id</span></span>

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

### <span data-ttu-id="b4e38-142">-OutputSchemaName</span><span class="sxs-lookup"><span data-stu-id="b4e38-142">-OutputSchemaName</span></span>
<span data-ttu-id="b4e38-143">Имя схемы вывода</span><span class="sxs-lookup"><span data-stu-id="b4e38-143">The output schema name</span></span>

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

### <span data-ttu-id="b4e38-144">-OutputTableName</span><span class="sxs-lookup"><span data-stu-id="b4e38-144">-OutputTableName</span></span>
<span data-ttu-id="b4e38-145">Имя выводной таблицы</span><span class="sxs-lookup"><span data-stu-id="b4e38-145">The output table name</span></span>

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

### <span data-ttu-id="b4e38-146">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b4e38-146">-ParentObject</span></span>
<span data-ttu-id="b4e38-147">Объект задания</span><span class="sxs-lookup"><span data-stu-id="b4e38-147">The job object</span></span>

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

### <span data-ttu-id="b4e38-148">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b4e38-148">-ParentResourceId</span></span>
<span data-ttu-id="b4e38-149">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="b4e38-149">The job resource id</span></span>

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

### <span data-ttu-id="b4e38-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e38-150">-ResourceGroupName</span></span>
<span data-ttu-id="b4e38-151">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b4e38-151">The resource group name</span></span>

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

### <span data-ttu-id="b4e38-152">-RetryAttempts</span><span class="sxs-lookup"><span data-stu-id="b4e38-152">-RetryAttempts</span></span>
<span data-ttu-id="b4e38-153">Повторить попытку</span><span class="sxs-lookup"><span data-stu-id="b4e38-153">The retry attempts</span></span>

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

### <span data-ttu-id="b4e38-154">-RetryIntervalBackoffMultiplier</span><span class="sxs-lookup"><span data-stu-id="b4e38-154">-RetryIntervalBackoffMultiplier</span></span>
<span data-ttu-id="b4e38-155">Множитель, отс множитель, возвращаясь назад</span><span class="sxs-lookup"><span data-stu-id="b4e38-155">The retry interval back off multiplier</span></span>

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

### <span data-ttu-id="b4e38-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b4e38-156">-ServerName</span></span>
<span data-ttu-id="b4e38-157">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="b4e38-157">The server name</span></span>

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

### <span data-ttu-id="b4e38-158">-StepId</span><span class="sxs-lookup"><span data-stu-id="b4e38-158">-StepId</span></span>
<span data-ttu-id="b4e38-159">Пошаговая пошаговая пошагов</span><span class="sxs-lookup"><span data-stu-id="b4e38-159">The step id</span></span>

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

### <span data-ttu-id="b4e38-160">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e38-160">-TargetGroupName</span></span>
<span data-ttu-id="b4e38-161">Название целевой группы</span><span class="sxs-lookup"><span data-stu-id="b4e38-161">The target group name</span></span>

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

### <span data-ttu-id="b4e38-162">-TimeoutSeconds</span><span class="sxs-lookup"><span data-stu-id="b4e38-162">-TimeoutSeconds</span></span>
<span data-ttu-id="b4e38-163">Время от времени отсек</span><span class="sxs-lookup"><span data-stu-id="b4e38-163">The time out seconds</span></span>

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

### <span data-ttu-id="b4e38-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b4e38-164">-Confirm</span></span>
<span data-ttu-id="b4e38-165">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b4e38-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4e38-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4e38-166">-WhatIf</span></span>
<span data-ttu-id="b4e38-167">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e38-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4e38-168">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b4e38-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4e38-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e38-169">CommonParameters</span></span>
<span data-ttu-id="b4e38-170">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e38-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e38-171">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4e38-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e38-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4e38-172">INPUTS</span></span>

### <span data-ttu-id="b4e38-173">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="b4e38-173">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="b4e38-174">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4e38-174">OUTPUTS</span></span>

### <span data-ttu-id="b4e38-175">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="b4e38-175">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="b4e38-176">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4e38-176">NOTES</span></span>

## <span data-ttu-id="b4e38-177">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4e38-177">RELATED LINKS</span></span>
