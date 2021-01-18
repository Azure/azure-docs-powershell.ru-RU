---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505721"
---
# <span data-ttu-id="893dc-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="893dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="893dc-102">SYNOPSIS</span></span>
<span data-ttu-id="893dc-103">Изменяет слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="893dc-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="893dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="893dc-104">SYNTAX</span></span>

### <span data-ttu-id="893dc-105">S1</span><span class="sxs-lookup"><span data-stu-id="893dc-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-AlwaysOn <Boolean>] [-MinTlsVersion <String>]
 [-FtpsState <String>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="893dc-106">S2</span><span class="sxs-lookup"><span data-stu-id="893dc-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="893dc-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="893dc-107">DESCRIPTION</span></span>
<span data-ttu-id="893dc-108">С **помощью cmdlet Set-AzWebApp** можно установить слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="893dc-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="893dc-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="893dc-109">EXAMPLES</span></span>

### <span data-ttu-id="893dc-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="893dc-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="893dc-111">Эта команда изменяет план службы приложений, связанный с Slot001, в веб-приложении ContosoWebApp, связанном с группой ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="893dc-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="893dc-112">Воспользуйтесь ссылкой, чтобы узнать больше об изменении плана службы приложения и связанных с ним ограничений.</span><span class="sxs-lookup"><span data-stu-id="893dc-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="893dc-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="893dc-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="893dc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="893dc-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="893dc-115">Эта команда задает для httpLoggingEnabled значение true в slot Slot001, относящуюся к Web App ContosoWebApp, связанному с группой ресурсов Default-Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="893dc-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="893dc-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="893dc-116">Example 3</span></span>

<span data-ttu-id="893dc-117">Изменяет слот Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="893dc-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="893dc-118">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="893dc-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="893dc-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="893dc-119">PARAMETERS</span></span>

### <span data-ttu-id="893dc-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="893dc-120">-AlwaysOn</span></span>
<span data-ttu-id="893dc-121">Убедитесь, что веб-приложение загружается постоянно, а не в режиме простоя.</span><span class="sxs-lookup"><span data-stu-id="893dc-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="893dc-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="893dc-122">-AppServicePlan</span></span>
<span data-ttu-id="893dc-123">Название плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="893dc-123">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="893dc-124">-AppSettings</span></span>
<span data-ttu-id="893dc-125">HashTable "Параметры приложений".</span><span class="sxs-lookup"><span data-stu-id="893dc-125">App Settings HashTable.</span></span> <span data-ttu-id="893dc-126">Существующие параметры приложения будут заменены, а не предоставленные параметры.</span><span class="sxs-lookup"><span data-stu-id="893dc-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="893dc-127">-AsJob</span></span>
<span data-ttu-id="893dc-128">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="893dc-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="893dc-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="893dc-129">-AssignIdentity</span></span>
<span data-ttu-id="893dc-130">Включить или отключить MSI в существующем слоте [PREVIEW]</span><span class="sxs-lookup"><span data-stu-id="893dc-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="893dc-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="893dc-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="893dc-132">Название места назначения для автоматического обмена</span><span class="sxs-lookup"><span data-stu-id="893dc-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="893dc-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="893dc-133">-AzureStoragePath</span></span>
<span data-ttu-id="893dc-134">Хранилище Azure для крепления в веб-приложении для контейнера.</span><span class="sxs-lookup"><span data-stu-id="893dc-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="893dc-135">Создание New-AzureRmWebAppAzureStoragePath с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="893dc-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="893dc-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="893dc-136">-ConnectionStrings</span></span>
<span data-ttu-id="893dc-137">Connection Strings HashTable</span><span class="sxs-lookup"><span data-stu-id="893dc-137">Connection Strings HashTable</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="893dc-138">-ContainerImageName</span></span>
<span data-ttu-id="893dc-139">Имя контейнера изображения</span><span class="sxs-lookup"><span data-stu-id="893dc-139">Container Image Name</span></span>

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

### <span data-ttu-id="893dc-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="893dc-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="893dc-141">Пароль регистратора личных контейнеров</span><span class="sxs-lookup"><span data-stu-id="893dc-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="893dc-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="893dc-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="893dc-143">URL-адрес сервера частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="893dc-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="893dc-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="893dc-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="893dc-145">Имя пользователя частного контейнера реестра</span><span class="sxs-lookup"><span data-stu-id="893dc-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="893dc-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="893dc-146">-DefaultDocuments</span></span>
<span data-ttu-id="893dc-147">Строка массива документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="893dc-147">Default Documents String Array</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893dc-148">-DefaultProfile</span></span>
<span data-ttu-id="893dc-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="893dc-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="893dc-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="893dc-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="893dc-151">Boolean (Boolean) с включенным ведением журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="893dc-151">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="893dc-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="893dc-153">Enables/Disables container continuous deployment webhook</span><span class="sxs-lookup"><span data-stu-id="893dc-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="893dc-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="893dc-154">-FtpsState</span></span>
<span data-ttu-id="893dc-155">Установите состояние FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="893dc-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="893dc-156">Разрешенные значения [AllAllowed | Отключено | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="893dc-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="893dc-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="893dc-157">-HandlerMappings</span></span>
<span data-ttu-id="893dc-158">IList сопоставлений обработбера</span><span class="sxs-lookup"><span data-stu-id="893dc-158">Handler Mappings IList</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="893dc-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="893dc-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="893dc-160">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="893dc-161">-HttpsOnly</span></span>
<span data-ttu-id="893dc-162">Включить или отключить перенаправление всего трафика в HTTPS в существующем слоте</span><span class="sxs-lookup"><span data-stu-id="893dc-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="893dc-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="893dc-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="893dc-164">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="893dc-164">Managed Pipeline Mode Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="893dc-165">-MinTlsVersion</span></span>
<span data-ttu-id="893dc-166">Минимальная версия TLS, необходимая для SSL-запросов.</span><span class="sxs-lookup"><span data-stu-id="893dc-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="893dc-167">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="893dc-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="893dc-168">-Name</span><span class="sxs-lookup"><span data-stu-id="893dc-168">-Name</span></span>
<span data-ttu-id="893dc-169">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="893dc-169">WebApp Name</span></span>

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

### <span data-ttu-id="893dc-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="893dc-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="893dc-171">Версия Net Framework</span><span class="sxs-lookup"><span data-stu-id="893dc-171">Net Framework Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="893dc-172">-NumberOfWorkers</span></span>
<span data-ttu-id="893dc-173">Количество сотрудников, которые должны быть выделены</span><span class="sxs-lookup"><span data-stu-id="893dc-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="893dc-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="893dc-174">-PhpVersion</span></span>
<span data-ttu-id="893dc-175">Php Version</span><span class="sxs-lookup"><span data-stu-id="893dc-175">Php Version</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="893dc-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="893dc-177">Request Tracing Enabled Boolean</span><span class="sxs-lookup"><span data-stu-id="893dc-177">Request Tracing Enabled Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893dc-178">-ResourceGroupName</span></span>
<span data-ttu-id="893dc-179">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="893dc-179">Resource Group Name</span></span>

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

### <span data-ttu-id="893dc-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="893dc-180">-Slot</span></span>
<span data-ttu-id="893dc-181">Название слота WebApp</span><span class="sxs-lookup"><span data-stu-id="893dc-181">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="893dc-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="893dc-183">Использование 32-битной оси рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="893dc-183">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="893dc-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="893dc-184">-WebApp</span></span>
<span data-ttu-id="893dc-185">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="893dc-185">WebApp Object</span></span>

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

### <span data-ttu-id="893dc-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="893dc-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="893dc-187">Web Sockets Enabled Boolean</span><span class="sxs-lookup"><span data-stu-id="893dc-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="893dc-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893dc-188">CommonParameters</span></span>
<span data-ttu-id="893dc-189">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893dc-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893dc-190">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="893dc-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893dc-191">INPUTS</span><span class="sxs-lookup"><span data-stu-id="893dc-191">INPUTS</span></span>

### <span data-ttu-id="893dc-192">System.Int32</span><span class="sxs-lookup"><span data-stu-id="893dc-192">System.Int32</span></span>

### <span data-ttu-id="893dc-193">System.String</span><span class="sxs-lookup"><span data-stu-id="893dc-193">System.String</span></span>

### <span data-ttu-id="893dc-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="893dc-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="893dc-195">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="893dc-195">OUTPUTS</span></span>

### <span data-ttu-id="893dc-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="893dc-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="893dc-197">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="893dc-197">NOTES</span></span>

## <span data-ttu-id="893dc-198">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="893dc-198">RELATED LINKS</span></span>

[<span data-ttu-id="893dc-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="893dc-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="893dc-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="893dc-202">Restart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="893dc-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="893dc-204">Stop-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="893dc-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="893dc-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="893dc-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
