---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodataconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDataConnection.md
ms.openlocfilehash: e1fee17e7f7bf58785c96c28bc6e1f3f66136bb6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505124"
---
# <span data-ttu-id="4bb5d-101">Get-AzKustoDataConnection</span><span class="sxs-lookup"><span data-stu-id="4bb5d-101">Get-AzKustoDataConnection</span></span>

## <span data-ttu-id="4bb5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4bb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb5d-103">Возвращает подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-103">Returns a data connection.</span></span>

## <span data-ttu-id="4bb5d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4bb5d-104">SYNTAX</span></span>

### <span data-ttu-id="4bb5d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4bb5d-105">List (Default)</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4bb5d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4bb5d-106">Get</span></span>
```
Get-AzKustoDataConnection -ClusterName <String> -DatabaseName <String> -Name <String>
 -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4bb5d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4bb5d-107">GetViaIdentity</span></span>
```
Get-AzKustoDataConnection -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4bb5d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4bb5d-108">DESCRIPTION</span></span>
<span data-ttu-id="4bb5d-109">Возвращает подключение к данным.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-109">Returns a data connection.</span></span>

## <span data-ttu-id="4bb5d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4bb5d-110">EXAMPLES</span></span>

### <span data-ttu-id="4bb5d-111">Пример 1. Список всех подключений к данным в определенной базе данных</span><span class="sxs-lookup"><span data-stu-id="4bb5d-111">Example 1: List all data connections in a specific database</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4bb5d-112">Она возвращает все базы данных "Кусто" из кластера testnewkustocluster, которые находятся в группе ресурсов Testrg.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-112">The above command returns all Kusto databases in the cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

### <span data-ttu-id="4bb5d-113">Пример 2. Подключение к данным по имени</span><span class="sxs-lookup"><span data-stu-id="4bb5d-113">Example 2: Get a specific data connection by name</span></span>
```powershell
PS C:\> Get-AzKustoDataConnection -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -DatabaseName "mykustodatabase" -DataConnectionName "mykustodataconnection"

Kind     Location Name                                               Type
----     -------- ----                                               ----
EventHub East US  testnewkustocluster/mykustodatabase/mykustodataconnection Microsoft.Kusto/Clusters/Databases/DataConnections
```

<span data-ttu-id="4bb5d-114">Команда выше возвращает подключение к данным "mykustodataconnection" в базе данных "mykustodatabase" существующего кластера testnewkustocluster, найденное в группе ресурсов testrg.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-114">The above command returns the data connection named "mykustodataconnection" in database "mykustodatabase" of the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="4bb5d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4bb5d-115">PARAMETERS</span></span>

### <span data-ttu-id="4bb5d-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4bb5d-116">-ClusterName</span></span>
<span data-ttu-id="4bb5d-117">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4bb5d-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4bb5d-118">-DatabaseName</span></span>
<span data-ttu-id="4bb5d-119">Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-119">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="4bb5d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb5d-120">-DefaultProfile</span></span>
<span data-ttu-id="4bb5d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4bb5d-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4bb5d-122">-InputObject</span></span>
<span data-ttu-id="4bb5d-123">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4bb5d-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4bb5d-124">-Name</span></span>
<span data-ttu-id="4bb5d-125">Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-125">The name of the data connection.</span></span>

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

### <span data-ttu-id="4bb5d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4bb5d-126">-ResourceGroupName</span></span>
<span data-ttu-id="4bb5d-127">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4bb5d-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4bb5d-128">-SubscriptionId</span></span>
<span data-ttu-id="4bb5d-129">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-129">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4bb5d-130">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4bb5d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb5d-131">CommonParameters</span></span>
<span data-ttu-id="4bb5d-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb5d-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4bb5d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb5d-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb5d-134">INPUTS</span></span>

### <span data-ttu-id="4bb5d-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="4bb5d-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="4bb5d-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4bb5d-136">OUTPUTS</span></span>

### <span data-ttu-id="4bb5d-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span><span class="sxs-lookup"><span data-stu-id="4bb5d-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDataConnection</span></span>

## <span data-ttu-id="4bb5d-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4bb5d-138">NOTES</span></span>

<span data-ttu-id="4bb5d-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4bb5d-139">ALIASES</span></span>

<span data-ttu-id="4bb5d-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4bb5d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4bb5d-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4bb5d-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4bb5d-143">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4bb5d-143">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4bb5d-144">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-144">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="4bb5d-145">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="4bb5d-145">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="4bb5d-146">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-146">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="4bb5d-147">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-147">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="4bb5d-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4bb5d-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4bb5d-149">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-149">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="4bb5d-150">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="4bb5d-150">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="4bb5d-151">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-151">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="4bb5d-152">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-152">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4bb5d-153">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="4bb5d-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4bb5d-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4bb5d-154">RELATED LINKS</span></span>

