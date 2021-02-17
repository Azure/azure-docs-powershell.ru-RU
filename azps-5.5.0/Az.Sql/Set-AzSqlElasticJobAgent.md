---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticJobAgent.md
ms.openlocfilehash: 58adbb3b160272007899dc8740e211b6e81a10a4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100230041"
---
# <span data-ttu-id="cb940-101">Set-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="cb940-101">Set-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="cb940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb940-102">SYNOPSIS</span></span>
<span data-ttu-id="cb940-103">Обновляет агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="cb940-103">Updates an elastic job agent</span></span>

## <span data-ttu-id="cb940-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cb940-104">SYNTAX</span></span>

### <span data-ttu-id="cb940-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cb940-105">DefaultSet (Default)</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb940-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="cb940-106">ObjectSet</span></span>
```
Set-AzSqlElasticJobAgent [-InputObject] <AzureSqlElasticJobAgentModel> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb940-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cb940-107">ResourceIdSet</span></span>
```
Set-AzSqlElasticJobAgent [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb940-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cb940-108">DESCRIPTION</span></span>
<span data-ttu-id="cb940-109">Set-AzSqlElasticJobAgent обновляет агенты эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="cb940-109">The Set-AzSqlElasticJobAgent cmdlet updates an Elastic Job agents</span></span>

## <span data-ttu-id="cb940-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cb940-110">EXAMPLES</span></span>

### <span data-ttu-id="cb940-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cb940-111">Example 1</span></span>
```
PS C:\> Set-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent -Tag @{ Octopus = "Agent" }

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready {[Octopus, Agent]}
```

<span data-ttu-id="cb940-112">Обновляет агент эластичного задания.</span><span class="sxs-lookup"><span data-stu-id="cb940-112">Updates an Elastic Job agent</span></span>

## <span data-ttu-id="cb940-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cb940-113">PARAMETERS</span></span>

### <span data-ttu-id="cb940-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb940-114">-DefaultProfile</span></span>
<span data-ttu-id="cb940-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cb940-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb940-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cb940-116">-InputObject</span></span>
<span data-ttu-id="cb940-117">Объект ввода агента</span><span class="sxs-lookup"><span data-stu-id="cb940-117">The agent input object</span></span>

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

### <span data-ttu-id="cb940-118">-Name</span><span class="sxs-lookup"><span data-stu-id="cb940-118">-Name</span></span>
<span data-ttu-id="cb940-119">Имя агента</span><span class="sxs-lookup"><span data-stu-id="cb940-119">The agent name</span></span>

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

### <span data-ttu-id="cb940-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb940-120">-ResourceGroupName</span></span>
<span data-ttu-id="cb940-121">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cb940-121">The resource group name</span></span>

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

### <span data-ttu-id="cb940-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb940-122">-ResourceId</span></span>
<span data-ttu-id="cb940-123">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="cb940-123">The agent resource id</span></span>

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

### <span data-ttu-id="cb940-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cb940-124">-ServerName</span></span>
<span data-ttu-id="cb940-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="cb940-125">The server name</span></span>

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

### <span data-ttu-id="cb940-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="cb940-126">-Tag</span></span>
<span data-ttu-id="cb940-127">Теги, которые нужно связать с агентом базы SQL Azure</span><span class="sxs-lookup"><span data-stu-id="cb940-127">The tags to associate with the Azure SQL Database Agent</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb940-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cb940-128">-Confirm</span></span>
<span data-ttu-id="cb940-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cb940-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb940-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb940-130">-WhatIf</span></span>
<span data-ttu-id="cb940-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb940-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb940-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cb940-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb940-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb940-133">CommonParameters</span></span>
<span data-ttu-id="cb940-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb940-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb940-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cb940-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb940-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cb940-136">INPUTS</span></span>

### <span data-ttu-id="cb940-137">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="cb940-137">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="cb940-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cb940-138">OUTPUTS</span></span>

### <span data-ttu-id="cb940-139">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="cb940-139">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="cb940-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cb940-140">NOTES</span></span>

## <span data-ttu-id="cb940-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cb940-141">RELATED LINKS</span></span>
