---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245243"
---
# <span data-ttu-id="4a132-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="4a132-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="4a132-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a132-102">SYNOPSIS</span></span>
<span data-ttu-id="4a132-103">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="4a132-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="4a132-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a132-104">SYNTAX</span></span>

### <span data-ttu-id="4a132-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4a132-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a132-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4a132-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4a132-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4a132-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a132-108">Список</span><span class="sxs-lookup"><span data-stu-id="4a132-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4a132-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a132-109">DESCRIPTION</span></span>
<span data-ttu-id="4a132-110">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="4a132-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="4a132-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a132-111">EXAMPLES</span></span>

### <span data-ttu-id="4a132-112">Пример 1: получение Deploymeng облачного приложения для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="4a132-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="4a132-113">Получение Deploymeng облачного приложения для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="4a132-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="4a132-114">Пример 2: список всех развертываний в соответствии с заданным приложением в облаке весны.</span><span class="sxs-lookup"><span data-stu-id="4a132-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="4a132-115">Перечислите все развертывание в соответствии с заданным приложением в облаке весны.</span><span class="sxs-lookup"><span data-stu-id="4a132-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="4a132-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a132-116">PARAMETERS</span></span>

### <span data-ttu-id="4a132-117">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="4a132-117">-AppName</span></span>
<span data-ttu-id="4a132-118">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="4a132-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="4a132-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a132-119">-DefaultProfile</span></span>
<span data-ttu-id="4a132-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a132-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a132-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a132-121">-InputObject</span></span>
<span data-ttu-id="4a132-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4a132-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4a132-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4a132-123">-Name</span></span>
<span data-ttu-id="4a132-124">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="4a132-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="4a132-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a132-125">-ResourceGroupName</span></span>
<span data-ttu-id="4a132-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="4a132-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4a132-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4a132-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4a132-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4a132-128">-ServiceName</span></span>
<span data-ttu-id="4a132-129">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="4a132-129">The name of the Service resource.</span></span>

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

### <span data-ttu-id="4a132-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4a132-130">-SubscriptionId</span></span>
<span data-ttu-id="4a132-131">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a132-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4a132-132">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4a132-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4a132-133">-Version</span><span class="sxs-lookup"><span data-stu-id="4a132-133">-Version</span></span>
<span data-ttu-id="4a132-134">Версия указанных развертываний</span><span class="sxs-lookup"><span data-stu-id="4a132-134">Version of the deployments to be listed</span></span>

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

### <span data-ttu-id="4a132-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a132-135">CommonParameters</span></span>
<span data-ttu-id="4a132-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a132-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a132-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a132-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a132-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a132-138">INPUTS</span></span>

### <span data-ttu-id="4a132-139">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="4a132-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="4a132-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a132-140">OUTPUTS</span></span>

### <span data-ttu-id="4a132-141">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="4a132-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="4a132-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a132-142">NOTES</span></span>

<span data-ttu-id="4a132-143">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4a132-143">ALIASES</span></span>

<span data-ttu-id="4a132-144">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4a132-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4a132-145">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4a132-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4a132-146">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4a132-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4a132-147">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4a132-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4a132-148">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="4a132-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="4a132-149">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="4a132-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="4a132-150">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="4a132-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="4a132-151">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="4a132-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="4a132-152">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="4a132-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="4a132-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4a132-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4a132-154">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="4a132-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="4a132-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="4a132-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4a132-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4a132-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4a132-157">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="4a132-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="4a132-158">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4a132-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="4a132-159">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="4a132-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="4a132-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a132-160">RELATED LINKS</span></span>

