---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250178"
---
# <span data-ttu-id="ede88-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="ede88-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="ede88-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ede88-102">SYNOPSIS</span></span>
<span data-ttu-id="ede88-103">Проверка того, что имя назначения участника является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="ede88-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ede88-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ede88-104">SYNTAX</span></span>

### <span data-ttu-id="ede88-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ede88-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ede88-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ede88-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ede88-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ede88-107">DESCRIPTION</span></span>
<span data-ttu-id="ede88-108">Проверка того, что имя назначения участника является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="ede88-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="ede88-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ede88-109">EXAMPLES</span></span>

### <span data-ttu-id="ede88-110">Пример 1: Проверка доступности имени кластера, используемого principalassignment</span><span class="sxs-lookup"><span data-stu-id="ede88-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="ede88-111">Указанная выше команда возвращает значение, указывающее, существует ли PrincipalAssignment с именем "MyPrincipal" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ede88-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="ede88-112">Пример 2: Проверка доступности неиспользуемого principalassignmentного имени кластера</span><span class="sxs-lookup"><span data-stu-id="ede88-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="ede88-113">Указанная выше команда возвращает значение, указывающее, существует ли PrincipalAssignment с именем "newprincipal" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="ede88-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="ede88-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ede88-114">PARAMETERS</span></span>

### <span data-ttu-id="ede88-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ede88-115">-ClusterName</span></span>
<span data-ttu-id="ede88-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ede88-116">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede88-117">-DefaultProfile</span></span>
<span data-ttu-id="ede88-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ede88-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ede88-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ede88-119">-InputObject</span></span>
<span data-ttu-id="ede88-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ede88-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity
Parameter Sets: CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ede88-121">-Name</span></span>
<span data-ttu-id="ede88-122">Имя ресурса назначения участника.</span><span class="sxs-lookup"><span data-stu-id="ede88-122">Principal Assignment resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede88-123">-ResourceGroupName</span></span>
<span data-ttu-id="ede88-124">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ede88-124">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ede88-125">-SubscriptionId</span></span>
<span data-ttu-id="ede88-126">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ede88-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ede88-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ede88-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="ede88-128">-Type</span></span>
<span data-ttu-id="ede88-129">Тип ресурсов, Microsoft. Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="ede88-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Type
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ede88-130">-Confirm</span></span>
<span data-ttu-id="ede88-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ede88-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede88-132">-WhatIf</span></span>
<span data-ttu-id="ede88-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ede88-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede88-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ede88-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede88-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede88-135">CommonParameters</span></span>
<span data-ttu-id="ede88-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ede88-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede88-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ede88-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede88-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ede88-138">INPUTS</span></span>

### <span data-ttu-id="ede88-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="ede88-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="ede88-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ede88-140">OUTPUTS</span></span>

### <span data-ttu-id="ede88-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="ede88-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="ede88-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="ede88-142">NOTES</span></span>

<span data-ttu-id="ede88-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ede88-143">ALIASES</span></span>

<span data-ttu-id="ede88-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ede88-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ede88-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ede88-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ede88-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ede88-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ede88-147">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ede88-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ede88-148">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="ede88-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="ede88-149">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="ede88-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="ede88-150">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="ede88-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="ede88-151">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="ede88-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="ede88-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ede88-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ede88-153">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="ede88-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="ede88-154">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="ede88-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="ede88-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="ede88-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="ede88-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ede88-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ede88-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ede88-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ede88-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ede88-158">RELATED LINKS</span></span>

