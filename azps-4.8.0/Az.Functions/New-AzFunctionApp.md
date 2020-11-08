---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236696"
---
# <span data-ttu-id="02232-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="02232-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="02232-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02232-102">SYNOPSIS</span></span>
<span data-ttu-id="02232-103">Создает приложение функции.</span><span class="sxs-lookup"><span data-stu-id="02232-103">Creates a function app.</span></span>

## <span data-ttu-id="02232-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02232-104">SYNTAX</span></span>

### <span data-ttu-id="02232-105">Потребление (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02232-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02232-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="02232-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02232-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="02232-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02232-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02232-108">DESCRIPTION</span></span>
<span data-ttu-id="02232-109">Создает приложение функции.</span><span class="sxs-lookup"><span data-stu-id="02232-109">Creates a function app.</span></span>

## <span data-ttu-id="02232-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02232-110">EXAMPLES</span></span>

### <span data-ttu-id="02232-111">Пример 1: создание приложения функции PowerShell для потребления в Центральной США.</span><span class="sxs-lookup"><span data-stu-id="02232-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="02232-112">Эта команда создает приложение функции PowerShell для потребления в Центральной США.</span><span class="sxs-lookup"><span data-stu-id="02232-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="02232-113">Пример 2: создание приложения функции PowerShell, которое будет размещено в плане служб.</span><span class="sxs-lookup"><span data-stu-id="02232-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="02232-114">Эта команда создает приложение функции PowerShell, которое будет размещено в плане служб.</span><span class="sxs-lookup"><span data-stu-id="02232-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="02232-115">Пример 3: создание приложения-функции с использованием закрытого изображения контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="02232-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="02232-116">Эта команда создает приложение-функцию с использованием закрытого изображения контроля доступа.</span><span class="sxs-lookup"><span data-stu-id="02232-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="02232-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02232-117">PARAMETERS</span></span>

### <span data-ttu-id="02232-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="02232-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="02232-119">Клавиша инструментирования для добавляемого приложения Application Insights.</span><span class="sxs-lookup"><span data-stu-id="02232-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="02232-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="02232-121">Имя существующего проекта Application Insights, который нужно добавить в приложение Function.</span><span class="sxs-lookup"><span data-stu-id="02232-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="02232-122">-AppSetting</span></span>
<span data-ttu-id="02232-123">Функциональные параметры приложения.</span><span class="sxs-lookup"><span data-stu-id="02232-123">Function app settings.</span></span>

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

### <span data-ttu-id="02232-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02232-124">-AsJob</span></span>
<span data-ttu-id="02232-125">Запускает командлет в качестве фонового задания.</span><span class="sxs-lookup"><span data-stu-id="02232-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="02232-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02232-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="02232-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="02232-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="02232-128">Отключение возможности создания ресурсов Application Insights во время создания приложения функции.</span><span class="sxs-lookup"><span data-stu-id="02232-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="02232-129">Журналы не будут доступны.</span><span class="sxs-lookup"><span data-stu-id="02232-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="02232-130">-DockerImageName</span></span>
<span data-ttu-id="02232-131">Только для Linux.</span><span class="sxs-lookup"><span data-stu-id="02232-131">Linux only.</span></span>
<span data-ttu-id="02232-132">Имя контейнера в реестре, например Publisher/Image-Name: Tag.</span><span class="sxs-lookup"><span data-stu-id="02232-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="02232-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="02232-134">Имя пользователя и пароль в реестре контейнера.</span><span class="sxs-lookup"><span data-stu-id="02232-134">The container registry user name and password.</span></span>
<span data-ttu-id="02232-135">Требуется для закрытых реестров.</span><span class="sxs-lookup"><span data-stu-id="02232-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="02232-136">-FunctionsVersion</span></span>
<span data-ttu-id="02232-137">Версия функции.</span><span class="sxs-lookup"><span data-stu-id="02232-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="02232-138">-IdentityID</span></span>
<span data-ttu-id="02232-139">Указывает список удостоверений пользователей, связанных с приложением "функция".</span><span class="sxs-lookup"><span data-stu-id="02232-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="02232-140">Ссылки на удостоверения пользователей будут идентификаторами ресурсов ARM в форме "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}".</span><span class="sxs-lookup"><span data-stu-id="02232-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="02232-141">-IdentityType</span></span>
<span data-ttu-id="02232-142">Указывает тип удостоверения, используемого для приложения функции.</span><span class="sxs-lookup"><span data-stu-id="02232-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="02232-143">Допустимые значения этого параметра:-SystemAssigned-UserAssigned</span><span class="sxs-lookup"><span data-stu-id="02232-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-144">-Location</span><span class="sxs-lookup"><span data-stu-id="02232-144">-Location</span></span>
<span data-ttu-id="02232-145">Место для плана потребления.</span><span class="sxs-lookup"><span data-stu-id="02232-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02232-146">-Name</span></span>
<span data-ttu-id="02232-147">Имя приложения функции.</span><span class="sxs-lookup"><span data-stu-id="02232-147">The name of the function app.</span></span>

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

