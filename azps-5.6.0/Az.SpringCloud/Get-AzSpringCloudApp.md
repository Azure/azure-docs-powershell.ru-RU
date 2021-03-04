---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 62a0398ca117ac623d0b21cc89908b25a4e7e1e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955315"
---
# <span data-ttu-id="d79f4-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="d79f4-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="d79f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d79f4-103">Получите приложение и его свойства.</span><span class="sxs-lookup"><span data-stu-id="d79f4-103">Get an App and its properties.</span></span>

## <span data-ttu-id="d79f4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d79f4-104">SYNTAX</span></span>

### <span data-ttu-id="d79f4-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d79f4-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d79f4-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d79f4-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d79f4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d79f4-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d79f4-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d79f4-108">DESCRIPTION</span></span>
<span data-ttu-id="d79f4-109">Получите приложение и его свойства.</span><span class="sxs-lookup"><span data-stu-id="d79f4-109">Get an App and its properties.</span></span>

## <span data-ttu-id="d79f4-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d79f4-110">EXAMPLES</span></span>

### <span data-ttu-id="d79f4-111">Пример 1. Получить приложение Spring Cloud По имени.</span><span class="sxs-lookup"><span data-stu-id="d79f4-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="d79f4-112">Получите приложение Spring Cloud по имени.</span><span class="sxs-lookup"><span data-stu-id="d79f4-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="d79f4-113">Пример 2. Перечислить все приложение в заданной весенних облачных службах.</span><span class="sxs-lookup"><span data-stu-id="d79f4-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="d79f4-114">Перечислить все приложение в заданной весенних облачных службах.</span><span class="sxs-lookup"><span data-stu-id="d79f4-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="d79f4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d79f4-115">PARAMETERS</span></span>

### <span data-ttu-id="d79f4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79f4-116">-DefaultProfile</span></span>
<span data-ttu-id="d79f4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d79f4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d79f4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d79f4-118">-InputObject</span></span>
<span data-ttu-id="d79f4-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d79f4-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d79f4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d79f4-120">-Name</span></span>
<span data-ttu-id="d79f4-121">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="d79f4-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="d79f4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79f4-122">-ResourceGroupName</span></span>
<span data-ttu-id="d79f4-123">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d79f4-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d79f4-124">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d79f4-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d79f4-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d79f4-125">-ServiceName</span></span>
<span data-ttu-id="d79f4-126">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d79f4-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="d79f4-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d79f4-127">-SubscriptionId</span></span>
<span data-ttu-id="d79f4-128">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d79f4-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d79f4-129">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d79f4-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d79f4-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="d79f4-130">-SyncStatus</span></span>
<span data-ttu-id="d79f4-131">Указывает, является ли состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="d79f4-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="d79f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79f4-132">CommonParameters</span></span>
<span data-ttu-id="d79f4-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d79f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79f4-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d79f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79f4-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d79f4-135">INPUTS</span></span>

### <span data-ttu-id="d79f4-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d79f4-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d79f4-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d79f4-137">OUTPUTS</span></span>

### <span data-ttu-id="d79f4-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="d79f4-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="d79f4-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d79f4-139">NOTES</span></span>

<span data-ttu-id="d79f4-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d79f4-140">ALIASES</span></span>

<span data-ttu-id="d79f4-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d79f4-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d79f4-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d79f4-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d79f4-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d79f4-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d79f4-144">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d79f4-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d79f4-145">`[AppName <String>]`: Название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="d79f4-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d79f4-146">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="d79f4-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d79f4-147">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="d79f4-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d79f4-148">`[DeploymentName <String>]`: Название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="d79f4-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d79f4-149">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="d79f4-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d79f4-150">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d79f4-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d79f4-151">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="d79f4-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d79f4-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="d79f4-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d79f4-153">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="d79f4-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d79f4-154">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="d79f4-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d79f4-155">`[SubscriptionId <String>]`: получает ИД подписки, который однозначно определяет подписку microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d79f4-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d79f4-156">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="d79f4-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d79f4-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d79f4-157">RELATED LINKS</span></span>

