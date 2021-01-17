---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudApp.md
ms.openlocfilehash: c8f723a66ee388244f2aab9ab556ea315f44e72c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398964"
---
# <span data-ttu-id="82fd9-101">New-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="82fd9-101">New-AzSpringCloudApp</span></span>

## <span data-ttu-id="82fd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82fd9-102">SYNOPSIS</span></span>
<span data-ttu-id="82fd9-103">Создайте новое приложение или обновйте приложение, выйдите из него.</span><span class="sxs-lookup"><span data-stu-id="82fd9-103">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="82fd9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82fd9-104">SYNTAX</span></span>

```
New-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="82fd9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82fd9-105">DESCRIPTION</span></span>
<span data-ttu-id="82fd9-106">Создайте новое приложение или обновйте приложение, выйдите из него.</span><span class="sxs-lookup"><span data-stu-id="82fd9-106">Create a new App or update an exiting App.</span></span>

## <span data-ttu-id="82fd9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82fd9-107">EXAMPLES</span></span>

### <span data-ttu-id="82fd9-108">Пример 1. Создание весенних облачных приложений.</span><span class="sxs-lookup"><span data-stu-id="82fd9-108">Example 1: Create a spring cloud app.</span></span>
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

<span data-ttu-id="82fd9-109">Создайте весенние облачные приложения.</span><span class="sxs-lookup"><span data-stu-id="82fd9-109">Create a spring cloud app.</span></span>

## <span data-ttu-id="82fd9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82fd9-110">PARAMETERS</span></span>

### <span data-ttu-id="82fd9-111">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="82fd9-111">-ActiveDeploymentName</span></span>
<span data-ttu-id="82fd9-112">Имя активного развертывания Приложения</span><span class="sxs-lookup"><span data-stu-id="82fd9-112">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="82fd9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82fd9-113">-AsJob</span></span>
<span data-ttu-id="82fd9-114">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="82fd9-114">Run the command as a job</span></span>

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

### <span data-ttu-id="82fd9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fd9-115">-DefaultProfile</span></span>
<span data-ttu-id="82fd9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82fd9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82fd9-117">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="82fd9-117">-Fqdn</span></span>
<span data-ttu-id="82fd9-118">Полное имя DNS.</span><span class="sxs-lookup"><span data-stu-id="82fd9-118">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="82fd9-119">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="82fd9-119">-HttpsOnly</span></span>
<span data-ttu-id="82fd9-120">Указать, разрешено ли использовать только https.</span><span class="sxs-lookup"><span data-stu-id="82fd9-120">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="82fd9-121">-Location</span><span class="sxs-lookup"><span data-stu-id="82fd9-121">-Location</span></span>
<span data-ttu-id="82fd9-122">Географическое расположение приложения всегда одинаковое с родительским ресурсом</span><span class="sxs-lookup"><span data-stu-id="82fd9-122">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="82fd9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="82fd9-123">-Name</span></span>
<span data-ttu-id="82fd9-124">Имя ресурса Приложения.</span><span class="sxs-lookup"><span data-stu-id="82fd9-124">The name of the App resource.</span></span>

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

### <span data-ttu-id="82fd9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="82fd9-125">-NoWait</span></span>
<span data-ttu-id="82fd9-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="82fd9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="82fd9-127">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="82fd9-127">-PersistentDiskMountPath</span></span>
<span data-ttu-id="82fd9-128">Путь к сохраняемого диска</span><span class="sxs-lookup"><span data-stu-id="82fd9-128">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="82fd9-129">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="82fd9-129">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="82fd9-130">Размер сохраняемого диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="82fd9-130">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="82fd9-131">-Public</span><span class="sxs-lookup"><span data-stu-id="82fd9-131">-Public</span></span>
<span data-ttu-id="82fd9-132">Указывает на то, является ли приложение общедоступным конечным точкой</span><span class="sxs-lookup"><span data-stu-id="82fd9-132">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="82fd9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82fd9-133">-ResourceGroupName</span></span>
<span data-ttu-id="82fd9-134">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="82fd9-134">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="82fd9-135">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="82fd9-135">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="82fd9-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="82fd9-136">-ServiceName</span></span>
<span data-ttu-id="82fd9-137">Имя ресурса службы.</span><span class="sxs-lookup"><span data-stu-id="82fd9-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="82fd9-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="82fd9-138">-SubscriptionId</span></span>
<span data-ttu-id="82fd9-139">Возвращает ИД подписки, однозначно определяемую подпиской Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="82fd9-139">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="82fd9-140">Он является частью URI каждого звонка службы.</span><span class="sxs-lookup"><span data-stu-id="82fd9-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="82fd9-141">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="82fd9-141">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="82fd9-142">Путь к временному диску</span><span class="sxs-lookup"><span data-stu-id="82fd9-142">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="82fd9-143">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="82fd9-143">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="82fd9-144">Размер временного диска в ГБ</span><span class="sxs-lookup"><span data-stu-id="82fd9-144">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="82fd9-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82fd9-145">-Confirm</span></span>
<span data-ttu-id="82fd9-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82fd9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82fd9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82fd9-147">-WhatIf</span></span>
<span data-ttu-id="82fd9-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82fd9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82fd9-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82fd9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82fd9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fd9-150">CommonParameters</span></span>
<span data-ttu-id="82fd9-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82fd9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fd9-152">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82fd9-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fd9-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82fd9-153">INPUTS</span></span>

## <span data-ttu-id="82fd9-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82fd9-154">OUTPUTS</span></span>

### <span data-ttu-id="82fd9-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="82fd9-155">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="82fd9-156">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82fd9-156">NOTES</span></span>

<span data-ttu-id="82fd9-157">ALIASES</span><span class="sxs-lookup"><span data-stu-id="82fd9-157">ALIASES</span></span>

## <span data-ttu-id="82fd9-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82fd9-158">RELATED LINKS</span></span>

