---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98419724"
---
# <span data-ttu-id="d2946-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d2946-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="d2946-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2946-102">SYNOPSIS</span></span>
<span data-ttu-id="d2946-103">Операция обновления выйдите из приложения.</span><span class="sxs-lookup"><span data-stu-id="d2946-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="d2946-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d2946-104">SYNTAX</span></span>

### <span data-ttu-id="d2946-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2946-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d2946-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d2946-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d2946-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2946-107">DESCRIPTION</span></span>
<span data-ttu-id="d2946-108">Операция обновления выйдите из приложения.</span><span class="sxs-lookup"><span data-stu-id="d2946-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="d2946-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d2946-109">EXAMPLES</span></span>

### <span data-ttu-id="d2946-110">Пример 1. Обновление приложения "Весенний облако" по имени.</span><span class="sxs-lookup"><span data-stu-id="d2946-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="d2946-111">Обновление приложения Spring Cloud по имени.</span><span class="sxs-lookup"><span data-stu-id="d2946-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="d2946-112">Пример 2. Обновление приложения "Весенние облака" из трубы.</span><span class="sxs-lookup"><span data-stu-id="d2946-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="d2946-113">Обновление приложения "Весенний облако" из канала.</span><span class="sxs-lookup"><span data-stu-id="d2946-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="d2946-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2946-114">PARAMETERS</span></span>

### <span data-ttu-id="d2946-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="d2946-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="d2946-116">Имя активного развертывания Приложения</span><span class="sxs-lookup"><span data-stu-id="d2946-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="d2946-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2946-117">-AsJob</span></span>
<span data-ttu-id="d2946-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="d2946-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d2946-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2946-119">-DefaultProfile</span></span>
<span data-ttu-id="d2946-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2946-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2946-121">-FQDN</span><span class="sxs-lookup"><span data-stu-id="d2946-121">-Fqdn</span></span>
<span data-ttu-id="d2946-122">Полное имя DNS.</span><span class="sxs-lookup"><span data-stu-id="d2946-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="d2946-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="d2946-123">-HttpsOnly</span></span>
<span data-ttu-id="d2946-124">Указать, разрешено ли использовать только https.</span><span class="sxs-lookup"><span data-stu-id="d2946-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="d2946-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2946-125">-InputObject</span></span>
<span data-ttu-id="d2946-126">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d2946-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d2946-127">-Location</span><span class="sxs-lookup"><span data-stu-id="d2946-127">-Location</span></span>
<span data-ttu-id="d2946-128">Расположение с помощью GEO приложения, всегда одинаковое с родительским ресурсом</span><span class="sxs-lookup"><span data-stu-id="d2946-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="d2946-129">-Name</span><span class="sxs-lookup"><span data-stu-id="d2946-129">-Name</span></span>
<span data-ttu-id="d2946-130">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="d2946-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="d2946-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d2946-131">-NoWait</span></span>
<span data-ttu-id="d2946-132">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="d2946-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d2946-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="d2946-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="d2946-134">Путь к сохраняемого диска</span><span class="sxs-lookup"><span data-stu-id="d2946-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="d2946-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="d2946-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="d2946-136">Размер сохраняемого диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="d2946-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="d2946-137">-Public</span><span class="sxs-lookup"><span data-stu-id="d2946-137">-Public</span></span>
<span data-ttu-id="d2946-138">Указывает на то, является ли приложение общедоступным конечным точкой</span><span class="sxs-lookup"><span data-stu-id="d2946-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="d2946-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2946-139">-ResourceGroupName</span></span>
<span data-ttu-id="d2946-140">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d2946-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d2946-141">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d2946-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d2946-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d2946-142">-ServiceName</span></span>
<span data-ttu-id="d2946-143">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d2946-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d2946-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d2946-144">-SubscriptionId</span></span>
<span data-ttu-id="d2946-145">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2946-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d2946-146">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d2946-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d2946-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="d2946-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="d2946-148">Путь к временному диску</span><span class="sxs-lookup"><span data-stu-id="d2946-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="d2946-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="d2946-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="d2946-150">Размер временного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="d2946-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="d2946-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2946-151">-Confirm</span></span>
<span data-ttu-id="d2946-152">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d2946-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2946-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2946-153">-WhatIf</span></span>
<span data-ttu-id="d2946-154">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2946-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2946-155">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d2946-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2946-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2946-156">CommonParameters</span></span>
<span data-ttu-id="d2946-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2946-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2946-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2946-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2946-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2946-159">INPUTS</span></span>

### <span data-ttu-id="d2946-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d2946-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d2946-161">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d2946-161">OUTPUTS</span></span>

### <span data-ttu-id="d2946-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="d2946-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="d2946-163">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d2946-163">NOTES</span></span>

<span data-ttu-id="d2946-164">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d2946-164">ALIASES</span></span>

<span data-ttu-id="d2946-165">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d2946-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d2946-166">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d2946-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d2946-167">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d2946-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d2946-168">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d2946-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d2946-169">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="d2946-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d2946-170">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="d2946-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d2946-171">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="d2946-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d2946-172">`[DeploymentName <String>]`: Название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="d2946-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d2946-173">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d2946-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d2946-174">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d2946-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d2946-175">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="d2946-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d2946-176">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d2946-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d2946-177">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d2946-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d2946-178">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d2946-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d2946-179">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d2946-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d2946-180">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d2946-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d2946-181">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2946-181">RELATED LINKS</span></span>

