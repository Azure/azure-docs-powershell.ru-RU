---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: a39578ffb7a0f3a5ecc6abc873f659b5d170aff5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219305"
---
# <span data-ttu-id="679c9-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="679c9-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="679c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="679c9-102">SYNOPSIS</span></span>
<span data-ttu-id="679c9-103">Возвращает базу данных.</span><span class="sxs-lookup"><span data-stu-id="679c9-103">Returns a database.</span></span>

## <span data-ttu-id="679c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="679c9-104">SYNTAX</span></span>

### <span data-ttu-id="679c9-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="679c9-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="679c9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="679c9-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="679c9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="679c9-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="679c9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="679c9-108">DESCRIPTION</span></span>
<span data-ttu-id="679c9-109">Возвращает базу данных.</span><span class="sxs-lookup"><span data-stu-id="679c9-109">Returns a database.</span></span>

## <span data-ttu-id="679c9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="679c9-110">EXAMPLES</span></span>

### <span data-ttu-id="679c9-111">Пример 1. Список всех баз данных "Кузто" в кластере по имени</span><span class="sxs-lookup"><span data-stu-id="679c9-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="679c9-112">Она возвращает все базы данных "Кузто" из кластера testnewkustocluster, которые находятся в группе ресурсов testrg.</span><span class="sxs-lookup"><span data-stu-id="679c9-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="679c9-113">Пример 2. Получить конкретную базу данных "Кузто" по имени</span><span class="sxs-lookup"><span data-stu-id="679c9-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="679c9-114">Она возвращает базу данных "Кузто" с именем "mykustodatabase" в кластере "testnewkustocluster", которая находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="679c9-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="679c9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="679c9-115">PARAMETERS</span></span>

### <span data-ttu-id="679c9-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="679c9-116">-ClusterName</span></span>
<span data-ttu-id="679c9-117">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="679c9-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="679c9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="679c9-118">-DefaultProfile</span></span>
<span data-ttu-id="679c9-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="679c9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="679c9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="679c9-120">-InputObject</span></span>
<span data-ttu-id="679c9-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="679c9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="679c9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="679c9-122">-Name</span></span>
<span data-ttu-id="679c9-123">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="679c9-123">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="679c9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="679c9-124">-ResourceGroupName</span></span>
<span data-ttu-id="679c9-125">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="679c9-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="679c9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="679c9-126">-SubscriptionId</span></span>
<span data-ttu-id="679c9-127">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="679c9-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="679c9-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="679c9-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="679c9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="679c9-129">CommonParameters</span></span>
<span data-ttu-id="679c9-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="679c9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="679c9-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="679c9-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="679c9-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="679c9-132">INPUTS</span></span>

### <span data-ttu-id="679c9-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="679c9-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="679c9-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="679c9-134">OUTPUTS</span></span>

### <span data-ttu-id="679c9-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="679c9-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="679c9-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="679c9-136">NOTES</span></span>

<span data-ttu-id="679c9-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="679c9-137">ALIASES</span></span>

<span data-ttu-id="679c9-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="679c9-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="679c9-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="679c9-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="679c9-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="679c9-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="679c9-141">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="679c9-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="679c9-142">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="679c9-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="679c9-143">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="679c9-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="679c9-144">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="679c9-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="679c9-145">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="679c9-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="679c9-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="679c9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="679c9-147">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="679c9-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="679c9-148">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="679c9-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="679c9-149">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="679c9-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="679c9-150">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="679c9-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="679c9-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="679c9-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="679c9-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="679c9-152">RELATED LINKS</span></span>

