---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.addomainservices/new-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/New-AzADDomainService.md
ms.openlocfilehash: 977621a3f92a8239925494102aed8c672509b222
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210668"
---
# <span data-ttu-id="919a5-101">New-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="919a5-101">New-AzADDomainService</span></span>

## <span data-ttu-id="919a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="919a5-102">SYNOPSIS</span></span>
<span data-ttu-id="919a5-103">В ходе операции создания службы домена создается новая доменная служба с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="919a5-103">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="919a5-104">Если определенная служба уже существует, все исправления будут обновлены и неизменяемые свойства останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="919a5-104">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="919a5-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="919a5-105">SYNTAX</span></span>

```
New-AzADDomainService -Name <String> -ResourceGroupName <String> -DomainName <String>
 -ReplicaSet <IReplicaSet[]> [-SubscriptionId <String>] [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="919a5-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="919a5-106">DESCRIPTION</span></span>
<span data-ttu-id="919a5-107">В ходе операции создания службы домена создается новая доменная служба с указанными параметрами.</span><span class="sxs-lookup"><span data-stu-id="919a5-107">The Create Domain Service operation creates a new domain service with the specified parameters.</span></span>
<span data-ttu-id="919a5-108">Если определенная служба уже существует, все исправления будут обновлены и неизменяемые свойства останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="919a5-108">If the specific service already exists, then any patchable properties will be updated and any immutable properties will remain unchanged.</span></span>

## <span data-ttu-id="919a5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="919a5-109">EXAMPLES</span></span>

### <span data-ttu-id="919a5-110">Пример 1. Создание новой службы ADDomainService</span><span class="sxs-lookup"><span data-stu-id="919a5-110">Example 1: Create new ADDomainService</span></span>
```powershell
PS C:\> $replicaSet = New-AzADDomainServiceReplicaSetObject -Location westus -SubnetId /subscriptions/********-****-****-****-**********/resourceGroups/yishitest/providers/Microsoft.Network/virtualNetworks/aadds-vnet/subnets/default
New-AzADDomainService -name youriADdomain -ResourceGroupName youriAddomain -DomainName youriAddomain.com -ReplicaSet $replicaSet -debug

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="919a5-111">Создание ADDomainService</span><span class="sxs-lookup"><span data-stu-id="919a5-111">Create new ADDomainService</span></span>

## <span data-ttu-id="919a5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="919a5-112">PARAMETERS</span></span>

### <span data-ttu-id="919a5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="919a5-113">-AsJob</span></span>
<span data-ttu-id="919a5-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="919a5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="919a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="919a5-115">-DefaultProfile</span></span>
<span data-ttu-id="919a5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="919a5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="919a5-117">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="919a5-117">-DomainConfigurationType</span></span>
<span data-ttu-id="919a5-118">Тип конфигурации домена</span><span class="sxs-lookup"><span data-stu-id="919a5-118">Domain Configuration Type</span></span>

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

### <span data-ttu-id="919a5-119">-DomainName</span><span class="sxs-lookup"><span data-stu-id="919a5-119">-DomainName</span></span>
<span data-ttu-id="919a5-120">Имя домена Azure, для которого пользователь хочет развернуть доменные службы.</span><span class="sxs-lookup"><span data-stu-id="919a5-120">The name of the Azure domain that the user would like to deploy Domain Services to.</span></span>

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

