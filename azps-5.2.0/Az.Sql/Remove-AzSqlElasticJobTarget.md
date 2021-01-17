---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415908"
---
# <span data-ttu-id="4e412-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="4e412-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="4e412-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e412-102">SYNOPSIS</span></span>
<span data-ttu-id="4e412-103">Удаляет целевой объект из целевой группы.</span><span class="sxs-lookup"><span data-stu-id="4e412-103">Removes the target from the target group</span></span>

## <span data-ttu-id="4e412-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e412-104">SYNTAX</span></span>

### <span data-ttu-id="4e412-105">База данных Sql (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e412-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="4e412-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="4e412-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e412-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4e412-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4e412-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="4e412-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e412-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e412-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e412-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4e412-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e412-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e412-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e412-114">DESCRIPTION</span></span>
<span data-ttu-id="4e412-115">С Remove-AzSqlElasticJobTarget целевой ресурс удаляется из целевой группы.</span><span class="sxs-lookup"><span data-stu-id="4e412-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="4e412-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e412-116">EXAMPLES</span></span>

### <span data-ttu-id="4e412-117">Пример 1. Удаление целевого сервера</span><span class="sxs-lookup"><span data-stu-id="4e412-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="4e412-118">Пример 2. Удаление целевого сайта базы данных</span><span class="sxs-lookup"><span data-stu-id="4e412-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="4e412-119">Пример 3. Удаление целевого пула в качестве эластичного пула</span><span class="sxs-lookup"><span data-stu-id="4e412-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="4e412-120">Пример 4. Удаление целевой карты в области «Карта»</span><span class="sxs-lookup"><span data-stu-id="4e412-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="4e412-121">Удаляет целевую группу (серверную, эластичный пул, базу данных и карту shard) из целевой группы.</span><span class="sxs-lookup"><span data-stu-id="4e412-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="4e412-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e412-122">PARAMETERS</span></span>

### <span data-ttu-id="4e412-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="4e412-123">-AgentName</span></span>
<span data-ttu-id="4e412-124">SQL имя агента базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e412-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="4e412-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="4e412-125">-AgentServerName</span></span>
<span data-ttu-id="4e412-126">SQL имя сервера агента базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e412-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="4e412-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e412-127">-DatabaseName</span></span>
<span data-ttu-id="4e412-128">Имя целевой базы данных</span><span class="sxs-lookup"><span data-stu-id="4e412-128">Database Target Name</span></span>

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

### <span data-ttu-id="4e412-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e412-129">-DefaultProfile</span></span>
<span data-ttu-id="4e412-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e412-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e412-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4e412-131">-ElasticPoolName</span></span>
<span data-ttu-id="4e412-132">Целевое имя целевого пула в эластичном пуле</span><span class="sxs-lookup"><span data-stu-id="4e412-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="4e412-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="4e412-133">-ParentObject</span></span>
<span data-ttu-id="4e412-134">Объект целевой группы.</span><span class="sxs-lookup"><span data-stu-id="4e412-134">The target group object.</span></span>

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

### <span data-ttu-id="4e412-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="4e412-135">-ParentResourceId</span></span>
<span data-ttu-id="4e412-136">ИД ресурса целевой группы.</span><span class="sxs-lookup"><span data-stu-id="4e412-136">The target group resource id.</span></span>

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

### <span data-ttu-id="4e412-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="4e412-137">-RefreshCredentialName</span></span>
<span data-ttu-id="4e412-138">Обновление имени учетных данных</span><span class="sxs-lookup"><span data-stu-id="4e412-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="4e412-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e412-139">-ResourceGroupName</span></span>
<span data-ttu-id="4e412-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e412-140">Resource Group Name</span></span>

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

### <span data-ttu-id="4e412-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4e412-141">-ServerName</span></span>
<span data-ttu-id="4e412-142">Целевое имя сервера</span><span class="sxs-lookup"><span data-stu-id="4e412-142">Server Target Name</span></span>

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

### <span data-ttu-id="4e412-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="4e412-143">-ShardMapName</span></span>
<span data-ttu-id="4e412-144">Shard Map Target Name</span><span class="sxs-lookup"><span data-stu-id="4e412-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="4e412-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="4e412-145">-TargetGroupName</span></span>
<span data-ttu-id="4e412-146">SQL имя агента базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e412-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="4e412-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e412-147">-Confirm</span></span>
<span data-ttu-id="4e412-148">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e412-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e412-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e412-149">-WhatIf</span></span>
<span data-ttu-id="4e412-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e412-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e412-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4e412-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e412-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e412-152">CommonParameters</span></span>
<span data-ttu-id="4e412-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e412-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e412-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e412-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e412-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e412-155">INPUTS</span></span>

### <span data-ttu-id="4e412-156">Microsoft.Azure.Commands.Sql.AsticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="4e412-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="4e412-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e412-157">OUTPUTS</span></span>

### <span data-ttu-id="4e412-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="4e412-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="4e412-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e412-159">NOTES</span></span>

## <span data-ttu-id="4e412-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e412-160">RELATED LINKS</span></span>
