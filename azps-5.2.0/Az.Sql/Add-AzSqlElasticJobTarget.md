---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392740"
---
# <span data-ttu-id="40116-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="40116-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="40116-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40116-102">SYNOPSIS</span></span>
<span data-ttu-id="40116-103">Добавляет целевой объект в целевую группу</span><span class="sxs-lookup"><span data-stu-id="40116-103">Adds a target to a target group</span></span>

## <span data-ttu-id="40116-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40116-104">SYNTAX</span></span>

### <span data-ttu-id="40116-105">SqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40116-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="40116-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40116-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="40116-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="40116-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="40116-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="40116-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40116-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40116-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40116-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40116-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40116-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40116-114">DESCRIPTION</span></span>
<span data-ttu-id="40116-115">С Add-AzSqlElasticJobTarget добавляет целевой ресурс в целевую группу.</span><span class="sxs-lookup"><span data-stu-id="40116-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="40116-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40116-116">EXAMPLES</span></span>

### <span data-ttu-id="40116-117">Пример 1. Добавление целевого сервера</span><span class="sxs-lookup"><span data-stu-id="40116-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="40116-118">Пример 2. Добавление целевого сайта базы данных</span><span class="sxs-lookup"><span data-stu-id="40116-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="40116-119">Пример 3. Добавление целевого пула в качестве эластичного пула</span><span class="sxs-lookup"><span data-stu-id="40116-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="40116-120">Пример 4. Добавление целевой карты в качестве карты</span><span class="sxs-lookup"><span data-stu-id="40116-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="40116-121">Добавляет целевую группу (серверную, эластичный пул, базу данных и карту shard) в целевую группу.</span><span class="sxs-lookup"><span data-stu-id="40116-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="40116-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40116-122">PARAMETERS</span></span>

### <span data-ttu-id="40116-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="40116-123">-AgentName</span></span>
<span data-ttu-id="40116-124">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="40116-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40116-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="40116-125">-AgentServerName</span></span>
<span data-ttu-id="40116-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="40116-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40116-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40116-127">-DatabaseName</span></span>
<span data-ttu-id="40116-128">Имя целевой базы данных</span><span class="sxs-lookup"><span data-stu-id="40116-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40116-129">-DefaultProfile</span></span>
<span data-ttu-id="40116-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40116-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40116-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="40116-131">-ElasticPoolName</span></span>
<span data-ttu-id="40116-132">Имя целевого пула в эластичном пуле</span><span class="sxs-lookup"><span data-stu-id="40116-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="40116-133">-Exclude</span></span>
<span data-ttu-id="40116-134">Исключает целевой объект.</span><span class="sxs-lookup"><span data-stu-id="40116-134">Excludes a target.</span></span>

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

### <span data-ttu-id="40116-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="40116-135">-ParentObject</span></span>
<span data-ttu-id="40116-136">Объект целевой группы.</span><span class="sxs-lookup"><span data-stu-id="40116-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="40116-137">-ParentResourceId</span></span>
<span data-ttu-id="40116-138">ИД ресурса целевой группы.</span><span class="sxs-lookup"><span data-stu-id="40116-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="40116-139">-RefreshCredentialName</span></span>
<span data-ttu-id="40116-140">Обновить имя учетной данные</span><span class="sxs-lookup"><span data-stu-id="40116-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40116-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40116-141">-ResourceGroupName</span></span>
<span data-ttu-id="40116-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="40116-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40116-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40116-143">-ServerName</span></span>
<span data-ttu-id="40116-144">Целевое имя сервера</span><span class="sxs-lookup"><span data-stu-id="40116-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="40116-145">-ShardMapName</span></span>
<span data-ttu-id="40116-146">Shard Map Target Name</span><span class="sxs-lookup"><span data-stu-id="40116-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40116-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="40116-147">-TargetGroupName</span></span>
<span data-ttu-id="40116-148">Имя целевой группы.</span><span class="sxs-lookup"><span data-stu-id="40116-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40116-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40116-149">-Confirm</span></span>
<span data-ttu-id="40116-150">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40116-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40116-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40116-151">-WhatIf</span></span>
<span data-ttu-id="40116-152">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40116-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40116-153">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40116-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40116-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40116-154">CommonParameters</span></span>
<span data-ttu-id="40116-155">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40116-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40116-156">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40116-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40116-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40116-157">INPUTS</span></span>

### <span data-ttu-id="40116-158">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="40116-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="40116-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40116-159">OUTPUTS</span></span>

### <span data-ttu-id="40116-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="40116-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="40116-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40116-161">NOTES</span></span>

## <span data-ttu-id="40116-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40116-162">RELATED LINKS</span></span>
