---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98405052"
---
# <span data-ttu-id="2939d-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="2939d-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="2939d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2939d-102">SYNOPSIS</span></span>
<span data-ttu-id="2939d-103">Проверяет, является ли имя назначения действительным и не используется.</span><span class="sxs-lookup"><span data-stu-id="2939d-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="2939d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2939d-104">SYNTAX</span></span>

### <span data-ttu-id="2939d-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2939d-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2939d-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2939d-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2939d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2939d-107">DESCRIPTION</span></span>
<span data-ttu-id="2939d-108">Проверяет, является ли имя назначения действительным и не используется.</span><span class="sxs-lookup"><span data-stu-id="2939d-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="2939d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2939d-109">EXAMPLES</span></span>

### <span data-ttu-id="2939d-110">Пример 1. Проверка доступности имени кластера principalassignment, которое используется</span><span class="sxs-lookup"><span data-stu-id="2939d-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="2939d-111">Она возвращает, существует ли в кластере testnewkustocluster имя PrincipalAssignment myprincipal или нет.</span><span class="sxs-lookup"><span data-stu-id="2939d-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="2939d-112">Пример 2. Проверка доступности имени кластера principalassignment, которое не используется</span><span class="sxs-lookup"><span data-stu-id="2939d-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="2939d-113">Она возвращает, существует ли в кластере "testnewkustocluster" пункт PrincipalAssignment с именем newprincipal.</span><span class="sxs-lookup"><span data-stu-id="2939d-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="2939d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2939d-114">PARAMETERS</span></span>

### <span data-ttu-id="2939d-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2939d-115">-ClusterName</span></span>
<span data-ttu-id="2939d-116">Название кластера Кусто.</span><span class="sxs-lookup"><span data-stu-id="2939d-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2939d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2939d-117">-DefaultProfile</span></span>
<span data-ttu-id="2939d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2939d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2939d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2939d-119">-InputObject</span></span>
<span data-ttu-id="2939d-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2939d-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2939d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2939d-121">-Name</span></span>
<span data-ttu-id="2939d-122">Имя ресурса основного назначения.</span><span class="sxs-lookup"><span data-stu-id="2939d-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="2939d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2939d-123">-ResourceGroupName</span></span>
<span data-ttu-id="2939d-124">Имя группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="2939d-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2939d-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2939d-125">-SubscriptionId</span></span>
<span data-ttu-id="2939d-126">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2939d-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2939d-127">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2939d-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2939d-128">-Type</span><span class="sxs-lookup"><span data-stu-id="2939d-128">-Type</span></span>
<span data-ttu-id="2939d-129">Тип ресурса: Microsoft.Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="2939d-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="2939d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2939d-130">-Confirm</span></span>
<span data-ttu-id="2939d-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2939d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2939d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2939d-132">-WhatIf</span></span>
<span data-ttu-id="2939d-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2939d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2939d-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2939d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2939d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2939d-135">CommonParameters</span></span>
<span data-ttu-id="2939d-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2939d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2939d-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2939d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2939d-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2939d-138">INPUTS</span></span>

### <span data-ttu-id="2939d-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="2939d-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="2939d-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2939d-140">OUTPUTS</span></span>

### <span data-ttu-id="2939d-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="2939d-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="2939d-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2939d-142">NOTES</span></span>

<span data-ttu-id="2939d-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2939d-143">ALIASES</span></span>

<span data-ttu-id="2939d-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2939d-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2939d-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2939d-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2939d-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2939d-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2939d-147">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2939d-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2939d-148">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="2939d-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="2939d-149">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="2939d-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="2939d-150">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="2939d-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="2939d-151">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="2939d-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="2939d-152">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2939d-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2939d-153">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="2939d-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="2939d-154">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="2939d-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="2939d-155">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="2939d-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="2939d-156">`[SubscriptionId <String>]`: получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="2939d-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2939d-157">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="2939d-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2939d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2939d-158">RELATED LINKS</span></span>

