---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413012"
---
# <span data-ttu-id="b2e03-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b2e03-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b2e03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2e03-102">SYNOPSIS</span></span>
<span data-ttu-id="b2e03-103">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e03-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="b2e03-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2e03-104">SYNTAX</span></span>

### <span data-ttu-id="b2e03-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2e03-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2e03-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b2e03-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b2e03-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b2e03-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b2e03-108">Список</span><span class="sxs-lookup"><span data-stu-id="b2e03-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b2e03-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2e03-109">DESCRIPTION</span></span>
<span data-ttu-id="b2e03-110">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e03-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="b2e03-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2e03-111">EXAMPLES</span></span>

### <span data-ttu-id="b2e03-112">Пример 1. Получите приложение Spring Cloud App Deploymeng по имени.</span><span class="sxs-lookup"><span data-stu-id="b2e03-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="b2e03-113">Получите Приложение Spring Cloud Deploymeng по имени.</span><span class="sxs-lookup"><span data-stu-id="b2e03-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="b2e03-114">Пример 2. Перечислить все развертывание в заданное весенним облачным приложением.</span><span class="sxs-lookup"><span data-stu-id="b2e03-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="b2e03-115">Перечислить все развертывание в заданное весенним облачным приложением.</span><span class="sxs-lookup"><span data-stu-id="b2e03-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="b2e03-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2e03-116">PARAMETERS</span></span>

### <span data-ttu-id="b2e03-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="b2e03-117">-AppName</span></span>
<span data-ttu-id="b2e03-118">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="b2e03-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="b2e03-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2e03-119">-DefaultProfile</span></span>
<span data-ttu-id="b2e03-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e03-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2e03-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2e03-121">-InputObject</span></span>
<span data-ttu-id="b2e03-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b2e03-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b2e03-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b2e03-123">-Name</span></span>
<span data-ttu-id="b2e03-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="b2e03-124">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e03-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2e03-125">-ResourceGroupName</span></span>
<span data-ttu-id="b2e03-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b2e03-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b2e03-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b2e03-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e03-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b2e03-128">-ServiceName</span></span>
<span data-ttu-id="b2e03-129">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="b2e03-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e03-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b2e03-130">-SubscriptionId</span></span>
<span data-ttu-id="b2e03-131">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e03-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b2e03-132">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b2e03-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e03-133">-Версия</span><span class="sxs-lookup"><span data-stu-id="b2e03-133">-Version</span></span>
<span data-ttu-id="b2e03-134">Версия развертывается, которая будет указана в списке</span><span class="sxs-lookup"><span data-stu-id="b2e03-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2e03-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2e03-135">CommonParameters</span></span>
<span data-ttu-id="b2e03-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2e03-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2e03-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2e03-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2e03-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e03-138">INPUTS</span></span>

### <span data-ttu-id="b2e03-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="b2e03-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b2e03-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2e03-140">OUTPUTS</span></span>

### <span data-ttu-id="b2e03-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="b2e03-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="b2e03-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2e03-142">NOTES</span></span>

<span data-ttu-id="b2e03-143">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b2e03-143">ALIASES</span></span>

<span data-ttu-id="b2e03-144">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b2e03-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b2e03-145">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b2e03-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b2e03-146">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b2e03-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b2e03-147">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b2e03-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b2e03-148">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="b2e03-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b2e03-149">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="b2e03-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b2e03-150">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="b2e03-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b2e03-151">`[DeploymentName <String>]`: название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="b2e03-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b2e03-152">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="b2e03-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b2e03-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b2e03-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b2e03-154">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="b2e03-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b2e03-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b2e03-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b2e03-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b2e03-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b2e03-157">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="b2e03-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b2e03-158">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b2e03-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b2e03-159">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="b2e03-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b2e03-160">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2e03-160">RELATED LINKS</span></span>

