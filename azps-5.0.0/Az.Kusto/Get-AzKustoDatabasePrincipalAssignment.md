---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 4becbb8285685c923fe6b0ec2174e7e84824a106
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249009"
---
# <span data-ttu-id="0a0e8-101">Get-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0a0e8-101">Get-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0a0e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a0e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0a0e8-103">Возвращает principalAssignment базу данных Kusto Cluster.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-103">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0a0e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a0e8-104">SYNTAX</span></span>

### <span data-ttu-id="0a0e8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a0e8-105">List (Default)</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a0e8-106">Получить</span><span class="sxs-lookup"><span data-stu-id="0a0e8-106">Get</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0a0e8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a0e8-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabasePrincipalAssignment -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a0e8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-108">DESCRIPTION</span></span>
<span data-ttu-id="0a0e8-109">Возвращает principalAssignment базу данных Kusto Cluster.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-109">Gets a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="0a0e8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-110">EXAMPLES</span></span>

### <span data-ttu-id="0a0e8-111">Пример 1: список всех PrincipalAssignment в базе данных по имени</span><span class="sxs-lookup"><span data-stu-id="0a0e8-111">Example 1: List all PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

Name                                                                     Type
----                                                                     ----
testnewkustocluster/mykustodatabase/kustoprincipal1                      Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
testnewkustocluster/mykustodatabase/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="0a0e8-112">Вышеприведенная команда возвращает все все PrincipalAssignment в базе данных "mykustodatabase", обнаруженной в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0a0e8-112">The above command returns all all PrincipalAssignment in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="0a0e8-113">Пример 2: получение определенного имени PrincipalAssignment в базе данных</span><span class="sxs-lookup"><span data-stu-id="0a0e8-113">Example 2: Get a specific PrincipalAssignment in a database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="0a0e8-114">Вышеприведенная команда возвращает все все PrincipalAssignment с именем "kustoprincipal1" в базе данных "mykustodatabase", обнаруженной в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="0a0e8-114">The above command returns all all PrincipalAssignment named "kustoprincipal1" in the database "mykustodatabase" found in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="0a0e8-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-115">PARAMETERS</span></span>

### <span data-ttu-id="0a0e8-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="0a0e8-116">-ClusterName</span></span>
<span data-ttu-id="0a0e8-117">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="0a0e8-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a0e8-118">-DatabaseName</span></span>
<span data-ttu-id="0a0e8-119">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="0a0e8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a0e8-120">-DefaultProfile</span></span>
<span data-ttu-id="0a0e8-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a0e8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a0e8-122">-InputObject</span></span>
<span data-ttu-id="0a0e8-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a0e8-124">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="0a0e8-124">-PrincipalAssignmentName</span></span>
<span data-ttu-id="0a0e8-125">Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-125">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="0a0e8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a0e8-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a0e8-127">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="0a0e8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a0e8-128">-SubscriptionId</span></span>
<span data-ttu-id="0a0e8-129">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a0e8-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a0e8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a0e8-131">CommonParameters</span></span>
<span data-ttu-id="0a0e8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a0e8-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a0e8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a0e8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a0e8-134">INPUTS</span></span>

### <span data-ttu-id="0a0e8-135">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="0a0e8-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="0a0e8-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-136">OUTPUTS</span></span>

### <span data-ttu-id="0a0e8-137">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="0a0e8-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="0a0e8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a0e8-138">NOTES</span></span>

<span data-ttu-id="0a0e8-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-139">ALIASES</span></span>

<span data-ttu-id="0a0e8-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0a0e8-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a0e8-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0a0e8-143">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0a0e8-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a0e8-144">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="0a0e8-145">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="0a0e8-146">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="0a0e8-147">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="0a0e8-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0a0e8-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a0e8-149">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="0a0e8-150">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="0a0e8-151">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="0a0e8-152">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0a0e8-153">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="0a0e8-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0a0e8-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a0e8-154">RELATED LINKS</span></span>

