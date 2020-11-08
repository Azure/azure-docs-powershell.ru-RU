---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245242"
---
# <span data-ttu-id="154bf-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="154bf-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="154bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="154bf-102">SYNOPSIS</span></span>
<span data-ttu-id="154bf-103">Получение приложения и его свойств.</span><span class="sxs-lookup"><span data-stu-id="154bf-103">Get an App and its properties.</span></span>

## <span data-ttu-id="154bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="154bf-104">SYNTAX</span></span>

### <span data-ttu-id="154bf-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="154bf-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="154bf-106">Получить</span><span class="sxs-lookup"><span data-stu-id="154bf-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="154bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="154bf-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="154bf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="154bf-108">DESCRIPTION</span></span>
<span data-ttu-id="154bf-109">Получение приложения и его свойств.</span><span class="sxs-lookup"><span data-stu-id="154bf-109">Get an App and its properties.</span></span>

## <span data-ttu-id="154bf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="154bf-110">EXAMPLES</span></span>

### <span data-ttu-id="154bf-111">Пример 1: получение облачного приложения весны по имени.</span><span class="sxs-lookup"><span data-stu-id="154bf-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="154bf-112">Получить облачное приложение пружины по названию.</span><span class="sxs-lookup"><span data-stu-id="154bf-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="154bf-113">Пример 2: список всех приложений в рамках заданной весны облачной службы.</span><span class="sxs-lookup"><span data-stu-id="154bf-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="154bf-114">Перечислите все приложения в рамках данной высокооблачной службы весны.</span><span class="sxs-lookup"><span data-stu-id="154bf-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="154bf-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="154bf-115">PARAMETERS</span></span>

### <span data-ttu-id="154bf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="154bf-116">-DefaultProfile</span></span>
<span data-ttu-id="154bf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="154bf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="154bf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="154bf-118">-InputObject</span></span>
<span data-ttu-id="154bf-119">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="154bf-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="154bf-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="154bf-120">-Name</span></span>
<span data-ttu-id="154bf-121">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="154bf-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="154bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="154bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="154bf-123">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="154bf-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="154bf-124">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="154bf-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="154bf-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="154bf-125">-ServiceName</span></span>
<span data-ttu-id="154bf-126">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="154bf-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="154bf-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="154bf-127">-SubscriptionId</span></span>
<span data-ttu-id="154bf-128">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="154bf-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="154bf-129">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="154bf-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="154bf-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="154bf-130">-SyncStatus</span></span>
<span data-ttu-id="154bf-131">Указывает, является ли состояние синхронизации</span><span class="sxs-lookup"><span data-stu-id="154bf-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="154bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="154bf-132">CommonParameters</span></span>
<span data-ttu-id="154bf-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="154bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="154bf-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="154bf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="154bf-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="154bf-135">INPUTS</span></span>

### <span data-ttu-id="154bf-136">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="154bf-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="154bf-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="154bf-137">OUTPUTS</span></span>

### <span data-ttu-id="154bf-138">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="154bf-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="154bf-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="154bf-139">NOTES</span></span>

<span data-ttu-id="154bf-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="154bf-140">ALIASES</span></span>

<span data-ttu-id="154bf-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="154bf-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="154bf-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="154bf-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="154bf-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="154bf-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="154bf-144">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="154bf-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="154bf-145">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="154bf-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="154bf-146">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="154bf-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="154bf-147">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="154bf-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="154bf-148">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="154bf-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="154bf-149">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="154bf-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="154bf-150">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="154bf-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="154bf-151">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="154bf-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="154bf-152">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="154bf-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="154bf-153">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="154bf-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="154bf-154">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="154bf-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="154bf-155">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="154bf-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="154bf-156">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="154bf-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="154bf-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="154bf-157">RELATED LINKS</span></span>

