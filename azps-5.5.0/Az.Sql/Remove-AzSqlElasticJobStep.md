---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobStep.md
ms.openlocfilehash: b097c95f45700afabd3317a1014641da061d410d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210892"
---
# <span data-ttu-id="c8c1c-101">Remove-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="c8c1c-101">Remove-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="c8c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c1c-103">Удаление шага задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-103">Removes the job step</span></span>

## <span data-ttu-id="c8c1c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c8c1c-104">SYNTAX</span></span>

### <span data-ttu-id="c8c1c-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c8c1c-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c1c-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="c8c1c-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobStep [-InputObject] <AzureSqlElasticJobStepModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8c1c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c8c1c-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobStep [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c1c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8c1c-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c1c-109">Новый Remove-AzSqlElasticJobStep удаляет из задания шаг задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-109">The Remove-AzSqlElasticJobStep cmdlet removes a job step from a job</span></span>

## <span data-ttu-id="c8c1c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c8c1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c1c-111">Пример 1. Удаление шага задания из задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-111">Example 1: Removes a job step from a job</span></span>
```powershell
PS C:\> $jobStep = Get-AzSqlElasticJobStep -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -JobName job1 -Name step1
$jobStep | Remove-AzSqlElasticJobStep

JobName StepName StepId TargetGroupName CredentialName Output CommandText
------- -------- ------ --------------- -------------- ------ -----------
job1    step1    1      tg1             cred1                 SELECT 1
```

<span data-ttu-id="c8c1c-112">Удаление шага задания из задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-112">Removes a job step from a job</span></span>

### <span data-ttu-id="c8c1c-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c8c1c-113">Example 2</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Remove-AzSqlElasticJobStep -AgentName agent -JobName job1 -Name step1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="c8c1c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c8c1c-114">PARAMETERS</span></span>

### <span data-ttu-id="c8c1c-115">-AgentName</span><span class="sxs-lookup"><span data-stu-id="c8c1c-115">-AgentName</span></span>
<span data-ttu-id="c8c1c-116">Имя агента</span><span class="sxs-lookup"><span data-stu-id="c8c1c-116">The agent name</span></span>

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

### <span data-ttu-id="c8c1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c1c-117">-DefaultProfile</span></span>
<span data-ttu-id="c8c1c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c1c-119">-InputObject</span></span>
<span data-ttu-id="c8c1c-120">Объект ввода шага задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-120">The job step input object</span></span>

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

### <span data-ttu-id="c8c1c-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="c8c1c-121">-JobName</span></span>
<span data-ttu-id="c8c1c-122">Имя задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-122">The job name</span></span>

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

### <span data-ttu-id="c8c1c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c8c1c-123">-Name</span></span>
<span data-ttu-id="c8c1c-124">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-124">The job step name</span></span>

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

### <span data-ttu-id="c8c1c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c1c-125">-ResourceGroupName</span></span>
<span data-ttu-id="c8c1c-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c8c1c-126">The resource group name</span></span>

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

### <span data-ttu-id="c8c1c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c1c-127">-ResourceId</span></span>
<span data-ttu-id="c8c1c-128">ИД ресурса шага задания</span><span class="sxs-lookup"><span data-stu-id="c8c1c-128">The job step resource id</span></span>

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

### <span data-ttu-id="c8c1c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c8c1c-129">-ServerName</span></span>
<span data-ttu-id="c8c1c-130">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="c8c1c-130">The server name</span></span>

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

### <span data-ttu-id="c8c1c-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c8c1c-131">-Confirm</span></span>
<span data-ttu-id="c8c1c-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c8c1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c1c-133">-WhatIf</span></span>
<span data-ttu-id="c8c1c-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c1c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8c1c-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c8c1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c1c-136">CommonParameters</span></span>
<span data-ttu-id="c8c1c-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c1c-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8c1c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c1c-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c8c1c-139">INPUTS</span></span>

### <span data-ttu-id="c8c1c-140">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="c8c1c-140">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c8c1c-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c8c1c-141">OUTPUTS</span></span>

### <span data-ttu-id="c8c1c-142">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="c8c1c-142">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="c8c1c-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c8c1c-143">NOTES</span></span>

## <span data-ttu-id="c8c1c-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8c1c-144">RELATED LINKS</span></span>
