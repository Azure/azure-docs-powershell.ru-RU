---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 533e247ed2a0b9682e2fe87699d0a77b51ed06ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219284"
---
# <span data-ttu-id="35a96-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="35a96-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="35a96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35a96-102">SYNOPSIS</span></span>
<span data-ttu-id="35a96-103">Получает principalAssignment базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="35a96-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="35a96-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="35a96-104">SYNTAX</span></span>

### <span data-ttu-id="35a96-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35a96-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35a96-106">Получить</span><span class="sxs-lookup"><span data-stu-id="35a96-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35a96-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35a96-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="35a96-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35a96-108">DESCRIPTION</span></span>
<span data-ttu-id="35a96-109">Получает principalAssignment базы данных "Кузто".</span><span class="sxs-lookup"><span data-stu-id="35a96-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="35a96-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="35a96-110">EXAMPLES</span></span>

### <span data-ttu-id="35a96-111">Пример 1. Список всех principalAssignment в базе данных по имени</span><span class="sxs-lookup"><span data-stu-id="35a96-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="35a96-112">Команда выше возвращает все principalAssignment в базе данных "mykustodatabase", найденную в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="35a96-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="35a96-113">Пример 2. Получить определенное имя PrincipalAssignment в базе данных</span><span class="sxs-lookup"><span data-stu-id="35a96-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="35a96-114">Команда выше возвращает все PrincipalAssignment с именем "kustoprincipal1" в базе данных "mykustodatabase", найденной в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="35a96-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="35a96-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35a96-115">PARAMETERS</span></span>

### <span data-ttu-id="35a96-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="35a96-116">-ClusterName</span></span>
<span data-ttu-id="35a96-117">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="35a96-117">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="35a96-118">-DatabaseName</span></span>
<span data-ttu-id="35a96-119">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="35a96-119">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35a96-120">-DefaultProfile</span></span>
<span data-ttu-id="35a96-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35a96-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35a96-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35a96-122">-InputObject</span></span>
<span data-ttu-id="35a96-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="35a96-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="35a96-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="35a96-125">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="35a96-125">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35a96-126">-ResourceGroupName</span></span>
<span data-ttu-id="35a96-127">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="35a96-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35a96-128">-SubscriptionId</span></span>
<span data-ttu-id="35a96-129">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a96-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="35a96-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="35a96-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35a96-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35a96-131">CommonParameters</span></span>
<span data-ttu-id="35a96-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35a96-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35a96-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35a96-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35a96-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="35a96-134">INPUTS</span></span>

### <span data-ttu-id="35a96-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="35a96-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="35a96-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="35a96-136">OUTPUTS</span></span>

### <span data-ttu-id="35a96-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="35a96-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="35a96-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="35a96-138">NOTES</span></span>

<span data-ttu-id="35a96-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="35a96-139">ALIASES</span></span>

<span data-ttu-id="35a96-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="35a96-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35a96-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="35a96-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35a96-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35a96-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35a96-143">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="35a96-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35a96-144">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="35a96-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="35a96-145">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="35a96-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="35a96-146">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="35a96-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="35a96-147">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="35a96-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="35a96-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="35a96-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35a96-149">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="35a96-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="35a96-150">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="35a96-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="35a96-151">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="35a96-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="35a96-152">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="35a96-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="35a96-153">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="35a96-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="35a96-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35a96-154">RELATED LINKS</span></span>

