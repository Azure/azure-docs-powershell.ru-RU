---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245224"
---
# <span data-ttu-id="90e57-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="90e57-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="90e57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="90e57-102">SYNOPSIS</span></span>
<span data-ttu-id="90e57-103">Операция обновления завершающего приложения.</span><span class="sxs-lookup"><span data-stu-id="90e57-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="90e57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="90e57-104">SYNTAX</span></span>

### <span data-ttu-id="90e57-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90e57-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90e57-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="90e57-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90e57-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90e57-107">DESCRIPTION</span></span>
<span data-ttu-id="90e57-108">Операция обновления завершающего приложения.</span><span class="sxs-lookup"><span data-stu-id="90e57-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="90e57-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="90e57-109">EXAMPLES</span></span>

### <span data-ttu-id="90e57-110">Пример 1: обновление облачного приложения весны по имени.</span><span class="sxs-lookup"><span data-stu-id="90e57-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="90e57-111">Обновите облачное приложение весны по имени.</span><span class="sxs-lookup"><span data-stu-id="90e57-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="90e57-112">Пример 2. Обновите облачное приложение пружины в канале.</span><span class="sxs-lookup"><span data-stu-id="90e57-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="90e57-113">Обновите облачное приложение весны из канала.</span><span class="sxs-lookup"><span data-stu-id="90e57-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="90e57-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="90e57-114">PARAMETERS</span></span>

### <span data-ttu-id="90e57-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="90e57-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="90e57-116">Имя активного развертывания приложения</span><span class="sxs-lookup"><span data-stu-id="90e57-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="90e57-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90e57-117">-AsJob</span></span>
<span data-ttu-id="90e57-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="90e57-118">Run the command as a job</span></span>

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

### <span data-ttu-id="90e57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e57-119">-DefaultProfile</span></span>
<span data-ttu-id="90e57-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90e57-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90e57-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="90e57-121">-Fqdn</span></span>
<span data-ttu-id="90e57-122">Полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="90e57-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="90e57-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="90e57-123">-HttpsOnly</span></span>
<span data-ttu-id="90e57-124">Укажите, разрешено ли использование HTTPS.</span><span class="sxs-lookup"><span data-stu-id="90e57-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="90e57-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90e57-125">-InputObject</span></span>
<span data-ttu-id="90e57-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="90e57-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90e57-127">-Location</span><span class="sxs-lookup"><span data-stu-id="90e57-127">-Location</span></span>
<span data-ttu-id="90e57-128">Географическое расположение приложения, которое всегда одинаково с родительским ресурсом</span><span class="sxs-lookup"><span data-stu-id="90e57-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="90e57-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="90e57-129">-Name</span></span>
<span data-ttu-id="90e57-130">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="90e57-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90e57-131">-Wait</span><span class="sxs-lookup"><span data-stu-id="90e57-131">-NoWait</span></span>
<span data-ttu-id="90e57-132">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="90e57-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90e57-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="90e57-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="90e57-134">Путь подключения постоянного диска</span><span class="sxs-lookup"><span data-stu-id="90e57-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="90e57-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="90e57-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="90e57-136">Размер постоянного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="90e57-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="90e57-137">-Public</span><span class="sxs-lookup"><span data-stu-id="90e57-137">-Public</span></span>
<span data-ttu-id="90e57-138">Указывает, предоставляет ли приложение общедоступную конечную точку</span><span class="sxs-lookup"><span data-stu-id="90e57-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="90e57-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90e57-139">-ResourceGroupName</span></span>
<span data-ttu-id="90e57-140">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="90e57-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="90e57-141">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="90e57-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="90e57-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="90e57-142">-ServiceName</span></span>
<span data-ttu-id="90e57-143">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="90e57-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="90e57-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90e57-144">-SubscriptionId</span></span>
<span data-ttu-id="90e57-145">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90e57-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="90e57-146">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="90e57-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90e57-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="90e57-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="90e57-148">Путь к временному диску для подключения</span><span class="sxs-lookup"><span data-stu-id="90e57-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="90e57-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="90e57-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="90e57-150">Размер временного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="90e57-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="90e57-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90e57-151">-Confirm</span></span>
<span data-ttu-id="90e57-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="90e57-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e57-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e57-153">-WhatIf</span></span>
<span data-ttu-id="90e57-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="90e57-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e57-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="90e57-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e57-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e57-156">CommonParameters</span></span>
<span data-ttu-id="90e57-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="90e57-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e57-158">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90e57-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e57-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="90e57-159">INPUTS</span></span>

### <span data-ttu-id="90e57-160">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="90e57-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="90e57-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="90e57-161">OUTPUTS</span></span>

### <span data-ttu-id="90e57-162">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="90e57-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="90e57-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="90e57-163">NOTES</span></span>

<span data-ttu-id="90e57-164">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="90e57-164">ALIASES</span></span>

<span data-ttu-id="90e57-165">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="90e57-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90e57-166">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="90e57-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90e57-167">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90e57-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90e57-168">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="90e57-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90e57-169">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="90e57-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="90e57-170">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="90e57-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="90e57-171">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="90e57-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="90e57-172">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="90e57-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="90e57-173">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="90e57-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="90e57-174">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="90e57-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90e57-175">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="90e57-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="90e57-176">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="90e57-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="90e57-177">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="90e57-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="90e57-178">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="90e57-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="90e57-179">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="90e57-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="90e57-180">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="90e57-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="90e57-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90e57-181">RELATED LINKS</span></span>

