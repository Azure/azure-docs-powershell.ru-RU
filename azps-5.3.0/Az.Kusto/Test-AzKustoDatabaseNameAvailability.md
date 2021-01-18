---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustodatabasenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoDatabaseNameAvailability.md
ms.openlocfilehash: 01f22e069e1e5d664ceac5c6cef7698cf9ffa980
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508269"
---
# <span data-ttu-id="0aee5-101">Test-AzKustoDatabaseNameAvailability</span><span class="sxs-lookup"><span data-stu-id="0aee5-101">Test-AzKustoDatabaseNameAvailability</span></span>

## <span data-ttu-id="0aee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0aee5-102">SYNOPSIS</span></span>
<span data-ttu-id="0aee5-103">Проверяет, является ли имя базы данных допустимой и не используется.</span><span class="sxs-lookup"><span data-stu-id="0aee5-103">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="0aee5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0aee5-104">SYNTAX</span></span>

### <span data-ttu-id="0aee5-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0aee5-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoDatabaseNameAvailability -ClusterName <String> -ResourceGroupName <String> -Name <String>
 -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0aee5-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0aee5-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoDatabaseNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0aee5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aee5-107">DESCRIPTION</span></span>
<span data-ttu-id="0aee5-108">Проверяет, является ли имя базы данных допустимой и не используется.</span><span class="sxs-lookup"><span data-stu-id="0aee5-108">Checks that the database name is valid and is not already in use.</span></span>

## <span data-ttu-id="0aee5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0aee5-109">EXAMPLES</span></span>

### <span data-ttu-id="0aee5-110">Пример 1. Проверка доступности имени базы данных "Кузто", которая используется</span><span class="sxs-lookup"><span data-stu-id="0aee5-110">Example 1: Check the availability of a Kusto database name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Type Microsoft.Kusto/Clusters/Databases

Message                                                                                                          Name            NameAvailable Reason
-------                                                                                                          ----            ------------- ------
Database mykustodatabase already exists in cluster testnewkustocluster. Please select a different database name. mykustodatabase False
```

<span data-ttu-id="0aee5-111">Она возвращает, существует ли база данных кусто с именем "mykustodatabase" в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="0aee5-111">The above command returns whether or not a Kusto database named "mykustodatabase" exists in the "testnewkustocluster" cluster.</span></span>

### <span data-ttu-id="0aee5-112">Пример 2. Проверка доступности имени базы данных "Кузто", которая не используется</span><span class="sxs-lookup"><span data-stu-id="0aee5-112">Example 2: Check the availability of a Kusto database name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoDatabaseNameAvailability -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase2 -Type Microsoft.Kusto/Clusters/Databases

Message Name             NameAvailable Reason
------- ----             ------------- ------
        mykustodatabase2 True
```

<span data-ttu-id="0aee5-113">Она возвращает, существует ли база данных Кусто с именем "mykustodatabase2" в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="0aee5-113">The above command returns whether or not a Kusto database named "mykustodatabase2" exists in the "testnewkustocluster" cluster.</span></span>

## <span data-ttu-id="0aee5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0aee5-114">PARAMETERS</span></span>

### <span data-ttu-id="0aee5-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="0aee5-115">-ClusterName</span></span>
<span data-ttu-id="0aee5-116">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="0aee5-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0aee5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aee5-117">-DefaultProfile</span></span>
<span data-ttu-id="0aee5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0aee5-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aee5-119">-InputObject</span></span>
<span data-ttu-id="0aee5-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0aee5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0aee5-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0aee5-121">-Name</span></span>
<span data-ttu-id="0aee5-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="0aee5-122">Resource name.</span></span>

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

### <span data-ttu-id="0aee5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0aee5-123">-ResourceGroupName</span></span>
<span data-ttu-id="0aee5-124">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="0aee5-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0aee5-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0aee5-125">-SubscriptionId</span></span>
<span data-ttu-id="0aee5-126">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee5-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0aee5-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0aee5-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0aee5-128">-Type</span><span class="sxs-lookup"><span data-stu-id="0aee5-128">-Type</span></span>
<span data-ttu-id="0aee5-129">Тип ресурса, например Microsoft.Kusto/Clusters/databases.</span><span class="sxs-lookup"><span data-stu-id="0aee5-129">The type of resource, for instance Microsoft.Kusto/Clusters/databases.</span></span>

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

### <span data-ttu-id="0aee5-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0aee5-130">-Confirm</span></span>
<span data-ttu-id="0aee5-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aee5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aee5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aee5-132">-WhatIf</span></span>
<span data-ttu-id="0aee5-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aee5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aee5-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0aee5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aee5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aee5-135">CommonParameters</span></span>
<span data-ttu-id="0aee5-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aee5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aee5-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0aee5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aee5-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0aee5-138">INPUTS</span></span>

### <span data-ttu-id="0aee5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0aee5-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0aee5-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0aee5-140">OUTPUTS</span></span>

### <span data-ttu-id="0aee5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="0aee5-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="0aee5-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0aee5-142">NOTES</span></span>

<span data-ttu-id="0aee5-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0aee5-143">ALIASES</span></span>

<span data-ttu-id="0aee5-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0aee5-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0aee5-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0aee5-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0aee5-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0aee5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0aee5-147">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0aee5-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0aee5-148">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0aee5-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0aee5-149">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="0aee5-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0aee5-150">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0aee5-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0aee5-151">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="0aee5-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0aee5-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0aee5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0aee5-153">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee5-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0aee5-154">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="0aee5-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0aee5-155">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="0aee5-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0aee5-156">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0aee5-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0aee5-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="0aee5-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0aee5-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aee5-158">RELATED LINKS</span></span>