### <span data-ttu-id="02232-148">-Wait</span><span class="sxs-lookup"><span data-stu-id="02232-148">-NoWait</span></span>
<span data-ttu-id="02232-149">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="02232-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="02232-150">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="02232-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="02232-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="02232-151">-OSType</span></span>
<span data-ttu-id="02232-152">Операционная система, в которой будет размещено приложение "функция".</span><span class="sxs-lookup"><span data-stu-id="02232-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02232-153">-PassThru</span></span>
<span data-ttu-id="02232-154">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="02232-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="02232-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="02232-155">-PlanName</span></span>
<span data-ttu-id="02232-156">Имя плана обслуживания.</span><span class="sxs-lookup"><span data-stu-id="02232-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02232-157">-ResourceGroupName</span></span>
<span data-ttu-id="02232-158">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02232-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="02232-159">-Runtime</span><span class="sxs-lookup"><span data-stu-id="02232-159">-Runtime</span></span>
<span data-ttu-id="02232-160">Среда выполнения функции.</span><span class="sxs-lookup"><span data-stu-id="02232-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="02232-161">-RuntimeVersion</span></span>
<span data-ttu-id="02232-162">Среда выполнения функции.</span><span class="sxs-lookup"><span data-stu-id="02232-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02232-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02232-163">-StorageAccountName</span></span>
<span data-ttu-id="02232-164">Имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="02232-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="02232-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02232-165">-SubscriptionId</span></span>
<span data-ttu-id="02232-166">Идентификатор подписки Azure.</span><span class="sxs-lookup"><span data-stu-id="02232-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="02232-167">-Тег</span><span class="sxs-lookup"><span data-stu-id="02232-167">-Tag</span></span>
<span data-ttu-id="02232-168">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="02232-168">Resource tags.</span></span>

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

### <span data-ttu-id="02232-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02232-169">-Confirm</span></span>
<span data-ttu-id="02232-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02232-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02232-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02232-171">-WhatIf</span></span>
<span data-ttu-id="02232-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02232-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02232-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02232-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02232-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02232-174">CommonParameters</span></span>
<span data-ttu-id="02232-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02232-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02232-176">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02232-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02232-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02232-177">INPUTS</span></span>

## <span data-ttu-id="02232-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02232-178">OUTPUTS</span></span>

### <span data-ttu-id="02232-179">Microsoft. Azure. PowerShell. командлеты. functions. Models. Api20190801. ISite</span><span class="sxs-lookup"><span data-stu-id="02232-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="02232-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="02232-180">NOTES</span></span>

<span data-ttu-id="02232-181">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="02232-181">ALIASES</span></span>

## <span data-ttu-id="02232-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02232-182">RELATED LINKS</span></span>

