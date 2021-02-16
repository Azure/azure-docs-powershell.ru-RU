---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdHostPool.md
ms.openlocfilehash: 6f579dfcba74f68eafaa149be15649e496c46f82
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238073"
---
# <span data-ttu-id="b71a4-101">New-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="b71a4-101">New-AzWvdHostPool</span></span>

## <span data-ttu-id="b71a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b71a4-102">SYNOPSIS</span></span>
<span data-ttu-id="b71a4-103">Создание и обновление пула хостов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-103">Create or update a host pool.</span></span>

## <span data-ttu-id="b71a4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b71a4-104">SYNTAX</span></span>

### <span data-ttu-id="b71a4-105">CreateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b71a4-105">CreateExpanded (Default)</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CustomRdpProperty <String>] [-Description <String>] [-ExpirationTime <DateTime>]
 [-FriendlyName <String>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>] [-RegistrationInfoToken <String>]
 [-RegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>] [-SsoadfsAuthority <String>]
 [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>] [-SsoContext <String>]
 [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>] [-ValidationEnvironment]
 [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b71a4-106">FullSenerioCreate</span><span class="sxs-lookup"><span data-stu-id="b71a4-106">FullSenerioCreate</span></span>
```
New-AzWvdHostPool -HostPoolType <HostPoolType> -LoadBalancerType <LoadBalancerType> -Location <String>
 -Name <String> -PreferredAppGroupType <PreferredAppGroupType> -ResourceGroupName <String>
 [-DesktopAppGroupName <String>] [-SubscriptionId <String>] [-WorkspaceName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b71a4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b71a4-107">DESCRIPTION</span></span>
<span data-ttu-id="b71a4-108">Создание и обновление пула хостов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-108">Create or update a host pool.</span></span>

## <span data-ttu-id="b71a4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b71a4-109">EXAMPLES</span></span>

### <span data-ttu-id="b71a4-110">Пример 1. Создание виртуального рабочего стола Windows hostPool по имени</span><span class="sxs-lookup"><span data-stu-id="b71a4-110">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="b71a4-111">Эта команда создает виртуальный настольный принтер Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-111">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

### <span data-ttu-id="b71a4-112">Пример 1. Создание виртуального рабочего стола Windows hostPool по имени</span><span class="sxs-lookup"><span data-stu-id="b71a4-112">Example 1: Create a Windows Virtual Desktop HostPool by name</span></span>
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
                            -SsoClientId $null `
                            -SsoClientSecretKeyVaultPath $null `
                            -SsoSecretType $null `
                            -SsoadfsAuthority $null `
                            -CustomRdpProperty $null `
                            -Ring $null `
                            -ValidationEnvironment:$false

Location   Name                 Type
--------   ----                 ----
eastus     HostPoolName Microsoft.DesktopVirtualization/hostpools
```

<span data-ttu-id="b71a4-113">Эта команда создает виртуальный настольный принтер Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-113">This command creates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="b71a4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b71a4-114">PARAMETERS</span></span>

### <span data-ttu-id="b71a4-115">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="b71a4-115">-CustomRdpProperty</span></span>
<span data-ttu-id="b71a4-116">Настраиваемая свойство RDP hostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-116">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="b71a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b71a4-117">-DefaultProfile</span></span>
<span data-ttu-id="b71a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b71a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b71a4-119">-Description</span><span class="sxs-lookup"><span data-stu-id="b71a4-119">-Description</span></span>
<span data-ttu-id="b71a4-120">Описание HostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-120">Description of HostPool.</span></span>

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

### <span data-ttu-id="b71a4-121">-DesktopAppGroupName</span><span class="sxs-lookup"><span data-stu-id="b71a4-121">-DesktopAppGroupName</span></span>
<span data-ttu-id="b71a4-122">Имя группы в приложении для настольных систем</span><span class="sxs-lookup"><span data-stu-id="b71a4-122">Desktop App Group Name</span></span>

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

### <span data-ttu-id="b71a4-123">-ExpirationTime</span><span class="sxs-lookup"><span data-stu-id="b71a4-123">-ExpirationTime</span></span>
<span data-ttu-id="b71a4-124">Время окончания срока действия маркера регистрации.</span><span class="sxs-lookup"><span data-stu-id="b71a4-124">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="b71a4-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b71a4-125">-FriendlyName</span></span>
<span data-ttu-id="b71a4-126">Удобное имя HostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-126">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="b71a4-127">-HostPoolType</span><span class="sxs-lookup"><span data-stu-id="b71a4-127">-HostPoolType</span></span>
<span data-ttu-id="b71a4-128">Тип hostPool для рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="b71a4-128">HostPool type for desktop.</span></span>

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

### <span data-ttu-id="b71a4-129">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="b71a4-129">-LoadBalancerType</span></span>
<span data-ttu-id="b71a4-130">Тип балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="b71a4-130">The type of the load balancer.</span></span>

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

### <span data-ttu-id="b71a4-131">-Location</span><span class="sxs-lookup"><span data-stu-id="b71a4-131">-Location</span></span>
<span data-ttu-id="b71a4-132">Географическое расположение ресурса</span><span class="sxs-lookup"><span data-stu-id="b71a4-132">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="b71a4-133">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="b71a4-133">-MaxSessionLimit</span></span>
<span data-ttu-id="b71a4-134">Максимальное ограничение сеанса в HostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-134">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="b71a4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="b71a4-135">-Name</span></span>
<span data-ttu-id="b71a4-136">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="b71a4-136">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="b71a4-137">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="b71a4-137">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="b71a4-138">Тип PersonalDesktopAssignment для HostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-138">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="b71a4-139">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="b71a4-139">-PreferredAppGroupType</span></span>
<span data-ttu-id="b71a4-140">Тип предпочитаемого типа группы приложений (по умолчанию — группа классических приложений)</span><span class="sxs-lookup"><span data-stu-id="b71a4-140">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="b71a4-141">-RegistrationInfoToken</span><span class="sxs-lookup"><span data-stu-id="b71a4-141">-RegistrationInfoToken</span></span>
<span data-ttu-id="b71a4-142">Кодированная строка маркера регистрации (base64).</span><span class="sxs-lookup"><span data-stu-id="b71a4-142">The registration token base64 encoded string.</span></span>

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

### <span data-ttu-id="b71a4-143">-RegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="b71a4-143">-RegistrationTokenOperation</span></span>
<span data-ttu-id="b71a4-144">Тип сброса маркера.</span><span class="sxs-lookup"><span data-stu-id="b71a4-144">The type of resetting the token.</span></span>

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

### <span data-ttu-id="b71a4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b71a4-145">-ResourceGroupName</span></span>
<span data-ttu-id="b71a4-146">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-146">The name of the resource group.</span></span>
<span data-ttu-id="b71a4-147">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b71a4-147">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b71a4-148">-Позвонить</span><span class="sxs-lookup"><span data-stu-id="b71a4-148">-Ring</span></span>
<span data-ttu-id="b71a4-149">Номер звонка HostPool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-149">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="b71a4-150">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="b71a4-150">-SsoadfsAuthority</span></span>
<span data-ttu-id="b71a4-151">URL-адрес сервера ADFS клиента для подписи сертификатов SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="b71a4-151">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="b71a4-152">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="b71a4-152">-SsoClientId</span></span>
<span data-ttu-id="b71a4-153">ClientId зарегистрированной стороны, которая использовалась для выпуска сертификатов SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="b71a4-153">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="b71a4-154">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="b71a4-154">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="b71a4-155">Путь к ключам Azure KeyVault для хранения секретов, используемых для связи с ADFS.</span><span class="sxs-lookup"><span data-stu-id="b71a4-155">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="b71a4-156">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="b71a4-156">-SsoContext</span></span>
<span data-ttu-id="b71a4-157">Путь к клавишам, содержащим секрет сoContext.</span><span class="sxs-lookup"><span data-stu-id="b71a4-157">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="b71a4-158">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="b71a4-158">-SsoSecretType</span></span>
<span data-ttu-id="b71a4-159">Тип единого знака для секретного типа.</span><span class="sxs-lookup"><span data-stu-id="b71a4-159">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b71a4-160">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="b71a4-160">-StartVMOnConnect</span></span>
<span data-ttu-id="b71a4-161">Флажок для отключения функции StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="b71a4-161">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="b71a4-162">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b71a4-162">-SubscriptionId</span></span>
<span data-ttu-id="b71a4-163">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b71a4-163">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b71a4-164">-Tag</span><span class="sxs-lookup"><span data-stu-id="b71a4-164">-Tag</span></span>
<span data-ttu-id="b71a4-165">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b71a4-165">Resource tags.</span></span>

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

### <span data-ttu-id="b71a4-166">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="b71a4-166">-ValidationEnvironment</span></span>
<span data-ttu-id="b71a4-167">Это среда проверки.</span><span class="sxs-lookup"><span data-stu-id="b71a4-167">Is validation environment.</span></span>

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

### <span data-ttu-id="b71a4-168">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="b71a4-168">-VMTemplate</span></span>
<span data-ttu-id="b71a4-169">Шаблон VM для настройки sessionhosts в рамках hostpool.</span><span class="sxs-lookup"><span data-stu-id="b71a4-169">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="b71a4-170">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b71a4-170">-WorkspaceName</span></span>
<span data-ttu-id="b71a4-171">Имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="b71a4-171">Workspace Name</span></span>

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

### <span data-ttu-id="b71a4-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b71a4-172">-Confirm</span></span>
<span data-ttu-id="b71a4-173">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b71a4-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b71a4-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b71a4-174">-WhatIf</span></span>
<span data-ttu-id="b71a4-175">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b71a4-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b71a4-176">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b71a4-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b71a4-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b71a4-177">CommonParameters</span></span>
<span data-ttu-id="b71a4-178">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b71a4-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b71a4-179">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b71a4-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b71a4-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b71a4-180">INPUTS</span></span>

## <span data-ttu-id="b71a4-181">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b71a4-181">OUTPUTS</span></span>

### <span data-ttu-id="b71a4-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="b71a4-182">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="b71a4-183">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b71a4-183">NOTES</span></span>

<span data-ttu-id="b71a4-184">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b71a4-184">ALIASES</span></span>

## <span data-ttu-id="b71a4-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b71a4-185">RELATED LINKS</span></span>

