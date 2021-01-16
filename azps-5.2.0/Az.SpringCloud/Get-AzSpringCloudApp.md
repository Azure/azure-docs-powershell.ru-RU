---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409900"
---
# <span data-ttu-id="8b507-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="8b507-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="8b507-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b507-102">SYNOPSIS</span></span>
<span data-ttu-id="8b507-103">Получите приложение и его свойства.</span><span class="sxs-lookup"><span data-stu-id="8b507-103">Get an App and its properties.</span></span>

## <span data-ttu-id="8b507-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8b507-104">SYNTAX</span></span>

### <span data-ttu-id="8b507-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8b507-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b507-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8b507-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8b507-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8b507-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b507-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8b507-108">DESCRIPTION</span></span>
<span data-ttu-id="8b507-109">Получите приложение и его свойства.</span><span class="sxs-lookup"><span data-stu-id="8b507-109">Get an App and its properties.</span></span>

## <span data-ttu-id="8b507-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8b507-110">EXAMPLES</span></span>

### <span data-ttu-id="8b507-111">Пример 1. Получить приложение Spring Cloud По имени.</span><span class="sxs-lookup"><span data-stu-id="8b507-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="8b507-112">Получите приложение Spring Cloud по имени.</span><span class="sxs-lookup"><span data-stu-id="8b507-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="8b507-113">Пример 2. Перечислить все приложение в заданной весенних облачных службах.</span><span class="sxs-lookup"><span data-stu-id="8b507-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="8b507-114">Перечислить все приложение в заданной весенних облачных службах.</span><span class="sxs-lookup"><span data-stu-id="8b507-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="8b507-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b507-115">PARAMETERS</span></span>

### <span data-ttu-id="8b507-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b507-116">-DefaultProfile</span></span>
<span data-ttu-id="8b507-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8b507-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b507-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8b507-118">-InputObject</span></span>
<span data-ttu-id="8b507-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="8b507-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8b507-120">-Name</span></span>
<span data-ttu-id="8b507-121">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="8b507-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b507-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b507-123">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b507-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8b507-124">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8b507-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8b507-125">-ServiceName</span></span>
<span data-ttu-id="8b507-126">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="8b507-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b507-127">-SubscriptionId</span></span>
<span data-ttu-id="8b507-128">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b507-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8b507-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8b507-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="8b507-130">-SyncStatus</span></span>
<span data-ttu-id="8b507-131">Указывает, является ли состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="8b507-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b507-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b507-132">CommonParameters</span></span>
<span data-ttu-id="8b507-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b507-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b507-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b507-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b507-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b507-135">INPUTS</span></span>

### <span data-ttu-id="8b507-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8b507-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8b507-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8b507-137">OUTPUTS</span></span>

### <span data-ttu-id="8b507-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="8b507-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="8b507-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8b507-139">NOTES</span></span>

<span data-ttu-id="8b507-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="8b507-140">ALIASES</span></span>

<span data-ttu-id="8b507-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8b507-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8b507-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="8b507-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8b507-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8b507-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8b507-144">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="8b507-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8b507-145">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="8b507-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8b507-146">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="8b507-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8b507-147">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="8b507-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8b507-148">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="8b507-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8b507-149">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="8b507-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8b507-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="8b507-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8b507-151">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="8b507-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8b507-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="8b507-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8b507-153">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8b507-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8b507-154">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="8b507-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8b507-155">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8b507-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8b507-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="8b507-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8b507-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8b507-157">RELATED LINKS</span></span>

