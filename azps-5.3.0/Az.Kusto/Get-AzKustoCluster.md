---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: 99afad24d33cfd6a614100b5bc53406f04965ba9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518554"
---
# <span data-ttu-id="a529e-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="a529e-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="a529e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a529e-102">SYNOPSIS</span></span>
<span data-ttu-id="a529e-103">Получает кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="a529e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a529e-104">SYNTAX</span></span>

### <span data-ttu-id="a529e-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a529e-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a529e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="a529e-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a529e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a529e-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a529e-108">Список</span><span class="sxs-lookup"><span data-stu-id="a529e-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a529e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a529e-109">DESCRIPTION</span></span>
<span data-ttu-id="a529e-110">Получает кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="a529e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a529e-111">EXAMPLES</span></span>

### <span data-ttu-id="a529e-112">Пример 1. Список всех кластеров кусто в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="a529e-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="a529e-113">В этой команде перечислены все кластеры Кусто в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="a529e-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="a529e-114">Пример 2. Получить конкретный кластер кусто по имени</span><span class="sxs-lookup"><span data-stu-id="a529e-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="a529e-115">Она возвращает кластер "Кузто" с именем "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="a529e-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="a529e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a529e-116">PARAMETERS</span></span>

### <span data-ttu-id="a529e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a529e-117">-DefaultProfile</span></span>
<span data-ttu-id="a529e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a529e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a529e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a529e-119">-InputObject</span></span>
<span data-ttu-id="a529e-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="a529e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a529e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="a529e-121">-Name</span></span>
<span data-ttu-id="a529e-122">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-122">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a529e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a529e-123">-ResourceGroupName</span></span>
<span data-ttu-id="a529e-124">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a529e-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a529e-125">-SubscriptionId</span></span>
<span data-ttu-id="a529e-126">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a529e-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a529e-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a529e-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a529e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a529e-128">CommonParameters</span></span>
<span data-ttu-id="a529e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a529e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a529e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a529e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a529e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a529e-131">INPUTS</span></span>

### <span data-ttu-id="a529e-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="a529e-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="a529e-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a529e-133">OUTPUTS</span></span>

### <span data-ttu-id="a529e-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span><span class="sxs-lookup"><span data-stu-id="a529e-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICluster</span></span>

## <span data-ttu-id="a529e-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a529e-135">NOTES</span></span>

<span data-ttu-id="a529e-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="a529e-136">ALIASES</span></span>

<span data-ttu-id="a529e-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="a529e-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a529e-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="a529e-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a529e-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a529e-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a529e-140">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="a529e-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a529e-141">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="a529e-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="a529e-142">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="a529e-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="a529e-143">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="a529e-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="a529e-144">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="a529e-145">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="a529e-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a529e-146">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="a529e-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="a529e-147">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="a529e-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="a529e-148">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="a529e-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="a529e-149">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a529e-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a529e-150">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="a529e-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a529e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a529e-151">RELATED LINKS</span></span>