### <span data-ttu-id="919a5-121">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="919a5-121">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="919a5-122">Флажок для определения того, включена ли NtlmV1.</span><span class="sxs-lookup"><span data-stu-id="919a5-122">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-123">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="919a5-123">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="919a5-124">Флаг для определения того, включена ли синхронизацияPasswords SyncKerberosPasswords.</span><span class="sxs-lookup"><span data-stu-id="919a5-124">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-125">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="919a5-125">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="919a5-126">Флаг для определения того, включена ли синхронизация SyncNtlmPasswords.</span><span class="sxs-lookup"><span data-stu-id="919a5-126">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-127">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="919a5-127">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="919a5-128">Флаг для определения того, включена ли синхронизацияOnPremPasswords.</span><span class="sxs-lookup"><span data-stu-id="919a5-128">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-129">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="919a5-129">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="919a5-130">Флажок для определения того, включена ли TlsV1.</span><span class="sxs-lookup"><span data-stu-id="919a5-130">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-131">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="919a5-131">-FilteredSync</span></span>
<span data-ttu-id="919a5-132">Включена или отключена пометка для включения отфильтрованной синхронизации с группировкой</span><span class="sxs-lookup"><span data-stu-id="919a5-132">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="919a5-133">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="919a5-133">-ForestTrust</span></span>
<span data-ttu-id="919a5-134">Список параметров для строительства леса ресурсов. См. раздел "ПРИМЕЧАНИЯ" для свойств FORESTTRUST и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="919a5-134">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IForestTrust[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919a5-135">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="919a5-135">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="919a5-136">Флажок для определения того, включен ли безопасный доступ LDAP через Интернет.</span><span class="sxs-lookup"><span data-stu-id="919a5-136">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-137">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="919a5-137">-LdapSettingLdaps</span></span>
<span data-ttu-id="919a5-138">Флаг для определения того, включена ли защита LDAP.</span><span class="sxs-lookup"><span data-stu-id="919a5-138">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="919a5-139">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="919a5-139">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="919a5-140">Сертификат, необходимый для настройки Secure LDAP.</span><span class="sxs-lookup"><span data-stu-id="919a5-140">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="919a5-141">Параметр, переданный здесь, должен быть основанием64encoded представления pfx-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="919a5-141">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="919a5-142">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="919a5-142">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="919a5-143">Пароль для расшифровки предоставленного PFX-файла сертификата Secure LDAP.</span><span class="sxs-lookup"><span data-stu-id="919a5-143">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919a5-144">-Name</span><span class="sxs-lookup"><span data-stu-id="919a5-144">-Name</span></span>
<span data-ttu-id="919a5-145">Имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="919a5-145">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919a5-146">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="919a5-146">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="919a5-147">Список дополнительных получателей</span><span class="sxs-lookup"><span data-stu-id="919a5-147">The list of additional recipients</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919a5-148">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="919a5-148">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="919a5-149">Следует ли уведомить администраторов контроллера домена</span><span class="sxs-lookup"><span data-stu-id="919a5-149">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="919a5-150">-NotificationSettingNotifyBalAdmin</span><span class="sxs-lookup"><span data-stu-id="919a5-150">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="919a5-151">Должны ли глобальные администраторы быть уведомлены</span><span class="sxs-lookup"><span data-stu-id="919a5-151">Should global admins be notified</span></span>

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

### <span data-ttu-id="919a5-152">-NoWait</span><span class="sxs-lookup"><span data-stu-id="919a5-152">-NoWait</span></span>
<span data-ttu-id="919a5-153">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="919a5-153">Run the command asynchronously</span></span>

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

### <span data-ttu-id="919a5-154">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="919a5-154">-ReplicaSet</span></span>
<span data-ttu-id="919a5-155">Список наборов реплик для сстройки, см. раздел "ЗАМЕТКИ" для свойств REPLICASET и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="919a5-155">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="919a5-156">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="919a5-156">-ResourceForest</span></span>
<span data-ttu-id="919a5-157">Лес ресурсов</span><span class="sxs-lookup"><span data-stu-id="919a5-157">Resource Forest</span></span>

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

### <span data-ttu-id="919a5-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="919a5-158">-ResourceGroupName</span></span>
<span data-ttu-id="919a5-159">Имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="919a5-159">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="919a5-160">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="919a5-160">The name is case insensitive.</span></span>

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

### <span data-ttu-id="919a5-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="919a5-161">-Sku</span></span>
<span data-ttu-id="919a5-162">Тип SKU</span><span class="sxs-lookup"><span data-stu-id="919a5-162">Sku Type</span></span>

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

### <span data-ttu-id="919a5-163">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="919a5-163">-SubscriptionId</span></span>
<span data-ttu-id="919a5-164">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="919a5-164">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="919a5-165">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="919a5-165">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="919a5-166">-Tag</span><span class="sxs-lookup"><span data-stu-id="919a5-166">-Tag</span></span>
<span data-ttu-id="919a5-167">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="919a5-167">Resource tags</span></span>

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

### <span data-ttu-id="919a5-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="919a5-168">-Confirm</span></span>
<span data-ttu-id="919a5-169">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919a5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="919a5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="919a5-170">-WhatIf</span></span>
<span data-ttu-id="919a5-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="919a5-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="919a5-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="919a5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="919a5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="919a5-173">CommonParameters</span></span>
<span data-ttu-id="919a5-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="919a5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="919a5-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="919a5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="919a5-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="919a5-176">INPUTS</span></span>

## <span data-ttu-id="919a5-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="919a5-177">OUTPUTS</span></span>

### <span data-ttu-id="919a5-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="919a5-178">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="919a5-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="919a5-179">NOTES</span></span>

<span data-ttu-id="919a5-180">ALIASES</span><span class="sxs-lookup"><span data-stu-id="919a5-180">ALIASES</span></span>

<span data-ttu-id="919a5-181">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="919a5-181">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="919a5-182">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="919a5-182">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="919a5-183">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="919a5-183">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="919a5-184">FORESTTRUST <IForestTrust[]>: список параметров для леса ресурсов</span><span class="sxs-lookup"><span data-stu-id="919a5-184">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="919a5-185">`[FriendlyName <String>]`: Удобное имя</span><span class="sxs-lookup"><span data-stu-id="919a5-185">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="919a5-186">`[RemoteDnsIP <String>]`: Remote DNS ips</span><span class="sxs-lookup"><span data-stu-id="919a5-186">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="919a5-187">`[TrustDirection <String>]`: Trust Direction</span><span class="sxs-lookup"><span data-stu-id="919a5-187">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="919a5-188">`[TrustPassword <String>]`: Trust Password</span><span class="sxs-lookup"><span data-stu-id="919a5-188">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="919a5-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span><span class="sxs-lookup"><span data-stu-id="919a5-189">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="919a5-190">REPLICASET <IReplicaSet[]>: список реплик</span><span class="sxs-lookup"><span data-stu-id="919a5-190">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="919a5-191">`[Location <String>]`: расположение в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="919a5-191">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="919a5-192">`[SubnetId <String>]`. Название виртуальной сети, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="919a5-192">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="919a5-193">Id подсеть, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="919a5-193">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="919a5-194">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="919a5-194">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="919a5-195">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="919a5-195">RELATED LINKS</span></span>

