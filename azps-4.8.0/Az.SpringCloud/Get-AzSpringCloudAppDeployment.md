---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243942"
---
# <span data-ttu-id="8f4ce-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="8f4ce-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="8f4ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="8f4ce-103">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="8f4ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f4ce-104">SYNTAX</span></span>

### <span data-ttu-id="8f4ce-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f4ce-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8f4ce-106">Получить</span><span class="sxs-lookup"><span data-stu-id="8f4ce-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8f4ce-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8f4ce-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f4ce-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-108">DESCRIPTION</span></span>
<span data-ttu-id="8f4ce-109">Получите развертывание и его свойства.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="8f4ce-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-110">EXAMPLES</span></span>

### <span data-ttu-id="8f4ce-111">Пример 1: получение Deploymeng облачного приложения для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="8f4ce-112">Получение Deploymeng облачного приложения для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="8f4ce-113">Пример 2: список всех развертываний в соответствии с заданным приложением в облаке весны.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="8f4ce-114">Перечислите все развертывание в соответствии с заданным приложением в облаке весны.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="8f4ce-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-115">PARAMETERS</span></span>

### <span data-ttu-id="8f4ce-116">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="8f4ce-116">-AppName</span></span>
<span data-ttu-id="8f4ce-117">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="8f4ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f4ce-118">-DefaultProfile</span></span>
<span data-ttu-id="8f4ce-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f4ce-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f4ce-120">-InputObject</span></span>
<span data-ttu-id="8f4ce-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8f4ce-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f4ce-122">-Name</span></span>
<span data-ttu-id="8f4ce-123">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-123">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="8f4ce-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f4ce-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f4ce-125">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8f4ce-126">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8f4ce-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8f4ce-127">-ServiceName</span></span>
<span data-ttu-id="8f4ce-128">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="8f4ce-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8f4ce-129">-SubscriptionId</span></span>
<span data-ttu-id="8f4ce-130">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8f4ce-131">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8f4ce-132">-Version</span><span class="sxs-lookup"><span data-stu-id="8f4ce-132">-Version</span></span>
<span data-ttu-id="8f4ce-133">Версия указанных развертываний</span><span class="sxs-lookup"><span data-stu-id="8f4ce-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f4ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f4ce-134">CommonParameters</span></span>
<span data-ttu-id="8f4ce-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f4ce-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f4ce-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f4ce-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f4ce-137">INPUTS</span></span>

### <span data-ttu-id="8f4ce-138">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="8f4ce-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="8f4ce-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-139">OUTPUTS</span></span>

### <span data-ttu-id="8f4ce-140">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="8f4ce-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="8f4ce-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f4ce-141">NOTES</span></span>

<span data-ttu-id="8f4ce-142">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-142">ALIASES</span></span>

<span data-ttu-id="8f4ce-143">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8f4ce-144">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8f4ce-145">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8f4ce-146">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="8f4ce-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8f4ce-147">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="8f4ce-148">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="8f4ce-149">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="8f4ce-150">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="8f4ce-151">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="8f4ce-152">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="8f4ce-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8f4ce-153">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="8f4ce-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="8f4ce-154">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8f4ce-155">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8f4ce-156">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="8f4ce-157">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="8f4ce-158">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="8f4ce-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="8f4ce-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f4ce-159">RELATED LINKS</span></span>

