---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdhostpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdHostPool.md
ms.openlocfilehash: 5b69ff6bb04f1e8b1ae5e13fbab2c6a5f7c67927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983587"
---
# <span data-ttu-id="27b78-101">Update-AzWvdHostPool</span><span class="sxs-lookup"><span data-stu-id="27b78-101">Update-AzWvdHostPool</span></span>

## <span data-ttu-id="27b78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b78-102">SYNOPSIS</span></span>
<span data-ttu-id="27b78-103">Обновление пула хостов.</span><span class="sxs-lookup"><span data-stu-id="27b78-103">Update a host pool.</span></span>

## <span data-ttu-id="27b78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="27b78-104">SYNTAX</span></span>

### <span data-ttu-id="27b78-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27b78-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdHostPool -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-CustomRdpProperty <String>] [-Description <String>] [-FriendlyName <String>]
 [-LoadBalancerType <LoadBalancerType>] [-MaxSessionLimit <Int32>]
 [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="27b78-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="27b78-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdHostPool -InputObject <IDesktopVirtualizationIdentity> [-CustomRdpProperty <String>]
 [-Description <String>] [-FriendlyName <String>] [-LoadBalancerType <LoadBalancerType>]
 [-MaxSessionLimit <Int32>] [-PersonalDesktopAssignmentType <PersonalDesktopAssignmentType>]
 [-PreferredAppGroupType <PreferredAppGroupType>] [-RegistrationInfoExpirationTime <DateTime>]
 [-RegistrationInfoRegistrationTokenOperation <RegistrationTokenOperation>] [-Ring <Int32>]
 [-SsoadfsAuthority <String>] [-SsoClientId <String>] [-SsoClientSecretKeyVaultPath <String>]
 [-SsoContext <String>] [-SsoSecretType <SsoSecretType>] [-StartVMOnConnect] [-Tag <Hashtable>]
 [-ValidationEnvironment] [-VMTemplate <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="27b78-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27b78-107">DESCRIPTION</span></span>
<span data-ttu-id="27b78-108">Обновление пула хостов.</span><span class="sxs-lookup"><span data-stu-id="27b78-108">Update a host pool.</span></span>

## <span data-ttu-id="27b78-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="27b78-109">EXAMPLES</span></span>

### <span data-ttu-id="27b78-110">Пример 1. Обновление по имени виртуального рабочего стола Windows</span><span class="sxs-lookup"><span data-stu-id="27b78-110">Example 1: Update a Windows Virtual Desktop HostPool by name</span></span>
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

<span data-ttu-id="27b78-111">Эта команда обновляет виртуальный настольный принтер Windows в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27b78-111">This command updates a Windows Virtual Desktop HostPool in a Resource Group.</span></span>

## <span data-ttu-id="27b78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b78-112">PARAMETERS</span></span>

### <span data-ttu-id="27b78-113">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="27b78-113">-CustomRdpProperty</span></span>
<span data-ttu-id="27b78-114">Настраиваемые свойства RDP hostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-114">Custom rdp property of HostPool.</span></span>

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

### <span data-ttu-id="27b78-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b78-115">-DefaultProfile</span></span>
<span data-ttu-id="27b78-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27b78-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27b78-117">-Description</span><span class="sxs-lookup"><span data-stu-id="27b78-117">-Description</span></span>
<span data-ttu-id="27b78-118">Описание HostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-118">Description of HostPool.</span></span>

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

### <span data-ttu-id="27b78-119">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="27b78-119">-FriendlyName</span></span>
<span data-ttu-id="27b78-120">Удобное имя HostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-120">Friendly name of HostPool.</span></span>

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

### <span data-ttu-id="27b78-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27b78-121">-InputObject</span></span>
<span data-ttu-id="27b78-122">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="27b78-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="27b78-123">-LoadBalancerType</span><span class="sxs-lookup"><span data-stu-id="27b78-123">-LoadBalancerType</span></span>
<span data-ttu-id="27b78-124">Тип балансиров нагрузки.</span><span class="sxs-lookup"><span data-stu-id="27b78-124">The type of the load balancer.</span></span>

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

### <span data-ttu-id="27b78-125">-MaxSessionLimit</span><span class="sxs-lookup"><span data-stu-id="27b78-125">-MaxSessionLimit</span></span>
<span data-ttu-id="27b78-126">Максимальное ограничение сеанса в HostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-126">The max session limit of HostPool.</span></span>

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

### <span data-ttu-id="27b78-127">-Name</span><span class="sxs-lookup"><span data-stu-id="27b78-127">-Name</span></span>
<span data-ttu-id="27b78-128">Имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="27b78-128">The name of the host pool within the specified resource group</span></span>

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

### <span data-ttu-id="27b78-129">-PersonalDesktopAssignmentType</span><span class="sxs-lookup"><span data-stu-id="27b78-129">-PersonalDesktopAssignmentType</span></span>
<span data-ttu-id="27b78-130">PersonalDesktopAssignment для HostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-130">PersonalDesktopAssignment type for HostPool.</span></span>

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

### <span data-ttu-id="27b78-131">-PreferredAppGroupType</span><span class="sxs-lookup"><span data-stu-id="27b78-131">-PreferredAppGroupType</span></span>
<span data-ttu-id="27b78-132">Тип предпочитаемого типа группы приложений (по умолчанию — группа классических приложений)</span><span class="sxs-lookup"><span data-stu-id="27b78-132">The type of preferred application group type, default to Desktop Application Group</span></span>

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

### <span data-ttu-id="27b78-133">-RegistrationInfoExpirationTime</span><span class="sxs-lookup"><span data-stu-id="27b78-133">-RegistrationInfoExpirationTime</span></span>
<span data-ttu-id="27b78-134">Время окончания срока действия маркера регистрации.</span><span class="sxs-lookup"><span data-stu-id="27b78-134">Expiration time of registration token.</span></span>

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

### <span data-ttu-id="27b78-135">-RegistrationInfoRegistrationTokenOperation</span><span class="sxs-lookup"><span data-stu-id="27b78-135">-RegistrationInfoRegistrationTokenOperation</span></span>
<span data-ttu-id="27b78-136">Тип сброса маркера.</span><span class="sxs-lookup"><span data-stu-id="27b78-136">The type of resetting the token.</span></span>

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

### <span data-ttu-id="27b78-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b78-137">-ResourceGroupName</span></span>
<span data-ttu-id="27b78-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27b78-138">The name of the resource group.</span></span>
<span data-ttu-id="27b78-139">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="27b78-139">The name is case insensitive.</span></span>

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

### <span data-ttu-id="27b78-140">-Позвонить</span><span class="sxs-lookup"><span data-stu-id="27b78-140">-Ring</span></span>
<span data-ttu-id="27b78-141">Номер звонка HostPool.</span><span class="sxs-lookup"><span data-stu-id="27b78-141">The ring number of HostPool.</span></span>

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

### <span data-ttu-id="27b78-142">-SsoadfsAuthority</span><span class="sxs-lookup"><span data-stu-id="27b78-142">-SsoadfsAuthority</span></span>
<span data-ttu-id="27b78-143">URL-адрес сервера ADFS клиента для подписи сертификатов SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="27b78-143">URL to customer ADFS server for signing WVD SSO certificates.</span></span>

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

### <span data-ttu-id="27b78-144">-SsoClientId</span><span class="sxs-lookup"><span data-stu-id="27b78-144">-SsoClientId</span></span>
<span data-ttu-id="27b78-145">ClientId зарегистрированной стороны, которая использовалась для выпуска сертификатов SSO WVD.</span><span class="sxs-lookup"><span data-stu-id="27b78-145">ClientId for the registered Relying Party used to issue WVD SSO certificates.</span></span>

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

### <span data-ttu-id="27b78-146">-SsoClientSecretKeyVaultPath</span><span class="sxs-lookup"><span data-stu-id="27b78-146">-SsoClientSecretKeyVaultPath</span></span>
<span data-ttu-id="27b78-147">Путь к ключам Azure KeyVault для хранения секретов, используемых для связи с ADFS.</span><span class="sxs-lookup"><span data-stu-id="27b78-147">Path to Azure KeyVault storing the secret used for communication to ADFS.</span></span>

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

### <span data-ttu-id="27b78-148">-SsoContext</span><span class="sxs-lookup"><span data-stu-id="27b78-148">-SsoContext</span></span>
<span data-ttu-id="27b78-149">Путь к клавишам, содержащим секрет сoContext.</span><span class="sxs-lookup"><span data-stu-id="27b78-149">Path to keyvault containing ssoContext secret.</span></span>

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

### <span data-ttu-id="27b78-150">-SsoSecretType</span><span class="sxs-lookup"><span data-stu-id="27b78-150">-SsoSecretType</span></span>
<span data-ttu-id="27b78-151">Тип единого знака для секретного типа.</span><span class="sxs-lookup"><span data-stu-id="27b78-151">The type of single sign on Secret Type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.SsoSecretType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b78-152">-StartVMOnConnect</span><span class="sxs-lookup"><span data-stu-id="27b78-152">-StartVMOnConnect</span></span>
<span data-ttu-id="27b78-153">Флажок для отключения функции StartVMOnConnect.</span><span class="sxs-lookup"><span data-stu-id="27b78-153">The flag to turn on/off StartVMOnConnect feature.</span></span>

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

### <span data-ttu-id="27b78-154">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="27b78-154">-SubscriptionId</span></span>
<span data-ttu-id="27b78-155">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="27b78-155">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="27b78-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="27b78-156">-Tag</span></span>
<span data-ttu-id="27b78-157">теги для обновления</span><span class="sxs-lookup"><span data-stu-id="27b78-157">tags to be updated</span></span>

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

### <span data-ttu-id="27b78-158">-ValidationEnvironment</span><span class="sxs-lookup"><span data-stu-id="27b78-158">-ValidationEnvironment</span></span>
<span data-ttu-id="27b78-159">Это среда проверки.</span><span class="sxs-lookup"><span data-stu-id="27b78-159">Is validation environment.</span></span>

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

### <span data-ttu-id="27b78-160">-VMTemplate</span><span class="sxs-lookup"><span data-stu-id="27b78-160">-VMTemplate</span></span>
<span data-ttu-id="27b78-161">Шаблон VM для настройки sessionhosts в рамках hostpool.</span><span class="sxs-lookup"><span data-stu-id="27b78-161">VM template for sessionhosts configuration within hostpool.</span></span>

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

### <span data-ttu-id="27b78-162">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27b78-162">-Confirm</span></span>
<span data-ttu-id="27b78-163">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b78-163">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b78-164">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b78-164">-WhatIf</span></span>
<span data-ttu-id="27b78-165">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b78-165">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27b78-166">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="27b78-166">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b78-167">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b78-167">CommonParameters</span></span>
<span data-ttu-id="27b78-168">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b78-168">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b78-169">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="27b78-169">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b78-170">INPUTS</span><span class="sxs-lookup"><span data-stu-id="27b78-170">INPUTS</span></span>

### <span data-ttu-id="27b78-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="27b78-171">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="27b78-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="27b78-172">OUTPUTS</span></span>

### <span data-ttu-id="27b78-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span><span class="sxs-lookup"><span data-stu-id="27b78-173">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IHostPool</span></span>

## <span data-ttu-id="27b78-174">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="27b78-174">NOTES</span></span>

<span data-ttu-id="27b78-175">ALIASES</span><span class="sxs-lookup"><span data-stu-id="27b78-175">ALIASES</span></span>

<span data-ttu-id="27b78-176">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="27b78-176">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="27b78-177">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="27b78-177">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="27b78-178">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="27b78-178">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="27b78-179">INPUTOBJECT <IDesktopVirtualizationIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="27b78-179">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="27b78-180">`[ApplicationGroupName <String>]`: имя группы приложений</span><span class="sxs-lookup"><span data-stu-id="27b78-180">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="27b78-181">`[ApplicationName <String>]`: имя приложения в указанной группе приложений</span><span class="sxs-lookup"><span data-stu-id="27b78-181">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="27b78-182">`[DesktopName <String>]`: имя рабочего стола в указанной группе рабочего стола</span><span class="sxs-lookup"><span data-stu-id="27b78-182">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="27b78-183">`[HostPoolName <String>]`: имя пула хостов в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="27b78-183">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="27b78-184">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="27b78-184">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="27b78-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span><span class="sxs-lookup"><span data-stu-id="27b78-185">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="27b78-186">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="27b78-186">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="27b78-187">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="27b78-187">The name is case insensitive.</span></span>
  - <span data-ttu-id="27b78-188">`[SessionHostName <String>]`: имя сеанса в указанном пуле хостов</span><span class="sxs-lookup"><span data-stu-id="27b78-188">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="27b78-189">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="27b78-189">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="27b78-190">`[UserSessionId <String>]`: имя сеанса пользователя в указанном хосте сеанса</span><span class="sxs-lookup"><span data-stu-id="27b78-190">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="27b78-191">`[WorkspaceName <String>]`: имя рабочей области</span><span class="sxs-lookup"><span data-stu-id="27b78-191">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="27b78-192">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27b78-192">RELATED LINKS</span></span>

