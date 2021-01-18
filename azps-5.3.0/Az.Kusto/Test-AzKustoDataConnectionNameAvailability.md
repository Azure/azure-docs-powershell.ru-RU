---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodataconnectionnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDataConnectionNameAvailability.md
ms.openlocfilehash: 14eee624f4de3129ddeefee05d402abb0cb686db
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508270"
---
# <span data-ttu-id="16e3a-101">Test-AzKustoDataConnectionNameAvailability</span><span class="sxs-lookup"><span data-stu-id="16e3a-101">Test-AzKustoDataConnectionNameAvailability</span></span>

## <span data-ttu-id="16e3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e3a-102">SYNOPSIS</span></span>
<span data-ttu-id="16e3a-103">Проверяет, допустимо ли имя подключения к данным и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="16e3a-103">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="16e3a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="16e3a-104">SYNTAX</span></span>

### <span data-ttu-id="16e3a-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="16e3a-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDataConnectionNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="16e3a-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="16e3a-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDataConnectionNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16e3a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="16e3a-107">DESCRIPTION</span></span>
<span data-ttu-id="16e3a-108">Проверяет, допустимо ли имя подключения к данным и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="16e3a-108">Checks that the data connection name is valid and is not already in use.</span></span>

## <span data-ttu-id="16e3a-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="16e3a-109">EXAMPLES</span></span>

### <span data-ttu-id="16e3a-110">Пример 1. Проверка доступности используемого имени подключения к данным</span><span class="sxs-lookup"><span data-stu-id="16e3a-110">Example 1: Check the availability of a Data Connection name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mykustodataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message                                                                                                                                                          Name                  NameAvailable Reason
-------                                                                                                                                                          ----                  ------------- ------
Data Connection mykustodataconnection already exists in database mykustodatabase in cluster testnewkustocluster. Please select a different data connection name. mykustodataconnection False         AlreadyExists
```

<span data-ttu-id="16e3a-111">Вышеуказанная команда возвращает, существует ли в базе данных "mykustodatabase" подключение к данным с именем "mykustodataconnection".</span><span class="sxs-lookup"><span data-stu-id="16e3a-111">The above command returns whether or not a Data Connection named "mykustodataconnection" exists in the "mykustodatabase" database.</span></span>

### <span data-ttu-id="16e3a-112">Пример 2. Проверка доступности имени подключения к данным, которое не используется</span><span class="sxs-lookup"><span data-stu-id="16e3a-112">Example 2: Check the availability of a Data Connection name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDataConnectionNameAvailability -ClusterName testnewkustocluster -DatabaseName mykustodatabase -ResourceGroupName testrg -Name mydataconnection -Type Microsoft.Kusto/Clusters/Databases/dataConnections

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mydataconnection True
```

<span data-ttu-id="16e3a-113">Вышеуказанная команда возвращает, существует ли подключение к данным с именем "mydataconnection" в базе данных "mykustodatabase".</span><span class="sxs-lookup"><span data-stu-id="16e3a-113">The above command returns whether or not a Data Connection named "mydataconnection" exists in the "mykustodatabase" database.</span></span>

## <span data-ttu-id="16e3a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16e3a-114">PARAMETERS</span></span>

### <span data-ttu-id="16e3a-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="16e3a-115">-ClusterName</span></span>
<span data-ttu-id="16e3a-116">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="16e3a-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="16e3a-117">-DatabaseName</span></span>
<span data-ttu-id="16e3a-118">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="16e3a-118">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e3a-119">-DefaultProfile</span></span>
<span data-ttu-id="16e3a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="16e3a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16e3a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16e3a-121">-InputObject</span></span>
<span data-ttu-id="16e3a-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="16e3a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="16e3a-123">-Name</span></span>
<span data-ttu-id="16e3a-124">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="16e3a-124">Data Connection name.</span></span>

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

### <span data-ttu-id="16e3a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e3a-125">-ResourceGroupName</span></span>
<span data-ttu-id="16e3a-126">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="16e3a-126">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16e3a-127">-SubscriptionId</span></span>
<span data-ttu-id="16e3a-128">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16e3a-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="16e3a-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="16e3a-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-130">-Type</span><span class="sxs-lookup"><span data-stu-id="16e3a-130">-Type</span></span>
<span data-ttu-id="16e3a-131">Тип ресурса: Microsoft.Kusto/Clusters/Databases/dataConnections.</span><span class="sxs-lookup"><span data-stu-id="16e3a-131">The type of resource, Microsoft.Kusto/Clusters/Databases/dataConnections.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16e3a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16e3a-132">-Confirm</span></span>
<span data-ttu-id="16e3a-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e3a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e3a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e3a-134">-WhatIf</span></span>
<span data-ttu-id="16e3a-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16e3a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16e3a-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="16e3a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e3a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e3a-137">CommonParameters</span></span>
<span data-ttu-id="16e3a-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16e3a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e3a-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e3a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e3a-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="16e3a-140">INPUTS</span></span>

### <span data-ttu-id="16e3a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="16e3a-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="16e3a-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="16e3a-142">OUTPUTS</span></span>

### <span data-ttu-id="16e3a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="16e3a-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="16e3a-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="16e3a-144">NOTES</span></span>

<span data-ttu-id="16e3a-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="16e3a-145">ALIASES</span></span>

<span data-ttu-id="16e3a-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="16e3a-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16e3a-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="16e3a-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16e3a-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="16e3a-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16e3a-149">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="16e3a-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="16e3a-150">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="16e3a-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="16e3a-151">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="16e3a-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="16e3a-152">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="16e3a-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="16e3a-153">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="16e3a-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="16e3a-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="16e3a-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="16e3a-155">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="16e3a-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="16e3a-156">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="16e3a-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="16e3a-157">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="16e3a-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="16e3a-158">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="16e3a-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="16e3a-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="16e3a-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="16e3a-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="16e3a-160">RELATED LINKS</span></span>

