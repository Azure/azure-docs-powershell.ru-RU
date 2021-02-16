---
external help file: ''
Module Name: Az.VMware
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMware/help/Update-AzVMwarePrivateCloud.md
ms.openlocfilehash: dbea608c24d8da8fa292316653b3e16953aed8b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242960"
---
# <span data-ttu-id="31816-101">Update-AzVMwarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="31816-101">Update-AzVMwarePrivateCloud</span></span>

## <span data-ttu-id="31816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31816-102">SYNOPSIS</span></span>
<span data-ttu-id="31816-103">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="31816-103">Update a private cloud</span></span>

## <span data-ttu-id="31816-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="31816-104">SYNTAX</span></span>

### <span data-ttu-id="31816-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31816-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMwarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31816-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="31816-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMwarePrivateCloud -InputObject <IVMwareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31816-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31816-107">DESCRIPTION</span></span>
<span data-ttu-id="31816-108">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="31816-108">Update a private cloud</span></span>

## <span data-ttu-id="31816-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="31816-109">EXAMPLES</span></span>

### <span data-ttu-id="31816-110">Пример 1. Обновление размера закрытого облака по имени</span><span class="sxs-lookup"><span data-stu-id="31816-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMwarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="31816-111">Обновление размера частного облака по имени</span><span class="sxs-lookup"><span data-stu-id="31816-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="31816-112">Пример 2. Обновление размера закрытого облака с помощью входного объекта</span><span class="sxs-lookup"><span data-stu-id="31816-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMwarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMwarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="31816-113">Обновление размера закрытого облака с помощью объекта ввода</span><span class="sxs-lookup"><span data-stu-id="31816-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="31816-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31816-114">PARAMETERS</span></span>

### <span data-ttu-id="31816-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="31816-115">-AsJob</span></span>
<span data-ttu-id="31816-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="31816-116">Run the command as a job</span></span>

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

### <span data-ttu-id="31816-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31816-117">-DefaultProfile</span></span>
<span data-ttu-id="31816-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31816-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31816-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="31816-119">-IdentitySource</span></span>
<span data-ttu-id="31816-120">VCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="31816-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31816-121">-InputObject</span></span>
<span data-ttu-id="31816-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="31816-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31816-123">-Интернет</span><span class="sxs-lookup"><span data-stu-id="31816-123">-Internet</span></span>
<span data-ttu-id="31816-124">Подключение к Интернету включено или отключено</span><span class="sxs-lookup"><span data-stu-id="31816-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMware.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="31816-125">-ManagementClusterSize</span></span>
<span data-ttu-id="31816-126">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="31816-126">The cluster size</span></span>

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

### <span data-ttu-id="31816-127">-Name</span><span class="sxs-lookup"><span data-stu-id="31816-127">-Name</span></span>
<span data-ttu-id="31816-128">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="31816-128">Name of the private cloud</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PrivateCloudName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31816-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="31816-129">-NoWait</span></span>
<span data-ttu-id="31816-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="31816-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="31816-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31816-131">-ResourceGroupName</span></span>
<span data-ttu-id="31816-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31816-132">The name of the resource group.</span></span>
<span data-ttu-id="31816-133">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="31816-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="31816-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31816-134">-SubscriptionId</span></span>
<span data-ttu-id="31816-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="31816-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="31816-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="31816-136">-Tag</span></span>
<span data-ttu-id="31816-137">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31816-137">Resource tags.</span></span>

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

### <span data-ttu-id="31816-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31816-138">-Confirm</span></span>
<span data-ttu-id="31816-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="31816-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31816-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31816-140">-WhatIf</span></span>
<span data-ttu-id="31816-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31816-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31816-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="31816-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31816-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31816-143">CommonParameters</span></span>
<span data-ttu-id="31816-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31816-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31816-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31816-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31816-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="31816-146">INPUTS</span></span>

### <span data-ttu-id="31816-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span><span class="sxs-lookup"><span data-stu-id="31816-147">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.IVMwareIdentity</span></span>

## <span data-ttu-id="31816-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="31816-148">OUTPUTS</span></span>

### <span data-ttu-id="31816-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="31816-149">Microsoft.Azure.PowerShell.Cmdlets.VMware.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="31816-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="31816-150">NOTES</span></span>

<span data-ttu-id="31816-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="31816-151">ALIASES</span></span>

<span data-ttu-id="31816-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="31816-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31816-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="31816-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31816-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="31816-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31816-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="31816-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="31816-156">`[Alias <String>]`: имя домена NetBIOS</span><span class="sxs-lookup"><span data-stu-id="31816-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="31816-157">`[BaseGroupDn <String>]`: базовое различается имя группы</span><span class="sxs-lookup"><span data-stu-id="31816-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="31816-158">`[BaseUserDn <String>]`: базовое различается имя для пользователей.</span><span class="sxs-lookup"><span data-stu-id="31816-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="31816-159">`[Domain <String>]`: DNS-имя домена</span><span class="sxs-lookup"><span data-stu-id="31816-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="31816-160">`[Name <String>]`: имя источника удостоверений</span><span class="sxs-lookup"><span data-stu-id="31816-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="31816-161">`[Password <String>]`Пароль пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="31816-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="31816-162">`[PrimaryServer <String>]`: URL-адрес основного сервера</span><span class="sxs-lookup"><span data-stu-id="31816-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="31816-163">`[SecondaryServer <String>]`: URL-адрес дополнительного сервера</span><span class="sxs-lookup"><span data-stu-id="31816-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="31816-164">`[Ssl <SslEnum?>]`: защита связи через LDAP с помощью SSL-сертификата (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="31816-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="31816-165">`[Username <String>]`: ИД пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="31816-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="31816-166">INPUTOBJECT <IVMwareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="31816-166">INPUTOBJECT <IVMwareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31816-167">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="31816-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="31816-168">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="31816-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="31816-169">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в закрытом облаке</span><span class="sxs-lookup"><span data-stu-id="31816-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="31816-170">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="31816-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31816-171">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="31816-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="31816-172">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="31816-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="31816-173">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31816-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="31816-174">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="31816-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="31816-175">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="31816-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="31816-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31816-176">RELATED LINKS</span></span>

