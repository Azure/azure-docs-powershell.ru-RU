---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: 6cfc5cdae87512245a573ed5c7ff9c746036c815
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079967"
---
# <span data-ttu-id="9d925-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="9d925-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="9d925-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9d925-102">SYNOPSIS</span></span>
<span data-ttu-id="9d925-103">Возвращает подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="9d925-103">Returns a data connection.</span></span>

## <span data-ttu-id="9d925-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9d925-104">SYNTAX</span></span>

### <span data-ttu-id="9d925-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d925-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d925-106">Получить</span><span class="sxs-lookup"><span data-stu-id="9d925-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9d925-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d925-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9d925-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d925-108">DESCRIPTION</span></span>
<span data-ttu-id="9d925-109">Возвращает подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="9d925-109">Returns a data connection.</span></span>

## <span data-ttu-id="9d925-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9d925-110">EXAMPLES</span></span>

### <span data-ttu-id="9d925-111">Пример 1: список всех подключений к данным в определенной базе данных</span><span class="sxs-lookup"><span data-stu-id="9d925-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="9d925-112">Приведенная выше команда возвращает все базы данных Kusto в кластере "testnewkustocluster", обнаруженные в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="9d925-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="9d925-113">Пример 2: получение определенного имени для подключения к данным</span><span class="sxs-lookup"><span data-stu-id="9d925-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="9d925-114">Приведенная выше команда возвращает подключение к данным "mykustodataconnection" в базе данных "mykustodatabase" существующего кластера "testnewkustocluster", обнаруженного в группе ресурсов "testrg".</span><span class="sxs-lookup"><span data-stu-id="9d925-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="9d925-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9d925-115">PARAMETERS</span></span>

### <span data-ttu-id="9d925-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="9d925-116">-ClusterName</span></span>
<span data-ttu-id="9d925-117">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="9d925-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9d925-118">-DatabaseName</span></span>
<span data-ttu-id="9d925-119">Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="9d925-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d925-120">-DefaultProfile</span></span>
<span data-ttu-id="9d925-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d925-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d925-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d925-122">-InputObject</span></span>
<span data-ttu-id="9d925-123">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="9d925-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9d925-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9d925-124">-Name</span></span>
<span data-ttu-id="9d925-125">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="9d925-125">The name of the data connection.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DataConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d925-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d925-126">-ResourceGroupName</span></span>
<span data-ttu-id="9d925-127">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="9d925-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9d925-128">-SubscriptionId</span></span>
<span data-ttu-id="9d925-129">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d925-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d925-130">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9d925-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9d925-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d925-131">CommonParameters</span></span>
<span data-ttu-id="9d925-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9d925-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d925-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d925-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d925-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9d925-134">INPUTS</span></span>

### <span data-ttu-id="9d925-135">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="9d925-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="9d925-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d925-136">OUTPUTS</span></span>

### <span data-ttu-id="9d925-137">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IDataConnection</span><span class="sxs-lookup"><span data-stu-id="9d925-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDataConnection</span></span>

## <span data-ttu-id="9d925-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9d925-138">NOTES</span></span>

<span data-ttu-id="9d925-139">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9d925-139">ALIASES</span></span>

<span data-ttu-id="9d925-140">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9d925-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9d925-141">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9d925-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d925-142">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9d925-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9d925-143">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="9d925-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d925-144">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="9d925-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="9d925-145">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="9d925-146">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="9d925-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="9d925-147">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="9d925-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="9d925-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d925-149">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="9d925-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="9d925-150">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="9d925-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="9d925-151">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="9d925-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="9d925-152">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9d925-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9d925-153">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="9d925-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="9d925-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d925-154">RELATED LINKS</span></span>

