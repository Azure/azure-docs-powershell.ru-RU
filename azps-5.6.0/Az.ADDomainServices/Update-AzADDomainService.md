---
external help file: ''
Module Name: Az.ADDomainServices
online version: https://docs.microsoft.com/powershell/module/az.addomainservices/update-azaddomainservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ADDomainServices/help/Update-AzADDomainService.md
ms.openlocfilehash: 4504eaf26331fa4e881d6a86f284a74b7f249565
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991791"
---
# <span data-ttu-id="9b85b-101">Update-AzADDomainService</span><span class="sxs-lookup"><span data-stu-id="9b85b-101">Update-AzADDomainService</span></span>

## <span data-ttu-id="9b85b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b85b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b85b-103">Операцию обновления доменной службы можно использовать для обновления существующего развертывания.</span><span class="sxs-lookup"><span data-stu-id="9b85b-103">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="9b85b-104">При вызове обновления поддерживаются только свойства, указанные в теле исправления.</span><span class="sxs-lookup"><span data-stu-id="9b85b-104">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="9b85b-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b85b-105">SYNTAX</span></span>

### <span data-ttu-id="9b85b-106">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b85b-106">UpdateExpanded (Default)</span></span>
```
Update-AzADDomainService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DomainConfigurationType <String>] [-DomainSecuritySettingNtlmV1 <String>]
 [-DomainSecuritySettingSyncKerberosPassword <String>] [-DomainSecuritySettingSyncNtlmPassword <String>]
 [-DomainSecuritySettingSyncOnPremPassword <String>] [-DomainSecuritySettingTlsV1 <String>]
 [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>] [-LdapSettingExternalAccess <String>]
 [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9b85b-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9b85b-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzADDomainService -InputObject <IAdDomainServicesIdentity> [-DomainConfigurationType <String>]
 [-DomainSecuritySettingNtlmV1 <String>] [-DomainSecuritySettingSyncKerberosPassword <String>]
 [-DomainSecuritySettingSyncNtlmPassword <String>] [-DomainSecuritySettingSyncOnPremPassword <String>]
 [-DomainSecuritySettingTlsV1 <String>] [-FilteredSync <String>] [-ForestTrust <IForestTrust[]>]
 [-LdapSettingExternalAccess <String>] [-LdapSettingLdaps <String>] [-LdapSettingPfxCertificate <String>]
 [-LdapSettingPfxCertificatePassword <SecureString>] [-NotificationSettingAdditionalRecipient <String[]>]
 [-NotificationSettingNotifyDcAdmin <String>] [-NotificationSettingNotifyGlobalAdmin <String>]
 [-ReplicaSet <IReplicaSet[]>] [-ResourceForest <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9b85b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b85b-108">DESCRIPTION</span></span>
<span data-ttu-id="9b85b-109">Операцию обновления доменной службы можно использовать для обновления существующего развертывания.</span><span class="sxs-lookup"><span data-stu-id="9b85b-109">The Update Domain Service operation can be used to update the existing deployment.</span></span>
<span data-ttu-id="9b85b-110">При вызове обновления поддерживаются только свойства, указанные в теле исправления.</span><span class="sxs-lookup"><span data-stu-id="9b85b-110">The update call only supports the properties listed in the PATCH body.</span></span>

## <span data-ttu-id="9b85b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b85b-111">EXAMPLES</span></span>

### <span data-ttu-id="9b85b-112">Пример 1. Обновление AzADDomainService по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="9b85b-112">Example 1: Update AzADDomainService By ResourceGroupName and Name</span></span>
```powershell
PS C:\> $ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="9b85b-113">Обновление AzADDomainService по resourceGroupName и Name</span><span class="sxs-lookup"><span data-stu-id="9b85b-113">Update AzADDomainService By ResourceGroupName and Name</span></span>

### <span data-ttu-id="9b85b-114">Пример 2. Обновление AzADDomainService с помощью inputobject</span><span class="sxs-lookup"><span data-stu-id="9b85b-114">Example 2: Update AzADDomainService By Inputobject</span></span>
```powershell
PS C:\> $getAzAddomain = Get-AzADDomainService -Name youriADdomain -ResourceGroupName youriADdomain
$ADDomainSetting = New-AzADDomainServiceDomainSecuritySettingObject -TlsV1 Disabled
Update-AzADDomainService -InputObject $getAzAddomain -DomainSecuritySetting $ADDomainSetting

Name          Domain Name       Location Sku
----          -----------       -------- ---
youriADdomain youriAddomain.com westus   Enterprise
```

