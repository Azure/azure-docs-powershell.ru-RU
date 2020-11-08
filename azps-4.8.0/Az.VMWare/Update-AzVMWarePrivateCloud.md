---
external help file: ''
Module Name: Az.VMWare
online version: https://docs.microsoft.com/en-us/powershell/module/az.vmware/update-azvmwareprivatecloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/VMWare/help/Update-AzVMWarePrivateCloud.md
ms.openlocfilehash: e47cf4fe3eef11664640e947b7093dc302f90ea3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236922"
---
# <span data-ttu-id="db058-101">Update-AzVMWarePrivateCloud</span><span class="sxs-lookup"><span data-stu-id="db058-101">Update-AzVMWarePrivateCloud</span></span>

## <span data-ttu-id="db058-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db058-102">SYNOPSIS</span></span>
<span data-ttu-id="db058-103">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="db058-103">Update a private cloud</span></span>

## <span data-ttu-id="db058-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db058-104">SYNTAX</span></span>

### <span data-ttu-id="db058-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="db058-105">UpdateExpanded (Default)</span></span>
```
Update-AzVMWarePrivateCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IdentitySource <IIdentitySource[]>] [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="db058-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="db058-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzVMWarePrivateCloud -InputObject <IVMWareIdentity> [-IdentitySource <IIdentitySource[]>]
 [-Internet <InternetEnum>] [-ManagementClusterSize <Int32>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="db058-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db058-107">DESCRIPTION</span></span>
<span data-ttu-id="db058-108">Обновление частного облака</span><span class="sxs-lookup"><span data-stu-id="db058-108">Update a private cloud</span></span>

## <span data-ttu-id="db058-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db058-109">EXAMPLES</span></span>

### <span data-ttu-id="db058-110">Пример 1: Обновление размера частного облака по имени</span><span class="sxs-lookup"><span data-stu-id="db058-110">Example 1: Update size of private cloud by name</span></span>
```powershell
PS C:\> Update-AzVMWarePrivateCloud -Name azps-test-cloud -ResourceGroupName azps-test-group -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="db058-111">Обновление размера частного облака по имени</span><span class="sxs-lookup"><span data-stu-id="db058-111">Update size of private cloud by name</span></span>

### <span data-ttu-id="db058-112">Пример 2: Обновление размера частного облака по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="db058-112">Example 2: Update size of private cloud by input object</span></span>
```powershell
PS C:\> Get-AzVMWarePrivateCloud -ResourceGroupName azps-test-group -Name azps-test-cloud | Update-AzVMWarePrivateCloud -ManagementClusterSize 4

Location      Name            Type
--------      ----            ----
australiaeast azps-test-cloud Microsoft.AVS/privateClouds
```

<span data-ttu-id="db058-113">Обновление размера частного облака по объекту ввода</span><span class="sxs-lookup"><span data-stu-id="db058-113">Update size of private cloud by input object</span></span>

## <span data-ttu-id="db058-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db058-114">PARAMETERS</span></span>

### <span data-ttu-id="db058-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="db058-115">-AsJob</span></span>
<span data-ttu-id="db058-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="db058-116">Run the command as a job</span></span>

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

### <span data-ttu-id="db058-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db058-117">-DefaultProfile</span></span>
<span data-ttu-id="db058-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db058-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db058-119">-IdentitySource</span><span class="sxs-lookup"><span data-stu-id="db058-119">-IdentitySource</span></span>
<span data-ttu-id="db058-120">Источники удостоверения единого входа vCenter для конструирования: раздел "Заметки" для свойств IDENTITYSOURCE и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="db058-120">vCenter Single Sign On Identity Sources To construct, see NOTES section for IDENTITYSOURCE properties and create a hash table.</span></span>

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

### <span data-ttu-id="db058-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="db058-121">-InputObject</span></span>
<span data-ttu-id="db058-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="db058-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="db058-123">-Интернет</span><span class="sxs-lookup"><span data-stu-id="db058-123">-Internet</span></span>
<span data-ttu-id="db058-124">Возможность подключения к Интернету включена или отключена</span><span class="sxs-lookup"><span data-stu-id="db058-124">Connectivity to internet is enabled or disabled</span></span>

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

### <span data-ttu-id="db058-125">-ManagementClusterSize</span><span class="sxs-lookup"><span data-stu-id="db058-125">-ManagementClusterSize</span></span>
<span data-ttu-id="db058-126">Размер кластера</span><span class="sxs-lookup"><span data-stu-id="db058-126">The cluster size</span></span>

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

### <span data-ttu-id="db058-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="db058-127">-Name</span></span>
<span data-ttu-id="db058-128">Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="db058-128">Name of the private cloud</span></span>

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

### <span data-ttu-id="db058-129">-Wait</span><span class="sxs-lookup"><span data-stu-id="db058-129">-NoWait</span></span>
<span data-ttu-id="db058-130">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="db058-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="db058-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db058-131">-ResourceGroupName</span></span>
<span data-ttu-id="db058-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db058-132">The name of the resource group.</span></span>
<span data-ttu-id="db058-133">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="db058-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="db058-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="db058-134">-SubscriptionId</span></span>
<span data-ttu-id="db058-135">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="db058-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="db058-136">-Тег</span><span class="sxs-lookup"><span data-stu-id="db058-136">-Tag</span></span>
<span data-ttu-id="db058-137">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db058-137">Resource tags.</span></span>

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

### <span data-ttu-id="db058-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db058-138">-Confirm</span></span>
<span data-ttu-id="db058-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="db058-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db058-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db058-140">-WhatIf</span></span>
<span data-ttu-id="db058-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="db058-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db058-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="db058-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db058-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db058-143">CommonParameters</span></span>
<span data-ttu-id="db058-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db058-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db058-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db058-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db058-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db058-146">INPUTS</span></span>

