---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 9ff5021e43b9d23fc79ffca81519809ae0052558
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505131"
---
# <span data-ttu-id="46941-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="46941-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="46941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46941-102">SYNOPSIS</span></span>
<span data-ttu-id="46941-103">Получает principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="46941-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="46941-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46941-104">SYNTAX</span></span>

### <span data-ttu-id="46941-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="46941-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46941-106">Получить</span><span class="sxs-lookup"><span data-stu-id="46941-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="46941-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="46941-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="46941-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46941-108">DESCRIPTION</span></span>
<span data-ttu-id="46941-109">Получает principalAssignment кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="46941-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="46941-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46941-110">EXAMPLES</span></span>

### <span data-ttu-id="46941-111">Пример 1. List all Kusto cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="46941-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="46941-112">В этой команде перечислены все principalAssignment в кластере testnewkustocluster.</span><span class="sxs-lookup"><span data-stu-id="46941-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="46941-113">Пример 2. Получает principalAssignment "Кусто" по имени</span><span class="sxs-lookup"><span data-stu-id="46941-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="46941-114">Вышеупомяненная команда возвращает кластер Кусто principalAssignment "kustoprincipal1" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="46941-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="46941-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46941-115">PARAMETERS</span></span>

### <span data-ttu-id="46941-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="46941-116">-ClusterName</span></span>
<span data-ttu-id="46941-117">Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="46941-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="46941-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46941-118">-DefaultProfile</span></span>
<span data-ttu-id="46941-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46941-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46941-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46941-120">-InputObject</span></span>
<span data-ttu-id="46941-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="46941-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="46941-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="46941-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="46941-123">Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="46941-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="46941-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46941-124">-ResourceGroupName</span></span>
<span data-ttu-id="46941-125">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="46941-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="46941-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46941-126">-SubscriptionId</span></span>
<span data-ttu-id="46941-127">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46941-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="46941-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="46941-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="46941-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46941-129">CommonParameters</span></span>
<span data-ttu-id="46941-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46941-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46941-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46941-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46941-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46941-132">INPUTS</span></span>

### <span data-ttu-id="46941-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="46941-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="46941-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46941-134">OUTPUTS</span></span>

### <span data-ttu-id="46941-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="46941-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="46941-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46941-136">NOTES</span></span>

<span data-ttu-id="46941-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="46941-137">ALIASES</span></span>

<span data-ttu-id="46941-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="46941-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="46941-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="46941-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="46941-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="46941-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="46941-141">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="46941-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="46941-142">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="46941-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="46941-143">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="46941-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="46941-144">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="46941-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="46941-145">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="46941-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="46941-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="46941-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="46941-147">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="46941-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="46941-148">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="46941-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="46941-149">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="46941-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="46941-150">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="46941-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="46941-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="46941-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="46941-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46941-152">RELATED LINKS</span></span>

