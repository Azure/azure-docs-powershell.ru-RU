---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245219"
---
# <span data-ttu-id="69f41-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="69f41-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="69f41-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69f41-102">SYNOPSIS</span></span>
<span data-ttu-id="69f41-103">Операция для обновления завершающего развертывания.</span><span class="sxs-lookup"><span data-stu-id="69f41-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="69f41-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69f41-104">SYNTAX</span></span>

### <span data-ttu-id="69f41-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="69f41-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="69f41-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="69f41-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69f41-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f41-107">DESCRIPTION</span></span>
<span data-ttu-id="69f41-108">Операция для обновления завершающего развертывания.</span><span class="sxs-lookup"><span data-stu-id="69f41-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="69f41-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69f41-109">EXAMPLES</span></span>

### <span data-ttu-id="69f41-110">Пример 1: обновление облачного развертывания весны по имени.</span><span class="sxs-lookup"><span data-stu-id="69f41-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="69f41-111">Обновите облачное развертывание для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="69f41-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="69f41-112">Пример 2: Обновление развертывания в облаке с пружиной из канала.</span><span class="sxs-lookup"><span data-stu-id="69f41-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="69f41-113">Обновите облачное развертывание для весны в канале.</span><span class="sxs-lookup"><span data-stu-id="69f41-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="69f41-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69f41-114">PARAMETERS</span></span>

### <span data-ttu-id="69f41-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="69f41-115">-AppName</span></span>
<span data-ttu-id="69f41-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="69f41-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="69f41-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69f41-117">-AsJob</span></span>
<span data-ttu-id="69f41-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="69f41-118">Run the command as a job</span></span>

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

### <span data-ttu-id="69f41-119">-ЦП</span><span class="sxs-lookup"><span data-stu-id="69f41-119">-Cpu</span></span>
<span data-ttu-id="69f41-120">Требуемый ЦП</span><span class="sxs-lookup"><span data-stu-id="69f41-120">Required CPU</span></span>

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

### <span data-ttu-id="69f41-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f41-121">-DefaultProfile</span></span>
<span data-ttu-id="69f41-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69f41-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69f41-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="69f41-123">-EnvironmentVariable</span></span>
<span data-ttu-id="69f41-124">Коллекция переменных среды</span><span class="sxs-lookup"><span data-stu-id="69f41-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="69f41-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69f41-125">-InputObject</span></span>
<span data-ttu-id="69f41-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="69f41-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="69f41-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="69f41-127">-JvmOption</span></span>
<span data-ttu-id="69f41-128">Параметр JVM</span><span class="sxs-lookup"><span data-stu-id="69f41-128">JVM parameter</span></span>

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

### <span data-ttu-id="69f41-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="69f41-129">-MemoryInGb</span></span>
<span data-ttu-id="69f41-130">Требуемый объем памяти в ГБ</span><span class="sxs-lookup"><span data-stu-id="69f41-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="69f41-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="69f41-131">-Name</span></span>
<span data-ttu-id="69f41-132">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="69f41-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f41-133">-Wait</span><span class="sxs-lookup"><span data-stu-id="69f41-133">-NoWait</span></span>
<span data-ttu-id="69f41-134">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="69f41-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69f41-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f41-135">-ResourceGroupName</span></span>
<span data-ttu-id="69f41-136">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="69f41-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="69f41-137">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="69f41-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="69f41-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="69f41-138">-RuntimeVersion</span></span>
<span data-ttu-id="69f41-139">Версия среды выполнения</span><span class="sxs-lookup"><span data-stu-id="69f41-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f41-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="69f41-140">-ServiceName</span></span>
<span data-ttu-id="69f41-141">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="69f41-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="69f41-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="69f41-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="69f41-143">Селектор для артефакта, который будет использоваться для развертывания проектов с несколькими модулями.</span><span class="sxs-lookup"><span data-stu-id="69f41-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="69f41-144">Это должен Bethe относительный путь к целевому модулю или проекту.</span><span class="sxs-lookup"><span data-stu-id="69f41-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="69f41-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="69f41-145">-SourceRelativePath</span></span>
<span data-ttu-id="69f41-146">Относительный путь к хранилищу, в котором хранится источник</span><span class="sxs-lookup"><span data-stu-id="69f41-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="69f41-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="69f41-147">-SourceType</span></span>
<span data-ttu-id="69f41-148">Тип источника, загруженного</span><span class="sxs-lookup"><span data-stu-id="69f41-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69f41-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="69f41-149">-SourceVersion</span></span>
<span data-ttu-id="69f41-150">Версия исходного кода</span><span class="sxs-lookup"><span data-stu-id="69f41-150">Version of the source</span></span>

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

### <span data-ttu-id="69f41-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69f41-151">-SubscriptionId</span></span>
<span data-ttu-id="69f41-152">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69f41-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="69f41-153">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="69f41-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="69f41-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69f41-154">-Confirm</span></span>
<span data-ttu-id="69f41-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69f41-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69f41-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69f41-156">-WhatIf</span></span>
<span data-ttu-id="69f41-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69f41-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69f41-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69f41-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69f41-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f41-159">CommonParameters</span></span>
<span data-ttu-id="69f41-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69f41-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f41-161">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69f41-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f41-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69f41-162">INPUTS</span></span>

### <span data-ttu-id="69f41-163">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="69f41-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="69f41-164">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f41-164">OUTPUTS</span></span>

### <span data-ttu-id="69f41-165">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="69f41-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="69f41-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="69f41-166">NOTES</span></span>

<span data-ttu-id="69f41-167">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="69f41-167">ALIASES</span></span>

<span data-ttu-id="69f41-168">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="69f41-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69f41-169">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="69f41-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69f41-170">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="69f41-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69f41-171">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="69f41-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69f41-172">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="69f41-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="69f41-173">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="69f41-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="69f41-174">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="69f41-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="69f41-175">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="69f41-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="69f41-176">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="69f41-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="69f41-177">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="69f41-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69f41-178">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="69f41-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="69f41-179">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="69f41-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="69f41-180">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="69f41-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="69f41-181">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="69f41-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="69f41-182">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="69f41-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="69f41-183">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="69f41-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="69f41-184">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69f41-184">RELATED LINKS</span></span>

