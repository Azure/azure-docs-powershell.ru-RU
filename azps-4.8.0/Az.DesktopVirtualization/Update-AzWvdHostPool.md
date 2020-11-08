---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: ffb38dd20c5bc43c3d243e5a6f320fdc5d48d008
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078313"
---
# <span data-ttu-id="715bf-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="715bf-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="715bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="715bf-102">SYNOPSIS</span></span>
<span data-ttu-id="715bf-103">Обновите пул узлов.</span><span class="sxs-lookup"><span data-stu-id="715bf-103">Update a host pool.</span></span>

## <span data-ttu-id="715bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="715bf-104">SYNTAX</span></span>

### <span data-ttu-id="715bf-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="715bf-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="715bf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="715bf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoContext <String>] [-Tag <Hashtable>] [-ValidationEnvironment] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="715bf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="715bf-107">DESCRIPTION</span></span>
<span data-ttu-id="715bf-108">Обновите пул узлов.</span><span class="sxs-lookup"><span data-stu-id="715bf-108">Update a host pool.</span></span>

## <span data-ttu-id="715bf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="715bf-109">EXAMPLES</span></span>

### <span data-ttu-id="715bf-110">Пример 1: Обновление виртуального рабочего стола Windows HostPool по имени</span><span class="sxs-lookup"><span data-stu-id="715bf-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> Update-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -LoadBalancerType 'BreadthFirst' `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 6 `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="715bf-111">Эта команда обновляет HostPool виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="715bf-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="715bf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="715bf-112">PARAMETERS</span></span>

### <span data-ttu-id="715bf-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="715bf-113">-CustomRdpProperty</span></span>
<span data-ttu-id="715bf-114">Настраиваемое свойство RDP для HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-114">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715bf-115">-DefaultProfile</span></span>
<span data-ttu-id="715bf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="715bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715bf-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="715bf-117">-Description</span></span>
<span data-ttu-id="715bf-118">Описание HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-118">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="715bf-119">-FriendlyName</span></span>
<span data-ttu-id="715bf-120">Понятное имя HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-120">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="715bf-121">-InputObject</span></span>
<span data-ttu-id="715bf-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="715bf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="715bf-123">-LoadBalancerType</span></span>
<span data-ttu-id="715bf-124">Тип подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="715bf-124">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="715bf-125">-MaxSessionLimit</span></span>
<span data-ttu-id="715bf-126">Максимальная длина сеанса в HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-126">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="715bf-127">-Name</span></span>
<span data-ttu-id="715bf-128">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="715bf-128">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="715bf-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="715bf-130">Тип PersonalDesktopAssignment для HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-130">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="715bf-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="715bf-132">Тип предпочтительного типа группы приложения, по умолчанию для группы приложений для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="715bf-132">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="715bf-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="715bf-134">Срок действия маркера регистрации.</span><span class="sxs-lookup"><span data-stu-id="715bf-134">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="715bf-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="715bf-136">Тип сброса маркера.</span><span class="sxs-lookup"><span data-stu-id="715bf-136">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715bf-137">-ResourceGroupName</span></span>
<span data-ttu-id="715bf-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="715bf-138">The name of the resource group.</span></span>
<span data-ttu-id="715bf-139">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="715bf-139">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-140">-Ring</span><span class="sxs-lookup"><span data-stu-id="715bf-140">-Ring</span></span>
<span data-ttu-id="715bf-141">Номер кольца HostPool.</span><span class="sxs-lookup"><span data-stu-id="715bf-141">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-142">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="715bf-142">-SsoContext</span></span>
<span data-ttu-id="715bf-143">Путь к keyvault, содержащему ssoContext секрет.</span><span class="sxs-lookup"><span data-stu-id="715bf-143">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="715bf-144">-SubscriptionId</span></span>
<span data-ttu-id="715bf-145">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="715bf-145">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="715bf-146">-Tag</span></span>
<span data-ttu-id="715bf-147">Теги для обновления</span><span class="sxs-lookup"><span data-stu-id="715bf-147">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-148">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="715bf-148">-ValidationEnvironment</span></span>
<span data-ttu-id="715bf-149">Является средой проверки.</span><span class="sxs-lookup"><span data-stu-id="715bf-149">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715bf-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="715bf-150">-Confirm</span></span>
<span data-ttu-id="715bf-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="715bf-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="715bf-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="715bf-152">-WhatIf</span></span>
<span data-ttu-id="715bf-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="715bf-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="715bf-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="715bf-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="715bf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715bf-155">CommonParameters</span></span>
<span data-ttu-id="715bf-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="715bf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715bf-157">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="715bf-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715bf-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="715bf-158">INPUTS</span></span>

### <span data-ttu-id="715bf-159">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="715bf-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="715bf-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="715bf-160">OUTPUTS</span></span>

### <span data-ttu-id="715bf-161">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="715bf-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="715bf-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="715bf-162">NOTES</span></span>

<span data-ttu-id="715bf-163">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="715bf-163">ALIASES</span></span>

<span data-ttu-id="715bf-164">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="715bf-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="715bf-165">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="715bf-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="715bf-166">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="715bf-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="715bf-167">INPUTOBJECT <IDesktopVirtualizationIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="715bf-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="715bf-168">`[ApplicationGroupName <String>]`: Имя группы приложения.</span><span class="sxs-lookup"><span data-stu-id="715bf-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="715bf-169">`[ApplicationName <String>]`: Имя приложения в указанной группе приложения.</span><span class="sxs-lookup"><span data-stu-id="715bf-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="715bf-170">`[DesktopName <String>]`: Имя рабочего стола в пределах указанной группы рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="715bf-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="715bf-171">`[HostPoolName <String>]`: Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="715bf-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="715bf-172">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="715bf-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="715bf-173">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="715bf-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="715bf-174">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="715bf-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="715bf-175">`[SessionHostName <String>]`: Имя узла сеанса в указанном пуле узлов.</span><span class="sxs-lookup"><span data-stu-id="715bf-175">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="715bf-176">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="715bf-176">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="715bf-177">`[UserSessionId <String>]`: Имя сеанса пользователя на указанном узле сеансов</span><span class="sxs-lookup"><span data-stu-id="715bf-177">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="715bf-178">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="715bf-178">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="715bf-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="715bf-179">RELATED LINKS</span></span>

