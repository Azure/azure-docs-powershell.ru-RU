---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 37538cddb7654b665b2b2dd4935414a2cb76b45a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235620"
---
# <span data-ttu-id="c7a9c-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c7a9c-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c7a9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7a9c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a9c-103">Создайте новое развертывание или обновйте развертывание, выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c7a9c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7a9c-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a9c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7a9c-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a9c-106">Создайте новое развертывание или обновйте развертывание, выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="c7a9c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7a9c-107">EXAMPLES</span></span>

### <span data-ttu-id="c7a9c-108">Пример 1. Пример 1. Создание весенних облачных развертыванию.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="c7a9c-109">Создайте весенний облачный развертывание.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="c7a9c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7a9c-110">PARAMETERS</span></span>

### <span data-ttu-id="c7a9c-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="c7a9c-111">-AppName</span></span>
<span data-ttu-id="c7a9c-112">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="c7a9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7a9c-113">-AsJob</span></span>
<span data-ttu-id="c7a9c-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="c7a9c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c7a9c-115">-CPU</span><span class="sxs-lookup"><span data-stu-id="c7a9c-115">-Cpu</span></span>
<span data-ttu-id="c7a9c-116">Требуемая ЦП</span><span class="sxs-lookup"><span data-stu-id="c7a9c-116">Required CPU</span></span>

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

### <span data-ttu-id="c7a9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a9c-117">-DefaultProfile</span></span>
<span data-ttu-id="c7a9c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7a9c-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c7a9c-119">-EnvironmentVariable</span></span>
<span data-ttu-id="c7a9c-120">Набор переменных среды</span><span class="sxs-lookup"><span data-stu-id="c7a9c-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="c7a9c-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c7a9c-121">-JvmOption</span></span>
<span data-ttu-id="c7a9c-122">Параметр JVM</span><span class="sxs-lookup"><span data-stu-id="c7a9c-122">JVM parameter</span></span>

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

### <span data-ttu-id="c7a9c-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c7a9c-123">-MemoryInGb</span></span>
<span data-ttu-id="c7a9c-124">Необходимый размер памяти в ГБ</span><span class="sxs-lookup"><span data-stu-id="c7a9c-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="c7a9c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c7a9c-125">-Name</span></span>
<span data-ttu-id="c7a9c-126">Имя ресурса развертывания.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-126">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="c7a9c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c7a9c-127">-NoWait</span></span>
<span data-ttu-id="c7a9c-128">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="c7a9c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c7a9c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a9c-129">-ResourceGroupName</span></span>
<span data-ttu-id="c7a9c-130">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c7a9c-131">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c7a9c-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c7a9c-132">-RuntimeVersion</span></span>
<span data-ttu-id="c7a9c-133">Версия Runtime</span><span class="sxs-lookup"><span data-stu-id="c7a9c-133">Runtime version</span></span>

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

### <span data-ttu-id="c7a9c-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c7a9c-134">-ServiceName</span></span>
<span data-ttu-id="c7a9c-135">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c7a9c-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c7a9c-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="c7a9c-137">Селектор артефакта, который будет использоваться для развертывания проектов с несколькими модулями.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c7a9c-138">Это должен быть относительный путь к целевому модуле или проекту.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="c7a9c-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c7a9c-139">-SourceRelativePath</span></span>
<span data-ttu-id="c7a9c-140">Относительный путь к хранилищу, в котором хранится источник</span><span class="sxs-lookup"><span data-stu-id="c7a9c-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="c7a9c-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c7a9c-141">-SourceType</span></span>
<span data-ttu-id="c7a9c-142">Тип добавленного источника</span><span class="sxs-lookup"><span data-stu-id="c7a9c-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="c7a9c-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c7a9c-143">-SourceVersion</span></span>
<span data-ttu-id="c7a9c-144">Версия источника</span><span class="sxs-lookup"><span data-stu-id="c7a9c-144">Version of the source</span></span>

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

### <span data-ttu-id="c7a9c-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c7a9c-145">-SubscriptionId</span></span>
<span data-ttu-id="c7a9c-146">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c7a9c-147">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c7a9c-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7a9c-148">-Confirm</span></span>
<span data-ttu-id="c7a9c-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a9c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a9c-150">-WhatIf</span></span>
<span data-ttu-id="c7a9c-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a9c-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a9c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a9c-153">CommonParameters</span></span>
<span data-ttu-id="c7a9c-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a9c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a9c-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7a9c-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a9c-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a9c-156">INPUTS</span></span>

## <span data-ttu-id="c7a9c-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7a9c-157">OUTPUTS</span></span>

### <span data-ttu-id="c7a9c-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c7a9c-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="c7a9c-159">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7a9c-159">NOTES</span></span>

<span data-ttu-id="c7a9c-160">ALIASES</span><span class="sxs-lookup"><span data-stu-id="c7a9c-160">ALIASES</span></span>

## <span data-ttu-id="c7a9c-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7a9c-161">RELATED LINKS</span></span>

