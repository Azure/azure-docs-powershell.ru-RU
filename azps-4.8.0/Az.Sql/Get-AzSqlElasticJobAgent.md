---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/get-Azsqlelasticjobagent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobAgent.md
ms.openlocfilehash: 7d2985d2e5361f7594dbccac2e67c7c550c9b0a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080246"
---
# <span data-ttu-id="1d2be-101">Get-AzSqlElasticJobAgent</span><span class="sxs-lookup"><span data-stu-id="1d2be-101">Get-AzSqlElasticJobAgent</span></span>

## <span data-ttu-id="1d2be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1d2be-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2be-103">Получает агент заданий эластичных БД Azure SQL</span><span class="sxs-lookup"><span data-stu-id="1d2be-103">Gets a Azure SQL Elastic Job agent</span></span>

## <span data-ttu-id="1d2be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1d2be-104">SYNTAX</span></span>

### <span data-ttu-id="1d2be-105">Default (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1d2be-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobAgent [-ResourceGroupName] <String> [-ServerName] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2be-106">Объект</span><span class="sxs-lookup"><span data-stu-id="1d2be-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentObject] <AzureSqlServerModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d2be-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d2be-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobAgent [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d2be-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d2be-108">DESCRIPTION</span></span>
<span data-ttu-id="1d2be-109">Командлет Get-AzSqlElasticJobAgent получает один или несколько агентов эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="1d2be-109">The Get-AzSqlElasticJobAgent cmdlet gets one or more Elastic Job agents</span></span>

## <span data-ttu-id="1d2be-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1d2be-110">EXAMPLES</span></span>

### <span data-ttu-id="1d2be-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1d2be-111">Example 1</span></span>
```
PS C:\> Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent

ResourceGroupName ServerName       DatabaseName AgentName State Tags
----------------- ----------       ------------ --------- ----- ----
rg                elasticjobserver jobdb        agent     Ready
```

<span data-ttu-id="1d2be-112">Получает агент эластичных заданий</span><span class="sxs-lookup"><span data-stu-id="1d2be-112">Gets an Elastic Job agent</span></span>

## <span data-ttu-id="1d2be-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1d2be-113">PARAMETERS</span></span>

### <span data-ttu-id="1d2be-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d2be-114">-DefaultProfile</span></span>
<span data-ttu-id="1d2be-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1d2be-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d2be-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1d2be-116">-Name</span></span>
<span data-ttu-id="1d2be-117">Имя агента</span><span class="sxs-lookup"><span data-stu-id="1d2be-117">The agent name</span></span>

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

### <span data-ttu-id="1d2be-118">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="1d2be-118">-ParentObject</span></span>
<span data-ttu-id="1d2be-119">Входной объект сервера</span><span class="sxs-lookup"><span data-stu-id="1d2be-119">The server input object</span></span>

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

### <span data-ttu-id="1d2be-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1d2be-120">-ParentResourceId</span></span>
<span data-ttu-id="1d2be-121">Идентификатор ресурса сервера</span><span class="sxs-lookup"><span data-stu-id="1d2be-121">The server resource id</span></span>

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

### <span data-ttu-id="1d2be-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d2be-122">-ResourceGroupName</span></span>
<span data-ttu-id="1d2be-123">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1d2be-123">The resource group name</span></span>

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

### <span data-ttu-id="1d2be-124">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="1d2be-124">-ServerName</span></span>
<span data-ttu-id="1d2be-125">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="1d2be-125">The server name</span></span>

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

### <span data-ttu-id="1d2be-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2be-126">CommonParameters</span></span>
<span data-ttu-id="1d2be-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1d2be-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2be-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d2be-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2be-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1d2be-129">INPUTS</span></span>

### <span data-ttu-id="1d2be-130">Microsoft. Azure. Commands. SQL. Server. Model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1d2be-130">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

## <span data-ttu-id="1d2be-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1d2be-131">OUTPUTS</span></span>

### <span data-ttu-id="1d2be-132">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="1d2be-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="1d2be-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1d2be-133">NOTES</span></span>

## <span data-ttu-id="1d2be-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1d2be-134">RELATED LINKS</span></span>
