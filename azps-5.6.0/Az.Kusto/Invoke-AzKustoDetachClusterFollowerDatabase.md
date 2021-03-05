---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: f410ba5dc89f29c3a928ed459be87769bf5ffca7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960712"
---
# <span data-ttu-id="dfbbe-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="dfbbe-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="dfbbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfbbe-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbbe-103">Отсоединяет всех подписчиков базы данных, владельцем которой является этот кластер.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="dfbbe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dfbbe-104">SYNTAX</span></span>

### <span data-ttu-id="dfbbe-105">DetachExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dfbbe-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dfbbe-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dfbbe-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dfbbe-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfbbe-107">DESCRIPTION</span></span>
<span data-ttu-id="dfbbe-108">Отсоединяет всех подписчиков базы данных, владельцем которой является этот кластер.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="dfbbe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dfbbe-109">EXAMPLES</span></span>

### <span data-ttu-id="dfbbe-110">Пример 1. Отсоединения базы данных для последователя</span><span class="sxs-lookup"><span data-stu-id="dfbbe-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="dfbbe-111">Она отсоединяет базу данных, заданную в AttachedDatabaseConfiguration "myfollowerconfiguration", из кластера "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="dfbbe-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="dfbbe-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfbbe-112">PARAMETERS</span></span>

### <span data-ttu-id="dfbbe-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dfbbe-113">-AsJob</span></span>
<span data-ttu-id="dfbbe-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="dfbbe-114">Run the command as a job</span></span>

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

### <span data-ttu-id="dfbbe-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="dfbbe-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="dfbbe-116">Имя ресурса конфигурации подключенной базы данных в кластере, который вы отслеживаете.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="dfbbe-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="dfbbe-117">-ClusterName</span></span>
<span data-ttu-id="dfbbe-118">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-118">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbbe-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="dfbbe-119">-ClusterResourceId</span></span>
<span data-ttu-id="dfbbe-120">ИД ресурса кластера, который следует за базой данных, владельцем которой является этот кластер.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="dfbbe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbbe-121">-DefaultProfile</span></span>
<span data-ttu-id="dfbbe-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfbbe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfbbe-123">-InputObject</span></span>
<span data-ttu-id="dfbbe-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: DetachViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dfbbe-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="dfbbe-125">-NoWait</span></span>
<span data-ttu-id="dfbbe-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="dfbbe-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="dfbbe-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dfbbe-127">-PassThru</span></span>
<span data-ttu-id="dfbbe-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dfbbe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfbbe-129">-ResourceGroupName</span></span>
<span data-ttu-id="dfbbe-130">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-130">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbbe-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dfbbe-131">-SubscriptionId</span></span>
<span data-ttu-id="dfbbe-132">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dfbbe-133">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: DetachExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbbe-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfbbe-134">-Confirm</span></span>
<span data-ttu-id="dfbbe-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfbbe-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfbbe-136">-WhatIf</span></span>
<span data-ttu-id="dfbbe-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfbbe-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfbbe-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbbe-139">CommonParameters</span></span>
<span data-ttu-id="dfbbe-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbbe-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dfbbe-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbbe-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfbbe-142">INPUTS</span></span>

### <span data-ttu-id="dfbbe-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="dfbbe-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="dfbbe-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dfbbe-144">OUTPUTS</span></span>

### <span data-ttu-id="dfbbe-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dfbbe-145">System.Boolean</span></span>

## <span data-ttu-id="dfbbe-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dfbbe-146">NOTES</span></span>

<span data-ttu-id="dfbbe-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dfbbe-147">ALIASES</span></span>

<span data-ttu-id="dfbbe-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dfbbe-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dfbbe-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dfbbe-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dfbbe-151">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dfbbe-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dfbbe-152">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="dfbbe-153">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="dfbbe-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="dfbbe-154">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="dfbbe-155">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="dfbbe-156">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dfbbe-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dfbbe-157">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="dfbbe-158">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="dfbbe-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="dfbbe-159">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="dfbbe-160">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dfbbe-161">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="dfbbe-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="dfbbe-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfbbe-162">RELATED LINKS</span></span>

