---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: c0ebc561a047ffe6a62722012fd7ecd3d42e472a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073188"
---
# <span data-ttu-id="4438a-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="4438a-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="4438a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4438a-102">SYNOPSIS</span></span>
<span data-ttu-id="4438a-103">Удаление шага задания</span><span class="sxs-lookup"><span data-stu-id="4438a-103">Removes the job step</span></span>

## <span data-ttu-id="4438a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4438a-104">SYNTAX</span></span>

### <span data-ttu-id="4438a-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4438a-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4438a-106">Объект</span><span class="sxs-lookup"><span data-stu-id="4438a-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4438a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4438a-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4438a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4438a-108">DESCRIPTION</span></span>
<span data-ttu-id="4438a-109">Командлет Remove-AzSqlElasticJobStep удаляет шаг задания из задания</span><span class="sxs-lookup"><span data-stu-id="4438a-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="4438a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4438a-110">EXAMPLES</span></span>

### <span data-ttu-id="4438a-111">Пример 1: удаление шага задания из задания</span><span class="sxs-lookup"><span data-stu-id="4438a-111">Example 1 - Removes a job step from a job</span></span>
```
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="4438a-112">Удаление шага задания из задания</span><span class="sxs-lookup"><span data-stu-id="4438a-112">Removes a job step from a job</span></span>

## <span data-ttu-id="4438a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4438a-113">PARAMETERS</span></span>

### <span data-ttu-id="4438a-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4438a-114">-AgentName</span></span>
<span data-ttu-id="4438a-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="4438a-115">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4438a-116">-DefaultProfile</span></span>
<span data-ttu-id="4438a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4438a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4438a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4438a-118">-InputObject</span></span>
<span data-ttu-id="4438a-119">Входной объект шага задания</span><span class="sxs-lookup"><span data-stu-id="4438a-119">The job step input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-120">-JobName</span><span class="sxs-lookup"><span data-stu-id="4438a-120">-JobName</span></span>
<span data-ttu-id="4438a-121">Имя задания</span><span class="sxs-lookup"><span data-stu-id="4438a-121">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4438a-122">-Name</span></span>
<span data-ttu-id="4438a-123">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="4438a-123">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4438a-124">-ResourceGroupName</span></span>
<span data-ttu-id="4438a-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4438a-125">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4438a-126">-ResourceId</span></span>
<span data-ttu-id="4438a-127">Идентификатор ресурса шага задания</span><span class="sxs-lookup"><span data-stu-id="4438a-127">The job step resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4438a-128">-ServerName</span></span>
<span data-ttu-id="4438a-129">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="4438a-129">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4438a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4438a-130">-Confirm</span></span>
<span data-ttu-id="4438a-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4438a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4438a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4438a-132">-WhatIf</span></span>
<span data-ttu-id="4438a-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4438a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4438a-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4438a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4438a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4438a-135">CommonParameters</span></span>
<span data-ttu-id="4438a-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4438a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4438a-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4438a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4438a-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4438a-138">INPUTS</span></span>

### <span data-ttu-id="4438a-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4438a-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4438a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4438a-140">OUTPUTS</span></span>

### <span data-ttu-id="4438a-141">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="4438a-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="4438a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4438a-142">NOTES</span></span>

## <span data-ttu-id="4438a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4438a-143">RELATED LINKS</span></span>
