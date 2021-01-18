---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505914"
---
# <span data-ttu-id="b9f28-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="b9f28-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="b9f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9f28-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f28-103">Создание целевой группы</span><span class="sxs-lookup"><span data-stu-id="b9f28-103">Creates a new target group</span></span>

## <span data-ttu-id="b9f28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9f28-104">SYNTAX</span></span>

### <span data-ttu-id="b9f28-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9f28-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9f28-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="b9f28-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9f28-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b9f28-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9f28-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9f28-108">DESCRIPTION</span></span>
<span data-ttu-id="b9f28-109">С New-AzSqlElasticJobTargetGroup создается новая целевая группа.</span><span class="sxs-lookup"><span data-stu-id="b9f28-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="b9f28-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9f28-110">EXAMPLES</span></span>

### <span data-ttu-id="b9f28-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b9f28-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="b9f28-112">Создает пустую целевую группу.</span><span class="sxs-lookup"><span data-stu-id="b9f28-112">Creates an empty target group</span></span>

## <span data-ttu-id="b9f28-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9f28-113">PARAMETERS</span></span>

### <span data-ttu-id="b9f28-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b9f28-114">-AgentName</span></span>
<span data-ttu-id="b9f28-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="b9f28-115">The agent name</span></span>

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

### <span data-ttu-id="b9f28-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f28-116">-DefaultProfile</span></span>
<span data-ttu-id="b9f28-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9f28-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f28-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b9f28-118">-Name</span></span>
<span data-ttu-id="b9f28-119">Название целевой группы</span><span class="sxs-lookup"><span data-stu-id="b9f28-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9f28-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b9f28-120">-ParentObject</span></span>
<span data-ttu-id="b9f28-121">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="b9f28-121">The agent input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9f28-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b9f28-122">-ParentResourceId</span></span>
<span data-ttu-id="b9f28-123">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="b9f28-123">The agent resource id</span></span>

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

### <span data-ttu-id="b9f28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f28-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9f28-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b9f28-125">The resource group name</span></span>

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

### <span data-ttu-id="b9f28-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9f28-126">-ServerName</span></span>
<span data-ttu-id="b9f28-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="b9f28-127">The server name</span></span>

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

### <span data-ttu-id="b9f28-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9f28-128">-Confirm</span></span>
<span data-ttu-id="b9f28-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b9f28-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9f28-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f28-130">-WhatIf</span></span>
<span data-ttu-id="b9f28-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9f28-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f28-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b9f28-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9f28-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f28-133">CommonParameters</span></span>
<span data-ttu-id="b9f28-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9f28-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f28-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9f28-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f28-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9f28-136">INPUTS</span></span>

### <span data-ttu-id="b9f28-137">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="b9f28-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="b9f28-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9f28-138">OUTPUTS</span></span>

### <span data-ttu-id="b9f28-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="b9f28-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="b9f28-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9f28-140">NOTES</span></span>

## <span data-ttu-id="b9f28-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9f28-141">RELATED LINKS</span></span>
