---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 46c5dae54bf4f59556e62256797a43221d0650b7
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412356"
---
# <span data-ttu-id="c7d00-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-101">Set-AzWebApp</span></span>

## <span data-ttu-id="c7d00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7d00-102">SYNOPSIS</span></span>
<span data-ttu-id="c7d00-103">Изменяет Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c7d00-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="c7d00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c7d00-104">SYNTAX</span></span>

### <span data-ttu-id="c7d00-105">S1</span><span class="sxs-lookup"><span data-stu-id="c7d00-105">S1</span></span>
```
Set-AzWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>] [[-NetFrameworkVersion] <String>]
 [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>] [[-HttpLoggingEnabled] <Boolean>]
 [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>] [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-AzureStoragePath <WebAppAzureStoragePath[]>]
 [-AlwaysOn <Boolean>] [-MinTlsVersion <String>] [-FtpsState <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7d00-106">S2</span><span class="sxs-lookup"><span data-stu-id="c7d00-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7d00-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7d00-107">DESCRIPTION</span></span>
<span data-ttu-id="c7d00-108">С **помощью cmdlet Set-AzWebApp** можно установить приложение Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c7d00-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c7d00-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c7d00-109">EXAMPLES</span></span>

### <span data-ttu-id="c7d00-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7d00-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c7d00-111">Эта команда изменяет план службы приложений, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c7d00-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c7d00-112">Воспользуйтесь ссылкой, чтобы узнать больше об изменении плана службы приложения и связанных с ним ограничений.</span><span class="sxs-lookup"><span data-stu-id="c7d00-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c7d00-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c7d00-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c7d00-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c7d00-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c7d00-115">Эта команда задает для httpLoggingEnabled значение true для Web App ContosoWebApp, связанное с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c7d00-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c7d00-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c7d00-116">Example 3</span></span>

<span data-ttu-id="c7d00-117">Изменяет Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c7d00-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="c7d00-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c7d00-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="c7d00-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7d00-119">PARAMETERS</span></span>

### <span data-ttu-id="c7d00-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c7d00-120">-AlwaysOn</span></span>
<span data-ttu-id="c7d00-121">Убедитесь, что веб-приложение загружается постоянно, а не в режиме простоя.</span><span class="sxs-lookup"><span data-stu-id="c7d00-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c7d00-122">-AppServicePlan</span></span>
<span data-ttu-id="c7d00-123">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="c7d00-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c7d00-124">-AppSettings</span></span>
<span data-ttu-id="c7d00-125">HashTable "Параметры приложений".</span><span class="sxs-lookup"><span data-stu-id="c7d00-125">App Settings HashTable.</span></span> <span data-ttu-id="c7d00-126">Существующие параметры приложения будут заменены, а не предоставленные параметры.</span><span class="sxs-lookup"><span data-stu-id="c7d00-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7d00-127">-AsJob</span></span>
<span data-ttu-id="c7d00-128">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c7d00-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7d00-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c7d00-129">-AssignIdentity</span></span>
<span data-ttu-id="c7d00-130">Включить или отключить MSI в существующем веб-приложениях и приложениях Azure</span><span class="sxs-lookup"><span data-stu-id="c7d00-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c7d00-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="c7d00-132">Название слота назначения для автоматического обмена</span><span class="sxs-lookup"><span data-stu-id="c7d00-132">Destination slot name for auto swap</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c7d00-133">-AzureStoragePath</span></span>
<span data-ttu-id="c7d00-134">Хранилище Azure для крепления в веб-приложении для контейнера.</span><span class="sxs-lookup"><span data-stu-id="c7d00-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c7d00-135">Создание New-AzureRmWebAppAzureStoragePath с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c7d00-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c7d00-136">-ConnectionStrings</span></span>
<span data-ttu-id="c7d00-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="c7d00-137">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: S1
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c7d00-138">-ContainerImageName</span></span>
<span data-ttu-id="c7d00-139">Имя контейнера изображения</span><span class="sxs-lookup"><span data-stu-id="c7d00-139">Container Image Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c7d00-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c7d00-141">Пароль регистратора частного контейнера</span><span class="sxs-lookup"><span data-stu-id="c7d00-141">Private Container Registry Password</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c7d00-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c7d00-143">URL-адрес сервера частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="c7d00-143">Private Container Registry Server Url</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c7d00-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="c7d00-145">Имя пользователя частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="c7d00-145">Private Container Registry Username</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c7d00-146">-DefaultDocuments</span></span>
<span data-ttu-id="c7d00-147">Строка массива документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c7d00-147">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7d00-148">-DefaultProfile</span></span>
<span data-ttu-id="c7d00-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c7d00-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7d00-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c7d00-151">Boolean (Boolean) с включенным ведением журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="c7d00-151">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c7d00-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c7d00-153">Enables/Disables container continuous deployment webhook</span><span class="sxs-lookup"><span data-stu-id="c7d00-153">Enables/Disables container continuous deployment webhook</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c7d00-154">-FtpsState</span></span>
<span data-ttu-id="c7d00-155">Установите состояние FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="c7d00-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c7d00-156">Разрешенные значения [AllAllowed | Отключение | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c7d00-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c7d00-157">-HandlerMappings</span></span>
<span data-ttu-id="c7d00-158">IList сопоставлений обработбера</span><span class="sxs-lookup"><span data-stu-id="c7d00-158">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: S1
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-159">-HostNames</span><span class="sxs-lookup"><span data-stu-id="c7d00-159">-HostNames</span></span>
<span data-ttu-id="c7d00-160">Строковое массив WebApp HostNames</span><span class="sxs-lookup"><span data-stu-id="c7d00-160">WebApp HostNames String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7d00-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c7d00-162">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c7d00-162">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c7d00-163">-HttpsOnly</span></span>
<span data-ttu-id="c7d00-164">Включить или отключить перенаправление всего трафика в HTTPS в существующем веб-приложениях и приложениях Azure</span><span class="sxs-lookup"><span data-stu-id="c7d00-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c7d00-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="c7d00-166">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="c7d00-166">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c7d00-167">-MinTlsVersion</span></span>
<span data-ttu-id="c7d00-168">Минимальная версия TLS, необходимая для SSL-запросов.</span><span class="sxs-lookup"><span data-stu-id="c7d00-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c7d00-169">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c7d00-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-170">-Name</span><span class="sxs-lookup"><span data-stu-id="c7d00-170">-Name</span></span>
<span data-ttu-id="c7d00-171">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c7d00-171">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c7d00-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="c7d00-173">Версия Net Framework</span><span class="sxs-lookup"><span data-stu-id="c7d00-173">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c7d00-174">-NumberOfWorkers</span></span>
<span data-ttu-id="c7d00-175">Количество сотрудников, которые должны быть выделены</span><span class="sxs-lookup"><span data-stu-id="c7d00-175">The number of workers to be allocated</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c7d00-176">-PhpVersion</span></span>
<span data-ttu-id="c7d00-177">Php Version</span><span class="sxs-lookup"><span data-stu-id="c7d00-177">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c7d00-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="c7d00-179">Запрос на трассировку включен</span><span class="sxs-lookup"><span data-stu-id="c7d00-179">Request Tracing Enabled</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7d00-180">-ResourceGroupName</span></span>
<span data-ttu-id="c7d00-181">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c7d00-181">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c7d00-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c7d00-183">Использование 32-битной оси рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="c7d00-183">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-184">-WebApp</span></span>
<span data-ttu-id="c7d00-185">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-185">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c7d00-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="c7d00-187">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c7d00-187">WebSocketsEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases:

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7d00-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7d00-188">CommonParameters</span></span>
<span data-ttu-id="c7d00-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7d00-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7d00-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7d00-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7d00-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c7d00-191">INPUTS</span></span>

### <span data-ttu-id="c7d00-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c7d00-192">System.Int32</span></span>

### <span data-ttu-id="c7d00-193">System.String</span><span class="sxs-lookup"><span data-stu-id="c7d00-193">System.String</span></span>

### <span data-ttu-id="c7d00-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c7d00-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7d00-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7d00-195">OUTPUTS</span></span>

### <span data-ttu-id="c7d00-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c7d00-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c7d00-197">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c7d00-197">NOTES</span></span>
<span data-ttu-id="c7d00-198">С помощью приведенного ниже cmdlet можно обновить Azure Web App до **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="c7d00-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="c7d00-199">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="c7d00-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="c7d00-200">Замените значения default-Web-WestUS именем группы ресурсов веб-приложения и ContosoWebApp именем веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c7d00-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="c7d00-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7d00-201">RELATED LINKS</span></span>

[<span data-ttu-id="c7d00-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c7d00-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c7d00-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c7d00-205">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c7d00-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c7d00-207">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c7d00-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

