---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 5818bd11b3131ff340857e033053eb492a9178e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080239"
---
# <span data-ttu-id="00c62-101">New-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="00c62-101">New-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="00c62-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00c62-102">SYNOPSIS</span></span>
<span data-ttu-id="00c62-103">Создание новой конечной группы</span><span class="sxs-lookup"><span data-stu-id="00c62-103">Creates a new target group</span></span>

## <span data-ttu-id="00c62-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00c62-104">SYNTAX</span></span>

### <span data-ttu-id="00c62-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00c62-105">DefaultSet (Default)</span></span>
```
New-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00c62-106">Объект</span><span class="sxs-lookup"><span data-stu-id="00c62-106">ObjectSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00c62-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="00c62-107">ResourceIdSet</span></span>
```
New-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00c62-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00c62-108">DESCRIPTION</span></span>
<span data-ttu-id="00c62-109">Командлет New-AzSqlElasticJobTargetGroup создает новую конечную группу.</span><span class="sxs-lookup"><span data-stu-id="00c62-109">The New-AzSqlElasticJobTargetGroup cmdlet creates a new target group</span></span>

## <span data-ttu-id="00c62-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00c62-110">EXAMPLES</span></span>

### <span data-ttu-id="00c62-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="00c62-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | New-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1
```

<span data-ttu-id="00c62-112">Создает пустую целевую группу</span><span class="sxs-lookup"><span data-stu-id="00c62-112">Creates an empty target group</span></span>

## <span data-ttu-id="00c62-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00c62-113">PARAMETERS</span></span>

### <span data-ttu-id="00c62-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="00c62-114">-AgentName</span></span>
<span data-ttu-id="00c62-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="00c62-115">The agent name</span></span>

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

### <span data-ttu-id="00c62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00c62-116">-DefaultProfile</span></span>
<span data-ttu-id="00c62-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00c62-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00c62-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00c62-118">-Name</span></span>
<span data-ttu-id="00c62-119">Имя целевой группы</span><span class="sxs-lookup"><span data-stu-id="00c62-119">The target group name</span></span>

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

### <span data-ttu-id="00c62-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="00c62-120">-ParentObject</span></span>
<span data-ttu-id="00c62-121">Входной объект агента</span><span class="sxs-lookup"><span data-stu-id="00c62-121">The agent input object</span></span>

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

### <span data-ttu-id="00c62-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="00c62-122">-ParentResourceId</span></span>
<span data-ttu-id="00c62-123">Идентификатор ресурса агента</span><span class="sxs-lookup"><span data-stu-id="00c62-123">The agent resource id</span></span>

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

### <span data-ttu-id="00c62-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00c62-124">-ResourceGroupName</span></span>
<span data-ttu-id="00c62-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="00c62-125">The resource group name</span></span>

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

### <span data-ttu-id="00c62-126">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="00c62-126">-ServerName</span></span>
<span data-ttu-id="00c62-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="00c62-127">The server name</span></span>

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

### <span data-ttu-id="00c62-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="00c62-128">-Confirm</span></span>
<span data-ttu-id="00c62-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="00c62-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00c62-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00c62-130">-WhatIf</span></span>
<span data-ttu-id="00c62-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="00c62-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00c62-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00c62-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00c62-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00c62-133">CommonParameters</span></span>
<span data-ttu-id="00c62-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00c62-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00c62-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="00c62-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00c62-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00c62-136">INPUTS</span></span>

### <span data-ttu-id="00c62-137">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="00c62-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="00c62-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00c62-138">OUTPUTS</span></span>

### <span data-ttu-id="00c62-139">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="00c62-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="00c62-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="00c62-140">NOTES</span></span>

## <span data-ttu-id="00c62-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00c62-141">RELATED LINKS</span></span>
