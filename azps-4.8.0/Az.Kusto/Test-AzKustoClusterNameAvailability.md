---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/test-azkustoclusternameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Test-AzKustoClusterNameAvailability.md
ms.openlocfilehash: 15c052eedb0174b71581a390610274e10379035a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236321"
---
# <span data-ttu-id="88238-101">Test-AzKustoClusterNameAvailability</span><span class="sxs-lookup"><span data-stu-id="88238-101">Test-AzKustoClusterNameAvailability</span></span>

## <span data-ttu-id="88238-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="88238-102">SYNOPSIS</span></span>
<span data-ttu-id="88238-103">Проверка того, что имя кластера является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="88238-103">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="88238-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="88238-104">SYNTAX</span></span>

### <span data-ttu-id="88238-105">CheckExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="88238-105">CheckExpanded (Default)</span></span>
```
Test-AzKustoClusterNameAvailability -Location <String> -Name <String> -Type <Type> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="88238-106">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="88238-106">CheckViaIdentityExpanded</span></span>
```
Test-AzKustoClusterNameAvailability -InputObject <IKustoIdentity> -Name <String> -Type <Type>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="88238-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88238-107">DESCRIPTION</span></span>
<span data-ttu-id="88238-108">Проверка того, что имя кластера является допустимым и еще не используется.</span><span class="sxs-lookup"><span data-stu-id="88238-108">Checks that the cluster name is valid and is not already in use.</span></span>

## <span data-ttu-id="88238-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="88238-109">EXAMPLES</span></span>

### <span data-ttu-id="88238-110">Пример 1: Проверка доступности используемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="88238-110">Example 1: Check the availability of a Kusto cluster name which is in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name testnewkustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message                                                                                       Name                NameAvailable Reason
-------                                                                                       ----                ------------- ------
Name 'testnewkustocluster' with type Engine is already taken. Please specify a different name testnewkustocluster False
```

<span data-ttu-id="88238-111">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "testnewkustocluster" в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="88238-111">The above command returns whether or not a Kusto cluster named "testnewkustocluster" exists in the "East US" region.</span></span>

### <span data-ttu-id="88238-112">Пример 2: Проверка доступности неиспользуемого имени кластера Kusto</span><span class="sxs-lookup"><span data-stu-id="88238-112">Example 2: Check the availability of a Kusto cluster name which is not in use</span></span>
```powershell
PS C:\> Test-AzKustoClusterNameAvailability -Name availablekustocluster -Location 'East US' -Type Microsoft.Kusto/clusters

Message Name                  NameAvailable Reason
------- ----                  ------------- ------
        availablekustocluster True
```

<span data-ttu-id="88238-113">Указанная выше команда возвращает значение, указывающее, существует ли кластер Kusto с именем "availablekustocluster" в регионе "Восток США".</span><span class="sxs-lookup"><span data-stu-id="88238-113">The above command returns whether or not a Kusto cluster named "availablekustocluster" exists in the "East US" region.</span></span>

## <span data-ttu-id="88238-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="88238-114">PARAMETERS</span></span>

### <span data-ttu-id="88238-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88238-115">-DefaultProfile</span></span>
<span data-ttu-id="88238-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88238-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88238-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88238-117">-InputObject</span></span>
<span data-ttu-id="88238-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="88238-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="88238-119">-Location</span><span class="sxs-lookup"><span data-stu-id="88238-119">-Location</span></span>
<span data-ttu-id="88238-120">Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="88238-120">Azure location.</span></span>

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

### <span data-ttu-id="88238-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="88238-121">-Name</span></span>
<span data-ttu-id="88238-122">Имя кластера.</span><span class="sxs-lookup"><span data-stu-id="88238-122">Cluster name.</span></span>

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

### <span data-ttu-id="88238-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="88238-123">-SubscriptionId</span></span>
<span data-ttu-id="88238-124">Получение учетных данных подписки, однозначно идентифицирующей подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="88238-124">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="88238-125">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="88238-125">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="88238-126">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="88238-126">-Type</span></span>
<span data-ttu-id="88238-127">Тип ресурсов (Microsoft. Kusto/Clusters).</span><span class="sxs-lookup"><span data-stu-id="88238-127">The type of resource, Microsoft.Kusto/clusters.</span></span>

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

### <span data-ttu-id="88238-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88238-128">-Confirm</span></span>
<span data-ttu-id="88238-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="88238-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88238-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88238-130">-WhatIf</span></span>
<span data-ttu-id="88238-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="88238-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88238-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="88238-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88238-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88238-133">CommonParameters</span></span>
<span data-ttu-id="88238-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="88238-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88238-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88238-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88238-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="88238-136">INPUTS</span></span>

### <span data-ttu-id="88238-137">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. IKustoIdentity</span><span class="sxs-lookup"><span data-stu-id="88238-137">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.IKustoIdentity</span></span>

## <span data-ttu-id="88238-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="88238-138">OUTPUTS</span></span>

### <span data-ttu-id="88238-139">Microsoft. Azure. PowerShell. командлеты. Kusto. Models. Api20200614. ICheckNameResult</span><span class="sxs-lookup"><span data-stu-id="88238-139">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ICheckNameResult</span></span>

## <span data-ttu-id="88238-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="88238-140">NOTES</span></span>

<span data-ttu-id="88238-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="88238-141">ALIASES</span></span>

<span data-ttu-id="88238-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="88238-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="88238-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="88238-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="88238-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="88238-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="88238-145">INPUTOBJECT <IKustoIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="88238-145">INPUTOBJECT <IKustoIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="88238-146">`[AttachedDatabaseConfigurationName <String>]`: Имя конфигурации присоединенной базы данных.</span><span class="sxs-lookup"><span data-stu-id="88238-146">`[AttachedDatabaseConfigurationName <String>]`: The name of the attached database configuration.</span></span>
  - <span data-ttu-id="88238-147">`[ClusterName <String>]`: Имя кластера Kusto.</span><span class="sxs-lookup"><span data-stu-id="88238-147">`[ClusterName <String>]`: The name of the Kusto cluster.</span></span>
  - <span data-ttu-id="88238-148">`[DataConnectionName <String>]`: Имя подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="88238-148">`[DataConnectionName <String>]`: The name of the data connection.</span></span>
  - <span data-ttu-id="88238-149">`[DatabaseName <String>]`: Имя базы данных в кластере Kusto.</span><span class="sxs-lookup"><span data-stu-id="88238-149">`[DatabaseName <String>]`: The name of the database in the Kusto cluster.</span></span>
  - <span data-ttu-id="88238-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="88238-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="88238-151">`[Location <String>]`: Расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="88238-151">`[Location <String>]`: Azure location.</span></span>
  - <span data-ttu-id="88238-152">`[PrincipalAssignmentName <String>]`: Имя Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="88238-152">`[PrincipalAssignmentName <String>]`: The name of the Kusto principalAssignment.</span></span>
  - <span data-ttu-id="88238-153">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей кластер Kusto.</span><span class="sxs-lookup"><span data-stu-id="88238-153">`[ResourceGroupName <String>]`: The name of the resource group containing the Kusto cluster.</span></span>
  - <span data-ttu-id="88238-154">`[SubscriptionId <String>]`: Получение учетных данных подписки, которые уникально определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="88238-154">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="88238-155">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="88238-155">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="88238-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88238-156">RELATED LINKS</span></span>

