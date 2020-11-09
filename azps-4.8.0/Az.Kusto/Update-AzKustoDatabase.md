---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/update-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Update-AzKustoDatabase.md
ms.openlocfilehash: eb4c4e8318cf091662a9348ef9e786ec25d5436f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244497"
---
# <span data-ttu-id="01fcb-101">Update-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="01fcb-101">Update-AzKustoDatabase</span></span>

## <span data-ttu-id="01fcb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="01fcb-103">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="01fcb-103">Updates a database.</span></span>

## <span data-ttu-id="01fcb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01fcb-104">SYNTAX</span></span>

### <span data-ttu-id="01fcb-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01fcb-105">UpdateExpanded (Default)</span></span>
```
Update-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 -Location <String> [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01fcb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="01fcb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzKustoDatabase -InputObject <IKustoIdentity> -Kind <Kind> -Location <String>
 [-HotCachePeriod <TimeSpan>] [-SoftDeletePeriod <TimeSpan>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01fcb-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01fcb-107">DESCRIPTION</span></span>
<span data-ttu-id="01fcb-108">Обновляет базу данных.</span><span class="sxs-lookup"><span data-stu-id="01fcb-108">Updates a database.</span></span>

## <span data-ttu-id="01fcb-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01fcb-109">EXAMPLES</span></span>

### <span data-ttu-id="01fcb-110">Пример 1: обновление существующей базы данных по имени</span><span class="sxs-lookup"><span data-stu-id="01fcb-110">Example 1: Update an existing database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="01fcb-111">Эта команда обновляет период мягкого удаления и период оперативного кэша для базы данных Kusto "mykustodatabase" в кластере "testnewkustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="01fcb-111">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="01fcb-112">Пример 2: обновление существующей базы данных с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="01fcb-112">Example 2: Update an existing database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> $4ds = New-TimeSpan -Days 4
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadWrite -SoftDeletePeriod $4ds -HotCachePeriod $2ds -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="01fcb-113">Эта команда обновляет период мягкого удаления и период оперативного кэша для базы данных Kusto "mykustodatabase" в кластере "testnewkustocluster", который находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="01fcb-113">The above command updates the soft deletion period and hot cache period of the Kusto database "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="01fcb-114">Пример 3: обновление существующей базы данных только для чтения по имени</span><span class="sxs-lookup"><span data-stu-id="01fcb-114">Example 3: Update an existing ReadOnly database by name</span></span>
```powershell
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="01fcb-115">Эта команда обновляет период оперативного кэша базы данных Kusto "mykustodatabase" в кластере "myfollowercluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="01fcb-115">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="01fcb-116">Пример 4: обновление существующей базы данных с доступом только для чтения с помощью удостоверения</span><span class="sxs-lookup"><span data-stu-id="01fcb-116">Example 4: Update an existing ReadOnly database via identity</span></span>
```powershell
PS C:\> $database = Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName myfollowercluster -Name mykustodatabase
PS C:\> $2ds = New-TimeSpan -Days 2
PS C:\> Update-AzKustoDatabase -InputObject $database -Kind ReadOnlyFollowing -HotCachePeriod $2ds -Location 'East US'

Kind              Location Name                                Type
----              -------- ----                                ----
ReadOnlyFollowing East US  myfollowercluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="01fcb-117">Эта команда обновляет период оперативного кэша базы данных Kusto "mykustodatabase" в кластере "myfollowercluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="01fcb-117">The above command updates the hot cache period of the Kusto database "mykustodatabase" in the cluster "myfollowercluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="01fcb-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01fcb-118">PARAMETERS</span></span>

### <span data-ttu-id="01fcb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01fcb-119">-AsJob</span></span>
<span data-ttu-id="01fcb-120">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="01fcb-120">Run the command as a job</span></span>

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

### <span data-ttu-id="01fcb-121">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="01fcb-121">-ClusterName</span></span>
<span data-ttu-id="01fcb-122">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="01fcb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01fcb-123">-DefaultProfile</span></span>
<span data-ttu-id="01fcb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01fcb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01fcb-125">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="01fcb-125">-HotCachePeriod</span></span>
<span data-ttu-id="01fcb-126">Время, в течение которого данные будут храниться в кэше для ускорения запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="01fcb-126">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

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

### <span data-ttu-id="01fcb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01fcb-127">-InputObject</span></span>
<span data-ttu-id="01fcb-128">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="01fcb-128">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01fcb-129">-Видах</span><span class="sxs-lookup"><span data-stu-id="01fcb-129">-Kind</span></span>
<span data-ttu-id="01fcb-130">Ее вида</span><span class="sxs-lookup"><span data-stu-id="01fcb-130">Kind of the database</span></span>

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

### <span data-ttu-id="01fcb-131">-Location</span><span class="sxs-lookup"><span data-stu-id="01fcb-131">-Location</span></span>
<span data-ttu-id="01fcb-132">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="01fcb-132">Resource location.</span></span>

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

### <span data-ttu-id="01fcb-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01fcb-133">-Name</span></span>
<span data-ttu-id="01fcb-134">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-134">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="01fcb-135">-Wait</span><span class="sxs-lookup"><span data-stu-id="01fcb-135">-NoWait</span></span>
<span data-ttu-id="01fcb-136">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="01fcb-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01fcb-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01fcb-137">-ResourceGroupName</span></span>
<span data-ttu-id="01fcb-138">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-138">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="01fcb-139">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="01fcb-139">-SoftDeletePeriod</span></span>
<span data-ttu-id="01fcb-140">Время, в течение которого данные будут храниться до того, как она станет доступна для запросов в TimeSpan.</span><span class="sxs-lookup"><span data-stu-id="01fcb-140">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

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

### <span data-ttu-id="01fcb-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01fcb-141">-SubscriptionId</span></span>
<span data-ttu-id="01fcb-142">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01fcb-142">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="01fcb-143">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="01fcb-143">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="01fcb-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01fcb-144">-Confirm</span></span>
<span data-ttu-id="01fcb-145">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01fcb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01fcb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01fcb-146">-WhatIf</span></span>
<span data-ttu-id="01fcb-147">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="01fcb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01fcb-148">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="01fcb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01fcb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01fcb-149">CommonParameters</span></span>
<span data-ttu-id="01fcb-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01fcb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01fcb-151">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01fcb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01fcb-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01fcb-152">INPUTS</span></span>

### <span data-ttu-id="01fcb-153">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="01fcb-153">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="01fcb-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01fcb-154">OUTPUTS</span></span>

### <span data-ttu-id="01fcb-155">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="01fcb-155">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="01fcb-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="01fcb-156">NOTES</span></span>

<span data-ttu-id="01fcb-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="01fcb-157">ALIASES</span></span>

<span data-ttu-id="01fcb-158">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="01fcb-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01fcb-159">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="01fcb-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01fcb-160">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01fcb-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01fcb-161">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="01fcb-161">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01fcb-162">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="01fcb-162">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="01fcb-163">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-163">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="01fcb-164">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="01fcb-164">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="01fcb-165">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-165">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="01fcb-166">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="01fcb-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01fcb-167">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="01fcb-167">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="01fcb-168">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="01fcb-168">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="01fcb-169">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="01fcb-169">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="01fcb-170">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="01fcb-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="01fcb-171">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="01fcb-171">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="01fcb-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01fcb-172">RELATED LINKS</span></span>
