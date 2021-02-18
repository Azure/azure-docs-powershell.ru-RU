---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: d7dc3a154049e486490edddd5fbda52a552d32c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214505"
---
# <span data-ttu-id="3731f-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="3731f-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="3731f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3731f-102">SYNOPSIS</span></span>
<span data-ttu-id="3731f-103">Проверяет, допустимо ли имя кластера и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="3731f-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="3731f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3731f-104">SYNTAX</span></span>

### <span data-ttu-id="3731f-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3731f-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3731f-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3731f-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3731f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3731f-107">DESCRIPTION</span></span>
<span data-ttu-id="3731f-108">Проверяет, допустимо ли имя кластера и которое еще не используется.</span><span class="sxs-lookup"><span data-stu-id="3731f-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="3731f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3731f-109">EXAMPLES</span></span>

### <span data-ttu-id="3731f-110">Пример 1. Проверка доступности названия кластера "Кузто", который используется</span><span class="sxs-lookup"><span data-stu-id="3731f-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="3731f-111">Она возвращает, существует ли кластер кусто с именем testnewkustocluster в регионе "Восток.США".</span><span class="sxs-lookup"><span data-stu-id="3731f-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="3731f-112">Пример 2. Проверка доступности названия кластера "Кузто", которое не используется</span><span class="sxs-lookup"><span data-stu-id="3731f-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="3731f-113">Она возвращает, существует ли кластер кусто с именем "доступныйkustocluster" в регионе "Восток.США".</span><span class="sxs-lookup"><span data-stu-id="3731f-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="3731f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3731f-114">PARAMETERS</span></span>

### <span data-ttu-id="3731f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3731f-115">-DefaultProfile</span></span>
<span data-ttu-id="3731f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3731f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3731f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3731f-117">-InputObject</span></span>
<span data-ttu-id="3731f-118">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3731f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3731f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="3731f-119">-Location</span></span>
<span data-ttu-id="3731f-120">Расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="3731f-120">Azure location.</span></span>

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

### <span data-ttu-id="3731f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3731f-121">-Name</span></span>
<span data-ttu-id="3731f-122">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3731f-122">Cluster name.</span></span>

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

### <span data-ttu-id="3731f-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3731f-123">-SubscriptionId</span></span>
<span data-ttu-id="3731f-124">Получает учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3731f-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3731f-125">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3731f-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3731f-126">-Type</span><span class="sxs-lookup"><span data-stu-id="3731f-126">-Type</span></span>
<span data-ttu-id="3731f-127">Тип ресурса: Microsoft.Kusto или кластеры.</span><span class="sxs-lookup"><span data-stu-id="3731f-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="3731f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3731f-128">-Confirm</span></span>
<span data-ttu-id="3731f-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3731f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3731f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3731f-130">-WhatIf</span></span>
<span data-ttu-id="3731f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3731f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3731f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3731f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3731f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3731f-133">CommonParameters</span></span>
<span data-ttu-id="3731f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3731f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3731f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3731f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3731f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3731f-136">INPUTS</span></span>

### <span data-ttu-id="3731f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="3731f-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="3731f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3731f-138">OUTPUTS</span></span>

### <span data-ttu-id="3731f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="3731f-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.ICheckNameResult</span></span>

## <span data-ttu-id="3731f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3731f-140">NOTES</span></span>

<span data-ttu-id="3731f-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3731f-141">ALIASES</span></span>

<span data-ttu-id="3731f-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3731f-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3731f-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3731f-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3731f-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3731f-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3731f-145">INPUTOBJECT <IKustoIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3731f-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3731f-146">`[AttachedDatabaseConfigurationName <String>]`: имя конфигурации вложенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="3731f-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="3731f-147">`[ClusterName <String>]`Название кластера "Кусто".</span><span class="sxs-lookup"><span data-stu-id="3731f-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="3731f-148">`[DataConnectionName <String>]`: имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="3731f-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="3731f-149">`[DatabaseName <String>]`Имя базы данных в кластере Кусто.</span><span class="sxs-lookup"><span data-stu-id="3731f-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="3731f-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3731f-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3731f-151">`[Location <String>]`: расположение в Azure.</span><span class="sxs-lookup"><span data-stu-id="3731f-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="3731f-152">`[PrincipalAssignmentName <String>]`: Имя «Кусто principalAssignment».</span><span class="sxs-lookup"><span data-stu-id="3731f-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="3731f-153">`[ResourceGroupName <String>]`Название группы ресурсов, содержащей кластер Кусто.</span><span class="sxs-lookup"><span data-stu-id="3731f-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="3731f-154">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3731f-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3731f-155">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="3731f-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3731f-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3731f-156">RELATED LINKS</span></span>

