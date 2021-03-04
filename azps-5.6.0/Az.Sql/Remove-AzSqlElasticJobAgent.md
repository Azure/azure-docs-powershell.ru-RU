---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/remove-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobAgent.md
ms.openlocfilehash: 3c6a92a205aef19b1e4cef4842de4cf0414c2397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957891"
---
# <span data-ttu-id="8dc83-101">Remove-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="8dc83-101">Remove-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="8dc83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dc83-102">SYNOPSIS</span></span>
<span data-ttu-id="8dc83-103">Удаляет агент эластичного задания</span><span class="sxs-lookup"><span data-stu-id="8dc83-103">Removes the elastic job agent</span></span>

## <span data-ttu-id="8dc83-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dc83-104">SYNTAX</span></span>

### <span data-ttu-id="8dc83-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dc83-105">DefaultSet (Default)</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc83-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="8dc83-106">ObjectSet</span></span>
```
Remove-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dc83-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8dc83-107">ResourceIdSet</span></span>
```
Remove-AzSqlElasticJobAgent [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dc83-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dc83-108">DESCRIPTION</span></span>
<span data-ttu-id="8dc83-109">С Remove-AzSqlElasticJobAgent удаляется агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="8dc83-109">The Remove-AzSqlElasticJobAgent cmdlet removes an Elastic Job agent</span></span>

## <span data-ttu-id="8dc83-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dc83-110">EXAMPLES</span></span>

### <span data-ttu-id="8dc83-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dc83-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="8dc83-112">Удаляет агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="8dc83-112">Removes an Elastic Job agent</span></span>

## <span data-ttu-id="8dc83-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dc83-113">PARAMETERS</span></span>

### <span data-ttu-id="8dc83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dc83-114">-DefaultProfile</span></span>
<span data-ttu-id="8dc83-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dc83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dc83-116">-Force</span><span class="sxs-lookup"><span data-stu-id="8dc83-116">-Force</span></span>
<span data-ttu-id="8dc83-117">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="8dc83-117">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="8dc83-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dc83-118">-InputObject</span></span>
<span data-ttu-id="8dc83-119">Объект агента</span><span class="sxs-lookup"><span data-stu-id="8dc83-119">The agent object</span></span>

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

### <span data-ttu-id="8dc83-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8dc83-120">-Name</span></span>
<span data-ttu-id="8dc83-121">Имя агента</span><span class="sxs-lookup"><span data-stu-id="8dc83-121">The agent name</span></span>

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

### <span data-ttu-id="8dc83-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dc83-122">-ResourceGroupName</span></span>
<span data-ttu-id="8dc83-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8dc83-123">The resource group name</span></span>

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

### <span data-ttu-id="8dc83-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dc83-124">-ResourceId</span></span>
<span data-ttu-id="8dc83-125">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="8dc83-125">The agent resource id</span></span>

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

### <span data-ttu-id="8dc83-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8dc83-126">-ServerName</span></span>
<span data-ttu-id="8dc83-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="8dc83-127">The server name</span></span>

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

### <span data-ttu-id="8dc83-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8dc83-128">-Confirm</span></span>
<span data-ttu-id="8dc83-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8dc83-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dc83-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dc83-130">-WhatIf</span></span>
<span data-ttu-id="8dc83-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8dc83-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dc83-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8dc83-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dc83-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dc83-133">CommonParameters</span></span>
<span data-ttu-id="8dc83-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dc83-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dc83-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dc83-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dc83-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc83-136">INPUTS</span></span>

### <span data-ttu-id="8dc83-137">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8dc83-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8dc83-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dc83-138">OUTPUTS</span></span>

### <span data-ttu-id="8dc83-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="8dc83-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="8dc83-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dc83-140">NOTES</span></span>

## <span data-ttu-id="8dc83-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dc83-141">RELATED LINKS</span></span>
