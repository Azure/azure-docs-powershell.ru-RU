---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225156"
---
# <span data-ttu-id="72147-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="72147-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="72147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72147-102">SYNOPSIS</span></span>
<span data-ttu-id="72147-103">Получает агент a Azure SQL эластичного задания</span><span class="sxs-lookup"><span data-stu-id="72147-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="72147-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72147-104">SYNTAX</span></span>

### <span data-ttu-id="72147-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72147-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72147-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="72147-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72147-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72147-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72147-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72147-108">DESCRIPTION</span></span>
<span data-ttu-id="72147-109">Этот Get-AzSqlElasticJobAgent получает один или несколько агентов эластичности</span><span class="sxs-lookup"><span data-stu-id="72147-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="72147-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72147-110">EXAMPLES</span></span>

### <span data-ttu-id="72147-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="72147-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="72147-112">Получает агент эластичного задания</span><span class="sxs-lookup"><span data-stu-id="72147-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="72147-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72147-113">PARAMETERS</span></span>

### <span data-ttu-id="72147-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72147-114">-DefaultProfile</span></span>
<span data-ttu-id="72147-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72147-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72147-116">-Name</span><span class="sxs-lookup"><span data-stu-id="72147-116">-Name</span></span>
<span data-ttu-id="72147-117">Имя агента</span><span class="sxs-lookup"><span data-stu-id="72147-117">The agent name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AgentName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72147-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="72147-118">-ParentObject</span></span>
<span data-ttu-id="72147-119">Объект ввода сервера</span><span class="sxs-lookup"><span data-stu-id="72147-119">The server input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72147-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="72147-120">-ParentResourceId</span></span>
<span data-ttu-id="72147-121">ИД ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="72147-121">The server resource id</span></span>

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

### <span data-ttu-id="72147-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72147-122">-ResourceGroupName</span></span>
<span data-ttu-id="72147-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="72147-123">The resource group name</span></span>

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

### <span data-ttu-id="72147-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="72147-124">-ServerName</span></span>
<span data-ttu-id="72147-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="72147-125">The server name</span></span>

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

### <span data-ttu-id="72147-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72147-126">CommonParameters</span></span>
<span data-ttu-id="72147-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72147-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72147-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72147-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72147-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72147-129">INPUTS</span></span>

### <span data-ttu-id="72147-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="72147-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="72147-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72147-131">OUTPUTS</span></span>

### <span data-ttu-id="72147-132">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="72147-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="72147-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72147-133">NOTES</span></span>

## <span data-ttu-id="72147-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72147-134">RELATED LINKS</span></span>
