---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: 76e712a881c88490a71933056f82fe1959df2948
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955843"
---
# <span data-ttu-id="08305-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="08305-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="08305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08305-102">SYNOPSIS</span></span>
<span data-ttu-id="08305-103">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="08305-103">Updates a database.</span></span>

## <span data-ttu-id="08305-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="08305-104">SYNTAX</span></span>

### <span data-ttu-id="08305-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="08305-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="08305-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="08305-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="08305-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08305-107">DESCRIPTION</span></span>
<span data-ttu-id="08305-108">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="08305-108">Updates a database.</span></span>

## <span data-ttu-id="08305-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="08305-109">EXAMPLES</span></span>

### <span data-ttu-id="08305-110">Пример 1. Обновление существующей базы данных по имени</span><span class="sxs-lookup"><span data-stu-id="08305-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="08305-111">С этой командой обновляется период soft deletion и период кэша базы данных "Mykustodatabase" кисто в кластере testnewkustocluster, который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="08305-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="08305-112">Пример 2. Обновление существующей базы данных с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="08305-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="08305-113">С этой командой обновляется период soft deletion и hot cache базы данных Кусто "mykustodatabase" в кластере testnewkustocluster, который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="08305-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="08305-114">Пример 3. Обновление существующей базы данных ReadOnly по имени</span><span class="sxs-lookup"><span data-stu-id="08305-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="08305-115">Вышеуказанная команда обновляет период кэша базы данных Кусто "mykustodatabase" в кластере "myfollowercluster", найденном в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="08305-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="08305-116">Пример 4. Обновление существующей базы данных ReadOnly с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="08305-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="08305-117">Вышеуказанная команда обновляет период кэша базы данных Кусто "mykustodatabase" в кластере "myfollowercluster", найденном в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="08305-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="08305-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08305-118">PARAMETERS</span></span>

### <span data-ttu-id="08305-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08305-119">-AsJob</span></span>
<span data-ttu-id="08305-120">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="08305-120">Run the command as a job</span></span>

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

### <span data-ttu-id="08305-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="08305-121">-ClusterName</span></span>
<span data-ttu-id="08305-122">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="08305-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="08305-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08305-123">-DefaultProfile</span></span>
<span data-ttu-id="08305-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="08305-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08305-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="08305-125">-HotCachePeriod</span></span>
<span data-ttu-id="08305-126">Время хранения данных в кэше для быстрых запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="08305-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="08305-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08305-127">-InputObject</span></span>
<span data-ttu-id="08305-128">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="08305-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="08305-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="08305-129">-Kind</span></span>
<span data-ttu-id="08305-130">Тип базы данных</span><span class="sxs-lookup"><span data-stu-id="08305-130">Kind of the database</span></span>

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

### <span data-ttu-id="08305-131">-Location</span><span class="sxs-lookup"><span data-stu-id="08305-131">-Location</span></span>
<span data-ttu-id="08305-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="08305-132">Resource location.</span></span>

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

### <span data-ttu-id="08305-133">-Name</span><span class="sxs-lookup"><span data-stu-id="08305-133">-Name</span></span>
<span data-ttu-id="08305-134">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="08305-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="08305-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="08305-135">-NoWait</span></span>
<span data-ttu-id="08305-136">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="08305-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="08305-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08305-137">-ResourceGroupName</span></span>
<span data-ttu-id="08305-138">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="08305-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="08305-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="08305-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="08305-140">Время хранения данных, прежде чем они перестают быть доступны для запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="08305-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="08305-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="08305-141">-SubscriptionId</span></span>
<span data-ttu-id="08305-142">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08305-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="08305-143">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="08305-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="08305-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08305-144">-Confirm</span></span>
<span data-ttu-id="08305-145">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08305-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08305-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08305-146">-WhatIf</span></span>
<span data-ttu-id="08305-147">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08305-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08305-148">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="08305-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08305-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08305-149">CommonParameters</span></span>
<span data-ttu-id="08305-150">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08305-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08305-151">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08305-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08305-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08305-152">INPUTS</span></span>

### <span data-ttu-id="08305-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="08305-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="08305-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="08305-154">OUTPUTS</span></span>

### <span data-ttu-id="08305-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="08305-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="08305-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="08305-156">NOTES</span></span>

<span data-ttu-id="08305-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="08305-157">ALIASES</span></span>

<span data-ttu-id="08305-158">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="08305-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="08305-159">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="08305-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08305-160">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08305-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="08305-161">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="08305-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="08305-162">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="08305-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="08305-163">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="08305-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="08305-164">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="08305-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="08305-165">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="08305-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="08305-166">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="08305-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="08305-167">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="08305-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="08305-168">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="08305-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="08305-169">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="08305-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="08305-170">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08305-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="08305-171">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="08305-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="08305-172">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08305-172">RELATED LINKS</span></span>

