---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: 6ade592fde11c3bd614f602070fba87b60cdcda3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065741"
---
# <span data-ttu-id="3dba2-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="3dba2-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="3dba2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dba2-102">SYNOPSIS</span></span>
<span data-ttu-id="3dba2-103">Добавление целевого объекта в целевую группу</span><span class="sxs-lookup"><span data-stu-id="3dba2-103">Adds a target to a target group</span></span>

## <span data-ttu-id="3dba2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dba2-104">SYNTAX</span></span>

### <span data-ttu-id="3dba2-105">SqlDatabase (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3dba2-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="3dba2-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dba2-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="3dba2-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3dba2-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3dba2-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="3dba2-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3dba2-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3dba2-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dba2-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3dba2-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dba2-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dba2-114">DESCRIPTION</span></span>
<span data-ttu-id="3dba2-115">Командлет Add-AzSqlElasticJobTarget добавляет целевой ресурс в целевую группу.</span><span class="sxs-lookup"><span data-stu-id="3dba2-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="3dba2-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dba2-116">EXAMPLES</span></span>

### <span data-ttu-id="3dba2-117">Пример 1: Добавление целевого сервера</span><span class="sxs-lookup"><span data-stu-id="3dba2-117">Example 1 - Add a server target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="3dba2-118">Пример 2. Добавление целевого объекта базы данных</span><span class="sxs-lookup"><span data-stu-id="3dba2-118">Example 2 - Add a database target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="3dba2-119">Пример 3: Добавление целевого объекта эластичного пула</span><span class="sxs-lookup"><span data-stu-id="3dba2-119">Example 3 - Add an elastic pool target</span></span>
```
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="3dba2-120">Пример 4: Добавление цели карты сегментов</span><span class="sxs-lookup"><span data-stu-id="3dba2-120">Example 4 - Add a shard map target</span></span>
```
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="3dba2-121">Добавляет конечный объект (сервер, пул эластичных БД, базу данных и карту сегментов) в целевую группу</span><span class="sxs-lookup"><span data-stu-id="3dba2-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="3dba2-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dba2-122">PARAMETERS</span></span>

### <span data-ttu-id="3dba2-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="3dba2-123">-AgentName</span></span>
<span data-ttu-id="3dba2-124">Имя агента.</span><span class="sxs-lookup"><span data-stu-id="3dba2-124">The agent name.</span></span>

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

### <span data-ttu-id="3dba2-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="3dba2-125">-AgentServerName</span></span>
<span data-ttu-id="3dba2-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3dba2-126">The server name.</span></span>

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

### <span data-ttu-id="3dba2-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3dba2-127">-DatabaseName</span></span>
<span data-ttu-id="3dba2-128">Имя целевого объекта базы данных</span><span class="sxs-lookup"><span data-stu-id="3dba2-128">Database Target Name</span></span>

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

### <span data-ttu-id="3dba2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dba2-129">-DefaultProfile</span></span>
<span data-ttu-id="3dba2-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dba2-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dba2-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3dba2-131">-ElasticPoolName</span></span>
<span data-ttu-id="3dba2-132">Имя целевого объекта пула эластичных БД</span><span class="sxs-lookup"><span data-stu-id="3dba2-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="3dba2-133">-Исключить</span><span class="sxs-lookup"><span data-stu-id="3dba2-133">-Exclude</span></span>
<span data-ttu-id="3dba2-134">Исключение целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="3dba2-134">Excludes a target.</span></span>

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

### <span data-ttu-id="3dba2-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3dba2-135">-ParentObject</span></span>
<span data-ttu-id="3dba2-136">Целевой объект группы.</span><span class="sxs-lookup"><span data-stu-id="3dba2-136">The target group object.</span></span>

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

### <span data-ttu-id="3dba2-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3dba2-137">-ParentResourceId</span></span>
<span data-ttu-id="3dba2-138">Идентификатор ресурса целевой группы.</span><span class="sxs-lookup"><span data-stu-id="3dba2-138">The target group resource id.</span></span>

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

### <span data-ttu-id="3dba2-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="3dba2-139">-RefreshCredentialName</span></span>
<span data-ttu-id="3dba2-140">Имя учетных данных обновления</span><span class="sxs-lookup"><span data-stu-id="3dba2-140">Refresh Credential Name</span></span>

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

### <span data-ttu-id="3dba2-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dba2-141">-ResourceGroupName</span></span>
<span data-ttu-id="3dba2-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3dba2-142">Resource Group Name</span></span>

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

### <span data-ttu-id="3dba2-143">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="3dba2-143">-ServerName</span></span>
<span data-ttu-id="3dba2-144">Имя целевого сервера</span><span class="sxs-lookup"><span data-stu-id="3dba2-144">Server Target Name</span></span>

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

### <span data-ttu-id="3dba2-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="3dba2-145">-ShardMapName</span></span>
<span data-ttu-id="3dba2-146">Целевое имя карты сегментов</span><span class="sxs-lookup"><span data-stu-id="3dba2-146">Shard Map Target Name</span></span>

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

### <span data-ttu-id="3dba2-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="3dba2-147">-TargetGroupName</span></span>
<span data-ttu-id="3dba2-148">Имя целевой группы.</span><span class="sxs-lookup"><span data-stu-id="3dba2-148">The target group name.</span></span>

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

### <span data-ttu-id="3dba2-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dba2-149">-Confirm</span></span>
<span data-ttu-id="3dba2-150">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dba2-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dba2-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dba2-151">-WhatIf</span></span>
<span data-ttu-id="3dba2-152">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dba2-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dba2-153">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dba2-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dba2-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dba2-154">CommonParameters</span></span>
<span data-ttu-id="3dba2-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dba2-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dba2-156">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dba2-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dba2-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dba2-157">INPUTS</span></span>

### <span data-ttu-id="3dba2-158">Microsoft. Azure. Commands. SQL. ElasticJobs. Model. AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="3dba2-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="3dba2-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dba2-159">OUTPUTS</span></span>

### <span data-ttu-id="3dba2-160">Microsoft. Azure. Management. SQL. Models. JobTarget</span><span class="sxs-lookup"><span data-stu-id="3dba2-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="3dba2-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dba2-161">NOTES</span></span>

## <span data-ttu-id="3dba2-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dba2-162">RELATED LINKS</span></span>
