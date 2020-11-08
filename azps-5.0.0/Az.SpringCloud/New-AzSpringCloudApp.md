---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245237"
---
# <span data-ttu-id="ef5a4-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="ef5a4-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="ef5a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ef5a4-103">Создайте новое приложение или обновите приложение для выхода.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="ef5a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef5a4-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ef5a4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ef5a4-106">Создайте новое приложение или обновите приложение для выхода.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="ef5a4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ef5a4-108">Пример 1: создание веснного облачного приложения.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-108">Example 1: Create a spring cloud app.</span></span>
```powershell
PS C:\> New-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
ActiveDeploymentName    :
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

<span data-ttu-id="ef5a4-109">Создание приложения "пружинное облако".</span><span class="sxs-lookup"><span data-stu-id="ef5a4-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="ef5a4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-110">PARAMETERS</span></span>

### <span data-ttu-id="ef5a4-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="ef5a4-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="ef5a4-112">Имя активного развертывания приложения</span><span class="sxs-lookup"><span data-stu-id="ef5a4-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="ef5a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ef5a4-113">-AsJob</span></span>
<span data-ttu-id="ef5a4-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ef5a4-114">Run the command as a job</span></span>

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

### <span data-ttu-id="ef5a4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef5a4-115">-DefaultProfile</span></span>
<span data-ttu-id="ef5a4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef5a4-117">-FQDN</span><span class="sxs-lookup"><span data-stu-id="ef5a4-117">-Fqdn</span></span>
<span data-ttu-id="ef5a4-118">Полное DNS-имя.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="ef5a4-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="ef5a4-119">-HttpsOnly</span></span>
<span data-ttu-id="ef5a4-120">Укажите, разрешено ли использование HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="ef5a4-121">-Location</span><span class="sxs-lookup"><span data-stu-id="ef5a4-121">-Location</span></span>
<span data-ttu-id="ef5a4-122">Географическое расположение приложения, которое всегда одинаково с родительским ресурсом</span><span class="sxs-lookup"><span data-stu-id="ef5a4-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="ef5a4-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ef5a4-123">-Name</span></span>
<span data-ttu-id="ef5a4-124">Имя ресурса приложения.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-124">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef5a4-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="ef5a4-125">-NoWait</span></span>
<span data-ttu-id="ef5a4-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="ef5a4-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ef5a4-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="ef5a4-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="ef5a4-128">Путь подключения постоянного диска</span><span class="sxs-lookup"><span data-stu-id="ef5a4-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="ef5a4-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="ef5a4-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="ef5a4-130">Размер постоянного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="ef5a4-131">-Public</span><span class="sxs-lookup"><span data-stu-id="ef5a4-131">-Public</span></span>
<span data-ttu-id="ef5a4-132">Указывает, предоставляет ли приложение общедоступную конечную точку</span><span class="sxs-lookup"><span data-stu-id="ef5a4-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="ef5a4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef5a4-133">-ResourceGroupName</span></span>
<span data-ttu-id="ef5a4-134">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ef5a4-135">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="ef5a4-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ef5a4-136">-ServiceName</span></span>
<span data-ttu-id="ef5a4-137">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="ef5a4-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ef5a4-138">-SubscriptionId</span></span>
<span data-ttu-id="ef5a4-139">Получает идентификатор подписки, который однозначно определяет подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ef5a4-140">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ef5a4-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="ef5a4-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="ef5a4-142">Путь к временному диску для подключения</span><span class="sxs-lookup"><span data-stu-id="ef5a4-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="ef5a4-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="ef5a4-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="ef5a4-144">Размер временного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="ef5a4-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef5a4-145">-Confirm</span></span>
<span data-ttu-id="ef5a4-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef5a4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef5a4-147">-WhatIf</span></span>
<span data-ttu-id="ef5a4-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef5a4-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef5a4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef5a4-150">CommonParameters</span></span>
<span data-ttu-id="ef5a4-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef5a4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef5a4-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef5a4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef5a4-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef5a4-153">INPUTS</span></span>

## <span data-ttu-id="ef5a4-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-154">OUTPUTS</span></span>

### <span data-ttu-id="ef5a4-155">Microsoft. Azure. PowerShell. командлеты. SpringCloud. Models. Api20200701. IAppResource</span><span class="sxs-lookup"><span data-stu-id="ef5a4-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="ef5a4-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef5a4-156">NOTES</span></span>

<span data-ttu-id="ef5a4-157">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-157">ALIASES</span></span>

## <span data-ttu-id="ef5a4-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef5a4-158">RELATED LINKS</span></span>