<span data-ttu-id="9b85b-115">Обновление AzADDomainService по inputobject</span><span class="sxs-lookup"><span data-stu-id="9b85b-115">Update AzADDomainService By Inputobject</span></span>

## <span data-ttu-id="9b85b-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b85b-116">PARAMETERS</span></span>

### <span data-ttu-id="9b85b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b85b-117">-AsJob</span></span>
<span data-ttu-id="9b85b-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9b85b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="9b85b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b85b-119">-DefaultProfile</span></span>
<span data-ttu-id="9b85b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b85b-121">-DomainConfigurationType</span><span class="sxs-lookup"><span data-stu-id="9b85b-121">-DomainConfigurationType</span></span>
<span data-ttu-id="9b85b-122">Тип конфигурации домена</span><span class="sxs-lookup"><span data-stu-id="9b85b-122">Domain Configuration Type</span></span>

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

### <span data-ttu-id="9b85b-123">-DomainSecuritySettingNtlmV1</span><span class="sxs-lookup"><span data-stu-id="9b85b-123">-DomainSecuritySettingNtlmV1</span></span>
<span data-ttu-id="9b85b-124">Флажок для определения того, включена ли NtlmV1.</span><span class="sxs-lookup"><span data-stu-id="9b85b-124">A flag to determine whether or not NtlmV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-125">-DomainSecuritySettingSyncKerberosPassword</span><span class="sxs-lookup"><span data-stu-id="9b85b-125">-DomainSecuritySettingSyncKerberosPassword</span></span>
<span data-ttu-id="9b85b-126">Флаг для определения того, включена ли синхронизацияPasswords SyncKerberosPasswords.</span><span class="sxs-lookup"><span data-stu-id="9b85b-126">A flag to determine whether or not SyncKerberosPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-127">-DomainSecuritySettingSyncNtlmPassword</span><span class="sxs-lookup"><span data-stu-id="9b85b-127">-DomainSecuritySettingSyncNtlmPassword</span></span>
<span data-ttu-id="9b85b-128">Флаг для определения того, включена ли синхронизация SyncNtlmPasswords.</span><span class="sxs-lookup"><span data-stu-id="9b85b-128">A flag to determine whether or not SyncNtlmPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-129">-DomainSecuritySettingSyncOnPremPassword</span><span class="sxs-lookup"><span data-stu-id="9b85b-129">-DomainSecuritySettingSyncOnPremPassword</span></span>
<span data-ttu-id="9b85b-130">Флаг для определения того, включена ли синхронизацияOnPremPasswords.</span><span class="sxs-lookup"><span data-stu-id="9b85b-130">A flag to determine whether or not SyncOnPremPasswords is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-131">-DomainSecuritySettingTlsV1</span><span class="sxs-lookup"><span data-stu-id="9b85b-131">-DomainSecuritySettingTlsV1</span></span>
<span data-ttu-id="9b85b-132">Флажок для определения того, включена ли TlsV1.</span><span class="sxs-lookup"><span data-stu-id="9b85b-132">A flag to determine whether or not TlsV1 is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-133">-FilteredSync</span><span class="sxs-lookup"><span data-stu-id="9b85b-133">-FilteredSync</span></span>
<span data-ttu-id="9b85b-134">Включена или отключена пометка для включения отфильтрованной синхронизации с группировкой</span><span class="sxs-lookup"><span data-stu-id="9b85b-134">Enabled or Disabled flag to turn on Group-based filtered sync</span></span>

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

### <span data-ttu-id="9b85b-135">-ForestTrust</span><span class="sxs-lookup"><span data-stu-id="9b85b-135">-ForestTrust</span></span>
<span data-ttu-id="9b85b-136">Список параметров для строительства леса ресурсов. См. раздел "ПРИМЕЧАНИЯ" для свойств FORESTTRUST и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9b85b-136">List of settings for Resource Forest To construct, see NOTES section for FORESTTRUST properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b85b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b85b-137">-InputObject</span></span>
<span data-ttu-id="9b85b-138">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9b85b-138">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85b-139">-LdapSettingExternalAccess</span><span class="sxs-lookup"><span data-stu-id="9b85b-139">-LdapSettingExternalAccess</span></span>
<span data-ttu-id="9b85b-140">Флажок для определения того, включен ли безопасный доступ LDAP через Интернет.</span><span class="sxs-lookup"><span data-stu-id="9b85b-140">A flag to determine whether or not Secure LDAP access over the internet is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-141">-LdapSettingLdaps</span><span class="sxs-lookup"><span data-stu-id="9b85b-141">-LdapSettingLdaps</span></span>
<span data-ttu-id="9b85b-142">Флаг для определения того, включена ли защита LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b85b-142">A flag to determine whether or not Secure LDAP is enabled or disabled.</span></span>

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

