---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/get-Azsqlelasticjobtargetgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticJobTargetGroup.md
ms.openlocfilehash: 022ef6979ddac4fa31c0a1dae42ae04c044498dc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999619"
---
# <span data-ttu-id="faf17-101">Get-AzSqlElasticJobTargetGroup</span><span class="sxs-lookup"><span data-stu-id="faf17-101">Get-AzSqlElasticJobTargetGroup</span></span>

## <span data-ttu-id="faf17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faf17-102">SYNOPSIS</span></span>
<span data-ttu-id="faf17-103">Получает одну или несколько целевых групп задания</span><span class="sxs-lookup"><span data-stu-id="faf17-103">Gets one or more job target groups</span></span>

## <span data-ttu-id="faf17-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="faf17-104">SYNTAX</span></span>

### <span data-ttu-id="faf17-105">DefaultSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="faf17-105">DefaultSet (Default)</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ResourceGroupName] <String> [-ServerName] <String> [-AgentName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faf17-106">ObjectSet</span><span class="sxs-lookup"><span data-stu-id="faf17-106">ObjectSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentObject] <AzureSqlElasticJobAgentModel> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="faf17-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="faf17-107">ResourceIdSet</span></span>
```
Get-AzSqlElasticJobTargetGroup [-ParentResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faf17-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="faf17-108">DESCRIPTION</span></span>
<span data-ttu-id="faf17-109">Get-AzSqlElasticJobTargetGroup получает целевую группу и ее целевые объекты</span><span class="sxs-lookup"><span data-stu-id="faf17-109">The Get-AzSqlElasticJobTargetGroup cmdlet gets a target group and it's targets</span></span>

## <span data-ttu-id="faf17-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="faf17-110">EXAMPLES</span></span>

### <span data-ttu-id="faf17-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="faf17-111">Example 1</span></span>
```
PS C:\> $agent = Get-AzSqlElasticJobAgent -ResourceGroupName rg -ServerName elasticjobserver -Name agent
$agent | Get-AzSqlElasticJobTargetGroup -Name tg1

TargetGroupName Targets
--------------- -------
tg1             (s1,db1)
```

<span data-ttu-id="faf17-112">Получает целевую группу и ее целевые объекты</span><span class="sxs-lookup"><span data-stu-id="faf17-112">Gets a target group and it's targets</span></span>

## <span data-ttu-id="faf17-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="faf17-113">PARAMETERS</span></span>

### <span data-ttu-id="faf17-114">-AgentName</span><span class="sxs-lookup"><span data-stu-id="faf17-114">-AgentName</span></span>
<span data-ttu-id="faf17-115">Имя агента</span><span class="sxs-lookup"><span data-stu-id="faf17-115">The agent name</span></span>

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

### <span data-ttu-id="faf17-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faf17-116">-DefaultProfile</span></span>
<span data-ttu-id="faf17-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="faf17-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faf17-118">-Name</span><span class="sxs-lookup"><span data-stu-id="faf17-118">-Name</span></span>
<span data-ttu-id="faf17-119">Название целевой группы</span><span class="sxs-lookup"><span data-stu-id="faf17-119">The target group name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="faf17-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="faf17-120">-ParentObject</span></span>
<span data-ttu-id="faf17-121">Объект агента</span><span class="sxs-lookup"><span data-stu-id="faf17-121">The agent object</span></span>

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

### <span data-ttu-id="faf17-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="faf17-122">-ParentResourceId</span></span>
<span data-ttu-id="faf17-123">ИД агента ресурса</span><span class="sxs-lookup"><span data-stu-id="faf17-123">The agent resource id</span></span>

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

### <span data-ttu-id="faf17-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faf17-124">-ResourceGroupName</span></span>
<span data-ttu-id="faf17-125">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="faf17-125">The resource group name</span></span>

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

### <span data-ttu-id="faf17-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="faf17-126">-ServerName</span></span>
<span data-ttu-id="faf17-127">Имя сервера</span><span class="sxs-lookup"><span data-stu-id="faf17-127">The server name</span></span>

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

### <span data-ttu-id="faf17-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faf17-128">CommonParameters</span></span>
<span data-ttu-id="faf17-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faf17-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faf17-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="faf17-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faf17-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="faf17-131">INPUTS</span></span>

### <span data-ttu-id="faf17-132">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobAgentModel</span><span class="sxs-lookup"><span data-stu-id="faf17-132">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobAgentModel</span></span>

## <span data-ttu-id="faf17-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="faf17-133">OUTPUTS</span></span>

### <span data-ttu-id="faf17-134">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="faf17-134">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="faf17-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="faf17-135">NOTES</span></span>

## <span data-ttu-id="faf17-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="faf17-136">RELATED LINKS</span></span>
