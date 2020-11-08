---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243286"
---
# <span data-ttu-id="87a40-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="87a40-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="87a40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87a40-102">SYNOPSIS</span></span>
<span data-ttu-id="87a40-103">Операция для обновления завершающего развертывания.</span><span class="sxs-lookup"><span data-stu-id="87a40-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="87a40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87a40-104">SYNTAX</span></span>

### <span data-ttu-id="87a40-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87a40-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="87a40-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="87a40-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="87a40-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87a40-107">DESCRIPTION</span></span>
<span data-ttu-id="87a40-108">Операция для обновления завершающего развертывания.</span><span class="sxs-lookup"><span data-stu-id="87a40-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="87a40-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87a40-109">EXAMPLES</span></span>

### <span data-ttu-id="87a40-110">Пример 1: обновление облачного развертывания весны по имени.</span><span class="sxs-lookup"><span data-stu-id="87a40-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="87a40-111">Обновите облачное развертывание для весны по имени.</span><span class="sxs-lookup"><span data-stu-id="87a40-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="87a40-112">Пример 2: Обновление развертывания в облаке с пружиной из канала.</span><span class="sxs-lookup"><span data-stu-id="87a40-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="87a40-113">Обновите облачное развертывание для весны в канале.</span><span class="sxs-lookup"><span data-stu-id="87a40-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="87a40-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87a40-114">PARAMETERS</span></span>

### <span data-ttu-id="87a40-115">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="87a40-115">-AppName</span></span>
<span data-ttu-id="87a40-116">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="87a40-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="87a40-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87a40-117">-AsJob</span></span>
<span data-ttu-id="87a40-118">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="87a40-118">Run the command as a job</span></span>

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

### <span data-ttu-id="87a40-119">-ЦП</span><span class="sxs-lookup"><span data-stu-id="87a40-119">-Cpu</span></span>
<span data-ttu-id="87a40-120">Требуемый ЦП</span><span class="sxs-lookup"><span data-stu-id="87a40-120">Required CPU</span></span>

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

### <span data-ttu-id="87a40-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87a40-121">-DefaultProfile</span></span>
<span data-ttu-id="87a40-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87a40-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87a40-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="87a40-123">-EnvironmentVariable</span></span>
<span data-ttu-id="87a40-124">Коллекция переменных среды</span><span class="sxs-lookup"><span data-stu-id="87a40-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="87a40-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87a40-125">-InputObject</span></span>
<span data-ttu-id="87a40-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="87a40-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="87a40-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="87a40-127">-InstanceCount</span></span>
<span data-ttu-id="87a40-128">Число экземпляров</span><span class="sxs-lookup"><span data-stu-id="87a40-128">Instance count</span></span>

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

### <span data-ttu-id="87a40-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="87a40-129">-JvmOption</span></span>
<span data-ttu-id="87a40-130">Параметр JVM</span><span class="sxs-lookup"><span data-stu-id="87a40-130">JVM parameter</span></span>

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

### <span data-ttu-id="87a40-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="87a40-131">-MemoryInGb</span></span>
<span data-ttu-id="87a40-132">Требуемый объем памяти в ГБ</span><span class="sxs-lookup"><span data-stu-id="87a40-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="87a40-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="87a40-133">-Name</span></span>
<span data-ttu-id="87a40-134">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="87a40-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="87a40-135">-Wait</span><span class="sxs-lookup"><span data-stu-id="87a40-135">-NoWait</span></span>
<span data-ttu-id="87a40-136">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="87a40-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="87a40-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87a40-137">-ResourceGroupName</span></span>
<span data-ttu-id="87a40-138">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="87a40-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="87a40-139">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="87a40-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="87a40-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="87a40-140">-RuntimeVersion</span></span>
<span data-ttu-id="87a40-141">Версия среды выполнения</span><span class="sxs-lookup"><span data-stu-id="87a40-141">Runtime version</span></span>

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

### <span data-ttu-id="87a40-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="87a40-142">-ServiceName</span></span>
<span data-ttu-id="87a40-143">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="87a40-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="87a40-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="87a40-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="87a40-145">Селектор для артефакта, который будет использоваться для развертывания проектов с несколькими модулями.</span><span class="sxs-lookup"><span data-stu-id="87a40-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="87a40-146">Это должен Bethe относительный путь к целевому модулю или проекту.</span><span class="sxs-lookup"><span data-stu-id="87a40-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="87a40-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="87a40-147">-SourceRelativePath</span></span>
<span data-ttu-id="87a40-148">Относительный путь к хранилищу, в котором хранится источник</span><span class="sxs-lookup"><span data-stu-id="87a40-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="87a40-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="87a40-149">-SourceType</span></span>
<span data-ttu-id="87a40-150">Тип источника, загруженного</span><span class="sxs-lookup"><span data-stu-id="87a40-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="87a40-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="87a40-151">-SourceVersion</span></span>
<span data-ttu-id="87a40-152">Версия исходного кода</span><span class="sxs-lookup"><span data-stu-id="87a40-152">Version of the source</span></span>

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

### <span data-ttu-id="87a40-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87a40-153">-SubscriptionId</span></span>
<span data-ttu-id="87a40-154">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87a40-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="87a40-155">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="87a40-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="87a40-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87a40-156">-Confirm</span></span>
<span data-ttu-id="87a40-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87a40-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87a40-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87a40-158">-WhatIf</span></span>
<span data-ttu-id="87a40-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87a40-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87a40-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87a40-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87a40-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87a40-161">CommonParameters</span></span>
<span data-ttu-id="87a40-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87a40-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87a40-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87a40-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87a40-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87a40-164">INPUTS</span></span>

### <span data-ttu-id="87a40-165">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="87a40-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="87a40-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87a40-166">OUTPUTS</span></span>

### <span data-ttu-id="87a40-167">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="87a40-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="87a40-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="87a40-168">NOTES</span></span>

<span data-ttu-id="87a40-169">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="87a40-169">ALIASES</span></span>

<span data-ttu-id="87a40-170">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="87a40-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87a40-171">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87a40-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87a40-172">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87a40-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87a40-173">INPUTOBJECT <ISpringCloudIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="87a40-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87a40-174">`[AppName <String>]`: Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="87a40-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="87a40-175">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="87a40-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="87a40-176">`[CertificateName <String>]`: Имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="87a40-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="87a40-177">`[DeploymentName <String>]`: Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="87a40-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="87a40-178">`[DomainName <String>]`: Имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="87a40-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="87a40-179">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="87a40-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87a40-180">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="87a40-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="87a40-181">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="87a40-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="87a40-182">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="87a40-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="87a40-183">`[ServiceName <String>]`: Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="87a40-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="87a40-184">`[SubscriptionId <String>]`: Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="87a40-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="87a40-185">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="87a40-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="87a40-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87a40-186">RELATED LINKS</span></span>