### <span data-ttu-id="9b85b-143">-LdapSettingPfxCertificate</span><span class="sxs-lookup"><span data-stu-id="9b85b-143">-LdapSettingPfxCertificate</span></span>
<span data-ttu-id="9b85b-144">Сертификат, необходимый для настройки Secure LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b85b-144">The certificate required to configure Secure LDAP.</span></span>
<span data-ttu-id="9b85b-145">Параметр, переданный здесь, должен быть основанием64encoded представления pfx-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="9b85b-145">The parameter passed here should be a base64encoded representation of the certificate pfx file.</span></span>

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

### <span data-ttu-id="9b85b-146">-LdapSettingPfxCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="9b85b-146">-LdapSettingPfxCertificatePassword</span></span>
<span data-ttu-id="9b85b-147">Пароль для расшифровки предоставленного PFX-файла сертификата LDAP.</span><span class="sxs-lookup"><span data-stu-id="9b85b-147">The password to decrypt the provided Secure LDAP certificate pfx file.</span></span>

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

### <span data-ttu-id="9b85b-148">-Name</span><span class="sxs-lookup"><span data-stu-id="9b85b-148">-Name</span></span>
<span data-ttu-id="9b85b-149">Имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="9b85b-149">The name of the domain service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DomainServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85b-150">-NotificationSettingAdditionalRecipient</span><span class="sxs-lookup"><span data-stu-id="9b85b-150">-NotificationSettingAdditionalRecipient</span></span>
<span data-ttu-id="9b85b-151">Список дополнительных получателей</span><span class="sxs-lookup"><span data-stu-id="9b85b-151">The list of additional recipients</span></span>

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

### <span data-ttu-id="9b85b-152">-NotificationSettingNotifyDcAdmin</span><span class="sxs-lookup"><span data-stu-id="9b85b-152">-NotificationSettingNotifyDcAdmin</span></span>
<span data-ttu-id="9b85b-153">Следует ли уведомить администраторов контроллера домена</span><span class="sxs-lookup"><span data-stu-id="9b85b-153">Should domain controller admins be notified</span></span>

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

### <span data-ttu-id="9b85b-154">-NotificationSettingNotifyBalAdmin</span><span class="sxs-lookup"><span data-stu-id="9b85b-154">-NotificationSettingNotifyGlobalAdmin</span></span>
<span data-ttu-id="9b85b-155">Должны ли глобальные администраторы быть уведомлены</span><span class="sxs-lookup"><span data-stu-id="9b85b-155">Should global admins be notified</span></span>

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

