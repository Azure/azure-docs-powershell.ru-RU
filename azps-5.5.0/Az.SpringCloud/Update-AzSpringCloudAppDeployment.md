---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: ba31f4d7c81392a30f4f8b9073d967b2a57cfab7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223036"
---
# <span data-ttu-id="ae0f0-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="ae0f0-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="ae0f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae0f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae0f0-103">Операция обновления выйдите из развертывания.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="ae0f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ae0f0-104">SYNTAX</span></span>

### <span data-ttu-id="ae0f0-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ae0f0-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="ae0f0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ae0f0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae0f0-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ae0f0-108">Операция обновления выйдите из развертывания.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="ae0f0-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ae0f0-110">Пример 1. Обновление названия службы "Весенний облачный развертывание".</span><span class="sxs-lookup"><span data-stu-id="ae0f0-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="ae0f0-111">Обновление названия для развертывания в весенних облачных решениях.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="ae0f0-112">Пример 2. Обновление весенних облачных развертыванию из трубы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="ae0f0-113">Обновив весенний облачный развертывание из трубы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="ae0f0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae0f0-114">PARAMETERS</span></span>

### <span data-ttu-id="ae0f0-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="ae0f0-115">-AppName</span></span>
<span data-ttu-id="ae0f0-116">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="ae0f0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae0f0-117">-AsJob</span></span>
<span data-ttu-id="ae0f0-118">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ae0f0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="ae0f0-119">-CPU</span><span class="sxs-lookup"><span data-stu-id="ae0f0-119">-Cpu</span></span>
<span data-ttu-id="ae0f0-120">Требуемая ЦП</span><span class="sxs-lookup"><span data-stu-id="ae0f0-120">Required CPU</span></span>

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

### <span data-ttu-id="ae0f0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae0f0-121">-DefaultProfile</span></span>
<span data-ttu-id="ae0f0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae0f0-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="ae0f0-123">-EnvironmentVariable</span></span>
<span data-ttu-id="ae0f0-124">Набор переменных среды</span><span class="sxs-lookup"><span data-stu-id="ae0f0-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="ae0f0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae0f0-125">-InputObject</span></span>
<span data-ttu-id="ae0f0-126">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ae0f0-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="ae0f0-127">-JvmOption</span></span>
<span data-ttu-id="ae0f0-128">Параметр JVM</span><span class="sxs-lookup"><span data-stu-id="ae0f0-128">JVM parameter</span></span>

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

### <span data-ttu-id="ae0f0-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="ae0f0-129">-MemoryInGb</span></span>
<span data-ttu-id="ae0f0-130">Необходимый размер памяти в ГБ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="ae0f0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ae0f0-131">-Name</span></span>
<span data-ttu-id="ae0f0-132">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-132">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="ae0f0-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae0f0-133">-NoWait</span></span>
<span data-ttu-id="ae0f0-134">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="ae0f0-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae0f0-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae0f0-135">-ResourceGroupName</span></span>
<span data-ttu-id="ae0f0-136">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ae0f0-137">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ae0f0-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="ae0f0-138">-RuntimeVersion</span></span>
<span data-ttu-id="ae0f0-139">Версия Runtime</span><span class="sxs-lookup"><span data-stu-id="ae0f0-139">Runtime version</span></span>

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

### <span data-ttu-id="ae0f0-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ae0f0-140">-ServiceName</span></span>
<span data-ttu-id="ae0f0-141">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ae0f0-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="ae0f0-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="ae0f0-143">Селектор артефакта, который будет использоваться для развертывания проектов с несколькими модулями.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="ae0f0-144">Это должен быть относительный путь к целевому модуле или проекту.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="ae0f0-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="ae0f0-145">-SourceRelativePath</span></span>
<span data-ttu-id="ae0f0-146">Относительный путь к хранилищу, в котором хранится источник</span><span class="sxs-lookup"><span data-stu-id="ae0f0-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="ae0f0-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="ae0f0-147">-SourceType</span></span>
<span data-ttu-id="ae0f0-148">Тип добавленного источника</span><span class="sxs-lookup"><span data-stu-id="ae0f0-148">Type of the source uploaded</span></span>

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

### <span data-ttu-id="ae0f0-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="ae0f0-149">-SourceVersion</span></span>
<span data-ttu-id="ae0f0-150">Версия источника</span><span class="sxs-lookup"><span data-stu-id="ae0f0-150">Version of the source</span></span>

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

### <span data-ttu-id="ae0f0-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae0f0-151">-SubscriptionId</span></span>
<span data-ttu-id="ae0f0-152">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ae0f0-153">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ae0f0-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae0f0-154">-Confirm</span></span>
<span data-ttu-id="ae0f0-155">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae0f0-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae0f0-156">-WhatIf</span></span>
<span data-ttu-id="ae0f0-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae0f0-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae0f0-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae0f0-159">CommonParameters</span></span>
<span data-ttu-id="ae0f0-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae0f0-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae0f0-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae0f0-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae0f0-162">INPUTS</span></span>

### <span data-ttu-id="ae0f0-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ae0f0-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ae0f0-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ae0f0-164">OUTPUTS</span></span>

### <span data-ttu-id="ae0f0-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="ae0f0-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="ae0f0-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-166">NOTES</span></span>

<span data-ttu-id="ae0f0-167">ALIASES</span><span class="sxs-lookup"><span data-stu-id="ae0f0-167">ALIASES</span></span>

<span data-ttu-id="ae0f0-168">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ae0f0-169">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ae0f0-170">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ae0f0-171">INPUTOBJECT <ISpringCloudIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="ae0f0-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ae0f0-172">`[AppName <String>]`: название ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ae0f0-173">`[BindingName <String>]`: Имя ресурса привязки.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ae0f0-174">`[CertificateName <String>]`: имя ресурса сертификата.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ae0f0-175">`[DeploymentName <String>]`: Название ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ae0f0-176">`[DomainName <String>]`: имя ресурса настраиваемого домена.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ae0f0-177">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="ae0f0-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ae0f0-178">`[Location <String>]`: регион</span><span class="sxs-lookup"><span data-stu-id="ae0f0-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ae0f0-179">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ae0f0-180">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ae0f0-181">`[ServiceName <String>]`: Название ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ae0f0-182">`[SubscriptionId <String>]`. Получает ИД подписки, однозначно определяя подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ae0f0-183">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="ae0f0-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ae0f0-184">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae0f0-184">RELATED LINKS</span></span>