### <span data-ttu-id="db058-147">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. IVMWareIdentity</span><span class="sxs-lookup"><span data-stu-id="db058-147">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.IVMWareIdentity</span></span>

## <span data-ttu-id="db058-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db058-148">OUTPUTS</span></span>

### <span data-ttu-id="db058-149">Microsoft. Azure. PowerShell. командлеты. VMWare. Models. Api20200320. IPrivateCloud</span><span class="sxs-lookup"><span data-stu-id="db058-149">Microsoft.Azure.PowerShell.Cmdlets.VMWare.Models.Api20200320.IPrivateCloud</span></span>

## <span data-ttu-id="db058-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="db058-150">NOTES</span></span>

<span data-ttu-id="db058-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="db058-151">ALIASES</span></span>

<span data-ttu-id="db058-152">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="db058-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="db058-153">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="db058-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="db058-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="db058-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="db058-155">IDENTITYSOURCE <IIdentitySource [] >: источники удостоверений единого входа vCenter</span><span class="sxs-lookup"><span data-stu-id="db058-155">IDENTITYSOURCE <IIdentitySource[]>: vCenter Single Sign On Identity Sources</span></span>
  - <span data-ttu-id="db058-156">`[Alias <String>]`: NetBIOS-имя домена;</span><span class="sxs-lookup"><span data-stu-id="db058-156">`[Alias <String>]`: The domain's NetBIOS name</span></span>
  - <span data-ttu-id="db058-157">`[BaseGroupDn <String>]`: Базовое различающееся имя для групп</span><span class="sxs-lookup"><span data-stu-id="db058-157">`[BaseGroupDn <String>]`: The base distinguished name for groups</span></span>
  - <span data-ttu-id="db058-158">`[BaseUserDn <String>]`: Базовое различающееся имя для пользователей</span><span class="sxs-lookup"><span data-stu-id="db058-158">`[BaseUserDn <String>]`: The base distinguished name for users</span></span>
  - <span data-ttu-id="db058-159">`[Domain <String>]`: DNS-имя домена</span><span class="sxs-lookup"><span data-stu-id="db058-159">`[Domain <String>]`: The domain's dns name</span></span>
  - <span data-ttu-id="db058-160">`[Name <String>]`: Имя источника идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="db058-160">`[Name <String>]`: The name of the identity source</span></span>
  - <span data-ttu-id="db058-161">`[Password <String>]`: Пароль пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп.</span><span class="sxs-lookup"><span data-stu-id="db058-161">`[Password <String>]`: The password of the Active Directory user with a minimum of read-only access to Base DN for users and groups.</span></span>
  - <span data-ttu-id="db058-162">`[PrimaryServer <String>]`: URL-адрес основного сервера</span><span class="sxs-lookup"><span data-stu-id="db058-162">`[PrimaryServer <String>]`: Primary server URL</span></span>
  - <span data-ttu-id="db058-163">`[SecondaryServer <String>]`: URL-адрес дополнительного сервера</span><span class="sxs-lookup"><span data-stu-id="db058-163">`[SecondaryServer <String>]`: Secondary server URL</span></span>
  - <span data-ttu-id="db058-164">`[Ssl <SslEnum?>]`: Защита связи LDAP с помощью SSL-сертификата (LDAPs)</span><span class="sxs-lookup"><span data-stu-id="db058-164">`[Ssl <SslEnum?>]`: Protect LDAP communication using SSL certificate (LDAPS)</span></span>
  - <span data-ttu-id="db058-165">`[Username <String>]`: Идентификатор пользователя Active Directory с минимальным доступом только для чтения к базовому DN для пользователей и групп</span><span class="sxs-lookup"><span data-stu-id="db058-165">`[Username <String>]`: The ID of an Active Directory user with a minimum of read-only access to Base DN for users and group</span></span>

<span data-ttu-id="db058-166">INPUTOBJECT <IVMWareIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="db058-166">INPUTOBJECT <IVMWareIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="db058-167">`[AuthorizationName <String>]`: Имя авторизации канала ExpressRoute в частном облаке.</span><span class="sxs-lookup"><span data-stu-id="db058-167">`[AuthorizationName <String>]`: Name of the ExpressRoute Circuit Authorization in the private cloud</span></span>
  - <span data-ttu-id="db058-168">`[ClusterName <String>]`: Имя кластера в частном облаке</span><span class="sxs-lookup"><span data-stu-id="db058-168">`[ClusterName <String>]`: Name of the cluster in the private cloud</span></span>
  - <span data-ttu-id="db058-169">`[HcxEnterpriseSiteName <String>]`: Имя корпоративного сайта HCX в частном облаке</span><span class="sxs-lookup"><span data-stu-id="db058-169">`[HcxEnterpriseSiteName <String>]`: Name of the HCX Enterprise Site in the private cloud</span></span>
  - <span data-ttu-id="db058-170">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="db058-170">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="db058-171">`[Location <String>]`: Регион Azure</span><span class="sxs-lookup"><span data-stu-id="db058-171">`[Location <String>]`: Azure region</span></span>
  - <span data-ttu-id="db058-172">`[PrivateCloudName <String>]`: Имя частного облака</span><span class="sxs-lookup"><span data-stu-id="db058-172">`[PrivateCloudName <String>]`: Name of the private cloud</span></span>
  - <span data-ttu-id="db058-173">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="db058-173">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="db058-174">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="db058-174">The name is case insensitive.</span></span>
  - <span data-ttu-id="db058-175">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="db058-175">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="db058-176">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db058-176">RELATED LINKS</span></span>

