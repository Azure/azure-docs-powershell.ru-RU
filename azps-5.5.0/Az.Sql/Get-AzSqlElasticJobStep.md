---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobStep.md
ms.openlocfilehash: 3a749f02854a915792a12271b2cf59b1091fef70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232641"
---
# <span data-ttu-id="d5a3c-101">Get-AzSqlElasticJobStep</span><span class="sxs-lookup"><span data-stu-id="d5a3c-101">Get-AzSqlElasticJobStep</span></span>

## <span data-ttu-id="d5a3c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5a3c-102">SYNOPSIS</span></span>
<span data-ttu-id="d5a3c-103">Одно или несколько действий с заданием</span><span class="sxs-lookup"><span data-stu-id="d5a3c-103">Gets one or more job steps</span></span>

## <span data-ttu-id="d5a3c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5a3c-104">SYNTAX</span></span>

### <span data-ttu-id="d5a3c-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5a3c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a3c-106">GetVersion</span><span class="sxs-lookup"><span data-stu-id="d5a3c-106">GetVersion</span></span>
```
Get-AzSqlElasticJobStep [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-JobName] <String> -Name <String> -Version <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d5a3c-107">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5a3c-107">ObjectSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a3c-108">GetVersionUsingJobObject</span><span class="sxs-lookup"><span data-stu-id="d5a3c-108">GetVersionUsingJobObject</span></span>
```
Get-AzSqlElasticJobStep [-ParentObject] <AzureSqlElasticJobModel> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a3c-109">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5a3c-109">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5a3c-110">GetVersionUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a3c-110">GetVersionUsingParentResourceId</span></span>
```
Get-AzSqlElasticJobStep [-ParentResourceId] <String> -Name <String> -Version <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5a3c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5a3c-111">DESCRIPTION</span></span>
<span data-ttu-id="d5a3c-112">Новый Get-AzSqlElasticJobStep получает одно или несколько действий с заданием</span><span class="sxs-lookup"><span data-stu-id="d5a3c-112">The Get-AzSqlElasticJobStep cmdlet gets one or more job steps from a job</span></span>

## <span data-ttu-id="d5a3c-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5a3c-113">EXAMPLES</span></span>

### <span data-ttu-id="d5a3c-114">Пример 1. Получает задание с задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-114">Example 1: Gets a job step from a job</span></span>
```powershell
PS C:\> $job = Get-AzSqlElasticJob -ResourceGroupName rg -ServerName elasticjobserver -AgentName agent -Name job1
$job | Get-AzSqlElasticJobStep -Name step1

JobName StepName StepId TargetGroupName CredentialName Output ExecutionOptions   CommandText
------- -------- ------ --------------- -------------- ------ ----------------   -----------
job1    step1    1      tg1             cred1                 (43200,10,1,120,2) SELECT 1
```

<span data-ttu-id="d5a3c-115">Получает задание с задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-115">Gets a job step from a job</span></span>

## <span data-ttu-id="d5a3c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5a3c-116">PARAMETERS</span></span>

### <span data-ttu-id="d5a3c-117">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d5a3c-117">-AgentName</span></span>
<span data-ttu-id="d5a3c-118">Имя агента</span><span class="sxs-lookup"><span data-stu-id="d5a3c-118">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5a3c-119">-DefaultProfile</span></span>
<span data-ttu-id="d5a3c-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5a3c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5a3c-121">-JobName</span><span class="sxs-lookup"><span data-stu-id="d5a3c-121">-JobName</span></span>
<span data-ttu-id="d5a3c-122">Имя задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-122">The job name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d5a3c-123">-Name</span></span>
<span data-ttu-id="d5a3c-124">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-124">The job step name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, ObjectSet, ResourceIdSet
Aliases: StepName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetVersion, GetVersionUsingJobObject, GetVersionUsingParentResourceId
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d5a3c-125">-ParentObject</span></span>
<span data-ttu-id="d5a3c-126">Объект ввода задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-126">The job input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel
Parameter Sets: ObjectSet, GetVersionUsingJobObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d5a3c-127">-ParentResourceId</span></span>
<span data-ttu-id="d5a3c-128">ИД ресурса задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-128">The job resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet, GetVersionUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5a3c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d5a3c-130">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="d5a3c-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5a3c-131">-ServerName</span></span>
<span data-ttu-id="d5a3c-132">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="d5a3c-132">The server name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet, GetVersion
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-133">-Version</span><span class="sxs-lookup"><span data-stu-id="d5a3c-133">-Version</span></span>
<span data-ttu-id="d5a3c-134">Имя шага задания</span><span class="sxs-lookup"><span data-stu-id="d5a3c-134">The job step name</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingJobObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetVersionUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5a3c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5a3c-135">CommonParameters</span></span>
<span data-ttu-id="d5a3c-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5a3c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5a3c-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5a3c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5a3c-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a3c-138">INPUTS</span></span>

### <span data-ttu-id="d5a3c-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobModel</span><span class="sxs-lookup"><span data-stu-id="d5a3c-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobModel</span></span>

## <span data-ttu-id="d5a3c-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5a3c-140">OUTPUTS</span></span>

### <span data-ttu-id="d5a3c-141">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobStepModel</span><span class="sxs-lookup"><span data-stu-id="d5a3c-141">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobStepModel</span></span>

## <span data-ttu-id="d5a3c-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5a3c-142">NOTES</span></span>

## <span data-ttu-id="d5a3c-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5a3c-143">RELATED LINKS</span></span>
