---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 5594e43b2e6c67e9df5b526f753557edd8a4d5ea
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414736"
---
# <span data-ttu-id="c9ecd-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-101">Set-AzWebApp</span></span>

## <span data-ttu-id="c9ecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ecd-103">Изменяет Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="c9ecd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c9ecd-104">SYNTAX</span></span>

### <span data-ttu-id="c9ecd-105">S1</span><span class="sxs-lookup"><span data-stu-id="c9ecd-105">S1</span></span>
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

### <span data-ttu-id="c9ecd-106">S2</span><span class="sxs-lookup"><span data-stu-id="c9ecd-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ecd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="c9ecd-108">С **помощью cmdlet Set-AzWebApp** можно установить приложение Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c9ecd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c9ecd-109">EXAMPLES</span></span>

### <span data-ttu-id="c9ecd-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c9ecd-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="c9ecd-111">Эта команда изменяет план службы приложений, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="c9ecd-112">Воспользуйтесь ссылкой, чтобы узнать больше об изменении плана службы приложения и связанных с ним ограничений.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="c9ecd-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="c9ecd-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="c9ecd-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c9ecd-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c9ecd-115">Эта команда задает для httpLoggingEnabled значение true для Web App ContosoWebApp, связанное с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="c9ecd-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c9ecd-116">Example 3</span></span>

<span data-ttu-id="c9ecd-117">Изменяет Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="c9ecd-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c9ecd-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="c9ecd-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c9ecd-119">Example 4</span></span>

<span data-ttu-id="c9ecd-120">В следующем примере создается строка подключения с именем myConnectionString для Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="c9ecd-121">Эта строка заменяет все существующие строки подключения для Web App ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="c9ecd-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-122">PARAMETERS</span></span>

### <span data-ttu-id="c9ecd-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="c9ecd-123">-AlwaysOn</span></span>
<span data-ttu-id="c9ecd-124">Убедитесь, что веб-приложение загружается постоянно, а не в режиме простоя.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="c9ecd-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c9ecd-125">-AppServicePlan</span></span>
<span data-ttu-id="c9ecd-126">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="c9ecd-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="c9ecd-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c9ecd-127">-AppSettings</span></span>
<span data-ttu-id="c9ecd-128">HashTable "Параметры приложений".</span><span class="sxs-lookup"><span data-stu-id="c9ecd-128">App Settings HashTable.</span></span> <span data-ttu-id="c9ecd-129">Существующие параметры приложения будут заменены, а не предоставленные параметры.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="c9ecd-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c9ecd-130">-AsJob</span></span>
<span data-ttu-id="c9ecd-131">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c9ecd-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c9ecd-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c9ecd-132">-AssignIdentity</span></span>
<span data-ttu-id="c9ecd-133">Включить или отключить MSI в существующем веб-приложениях и приложениях Azure</span><span class="sxs-lookup"><span data-stu-id="c9ecd-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c9ecd-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c9ecd-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="c9ecd-135">Название слота назначения для автоматического обмена</span><span class="sxs-lookup"><span data-stu-id="c9ecd-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c9ecd-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c9ecd-136">-AzureStoragePath</span></span>
<span data-ttu-id="c9ecd-137">Хранилище Azure для крепления в веб-приложении для контейнера.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="c9ecd-138">Создание New-AzureRmWebAppAzureStoragePath с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="c9ecd-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="c9ecd-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c9ecd-139">-ConnectionStrings</span></span>
<span data-ttu-id="c9ecd-140">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="c9ecd-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c9ecd-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c9ecd-141">-ContainerImageName</span></span>
<span data-ttu-id="c9ecd-142">Имя контейнера изображения</span><span class="sxs-lookup"><span data-stu-id="c9ecd-142">Container Image Name</span></span>

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

