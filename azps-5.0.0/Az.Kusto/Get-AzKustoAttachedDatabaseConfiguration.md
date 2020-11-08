---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: fd735b1d343c046f9ca2f0528bff4bf7ce8a403d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249025"
---
# <span data-ttu-id="97220-101">Get-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="97220-101">Get-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="97220-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97220-102">SYNOPSIS</span></span>
<span data-ttu-id="97220-103">Возвращает конфигурацию присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="97220-103">Returns an attached database configuration.</span></span>

## <span data-ttu-id="97220-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97220-104">SYNTAX</span></span>

### <span data-ttu-id="97220-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="97220-105">List (Default)</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97220-106">Получить</span><span class="sxs-lookup"><span data-stu-id="97220-106">Get</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="97220-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="97220-107">GetViaIdentity</span></span>
```
Get-AzKustoAttachedDatabaseConfiguration -InputObject <IKustoIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="97220-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97220-108">DESCRIPTION</span></span>
<span data-ttu-id="97220-109">Возвращает конфигурацию присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="97220-109">Returns an attached database configuration.</span></span>

## <span data-ttu-id="97220-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97220-110">EXAMPLES</span></span>

### <span data-ttu-id="97220-111">Пример 1: список всех AttachedDatabaseConfigurations в кластере</span><span class="sxs-lookup"><span data-stu-id="97220-111">Example 1: List all the AttachedDatabaseConfigurations in a cluster</span></span>
```powershell
PS C:\> Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="97220-112">В приведенной выше команде перечислены все AttachedDatabaseConfigurations в кластере "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="97220-112">The above command lists all the AttachedDatabaseConfigurations in the cluster "testnewkustoclusterf".</span></span>

### <span data-ttu-id="97220-113">Пример 2: получение определенного AttachedDatabaseConfiguration в кластере</span><span class="sxs-lookup"><span data-stu-id="97220-113">Example 2: Get a specific AttachedDatabaseConfiguration in a cluster</span></span>
```powershell
PS C:\>  Get-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" 

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="97220-114">Приведенная выше команда возвращает AttachedDatabaseConfigurations с именем "myfollowerconfiguration" в кластере "testnewkustoclusterf".</span><span class="sxs-lookup"><span data-stu-id="97220-114">The above command returns the AttachedDatabaseConfigurations named "myfollowerconfiguration" in the cluster "testnewkustoclusterf".</span></span>

## <span data-ttu-id="97220-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97220-115">PARAMETERS</span></span>

### <span data-ttu-id="97220-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="97220-116">-ClusterName</span></span>
<span data-ttu-id="97220-117">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="97220-117">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="97220-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97220-118">-DefaultProfile</span></span>
<span data-ttu-id="97220-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97220-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97220-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="97220-120">-InputObject</span></span>
<span data-ttu-id="97220-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="97220-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="97220-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97220-122">-Name</span></span>
<span data-ttu-id="97220-123">Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="97220-123">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="97220-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97220-124">-ResourceGroupName</span></span>
<span data-ttu-id="97220-125">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="97220-125">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="97220-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97220-126">-SubscriptionId</span></span>
<span data-ttu-id="97220-127">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97220-127">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="97220-128">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="97220-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="97220-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97220-129">CommonParameters</span></span>
<span data-ttu-id="97220-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97220-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97220-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97220-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97220-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97220-132">INPUTS</span></span>

### <span data-ttu-id="97220-133">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="97220-133">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="97220-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97220-134">OUTPUTS</span></span>

### <span data-ttu-id="97220-135">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="97220-135">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="97220-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="97220-136">NOTES</span></span>

<span data-ttu-id="97220-137">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="97220-137">ALIASES</span></span>

<span data-ttu-id="97220-138">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="97220-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="97220-139">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97220-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="97220-140">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="97220-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="97220-141">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="97220-141">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="97220-142">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="97220-142">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="97220-143">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="97220-143">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="97220-144">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="97220-144">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="97220-145">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="97220-145">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="97220-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="97220-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="97220-147">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="97220-147">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="97220-148">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="97220-148">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="97220-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="97220-149">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="97220-150">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="97220-150">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="97220-151">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="97220-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="97220-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97220-152">RELATED LINKS</span></span>

