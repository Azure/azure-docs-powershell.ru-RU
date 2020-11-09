---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustocluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoCluster.md
ms.openlocfilehash: a95f8a00578ccf917a55cdfd9685dedf9a20734f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249022"
---
# <span data-ttu-id="d13ba-101">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="d13ba-101">Get-AzKustoCluster</span></span>

## <span data-ttu-id="d13ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d13ba-102">SYNOPSIS</span></span>
<span data-ttu-id="d13ba-103">Возвращает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-103">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="d13ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d13ba-104">SYNTAX</span></span>

### <span data-ttu-id="d13ba-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d13ba-105">List1 (Default)</span></span>
```
Get-AzKustoCluster [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d13ba-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d13ba-106">Get</span></span>
```
Get-AzKustoCluster -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d13ba-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d13ba-107">GetViaIdentity</span></span>
```
Get-AzKustoCluster -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d13ba-108">Список</span><span class="sxs-lookup"><span data-stu-id="d13ba-108">List</span></span>
```
Get-AzKustoCluster -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d13ba-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13ba-109">DESCRIPTION</span></span>
<span data-ttu-id="d13ba-110">Возвращает кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-110">Gets a Kusto cluster.</span></span>

## <span data-ttu-id="d13ba-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d13ba-111">EXAMPLES</span></span>

### <span data-ttu-id="d13ba-112">Пример 1: список всех кластеров Kusto в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="d13ba-112">Example 1: List all Kusto clusters in a resource group</span></span>
```powershell
PS C:\> Get-AzKustoCluster -ResourceGroupName testrg

Location Name                 Type                     Zone
-------- ----                 ----                     ----
East US  testnewkustocluster  Microsoft.Kusto/Clusters
East US  testnewkustocluster2 Microsoft.Kusto/Clusters
```

<span data-ttu-id="d13ba-113">В приведенной выше команде перечислены все кластеры Kusto в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="d13ba-113">The above command lists all Kusto clusters in the resource group "testrg".</span></span>

### <span data-ttu-id="d13ba-114">Пример 2: получение определенного имени Kusto кластера</span><span class="sxs-lookup"><span data-stu-id="d13ba-114">Example 2: Get a specific Kusto cluster by name</span></span>
```powershell
PS C:\>  Get-AzKustoCluster -ResourceGroupName testrg -Name testnewkustocluster

Location Name                Type                     Zone
-------- ----                ----                     ----
East US  testnewkustocluster Microsoft.Kusto/Clusters
```

<span data-ttu-id="d13ba-115">Приведенная выше команда возвращает кластер Kusto с именем "testnewkustocluster" в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="d13ba-115">The above command returns the Kusto cluster named "testnewkustocluster" in the resource group "testrg".</span></span>

## <span data-ttu-id="d13ba-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d13ba-116">PARAMETERS</span></span>

### <span data-ttu-id="d13ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d13ba-117">-DefaultProfile</span></span>
<span data-ttu-id="d13ba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d13ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d13ba-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d13ba-119">-InputObject</span></span>
<span data-ttu-id="d13ba-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="d13ba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d13ba-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d13ba-121">-Name</span></span>
<span data-ttu-id="d13ba-122">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-122">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d13ba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d13ba-123">-ResourceGroupName</span></span>
<span data-ttu-id="d13ba-124">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d13ba-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d13ba-125">-SubscriptionId</span></span>
<span data-ttu-id="d13ba-126">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d13ba-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d13ba-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d13ba-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d13ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d13ba-128">CommonParameters</span></span>
<span data-ttu-id="d13ba-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d13ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d13ba-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d13ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d13ba-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d13ba-131">INPUTS</span></span>

### <span data-ttu-id="d13ba-132">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="d13ba-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="d13ba-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d13ba-133">OUTPUTS</span></span>

### <span data-ttu-id="d13ba-134">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICluster</span><span class="sxs-lookup"><span data-stu-id="d13ba-134">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICluster</span></span>

## <span data-ttu-id="d13ba-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="d13ba-135">NOTES</span></span>

<span data-ttu-id="d13ba-136">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="d13ba-136">ALIASES</span></span>

<span data-ttu-id="d13ba-137">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d13ba-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d13ba-138">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d13ba-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d13ba-139">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d13ba-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d13ba-140">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="d13ba-140">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d13ba-141">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="d13ba-141">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="d13ba-142">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-142">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="d13ba-143">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="d13ba-143">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="d13ba-144">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-144">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="d13ba-145">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="d13ba-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d13ba-146">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="d13ba-146">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="d13ba-147">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d13ba-147">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="d13ba-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="d13ba-148">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="d13ba-149">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d13ba-149">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d13ba-150">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="d13ba-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d13ba-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d13ba-151">RELATED LINKS</span></span>
