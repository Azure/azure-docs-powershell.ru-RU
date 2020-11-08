---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/invoke-azkustodetachclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Invoke-AzKustoDetachClusterFollowerDatabase.md
ms.openlocfilehash: 80994e2966ccb33bfaff0e2de2c70827c491108b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236322"
---
# <span data-ttu-id="52a52-101">Invoke-AzKustoDetachClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="52a52-101">Invoke-AzKustoDetachClusterFollowerDatabase</span></span>

## <span data-ttu-id="52a52-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="52a52-102">SYNOPSIS</span></span>
<span data-ttu-id="52a52-103">Отсоединяет все подписчики базы данных, которыми владеет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="52a52-103">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="52a52-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="52a52-104">SYNTAX</span></span>

### <span data-ttu-id="52a52-105">DetachExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="52a52-105">DetachExpanded (Default)</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="52a52-106">DetachViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="52a52-106">DetachViaIdentityExpanded</span></span>
```
Invoke-AzKustoDetachClusterFollowerDatabase -InputObject <IKustoIdentity>
 -AttachedDatabaseConfigurationName <String> -ClusterResourceId <String> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="52a52-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="52a52-107">DESCRIPTION</span></span>
<span data-ttu-id="52a52-108">Отсоединяет все подписчики базы данных, которыми владеет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="52a52-108">Detaches all followers of a database owned by this cluster.</span></span>

## <span data-ttu-id="52a52-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="52a52-109">EXAMPLES</span></span>

### <span data-ttu-id="52a52-110">Пример 1: отключение базы данных подписаться</span><span class="sxs-lookup"><span data-stu-id="52a52-110">Example 1: Detach a follower database</span></span>
```powershell
PS C:\> Invoke-AzKustoDetachClusterFollowerDatabase -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -AttachedDatabaseConfigurationName "myfollowerconfiguration" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf"

```

<span data-ttu-id="52a52-111">Вышеприведенная команда отсоединяет базу данных следов, определенную в AttachedDatabaseConfiguration "myfollowerconfiguration" из кластера "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="52a52-111">The above command detaches the follower database defined in AttachedDatabaseConfiguration "myfollowerconfiguration" from cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="52a52-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="52a52-112">PARAMETERS</span></span>

### <span data-ttu-id="52a52-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52a52-113">-AsJob</span></span>
<span data-ttu-id="52a52-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="52a52-114">Run the command as a job</span></span>

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

### <span data-ttu-id="52a52-115">-AttachedDatabaseConfigurationName</span><span class="sxs-lookup"><span data-stu-id="52a52-115">-AttachedDatabaseConfigurationName</span></span>
<span data-ttu-id="52a52-116">Название ресурса конфигурации присоединенной базы данных в кластере подписаться.</span><span class="sxs-lookup"><span data-stu-id="52a52-116">Resource name of the attached database configuration in the follower cluster.</span></span>

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

### <span data-ttu-id="52a52-117">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="52a52-117">-ClusterName</span></span>
<span data-ttu-id="52a52-118">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="52a52-118">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="52a52-119">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="52a52-119">-ClusterResourceId</span></span>
<span data-ttu-id="52a52-120">Идентификатор ресурса кластера, который следует за базой данных, которой владеет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="52a52-120">Resource id of the cluster that follows a database owned by this cluster.</span></span>

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

### <span data-ttu-id="52a52-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a52-121">-DefaultProfile</span></span>
<span data-ttu-id="52a52-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="52a52-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52a52-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52a52-123">-InputObject</span></span>
<span data-ttu-id="52a52-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="52a52-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="52a52-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="52a52-125">-NoWait</span></span>
<span data-ttu-id="52a52-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="52a52-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="52a52-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52a52-127">-PassThru</span></span>
<span data-ttu-id="52a52-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="52a52-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="52a52-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52a52-129">-ResourceGroupName</span></span>
<span data-ttu-id="52a52-130">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="52a52-130">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="52a52-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52a52-131">-SubscriptionId</span></span>
<span data-ttu-id="52a52-132">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="52a52-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="52a52-133">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="52a52-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="52a52-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52a52-134">-Confirm</span></span>
<span data-ttu-id="52a52-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="52a52-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a52-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a52-136">-WhatIf</span></span>
<span data-ttu-id="52a52-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="52a52-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a52-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="52a52-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a52-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a52-139">CommonParameters</span></span>
<span data-ttu-id="52a52-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="52a52-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a52-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52a52-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a52-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="52a52-142">INPUTS</span></span>

### <span data-ttu-id="52a52-143">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="52a52-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="52a52-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="52a52-144">OUTPUTS</span></span>

### <span data-ttu-id="52a52-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="52a52-145">System.Boolean</span></span>

## <span data-ttu-id="52a52-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="52a52-146">NOTES</span></span>

<span data-ttu-id="52a52-147">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="52a52-147">ALIASES</span></span>

<span data-ttu-id="52a52-148">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="52a52-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52a52-149">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="52a52-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52a52-150">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52a52-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52a52-151">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="52a52-151">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52a52-152">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="52a52-152">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="52a52-153">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="52a52-153">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="52a52-154">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="52a52-154">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="52a52-155">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="52a52-155">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="52a52-156">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="52a52-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52a52-157">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="52a52-157">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="52a52-158">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="52a52-158">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="52a52-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="52a52-159">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="52a52-160">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="52a52-160">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="52a52-161">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="52a52-161">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="52a52-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="52a52-162">RELATED LINKS</span></span>
