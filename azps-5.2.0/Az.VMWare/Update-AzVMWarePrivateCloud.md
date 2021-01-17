---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403239"
---
# <span data-ttu-id="b15da-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="b15da-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="b15da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b15da-102">SYNOPSIS</span></span>
<span data-ttu-id="b15da-103">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="b15da-103">Update a private cloud</span></span>

## <span data-ttu-id="b15da-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b15da-104">SYNTAX</span></span>

### <span data-ttu-id="b15da-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b15da-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b15da-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b15da-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b15da-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b15da-107">DESCRIPTION</span></span>
<span data-ttu-id="b15da-108">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="b15da-108">Update a private cloud</span></span>

## <span data-ttu-id="b15da-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b15da-109">EXAMPLES</span></span>

### <span data-ttu-id="b15da-110">Пример 1. Обновление размера закрытого облака по имени</span><span class="sxs-lookup"><span data-stu-id="b15da-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="b15da-111">Обновление размера частного облака по имени</span><span class="sxs-lookup"><span data-stu-id="b15da-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="b15da-112">Пример 2. Обновление размера закрытого облака с помощью входного объекта</span><span class="sxs-lookup"><span data-stu-id="b15da-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="b15da-113">Обновление размера закрытого облака с помощью объекта ввода</span><span class="sxs-lookup"><span data-stu-id="b15da-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="b15da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b15da-114">PARAMETERS</span></span>

### <span data-ttu-id="b15da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b15da-115">-AsJob</span></span>
<span data-ttu-id="b15da-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="b15da-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b15da-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b15da-117">-DefaultProfile</span></span>
<span data-ttu-id="b15da-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b15da-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b15da-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="b15da-119">-IdentitySource</span></span>
<span data-ttu-id="b15da-120">VCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="b15da-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IIdentitySource[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15da-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b15da-121">-InputObject</span></span>
<span data-ttu-id="b15da-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b15da-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b15da-123">-Интернет</span><span class="sxs-lookup"><span data-stu-id="b15da-123">-Internet</span></span>
<span data-ttu-id="b15da-124">Подключение к Интернету включено или отключено</span><span class="sxs-lookup"><span data-stu-id="b15da-124">Connectivity to internet is enabled or disabled</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.VMWare.Support.InternetEnum
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b15da-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="b15da-125">-ManagementClusterSize</span></span>
<span data-ttu-id="b15da-126">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="b15da-126">The cluster size</span></span>

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

### <span data-ttu-id="b15da-127">-Name</span><span class="sxs-lookup"><span data-stu-id="b15da-127">-Name</span></span>
<span data-ttu-id="b15da-128">Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="b15da-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="b15da-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b15da-129">-NoWait</span></span>
<span data-ttu-id="b15da-130">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="b15da-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b15da-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b15da-131">-ResourceGroupName</span></span>
<span data-ttu-id="b15da-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b15da-132">The name of the resource group.</span></span>
<span data-ttu-id="b15da-133">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b15da-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b15da-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b15da-134">-SubscriptionId</span></span>
<span data-ttu-id="b15da-135">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b15da-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b15da-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="b15da-136">-Tag</span></span>
<span data-ttu-id="b15da-137">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b15da-137">Resource tags.</span></span>

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

### <span data-ttu-id="b15da-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b15da-138">-Confirm</span></span>
<span data-ttu-id="b15da-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b15da-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b15da-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b15da-140">-WhatIf</span></span>
<span data-ttu-id="b15da-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b15da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b15da-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b15da-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b15da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b15da-143">CommonParameters</span></span>
<span data-ttu-id="b15da-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b15da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b15da-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b15da-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b15da-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b15da-146">INPUTS</span></span>

### <span data-ttu-id="b15da-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="b15da-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="b15da-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b15da-148">OUTPUTS</span></span>

### <span data-ttu-id="b15da-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="b15da-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="b15da-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b15da-150">NOTES</span></span>

<span data-ttu-id="b15da-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b15da-151">ALIASES</span></span>

<span data-ttu-id="b15da-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b15da-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b15da-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b15da-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b15da-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b15da-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b15da-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span><span class="sxs-lookup"><span data-stu-id="b15da-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="b15da-156">`[Alias <String>]`: доменное имя NetBIOS</span><span class="sxs-lookup"><span data-stu-id="b15da-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="b15da-157">`[BaseGroupDn <String>]`: базовое различается имя группы</span><span class="sxs-lookup"><span data-stu-id="b15da-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="b15da-158">`[BaseUserDn <String>]`: базовое различается имя для пользователей.</span><span class="sxs-lookup"><span data-stu-id="b15da-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="b15da-159">`[Domain <String>]`: имя DNS домена</span><span class="sxs-lookup"><span data-stu-id="b15da-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="b15da-160">`[Name <String>]`: имя источника удостоверений</span><span class="sxs-lookup"><span data-stu-id="b15da-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="b15da-161">`[Password <String>]`Пароль пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="b15da-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="b15da-162">`[PrimaryServer <String>]`: URL-адрес основного сервера</span><span class="sxs-lookup"><span data-stu-id="b15da-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="b15da-163">`[SecondaryServer <String>]`: URL-адрес дополнительного сервера</span><span class="sxs-lookup"><span data-stu-id="b15da-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="b15da-164">`[Ssl <SslEnum?>]`: защита связи LDAP с помощью SSL-сертификата (LDAPS)</span><span class="sxs-lookup"><span data-stu-id="b15da-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="b15da-165">`[Username <String>]`: ИД пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="b15da-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="b15da-166">INPUTOBJECT <IVMWareIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b15da-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b15da-167">`[AuthorizationName <String>]`: Имя авторизации каналов ExpressRoute в частном облаке</span><span class="sxs-lookup"><span data-stu-id="b15da-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="b15da-168">`[ClusterName <String>]`: название кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="b15da-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="b15da-169">`[HcxEnterpriseSiteName <String>]`: имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="b15da-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="b15da-170">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b15da-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b15da-171">`[Location <String>]`: регион Azure</span><span class="sxs-lookup"><span data-stu-id="b15da-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="b15da-172">`[PrivateCloudName <String>]`: Имя закрытого облака</span><span class="sxs-lookup"><span data-stu-id="b15da-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="b15da-173">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b15da-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b15da-174">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="b15da-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="b15da-175">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="b15da-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="b15da-176">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b15da-176">RELATED LINKS</span></span>

