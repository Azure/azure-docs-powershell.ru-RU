---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: b7638780dc4fa360998d7d974d74c93ccd5c2afe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214484"
---
# <span data-ttu-id="1e5e6-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="1e5e6-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="1e5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e5e6-103">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-103">Updates a database.</span></span>

## <span data-ttu-id="1e5e6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e5e6-104">SYNTAX</span></span>

### <span data-ttu-id="1e5e6-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e5e6-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1e5e6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1e5e6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1e5e6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e5e6-107">DESCRIPTION</span></span>
<span data-ttu-id="1e5e6-108">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-108">Updates a database.</span></span>

## <span data-ttu-id="1e5e6-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e5e6-109">EXAMPLES</span></span>

### <span data-ttu-id="1e5e6-110">Пример 1. Обновление существующей базы данных по имени</span><span class="sxs-lookup"><span data-stu-id="1e5e6-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1e5e6-111">С этой командой обновляется период soft deletion и hot cache базы данных Кусто "mykustodatabase" в кластере testnewkustocluster, который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1e5e6-112">Пример 2. Обновление существующей базы данных с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="1e5e6-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1e5e6-113">С этой командой обновляется период soft deletion и период кэша базы данных "Mykustodatabase" кисто в кластере testnewkustocluster, который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1e5e6-114">Пример 3. Обновление существующей базы данных ReadOnly по имени</span><span class="sxs-lookup"><span data-stu-id="1e5e6-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1e5e6-115">Вышеуказанная команда обновляет период кэша базы данных Кусто "mykustodatabase" в кластере "myfollowercluster", найденном в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="1e5e6-116">Пример 4. Обновление существующей базы данных ReadOnly с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="1e5e6-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="1e5e6-117">Вышеуказанная команда обновляет период кэша базы данных Кусто "mykustodatabase" в кластере "myfollowercluster", найденном в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="1e5e6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e5e6-118">PARAMETERS</span></span>

### <span data-ttu-id="1e5e6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e5e6-119">-AsJob</span></span>
<span data-ttu-id="1e5e6-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="1e5e6-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1e5e6-121">-ClusterName</span></span>
<span data-ttu-id="1e5e6-122">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e5e6-123">-DefaultProfile</span></span>
<span data-ttu-id="1e5e6-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="1e5e6-125">-HotCachePeriod</span></span>
<span data-ttu-id="1e5e6-126">Время хранения данных в кэше для быстрых запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e5e6-127">-InputObject</span></span>
<span data-ttu-id="1e5e6-128">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="1e5e6-129">-Kind</span></span>
<span data-ttu-id="1e5e6-130">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="1e5e6-130">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-131">-Location</span><span class="sxs-lookup"><span data-stu-id="1e5e6-131">-Location</span></span>
<span data-ttu-id="1e5e6-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-132">Resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-133">-Name</span><span class="sxs-lookup"><span data-stu-id="1e5e6-133">-Name</span></span>
<span data-ttu-id="1e5e6-134">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-134">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e5e6-135">-NoWait</span></span>
<span data-ttu-id="1e5e6-136">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="1e5e6-136">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e5e6-137">-ResourceGroupName</span></span>
<span data-ttu-id="1e5e6-138">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-138">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="1e5e6-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="1e5e6-140">Время хранения данных, прежде чем они перестают быть доступны для запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e5e6-141">-SubscriptionId</span></span>
<span data-ttu-id="1e5e6-142">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1e5e6-143">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-143">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e5e6-144">-Confirm</span></span>
<span data-ttu-id="1e5e6-145">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e5e6-146">-WhatIf</span></span>
<span data-ttu-id="1e5e6-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e5e6-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-148">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e5e6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e5e6-149">CommonParameters</span></span>
<span data-ttu-id="1e5e6-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e5e6-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e5e6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e5e6-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e5e6-152">INPUTS</span></span>

### <span data-ttu-id="1e5e6-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="1e5e6-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="1e5e6-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e5e6-154">OUTPUTS</span></span>

### <span data-ttu-id="1e5e6-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="1e5e6-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="1e5e6-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e5e6-156">NOTES</span></span>

<span data-ttu-id="1e5e6-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="1e5e6-157">ALIASES</span></span>

<span data-ttu-id="1e5e6-158">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="1e5e6-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1e5e6-159">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1e5e6-160">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1e5e6-161">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="1e5e6-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1e5e6-162">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="1e5e6-163">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="1e5e6-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="1e5e6-164">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="1e5e6-165">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="1e5e6-166">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="1e5e6-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1e5e6-167">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="1e5e6-168">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="1e5e6-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="1e5e6-169">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="1e5e6-170">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1e5e6-171">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="1e5e6-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1e5e6-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e5e6-172">RELATED LINKS</span></span>