### <span data-ttu-id="c9ecd-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c9ecd-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c9ecd-144">Пароль регистратора частного контейнера</span><span class="sxs-lookup"><span data-stu-id="c9ecd-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c9ecd-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c9ecd-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c9ecd-146">URL-адрес сервера частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="c9ecd-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c9ecd-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c9ecd-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="c9ecd-148">Имя пользователя частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="c9ecd-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c9ecd-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c9ecd-149">-DefaultDocuments</span></span>
<span data-ttu-id="c9ecd-150">Строка массива документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c9ecd-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="c9ecd-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ecd-151">-DefaultProfile</span></span>
<span data-ttu-id="c9ecd-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9ecd-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9ecd-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c9ecd-154">Boolean (Boolean) с включенным ведением журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="c9ecd-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c9ecd-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c9ecd-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c9ecd-156">Enables/Disables container continuous deployment webhook</span><span class="sxs-lookup"><span data-stu-id="c9ecd-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c9ecd-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="c9ecd-157">-FtpsState</span></span>
<span data-ttu-id="c9ecd-158">Установите состояние FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="c9ecd-159">Разрешенные значения [AllAllowed | Отключение | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="c9ecd-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="c9ecd-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c9ecd-160">-HandlerMappings</span></span>
<span data-ttu-id="c9ecd-161">IList сопоставлений обработбера</span><span class="sxs-lookup"><span data-stu-id="c9ecd-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c9ecd-162">-HostNames</span><span class="sxs-lookup"><span data-stu-id="c9ecd-162">-HostNames</span></span>
<span data-ttu-id="c9ecd-163">Строковое массив WebApp HostNames</span><span class="sxs-lookup"><span data-stu-id="c9ecd-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="c9ecd-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9ecd-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c9ecd-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c9ecd-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c9ecd-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c9ecd-166">-HttpsOnly</span></span>
<span data-ttu-id="c9ecd-167">Включить или отключить перенаправление всего трафика в HTTPS в существующем веб-приложениях и приложениях Azure</span><span class="sxs-lookup"><span data-stu-id="c9ecd-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c9ecd-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c9ecd-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="c9ecd-169">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="c9ecd-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c9ecd-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c9ecd-170">-MinTlsVersion</span></span>
<span data-ttu-id="c9ecd-171">Минимальная версия TLS, необходимая для SSL-запросов.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="c9ecd-172">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="c9ecd-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="c9ecd-173">-Name</span><span class="sxs-lookup"><span data-stu-id="c9ecd-173">-Name</span></span>
<span data-ttu-id="c9ecd-174">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c9ecd-174">WebApp Name</span></span>

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

### <span data-ttu-id="c9ecd-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c9ecd-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="c9ecd-176">Версия Net Framework</span><span class="sxs-lookup"><span data-stu-id="c9ecd-176">Net Framework Version</span></span>

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

### <span data-ttu-id="c9ecd-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c9ecd-177">-NumberOfWorkers</span></span>
<span data-ttu-id="c9ecd-178">Количество сотрудников, которые должны быть выделены</span><span class="sxs-lookup"><span data-stu-id="c9ecd-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c9ecd-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c9ecd-179">-PhpVersion</span></span>
<span data-ttu-id="c9ecd-180">Php Version</span><span class="sxs-lookup"><span data-stu-id="c9ecd-180">Php Version</span></span>

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

### <span data-ttu-id="c9ecd-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c9ecd-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="c9ecd-182">Запрос на трассировку включен</span><span class="sxs-lookup"><span data-stu-id="c9ecd-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="c9ecd-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ecd-183">-ResourceGroupName</span></span>
<span data-ttu-id="c9ecd-184">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c9ecd-184">Resource Group Name</span></span>

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

### <span data-ttu-id="c9ecd-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c9ecd-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c9ecd-186">Использование 32-битной оси рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="c9ecd-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c9ecd-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-187">-WebApp</span></span>
<span data-ttu-id="c9ecd-188">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-188">WebApp Object</span></span>

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

### <span data-ttu-id="c9ecd-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c9ecd-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="c9ecd-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c9ecd-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="c9ecd-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ecd-191">CommonParameters</span></span>
<span data-ttu-id="c9ecd-192">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ecd-193">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c9ecd-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ecd-194">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-194">INPUTS</span></span>

### <span data-ttu-id="c9ecd-195">System.Int32</span><span class="sxs-lookup"><span data-stu-id="c9ecd-195">System.Int32</span></span>

### <span data-ttu-id="c9ecd-196">System.String</span><span class="sxs-lookup"><span data-stu-id="c9ecd-196">System.String</span></span>

### <span data-ttu-id="c9ecd-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c9ecd-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9ecd-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c9ecd-198">OUTPUTS</span></span>

### <span data-ttu-id="c9ecd-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="c9ecd-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="c9ecd-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c9ecd-200">NOTES</span></span>
<span data-ttu-id="c9ecd-201">С помощью приведенного ниже cmdlet можно обновить Azure Web App до **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="c9ecd-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="c9ecd-202">$PropertiesObject = @{ "CURRENT_STACK" = "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span><span class="sxs-lookup"><span data-stu-id="c9ecd-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="c9ecd-203">Замените значения default-Web-WestUS именем группы ресурсов веб-приложения и ContosoWebApp именем веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c9ecd-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="c9ecd-204">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9ecd-204">RELATED LINKS</span></span>

[<span data-ttu-id="c9ecd-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="c9ecd-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="c9ecd-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="c9ecd-208">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="c9ecd-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="c9ecd-210">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="c9ecd-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

