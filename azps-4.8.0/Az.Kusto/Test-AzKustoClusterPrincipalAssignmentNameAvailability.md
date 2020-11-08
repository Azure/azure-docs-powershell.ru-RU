---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusterprincipalassignmentnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterPrincipalAssignmentNameAvailability.md
ms.openlocfilehash: cb4f375632626ee3c3428e6a990a228dacecd288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244494"
---
# <span data-ttu-id="20a91-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span><span class="sxs-lookup"><span data-stu-id="20a91-101">Test-AzKustoClusterPrincipalAssignmentNameAvailability</span></span>

## <span data-ttu-id="20a91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20a91-102">SYNOPSIS</span></span>
<span data-ttu-id="20a91-103">Проверка того, что имя назначения участника является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="20a91-103">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="20a91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20a91-104">SYNTAX</span></span>

### <span data-ttu-id="20a91-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20a91-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -ClusterName <String> -ResourceGroupName <String>
 -Name <String> -Type <Type> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="20a91-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="20a91-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterPrincipalAssignmentNameAvailability -InputObject <IKustoIdentity> -Name <String>
 -Type <Type> [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20a91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20a91-107">DESCRIPTION</span></span>
<span data-ttu-id="20a91-108">Проверка того, что имя назначения участника является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="20a91-108">Checks that the principal assignment name is valid and is not already in use.</span></span>

## <span data-ttu-id="20a91-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20a91-109">EXAMPLES</span></span>

### <span data-ttu-id="20a91-110">Пример 1: Проверка доступности имени кластера, используемого principalassignment</span><span class="sxs-lookup"><span data-stu-id="20a91-110">Example 1: Check the availability of a cluster principalassignment name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "myprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments" 

Message                                                                                                        Name            NameAvailable Reason
-------                                                                                                        ----            ------------- ------
PrincipalAssignment myprincipal already exists in cluster testnewkustocluster. Please select a different name. myprincipal   False
```

<span data-ttu-id="20a91-111">Указанная выше команда возвращает значение, указывающее, существует ли PrincipalAssignment с именем "MyPrincipal" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="20a91-111">The above command returns whether or not a PrincipalAssignment named "myprincipal" exists in the cluster "testnewkustocluster".</span></span>

### <span data-ttu-id="20a91-112">Пример 2: Проверка доступности неиспользуемого principalassignmentного имени кластера</span><span class="sxs-lookup"><span data-stu-id="20a91-112">Example 2: Check the availability of a cluster principalassignment name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterPrincipalAssignmentNameAvailability -ResourceGroupName "testrg" -ClusterName "testnewkustocluster" -Name "newprincipal" -Type "Microsoft.Kusto/clusters/principalAssignments"

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="20a91-113">Указанная выше команда возвращает значение, указывающее, существует ли PrincipalAssignment с именем "newprincipal" в кластере "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="20a91-113">The above command returns whether or not a PrincipalAssignment named "newprincipal" exists in the cluster "testnewkustocluster".</span></span>

## <span data-ttu-id="20a91-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20a91-114">PARAMETERS</span></span>

### <span data-ttu-id="20a91-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="20a91-115">-ClusterName</span></span>
<span data-ttu-id="20a91-116">Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="20a91-116">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="20a91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a91-117">-DefaultProfile</span></span>
<span data-ttu-id="20a91-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20a91-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20a91-119">-InputObject</span></span>
<span data-ttu-id="20a91-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="20a91-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20a91-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20a91-121">-Name</span></span>
<span data-ttu-id="20a91-122">Имя ресурса назначения участника.</span><span class="sxs-lookup"><span data-stu-id="20a91-122">Principal Assignment resource name.</span></span>

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

### <span data-ttu-id="20a91-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a91-123">-ResourceGroupName</span></span>
<span data-ttu-id="20a91-124">Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="20a91-124">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="20a91-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20a91-125">-SubscriptionId</span></span>
<span data-ttu-id="20a91-126">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20a91-126">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="20a91-127">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="20a91-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="20a91-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="20a91-128">-Type</span></span>
<span data-ttu-id="20a91-129">Тип ресурсов, Microsoft. Kusto/Clusters/principalAssignments.</span><span class="sxs-lookup"><span data-stu-id="20a91-129">The type of resource, Microsoft.Kusto/Clusters/principalAssignments.</span></span>

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

### <span data-ttu-id="20a91-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20a91-130">-Confirm</span></span>
<span data-ttu-id="20a91-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20a91-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20a91-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20a91-132">-WhatIf</span></span>
<span data-ttu-id="20a91-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20a91-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20a91-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20a91-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20a91-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a91-135">CommonParameters</span></span>
<span data-ttu-id="20a91-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20a91-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a91-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a91-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a91-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20a91-138">INPUTS</span></span>

### <span data-ttu-id="20a91-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="20a91-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="20a91-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20a91-140">OUTPUTS</span></span>

### <span data-ttu-id="20a91-141">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="20a91-141">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="20a91-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="20a91-142">NOTES</span></span>

<span data-ttu-id="20a91-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="20a91-143">ALIASES</span></span>

<span data-ttu-id="20a91-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="20a91-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20a91-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20a91-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20a91-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20a91-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20a91-147">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="20a91-147">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20a91-148">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="20a91-148">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="20a91-149">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="20a91-149">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="20a91-150">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="20a91-150">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="20a91-151">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="20a91-151">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="20a91-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="20a91-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20a91-153">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="20a91-153">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="20a91-154">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="20a91-154">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="20a91-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="20a91-155">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="20a91-156">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20a91-156">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="20a91-157">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="20a91-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="20a91-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20a91-158">RELATED LINKS</span></span>

