---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabase.md
ms.openlocfilehash: cdcba65473974da6ba8d526247ca947daa97a55c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249013"
---
# <span data-ttu-id="15a29-101">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="15a29-101">Get-AzKustoDatabase</span></span>

## <span data-ttu-id="15a29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15a29-102">SYNOPSIS</span></span>
<span data-ttu-id="15a29-103">Возвращает базу данных.</span><span class="sxs-lookup"><span data-stu-id="15a29-103">Returns a database.</span></span>

## <span data-ttu-id="15a29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15a29-104">SYNTAX</span></span>

### <span data-ttu-id="15a29-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="15a29-105">List (Default)</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15a29-106">Получить</span><span class="sxs-lookup"><span data-stu-id="15a29-106">Get</span></span>
```
Get-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="15a29-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="15a29-107">GetViaIdentity</span></span>
```
Get-AzKustoDatabase -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="15a29-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a29-108">DESCRIPTION</span></span>
<span data-ttu-id="15a29-109">Возвращает базу данных.</span><span class="sxs-lookup"><span data-stu-id="15a29-109">Returns a database.</span></span>

## <span data-ttu-id="15a29-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15a29-110">EXAMPLES</span></span>

### <span data-ttu-id="15a29-111">Пример 1: список всех баз данных Kusto в кластере по имени</span><span class="sxs-lookup"><span data-stu-id="15a29-111">Example 1: List all Kusto databases in a cluster by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster

Kind      Location Name                                 Type
----      -------- ----                                 ----
ReadWrite East US  testnewkustocluster/mykustodatabase  Microsoft.Kusto/Clusters/Databases
ReadWrite East US  testnewkustocluster/mykustodatabase2 Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="15a29-112">Приведенная выше команда возвращает все базы данных Kusto в кластере "testnewkustocluster", обнаруженные в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="15a29-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="15a29-113">Пример 2: получение определенной базы данных Kusto по имени</span><span class="sxs-lookup"><span data-stu-id="15a29-113">Example 2: Get a specific Kusto database by name</span></span>
```powershell
PS C:\> Get-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="15a29-114">Вышеприведенная команда возвращает базу данных Kusto с именем "mykustodatabase" в кластере "testnewkustocluster", которая находится в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="15a29-114">The above command returns the Kusto database named "mykustodatabase" in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="15a29-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15a29-115">PARAMETERS</span></span>

### <span data-ttu-id="15a29-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="15a29-116">-ClusterName</span></span>
<span data-ttu-id="15a29-117">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="15a29-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a29-118">-DefaultProfile</span></span>
<span data-ttu-id="15a29-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15a29-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a29-120">-InputObject</span></span>
<span data-ttu-id="15a29-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="15a29-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="15a29-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15a29-122">-Name</span></span>
<span data-ttu-id="15a29-123">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-123">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="15a29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a29-124">-ResourceGroupName</span></span>
<span data-ttu-id="15a29-125">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="15a29-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15a29-126">-SubscriptionId</span></span>
<span data-ttu-id="15a29-127">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="15a29-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="15a29-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="15a29-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="15a29-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a29-129">CommonParameters</span></span>
<span data-ttu-id="15a29-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15a29-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a29-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15a29-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a29-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15a29-132">INPUTS</span></span>

### <span data-ttu-id="15a29-133">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="15a29-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="15a29-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a29-134">OUTPUTS</span></span>

### <span data-ttu-id="15a29-135">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDatabase</span><span class="sxs-lookup"><span data-stu-id="15a29-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabase</span></span>

## <span data-ttu-id="15a29-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="15a29-136">NOTES</span></span>

<span data-ttu-id="15a29-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="15a29-137">ALIASES</span></span>

<span data-ttu-id="15a29-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="15a29-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="15a29-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="15a29-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="15a29-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="15a29-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="15a29-141">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="15a29-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="15a29-142">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="15a29-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="15a29-143">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="15a29-144">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="15a29-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="15a29-145">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="15a29-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="15a29-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="15a29-147">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="15a29-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="15a29-148">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="15a29-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="15a29-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="15a29-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="15a29-150">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="15a29-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="15a29-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="15a29-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="15a29-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15a29-152">RELATED LINKS</span></span>