### <span data-ttu-id="9b85b-156">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9b85b-156">-NoWait</span></span>
<span data-ttu-id="9b85b-157">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9b85b-157">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9b85b-158">-ReplicaSet</span><span class="sxs-lookup"><span data-stu-id="9b85b-158">-ReplicaSet</span></span>
<span data-ttu-id="9b85b-159">Список наборов реплик для сстройки, см. раздел "ЗАМЕТКИ" для свойств REPLICASET и создание таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="9b85b-159">List of ReplicaSets To construct, see NOTES section for REPLICASET properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IReplicaSet[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85b-160">-ResourceForest</span><span class="sxs-lookup"><span data-stu-id="9b85b-160">-ResourceForest</span></span>
<span data-ttu-id="9b85b-161">Лес ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b85b-161">Resource Forest</span></span>

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

### <span data-ttu-id="9b85b-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b85b-162">-ResourceGroupName</span></span>
<span data-ttu-id="9b85b-163">Имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b85b-163">The name of the resource group within the user's subscription.</span></span>
<span data-ttu-id="9b85b-164">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9b85b-164">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9b85b-165">-SKU</span><span class="sxs-lookup"><span data-stu-id="9b85b-165">-Sku</span></span>
<span data-ttu-id="9b85b-166">Тип SKU</span><span class="sxs-lookup"><span data-stu-id="9b85b-166">Sku Type</span></span>

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

### <span data-ttu-id="9b85b-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9b85b-167">-SubscriptionId</span></span>
<span data-ttu-id="9b85b-168">Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85b-168">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9b85b-169">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9b85b-169">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b85b-170">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b85b-170">-Tag</span></span>
<span data-ttu-id="9b85b-171">Теги ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b85b-171">Resource tags</span></span>

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

### <span data-ttu-id="9b85b-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b85b-172">-Confirm</span></span>
<span data-ttu-id="9b85b-173">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b85b-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b85b-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b85b-174">-WhatIf</span></span>
<span data-ttu-id="9b85b-175">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b85b-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b85b-176">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b85b-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b85b-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b85b-177">CommonParameters</span></span>
<span data-ttu-id="9b85b-178">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b85b-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b85b-179">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b85b-179">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b85b-180">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b85b-180">INPUTS</span></span>

### <span data-ttu-id="9b85b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="9b85b-181">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.IAdDomainServicesIdentity</span></span>

## <span data-ttu-id="9b85b-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b85b-182">OUTPUTS</span></span>

### <span data-ttu-id="9b85b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span><span class="sxs-lookup"><span data-stu-id="9b85b-183">Microsoft.Azure.PowerShell.Cmdlets.ADDomainServices.Models.Api202001.IDomainService</span></span>

## <span data-ttu-id="9b85b-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b85b-184">NOTES</span></span>

<span data-ttu-id="9b85b-185">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9b85b-185">ALIASES</span></span>

<span data-ttu-id="9b85b-186">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9b85b-186">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b85b-187">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9b85b-187">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b85b-188">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b85b-188">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b85b-189">FORESTTRUST <IForestTrust[]>: список параметров для леса ресурсов</span><span class="sxs-lookup"><span data-stu-id="9b85b-189">FORESTTRUST <IForestTrust[]>: List of settings for Resource Forest</span></span>
  - <span data-ttu-id="9b85b-190">`[FriendlyName <String>]`: Удобное имя</span><span class="sxs-lookup"><span data-stu-id="9b85b-190">`[FriendlyName <String>]`: Friendly Name</span></span>
  - <span data-ttu-id="9b85b-191">`[RemoteDnsIP <String>]`: Remote DNS ips</span><span class="sxs-lookup"><span data-stu-id="9b85b-191">`[RemoteDnsIP <String>]`: Remote Dns ips</span></span>
  - <span data-ttu-id="9b85b-192">`[TrustDirection <String>]`: Trust Direction</span><span class="sxs-lookup"><span data-stu-id="9b85b-192">`[TrustDirection <String>]`: Trust Direction</span></span>
  - <span data-ttu-id="9b85b-193">`[TrustPassword <String>]`: Trust Password</span><span class="sxs-lookup"><span data-stu-id="9b85b-193">`[TrustPassword <String>]`: Trust Password</span></span>
  - <span data-ttu-id="9b85b-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span><span class="sxs-lookup"><span data-stu-id="9b85b-194">`[TrustedDomainFqdn <String>]`: Trusted Domain FQDN</span></span>

<span data-ttu-id="9b85b-195">INPUTOBJECT <IAdDomainServicesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9b85b-195">INPUTOBJECT <IAdDomainServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b85b-196">`[DomainServiceName <String>]`: имя службы домена.</span><span class="sxs-lookup"><span data-stu-id="9b85b-196">`[DomainServiceName <String>]`: The name of the domain service.</span></span>
  - <span data-ttu-id="9b85b-197">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9b85b-197">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b85b-198">`[ResourceGroupName <String>]`: имя группы ресурсов в подписке пользователя.</span><span class="sxs-lookup"><span data-stu-id="9b85b-198">`[ResourceGroupName <String>]`: The name of the resource group within the user's subscription.</span></span> <span data-ttu-id="9b85b-199">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9b85b-199">The name is case insensitive.</span></span>
  - <span data-ttu-id="9b85b-200">`[SubscriptionId <String>]`. Получает учетные данные подписки, которые однозначно определяют подписку на Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85b-200">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="9b85b-201">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="9b85b-201">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="9b85b-202">REPLICASET <IReplicaSet[]>: список реплик</span><span class="sxs-lookup"><span data-stu-id="9b85b-202">REPLICASET <IReplicaSet[]>: List of ReplicaSets</span></span>
  - <span data-ttu-id="9b85b-203">`[Location <String>]`: расположение в виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="9b85b-203">`[Location <String>]`: Virtual network location</span></span>
  - <span data-ttu-id="9b85b-204">`[SubnetId <String>]`. Название виртуальной сети, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="9b85b-204">`[SubnetId <String>]`: The name of the virtual network that Domain Services will be deployed on.</span></span> <span data-ttu-id="9b85b-205">Id подсеть, в которую будут развернуты доменные службы.</span><span class="sxs-lookup"><span data-stu-id="9b85b-205">The id of the subnet that Domain Services will be deployed on.</span></span> <span data-ttu-id="9b85b-206">/virtualNetwork/vnetName/subnets/subnetName.</span><span class="sxs-lookup"><span data-stu-id="9b85b-206">/virtualNetwork/vnetName/subnets/subnetName.</span></span>

## <span data-ttu-id="9b85b-207">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b85b-207">RELATED LINKS</span></span>

