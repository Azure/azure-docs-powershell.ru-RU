---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245233"
---
# <span data-ttu-id="89ccf-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="89ccf-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="89ccf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="89ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="89ccf-103">Создайте новое развертывание или обновите выходное развертывание.</span><span class="sxs-lookup"><span data-stu-id="89ccf-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="89ccf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="89ccf-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="89ccf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ccf-105">DESCRIPTION</span></span>
<span data-ttu-id="89ccf-106">Создайте новое развертывание или обновите выходное развертывание.</span><span class="sxs-lookup"><span data-stu-id="89ccf-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="89ccf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="89ccf-107">EXAMPLES</span></span>

### <span data-ttu-id="89ccf-108">Пример 1: Пример 1: создание веснного облачного развертывания.</span><span class="sxs-lookup"><span data-stu-id="89ccf-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

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

<span data-ttu-id="89ccf-109">Создание веснного облачного развертывания.</span><span class="sxs-lookup"><span data-stu-id="89ccf-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="89ccf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="89ccf-110">PARAMETERS</span></span>

### <span data-ttu-id="89ccf-111">-Имя_приложения</span><span class="sxs-lookup"><span data-stu-id="89ccf-111">-AppName</span></span>
<span data-ttu-id="89ccf-112">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="89ccf-112">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ccf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89ccf-113">-AsJob</span></span>
<span data-ttu-id="89ccf-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="89ccf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="89ccf-115">-ЦП</span><span class="sxs-lookup"><span data-stu-id="89ccf-115">-Cpu</span></span>
<span data-ttu-id="89ccf-116">Требуемый ЦП</span><span class="sxs-lookup"><span data-stu-id="89ccf-116">Required CPU</span></span>

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

### <span data-ttu-id="89ccf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89ccf-117">-DefaultProfile</span></span>
<span data-ttu-id="89ccf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89ccf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89ccf-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="89ccf-119">-EnvironmentVariable</span></span>
<span data-ttu-id="89ccf-120">Коллекция переменных среды</span><span class="sxs-lookup"><span data-stu-id="89ccf-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="89ccf-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="89ccf-121">-JvmOption</span></span>
<span data-ttu-id="89ccf-122">Параметр JVM</span><span class="sxs-lookup"><span data-stu-id="89ccf-122">JVM parameter</span></span>

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

### <span data-ttu-id="89ccf-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="89ccf-123">-MemoryInGb</span></span>
<span data-ttu-id="89ccf-124">Требуемый объем памяти в ГБ</span><span class="sxs-lookup"><span data-stu-id="89ccf-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="89ccf-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="89ccf-125">-Name</span></span>
<span data-ttu-id="89ccf-126">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="89ccf-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ccf-127">-Wait</span><span class="sxs-lookup"><span data-stu-id="89ccf-127">-NoWait</span></span>
<span data-ttu-id="89ccf-128">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="89ccf-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="89ccf-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89ccf-129">-ResourceGroupName</span></span>
<span data-ttu-id="89ccf-130">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="89ccf-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="89ccf-131">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="89ccf-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ccf-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="89ccf-132">-RuntimeVersion</span></span>
<span data-ttu-id="89ccf-133">Версия среды выполнения</span><span class="sxs-lookup"><span data-stu-id="89ccf-133">Runtime version</span></span>

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

### <span data-ttu-id="89ccf-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="89ccf-134">-ServiceName</span></span>
<span data-ttu-id="89ccf-135">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="89ccf-135">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ccf-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="89ccf-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="89ccf-137">Селектор для артефакта, который будет использоваться для развертывания проектов с несколькими модулями.</span><span class="sxs-lookup"><span data-stu-id="89ccf-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="89ccf-138">Это должен Bethe относительный путь к целевому модулю или проекту.</span><span class="sxs-lookup"><span data-stu-id="89ccf-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="89ccf-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="89ccf-139">-SourceRelativePath</span></span>
<span data-ttu-id="89ccf-140">Относительный путь к хранилищу, в котором хранится источник</span><span class="sxs-lookup"><span data-stu-id="89ccf-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="89ccf-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="89ccf-141">-SourceType</span></span>
<span data-ttu-id="89ccf-142">Тип источника, загруженного</span><span class="sxs-lookup"><span data-stu-id="89ccf-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="89ccf-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="89ccf-143">-SourceVersion</span></span>
<span data-ttu-id="89ccf-144">Версия исходного кода</span><span class="sxs-lookup"><span data-stu-id="89ccf-144">Version of the source</span></span>

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

### <span data-ttu-id="89ccf-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="89ccf-145">-SubscriptionId</span></span>
<span data-ttu-id="89ccf-146">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="89ccf-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="89ccf-147">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="89ccf-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89ccf-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89ccf-148">-Confirm</span></span>
<span data-ttu-id="89ccf-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="89ccf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89ccf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89ccf-150">-WhatIf</span></span>
<span data-ttu-id="89ccf-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="89ccf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89ccf-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="89ccf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89ccf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89ccf-153">CommonParameters</span></span>
<span data-ttu-id="89ccf-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="89ccf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89ccf-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89ccf-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89ccf-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="89ccf-156">INPUTS</span></span>

## <span data-ttu-id="89ccf-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="89ccf-157">OUTPUTS</span></span>

### <span data-ttu-id="89ccf-158">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="89ccf-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="89ccf-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="89ccf-159">NOTES</span></span>

<span data-ttu-id="89ccf-160">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="89ccf-160">ALIASES</span></span>

## <span data-ttu-id="89ccf-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89ccf-161">RELATED LINKS</span></span>

