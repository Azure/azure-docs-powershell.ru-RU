---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 94ad9cb0c6c1db6ebc7233c63dcd26e8eebb4bef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072954"
---
# <span data-ttu-id="e8c7d-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="e8c7d-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="e8c7d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8c7d-103">Удаление целевого объекта из целевой группы</span><span class="sxs-lookup"><span data-stu-id="e8c7d-103">Removes the target from the target group</span></span>

## <span data-ttu-id="e8c7d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8c7d-104">SYNTAX</span></span>

### <span data-ttu-id="e8c7d-105">SqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e8c7d-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="e8c7d-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="e8c7d-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e8c7d-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e8c7d-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="e8c7d-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e8c7d-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e8c7d-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8c7d-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e8c7d-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8c7d-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8c7d-114">DESCRIPTION</span></span>
<span data-ttu-id="e8c7d-115">Командлет Remove-AzSqlElasticJobTarget удаляет целевой ресурс в целевую группу.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="e8c7d-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8c7d-116">EXAMPLES</span></span>

### <span data-ttu-id="e8c7d-117">Пример 1: Удаление целевого сервера</span><span class="sxs-lookup"><span data-stu-id="e8c7d-117">Example 1 - Remove a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="e8c7d-118">Пример 2. Удаление целевого объекта базы данных</span><span class="sxs-lookup"><span data-stu-id="e8c7d-118">Example 2 - Remove a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="e8c7d-119">Пример 3. Удаление целевого объекта эластичного пула</span><span class="sxs-lookup"><span data-stu-id="e8c7d-119">Example 3 - Remove an elastic pool target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="e8c7d-120">Пример 4: удаление цели карты сегментов</span><span class="sxs-lookup"><span data-stu-id="e8c7d-120">Example 4 - Remove a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="e8c7d-121">Удаление целевого объекта (сервера, пула эластичных БД, базы данных и карты сегментов) из целевой группы</span><span class="sxs-lookup"><span data-stu-id="e8c7d-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="e8c7d-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8c7d-122">PARAMETERS</span></span>

### <span data-ttu-id="e8c7d-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-123">-AgentName</span></span>
<span data-ttu-id="e8c7d-124">Имя агента базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="e8c7d-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-125">-AgentServerName</span></span>
<span data-ttu-id="e8c7d-126">Имя сервера агента базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="e8c7d-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-127">-DatabaseName</span></span>
<span data-ttu-id="e8c7d-128">Имя целевого объекта базы данных</span><span class="sxs-lookup"><span data-stu-id="e8c7d-128">Database Target Name</span></span>

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

### <span data-ttu-id="e8c7d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8c7d-129">-DefaultProfile</span></span>
<span data-ttu-id="e8c7d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8c7d-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-131">-ElasticPoolName</span></span>
<span data-ttu-id="e8c7d-132">Имя целевого объекта пула эластичных БД</span><span class="sxs-lookup"><span data-stu-id="e8c7d-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="e8c7d-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e8c7d-133">-ParentObject</span></span>
<span data-ttu-id="e8c7d-134">Целевой объект группы.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-134">The target group object.</span></span>

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

### <span data-ttu-id="e8c7d-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e8c7d-135">-ParentResourceId</span></span>
<span data-ttu-id="e8c7d-136">Идентификатор ресурса целевой группы.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-136">The target group resource id.</span></span>

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

### <span data-ttu-id="e8c7d-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-137">-RefreshCredentialName</span></span>
<span data-ttu-id="e8c7d-138">Имя учетных данных обновления</span><span class="sxs-lookup"><span data-stu-id="e8c7d-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="e8c7d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-139">-ResourceGroupName</span></span>
<span data-ttu-id="e8c7d-140">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e8c7d-140">Resource Group Name</span></span>

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

### <span data-ttu-id="e8c7d-141">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="e8c7d-141">-ServerName</span></span>
<span data-ttu-id="e8c7d-142">Имя целевого сервера</span><span class="sxs-lookup"><span data-stu-id="e8c7d-142">Server Target Name</span></span>

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

### <span data-ttu-id="e8c7d-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-143">-ShardMapName</span></span>
<span data-ttu-id="e8c7d-144">Целевое имя карты сегментов</span><span class="sxs-lookup"><span data-stu-id="e8c7d-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="e8c7d-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="e8c7d-145">-TargetGroupName</span></span>
<span data-ttu-id="e8c7d-146">Имя агента базы данных SQL.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="e8c7d-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8c7d-147">-Confirm</span></span>
<span data-ttu-id="e8c7d-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8c7d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8c7d-149">-WhatIf</span></span>
<span data-ttu-id="e8c7d-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8c7d-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8c7d-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8c7d-152">CommonParameters</span></span>
<span data-ttu-id="e8c7d-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8c7d-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8c7d-154">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8c7d-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8c7d-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8c7d-155">INPUTS</span></span>

### <span data-ttu-id="e8c7d-156">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="e8c7d-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="e8c7d-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8c7d-157">OUTPUTS</span></span>

### <span data-ttu-id="e8c7d-158">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="e8c7d-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="e8c7d-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8c7d-159">NOTES</span></span>

## <span data-ttu-id="e8c7d-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8c7d-160">RELATED LINKS</span></span>
