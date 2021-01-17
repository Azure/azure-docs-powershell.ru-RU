---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 1352ef72ffc6fd757b4019e217ecb439495ebb44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406871"
---
# <span data-ttu-id="2c528-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="2c528-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="2c528-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c528-102">SYNOPSIS</span></span>
<span data-ttu-id="2c528-103">Удаляет агент эластичного задания</span><span class="sxs-lookup"><span data-stu-id="2c528-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="2c528-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2c528-104">SYNTAX</span></span>

### <span data-ttu-id="2c528-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2c528-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c528-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="2c528-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c528-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2c528-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c528-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2c528-108">DESCRIPTION</span></span>
<span data-ttu-id="2c528-109">С Remove-AzSqlElasticJobAgent удаляется агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="2c528-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="2c528-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2c528-110">EXAMPLES</span></span>

### <span data-ttu-id="2c528-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2c528-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="2c528-112">Удаляет агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="2c528-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="2c528-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c528-113">PARAMETERS</span></span>

### <span data-ttu-id="2c528-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c528-114">-DefaultProfile</span></span>
<span data-ttu-id="2c528-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2c528-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c528-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2c528-116">-Force</span></span>
<span data-ttu-id="2c528-117">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="2c528-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c528-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c528-118">-InputObject</span></span>
<span data-ttu-id="2c528-119">Объект агента</span><span class="sxs-lookup"><span data-stu-id="2c528-119">The agent object</span></span>

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

### <span data-ttu-id="2c528-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2c528-120">-Name</span></span>
<span data-ttu-id="2c528-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="2c528-121">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultSet
Aliases: AgentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c528-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c528-122">-ResourceGroupName</span></span>
<span data-ttu-id="2c528-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2c528-123">The resource group name</span></span>

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

### <span data-ttu-id="2c528-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c528-124">-ResourceId</span></span>
<span data-ttu-id="2c528-125">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="2c528-125">The agent resource id</span></span>

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

### <span data-ttu-id="2c528-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2c528-126">-ServerName</span></span>
<span data-ttu-id="2c528-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="2c528-127">The server name</span></span>

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

### <span data-ttu-id="2c528-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c528-128">-Confirm</span></span>
<span data-ttu-id="2c528-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c528-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c528-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c528-130">-WhatIf</span></span>
<span data-ttu-id="2c528-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c528-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c528-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2c528-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c528-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c528-133">CommonParameters</span></span>
<span data-ttu-id="2c528-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c528-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c528-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c528-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c528-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c528-136">INPUTS</span></span>

### <span data-ttu-id="2c528-137">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2c528-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2c528-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c528-138">OUTPUTS</span></span>

### <span data-ttu-id="2c528-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="2c528-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="2c528-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2c528-140">NOTES</span></span>

## <span data-ttu-id="2c528-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2c528-141">RELATED LINKS</span></span>
