---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b1a042eb96c1fa6acbcc22fbdd33aefd9d4d46b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219361"
---
# <span data-ttu-id="340c4-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="340c4-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="340c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="340c4-102">SYNOPSIS</span></span>
<span data-ttu-id="340c4-103">Возвращает конфигурацию вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="340c4-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="340c4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="340c4-104">SYNTAX</span></span>

### <span data-ttu-id="340c4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="340c4-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="340c4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="340c4-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="340c4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="340c4-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="340c4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="340c4-108">DESCRIPTION</span></span>
<span data-ttu-id="340c4-109">Возвращает конфигурацию вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="340c4-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="340c4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="340c4-110">EXAMPLES</span></span>

### <span data-ttu-id="340c4-111">Пример 1. Перечислите все вложенные базы данныхConfigurations в кластере</span><span class="sxs-lookup"><span data-stu-id="340c4-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="340c4-112">В командной группе выше перечислены все команды AttachedDatabaseConfigurations из кластера testnewkustoclusterf.</span><span class="sxs-lookup"><span data-stu-id="340c4-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="340c4-113">Пример 2. Получить определенную функцию AttachedDatabaseConfiguration в кластере</span><span class="sxs-lookup"><span data-stu-id="340c4-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="340c4-114">Она возвращает команду AttachedDatabaseConfigurations myfollowerconfiguration в кластере testnewkustoclusterf.</span><span class="sxs-lookup"><span data-stu-id="340c4-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="340c4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="340c4-115">PARAMETERS</span></span>

### <span data-ttu-id="340c4-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="340c4-116">-ClusterName</span></span>
<span data-ttu-id="340c4-117">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="340c4-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="340c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="340c4-118">-DefaultProfile</span></span>
<span data-ttu-id="340c4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="340c4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="340c4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="340c4-120">-InputObject</span></span>
<span data-ttu-id="340c4-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="340c4-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="340c4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="340c4-122">-Name</span></span>
<span data-ttu-id="340c4-123">Имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="340c4-123">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="340c4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="340c4-124">-ResourceGroupName</span></span>
<span data-ttu-id="340c4-125">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="340c4-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="340c4-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="340c4-126">-SubscriptionId</span></span>
<span data-ttu-id="340c4-127">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="340c4-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="340c4-128">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="340c4-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="340c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="340c4-129">CommonParameters</span></span>
<span data-ttu-id="340c4-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="340c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="340c4-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="340c4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="340c4-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="340c4-132">INPUTS</span></span>

### <span data-ttu-id="340c4-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="340c4-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="340c4-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="340c4-134">OUTPUTS</span></span>

### <span data-ttu-id="340c4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="340c4-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="340c4-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="340c4-136">NOTES</span></span>

<span data-ttu-id="340c4-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="340c4-137">ALIASES</span></span>

<span data-ttu-id="340c4-138">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="340c4-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="340c4-139">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="340c4-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="340c4-140">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="340c4-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="340c4-141">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="340c4-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="340c4-142">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="340c4-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="340c4-143">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="340c4-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="340c4-144">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="340c4-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="340c4-145">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="340c4-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="340c4-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="340c4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="340c4-147">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="340c4-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="340c4-148">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="340c4-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="340c4-149">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="340c4-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="340c4-150">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="340c4-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="340c4-151">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="340c4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="340c4-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="340c4-152">RELATED LINKS</span></span>

