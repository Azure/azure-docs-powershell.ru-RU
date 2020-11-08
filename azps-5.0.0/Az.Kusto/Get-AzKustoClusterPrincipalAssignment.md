---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 0a6643a4909bb2125e419e28fe3d7a8494760d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249017"
---
# <span data-ttu-id="77d56-101">Get-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="77d56-101">Get-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="77d56-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="77d56-102">SYNOPSIS</span></span>
<span data-ttu-id="77d56-103">Возвращает principalAssignment кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-103">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="77d56-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="77d56-104">SYNTAX</span></span>

### <span data-ttu-id="77d56-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="77d56-105">List (Default)</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77d56-106">Получить</span><span class="sxs-lookup"><span data-stu-id="77d56-106">Get</span></span>
```
Get-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="77d56-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="77d56-107">GetViaIdentity</span></span>
```
Get-AzKustoClusterPrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="77d56-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d56-108">DESCRIPTION</span></span>
<span data-ttu-id="77d56-109">Возвращает principalAssignment кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-109">Gets a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="77d56-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="77d56-110">EXAMPLES</span></span>

### <span data-ttu-id="77d56-111">Пример 1: список всех Kusto кластера principalAssignment</span><span class="sxs-lookup"><span data-stu-id="77d56-111">Example 1: List all Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="77d56-112">В приведенной выше команде перечислены все principalAssignment в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="77d56-112">The above command lists all principalAssignment in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="77d56-113">Пример 2: получение Kusto кластера principalAssignment по имени</span><span class="sxs-lookup"><span data-stu-id="77d56-113">Example 2: Gets a Kusto cluster principalAssignment by name</span></span>
```powershell
PS C:\> Get-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="77d56-114">Указанная выше команда возвращает кластер Kusto principalAssignment с именем "kustoprincipal1" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="77d56-114">The above command returns the Kusto cluster principalAssignment named "kustoprincipal1" in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="77d56-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="77d56-115">PARAMETERS</span></span>

### <span data-ttu-id="77d56-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="77d56-116">-ClusterName</span></span>
<span data-ttu-id="77d56-117">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="77d56-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d56-118">-DefaultProfile</span></span>
<span data-ttu-id="77d56-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="77d56-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77d56-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77d56-120">-InputObject</span></span>
<span data-ttu-id="77d56-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="77d56-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="77d56-122">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="77d56-122">-PrincipalAssignmentName</span></span>
<span data-ttu-id="77d56-123">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="77d56-123">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="77d56-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d56-124">-ResourceGroupName</span></span>
<span data-ttu-id="77d56-125">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="77d56-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="77d56-126">-SubscriptionId</span></span>
<span data-ttu-id="77d56-127">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77d56-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="77d56-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="77d56-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="77d56-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d56-129">CommonParameters</span></span>
<span data-ttu-id="77d56-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="77d56-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d56-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77d56-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d56-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="77d56-132">INPUTS</span></span>

### <span data-ttu-id="77d56-133">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="77d56-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="77d56-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="77d56-134">OUTPUTS</span></span>

### <span data-ttu-id="77d56-135">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="77d56-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="77d56-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="77d56-136">NOTES</span></span>

<span data-ttu-id="77d56-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="77d56-137">ALIASES</span></span>

<span data-ttu-id="77d56-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="77d56-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="77d56-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="77d56-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="77d56-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="77d56-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="77d56-141">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="77d56-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="77d56-142">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="77d56-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="77d56-143">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="77d56-144">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="77d56-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="77d56-145">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="77d56-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="77d56-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="77d56-147">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="77d56-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="77d56-148">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="77d56-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="77d56-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="77d56-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="77d56-150">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="77d56-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="77d56-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="77d56-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="77d56-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="77d56-152">RELATED LINKS</span></span>

