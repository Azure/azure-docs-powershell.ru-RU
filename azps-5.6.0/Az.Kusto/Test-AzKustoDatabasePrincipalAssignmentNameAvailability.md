---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/test-azkustodatabaseprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabasePrincipalAssignmentNameAvailability.md
ms.openlocfilehash: 6a151119552ab4b0e42d247641248dd110af4994
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972819"
---
# <span data-ttu-id="db5f5-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="db5f5-101">Test-AzKustoDatabasePrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="db5f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db5f5-102">SYNOPSIS</span></span>
<span data-ttu-id="db5f5-103">Проверяет, допустимо ли назначение основной базы данных и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="db5f5-103">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="db5f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="db5f5-104">SYNTAX</span></span>

### <span data-ttu-id="db5f5-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db5f5-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db5f5-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="db5f5-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabasePrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db5f5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db5f5-107">DESCRIPTION</span></span>
<span data-ttu-id="db5f5-108">Проверяет, допустимо ли назначение основной базы данных и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="db5f5-108">Checks that the database principal assignment is valid and is not already in use.</span></span>

## <span data-ttu-id="db5f5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="db5f5-109">EXAMPLES</span></span>

### <span data-ttu-id="db5f5-110">Пример 1. Проверка доступности имени основной структуры базы данных, которое используется</span><span class="sxs-lookup"><span data-stu-id="db5f5-110">Example 1: Check the availability of a database principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "myprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments" 

Message                                                                                                                                   Name            NameAvailable Reason
-------                                                                                                                                    ----            ------------- ------
Database principal assignment myprincipal already exists in database mykustodatabase. Please select a different principal assignment name. myprincipal   False
```

<span data-ttu-id="db5f5-111">Она возвращает, существует ли в базе данных "mykustodatabase" (mykustodatabase) режим PrincipalAssignment с именем Myprincipal из кластера testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="db5f5-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="db5f5-112">Пример 2. Проверка доступности имени основной структуры базы данных, которое не используется</span><span class="sxs-lookup"><span data-stu-id="db5f5-112">Example 2: Check the availability of a database principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -Name "newprincipal" -Type "Microsoft.Kusto/Clusters/Database/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="db5f5-113">Она возвращает, существует ли в базе данных "mykustodatabase" (mykustodatabase) имя PrincipalAssignment с именем Myprincipal из кластера testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="db5f5-113">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the database "mykustodatabase" from cluster "testnewkustocluster" .</span></span>

## <span data-ttu-id="db5f5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db5f5-114">PARAMETERS</span></span>

### <span data-ttu-id="db5f5-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="db5f5-115">-ClusterName</span></span>
<span data-ttu-id="db5f5-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="db5f5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="db5f5-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="db5f5-117">-DatabaseName</span></span>
<span data-ttu-id="db5f5-118">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="db5f5-118">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="db5f5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db5f5-119">-DefaultProfile</span></span>
<span data-ttu-id="db5f5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db5f5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db5f5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db5f5-121">-InputObject</span></span>
<span data-ttu-id="db5f5-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="db5f5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db5f5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="db5f5-123">-Name</span></span>
<span data-ttu-id="db5f5-124">Имя ресурса основного назначения.</span><span class="sxs-lookup"><span data-stu-id="db5f5-124">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="db5f5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db5f5-125">-ResourceGroupName</span></span>
<span data-ttu-id="db5f5-126">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="db5f5-126">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="db5f5-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db5f5-127">-SubscriptionId</span></span>
<span data-ttu-id="db5f5-128">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db5f5-128">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="db5f5-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="db5f5-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="db5f5-130">-Type</span><span class="sxs-lookup"><span data-stu-id="db5f5-130">-Type</span></span>
<span data-ttu-id="db5f5-131">Тип ресурса: Microsoft.Kusto/Clusters/Databases/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="db5f5-131">The type of resource, Microsoft.Kusto/Clusters/Databases/principalAssignments.</span></span>

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

### <span data-ttu-id="db5f5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db5f5-132">-Confirm</span></span>
<span data-ttu-id="db5f5-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db5f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db5f5-134">-WhatIf</span></span>
<span data-ttu-id="db5f5-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db5f5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db5f5-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="db5f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db5f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db5f5-137">CommonParameters</span></span>
<span data-ttu-id="db5f5-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db5f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db5f5-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="db5f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db5f5-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="db5f5-140">INPUTS</span></span>

### <span data-ttu-id="db5f5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="db5f5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="db5f5-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="db5f5-142">OUTPUTS</span></span>

### <span data-ttu-id="db5f5-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="db5f5-143">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="db5f5-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="db5f5-144">NOTES</span></span>

<span data-ttu-id="db5f5-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="db5f5-145">ALIASES</span></span>

<span data-ttu-id="db5f5-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="db5f5-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db5f5-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="db5f5-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db5f5-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db5f5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db5f5-149">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="db5f5-149">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db5f5-150">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="db5f5-150">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="db5f5-151">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="db5f5-151">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="db5f5-152">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="db5f5-152">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="db5f5-153">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="db5f5-153">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="db5f5-154">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="db5f5-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db5f5-155">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="db5f5-155">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="db5f5-156">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="db5f5-156">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="db5f5-157">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="db5f5-157">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="db5f5-158">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db5f5-158">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="db5f5-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="db5f5-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="db5f5-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db5f5-160">RELATED LINKS</span></span>

