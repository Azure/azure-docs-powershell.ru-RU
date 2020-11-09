---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: b91332fe8867283b5fff9cbbf1f5df96209fa2f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312545"
---
# <span data-ttu-id="9fb51-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="9fb51-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="9fb51-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fb51-102">SYNOPSIS</span></span>
<span data-ttu-id="9fb51-103">Создание и обновление пула узлов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-103">Create or update a host pool.</span></span>

## <span data-ttu-id="9fb51-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fb51-104">SYNTAX</span></span>

### <span data-ttu-id="9fb51-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9fb51-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoContext <String>]
 [-Tag <Hashtable>] [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9fb51-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="9fb51-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9fb51-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fb51-107">DESCRIPTION</span></span>
<span data-ttu-id="9fb51-108">Создание и обновление пула узлов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-108">Create or update a host pool.</span></span>

## <span data-ttu-id="9fb51-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fb51-109">EXAMPLES</span></span>

### <span data-ttu-id="9fb51-110">Пример 1: создание виртуального рабочего стола Windows HostPool по имени</span><span class="sxs-lookup"><span data-stu-id="9fb51-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Pooled' `
                            -LoadBalancerType 'DepthFirst' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="9fb51-111">Эта команда создает HostPool виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="9fb51-112">Пример 1: создание виртуального рабочего стола Windows HostPool по имени</span><span class="sxs-lookup"><span data-stu-id="9fb51-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
```powershell
PS C:\> New-AzWvdHostPool -ResourceGroupName ResourceGroupName `
                            -Name HostPoolName `
                            -Location 'eastus' `
                            -HostPoolType 'Personal' `
                            -LoadBalancerType 'Persistent' `
                            -RegistrationTokenOperation 'Update' `
                            -ExpirationTime $((get-date).ToUniversalTime().AddDays(1).ToString('yyyy-MM-ddTHH:mm:ss.fffffffZ')) `
                            -Description 'Description' `
                            -FriendlyName 'Friendly Name' `
                            -MaxSessionLimit 5 `
                            -VMTemplate $null `
                            -SsoContext $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="9fb51-113">Эта команда создает HostPool виртуальных рабочих столов Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="9fb51-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fb51-114">PARAMETERS</span></span>

### <span data-ttu-id="9fb51-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="9fb51-115">-CustomRdpProperty</span></span>
<span data-ttu-id="9fb51-116">Настраиваемое свойство RDP для HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-116">Custom rdp property of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fb51-117">-DefaultProfile</span></span>
<span data-ttu-id="9fb51-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fb51-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fb51-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="9fb51-119">-Description</span></span>
<span data-ttu-id="9fb51-120">Описание HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-120">Description of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb51-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="9fb51-122">Имя группы приложений для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="9fb51-122">Desktop App Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="9fb51-123">-ExpirationTime</span></span>
<span data-ttu-id="9fb51-124">Срок действия маркера регистрации.</span><span class="sxs-lookup"><span data-stu-id="9fb51-124">Expiration time of registration token.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9fb51-125">-FriendlyName</span></span>
<span data-ttu-id="9fb51-126">Понятное имя HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-126">Friendly name of HostPool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="9fb51-127">-HostPoolType</span></span>
<span data-ttu-id="9fb51-128">Тип HostPool для рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="9fb51-128">HostPool type for desktop.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.HostPoolType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="9fb51-129">-LoadBalancerType</span></span>
<span data-ttu-id="9fb51-130">Тип подсистемы балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9fb51-130">The type of the load balancer.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.LoadBalancerType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-131">-Location</span><span class="sxs-lookup"><span data-stu-id="9fb51-131">-Location</span></span>
<span data-ttu-id="9fb51-132">Географическое расположение, в котором находится ресурс</span><span class="sxs-lookup"><span data-stu-id="9fb51-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="9fb51-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="9fb51-133">-MaxSessionLimit</span></span>
<span data-ttu-id="9fb51-134">Максимальная длина сеанса в HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-134">The max session limit of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9fb51-135">-Name</span></span>
<span data-ttu-id="9fb51-136">Имя пула узлов в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-136">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HostPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="9fb51-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="9fb51-138">Тип PersonalDesktopAssignment для HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-138">PersonalDesktopAssignment type for HostPool.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PersonalDesktopAssignmentType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="9fb51-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="9fb51-140">Тип предпочтительного типа группы приложения, по умолчанию для группы приложений для настольных компьютеров</span><span class="sxs-lookup"><span data-stu-id="9fb51-140">The type of preferred application group type, default to Desktop Application Group</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.PreferredAppGroupType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="9fb51-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="9fb51-142">Строка маркера регистрации в кодировке Base64.</span><span class="sxs-lookup"><span data-stu-id="9fb51-142">The registration token base64 encoded string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="9fb51-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="9fb51-144">Тип сброса маркера.</span><span class="sxs-lookup"><span data-stu-id="9fb51-144">The type of resetting the token.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RegistrationTokenOperation
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fb51-145">-ResourceGroupName</span></span>
<span data-ttu-id="9fb51-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-146">The name of the resource group.</span></span>
<span data-ttu-id="9fb51-147">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="9fb51-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9fb51-148">-Ring</span><span class="sxs-lookup"><span data-stu-id="9fb51-148">-Ring</span></span>
<span data-ttu-id="9fb51-149">Номер кольца HostPool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-149">The ring number of HostPool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-150">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="9fb51-150">-SsoContext</span></span>
<span data-ttu-id="9fb51-151">Путь к keyvault, содержащему ssoContext секрет.</span><span class="sxs-lookup"><span data-stu-id="9fb51-151">Path to keyvault containing ssoContext secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9fb51-152">-SubscriptionId</span></span>
<span data-ttu-id="9fb51-153">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9fb51-153">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="9fb51-154">-Tag</span></span>
<span data-ttu-id="9fb51-155">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9fb51-155">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-156">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="9fb51-156">-ValidationEnvironment</span></span>
<span data-ttu-id="9fb51-157">Является средой проверки.</span><span class="sxs-lookup"><span data-stu-id="9fb51-157">Is validation environment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-158">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="9fb51-158">-VMTemplate</span></span>
<span data-ttu-id="9fb51-159">Шаблон ВМ для конфигурации sessionhosts в hostpool.</span><span class="sxs-lookup"><span data-stu-id="9fb51-159">VM template for sessionhosts configuration within hostpool.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-160">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9fb51-160">-WorkspaceName</span></span>
<span data-ttu-id="9fb51-161">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="9fb51-161">Workspace Name</span></span>

```yaml
Type: System.String
Parameter Sets: FullSenerioCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fb51-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9fb51-162">-Confirm</span></span>
<span data-ttu-id="9fb51-163">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9fb51-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fb51-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fb51-164">-WhatIf</span></span>
<span data-ttu-id="9fb51-165">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9fb51-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fb51-166">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9fb51-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fb51-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fb51-167">CommonParameters</span></span>
<span data-ttu-id="9fb51-168">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fb51-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fb51-169">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9fb51-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fb51-170">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fb51-170">INPUTS</span></span>

## <span data-ttu-id="9fb51-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fb51-171">OUTPUTS</span></span>

### <span data-ttu-id="9fb51-172">Microsoft. Azure. PowerShell. командлеты. DesktopVirtualization. Models. Api20191210Preview. IHostPool</span><span class="sxs-lookup"><span data-stu-id="9fb51-172">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IHostPool</span></span>

## <span data-ttu-id="9fb51-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fb51-173">NOTES</span></span>

<span data-ttu-id="9fb51-174">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="9fb51-174">ALIASES</span></span>

## <span data-ttu-id="9fb51-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fb51-175">RELATED LINKS</span></span>

