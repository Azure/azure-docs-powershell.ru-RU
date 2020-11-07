---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 80835d33f75517bea6a91e65f110f441d20ab59c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906378"
---
# <span data-ttu-id="ee49c-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="ee49c-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="ee49c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ee49c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee49c-103">Получает агент заданий эластичных БД Azure SQL</span><span class="sxs-lookup"><span data-stu-id="ee49c-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="ee49c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ee49c-104">SYNTAX</span></span>

### <span data-ttu-id="ee49c-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee49c-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee49c-106">Объект</span><span class="sxs-lookup"><span data-stu-id="ee49c-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee49c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ee49c-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee49c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee49c-108">DESCRIPTION</span></span>
<span data-ttu-id="ee49c-109">Командлет Get-AzSqlElasticJobAgent получает один или несколько агентов эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="ee49c-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="ee49c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ee49c-110">EXAMPLES</span></span>

### <span data-ttu-id="ee49c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ee49c-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="ee49c-112">Получает агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="ee49c-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="ee49c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ee49c-113">PARAMETERS</span></span>

### <span data-ttu-id="ee49c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee49c-114">-DefaultProfile</span></span>
<span data-ttu-id="ee49c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee49c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee49c-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ee49c-116">-Name</span></span>
<span data-ttu-id="ee49c-117">Имя агента</span><span class="sxs-lookup"><span data-stu-id="ee49c-117">The agent name</span></span>

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

### <span data-ttu-id="ee49c-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="ee49c-118">-ParentObject</span></span>
<span data-ttu-id="ee49c-119">Входной объект сервера</span><span class="sxs-lookup"><span data-stu-id="ee49c-119">The server input object</span></span>

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

### <span data-ttu-id="ee49c-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ee49c-120">-ParentResourceId</span></span>
<span data-ttu-id="ee49c-121">Идентификатор ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="ee49c-121">The server resource id</span></span>

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

### <span data-ttu-id="ee49c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee49c-122">-ResourceGroupName</span></span>
<span data-ttu-id="ee49c-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="ee49c-123">The resource group name</span></span>

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

### <span data-ttu-id="ee49c-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="ee49c-124">-ServerName</span></span>
<span data-ttu-id="ee49c-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="ee49c-125">The server name</span></span>

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

### <span data-ttu-id="ee49c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee49c-126">CommonParameters</span></span>
<span data-ttu-id="ee49c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ee49c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee49c-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee49c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee49c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ee49c-129">INPUTS</span></span>

### <span data-ttu-id="ee49c-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="ee49c-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="ee49c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee49c-131">OUTPUTS</span></span>

### <span data-ttu-id="ee49c-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="ee49c-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="ee49c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="ee49c-133">NOTES</span></span>

## <span data-ttu-id="ee49c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee49c-134">RELATED LINKS</span></span>
