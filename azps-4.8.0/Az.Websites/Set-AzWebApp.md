---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 0120bd19d1c8930129796e47758bd9f91dccfd5d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079295"
---
# <span data-ttu-id="63d35-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-101">Set-AzWebApp</span></span>

## <span data-ttu-id="63d35-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63d35-102">SYNOPSIS</span></span>
<span data-ttu-id="63d35-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="63d35-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="63d35-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63d35-104">SYNTAX</span></span>

### <span data-ttu-id="63d35-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="63d35-105">S1</span></span>
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

### <span data-ttu-id="63d35-106">S2</span><span class="sxs-lookup"><span data-stu-id="63d35-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63d35-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d35-107">DESCRIPTION</span></span>
<span data-ttu-id="63d35-108">Командлет **Set-AzWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="63d35-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="63d35-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63d35-109">EXAMPLES</span></span>

### <span data-ttu-id="63d35-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63d35-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="63d35-111">Эта команда изменяет план appservice, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="63d35-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="63d35-112">Воспользуйтесь ссылкой, чтобы узнать больше о том, как изменить план appservice и ограничения, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="63d35-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="63d35-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="63d35-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="63d35-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="63d35-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="63d35-115">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="63d35-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="63d35-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="63d35-116">Example 3</span></span>

<span data-ttu-id="63d35-117">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="63d35-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="63d35-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="63d35-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

## <span data-ttu-id="63d35-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63d35-119">PARAMETERS</span></span>

### <span data-ttu-id="63d35-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="63d35-120">-AlwaysOn</span></span>
<span data-ttu-id="63d35-121">Убедитесь, что веб-приложение загружено все время, а не выгружено после его бездействия.</span><span class="sxs-lookup"><span data-stu-id="63d35-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="63d35-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="63d35-122">-AppServicePlan</span></span>
<span data-ttu-id="63d35-123">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="63d35-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="63d35-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="63d35-124">-AppSettings</span></span>
<span data-ttu-id="63d35-125">Хэш-таблица параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="63d35-125">App Settings HashTable.</span></span> <span data-ttu-id="63d35-126">Существующие параметры приложения будут заменены, а не все параметры, которые не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="63d35-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="63d35-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63d35-127">-AsJob</span></span>
<span data-ttu-id="63d35-128">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="63d35-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63d35-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="63d35-129">-AssignIdentity</span></span>
<span data-ttu-id="63d35-130">Включение и отключение MSI для существующих Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="63d35-130">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="63d35-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="63d35-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="63d35-132">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="63d35-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="63d35-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="63d35-133">-AzureStoragePath</span></span>
<span data-ttu-id="63d35-134">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="63d35-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="63d35-135">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="63d35-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="63d35-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="63d35-136">-ConnectionStrings</span></span>
<span data-ttu-id="63d35-137">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="63d35-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="63d35-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="63d35-138">-ContainerImageName</span></span>
<span data-ttu-id="63d35-139">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="63d35-139">Container Image Name</span></span>

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

### <span data-ttu-id="63d35-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="63d35-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="63d35-141">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="63d35-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="63d35-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="63d35-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="63d35-143">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="63d35-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="63d35-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="63d35-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="63d35-145">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="63d35-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="63d35-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="63d35-146">-DefaultDocuments</span></span>
<span data-ttu-id="63d35-147">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="63d35-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="63d35-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d35-148">-DefaultProfile</span></span>
<span data-ttu-id="63d35-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63d35-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63d35-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="63d35-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="63d35-151">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="63d35-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="63d35-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="63d35-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="63d35-153">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="63d35-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="63d35-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="63d35-154">-FtpsState</span></span>
<span data-ttu-id="63d35-155">Установка значения состояния FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="63d35-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="63d35-156">Разрешенные значения [AllAllowed | Отключено | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="63d35-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="63d35-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="63d35-157">-HandlerMappings</span></span>
<span data-ttu-id="63d35-158">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="63d35-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="63d35-159">-HostName</span><span class="sxs-lookup"><span data-stu-id="63d35-159">-HostNames</span></span>
<span data-ttu-id="63d35-160">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-160">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="63d35-161">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="63d35-161">-HttpLoggingEnabled</span></span>
<span data-ttu-id="63d35-162">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="63d35-162">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="63d35-163">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="63d35-163">-HttpsOnly</span></span>
<span data-ttu-id="63d35-164">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="63d35-164">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="63d35-165">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="63d35-165">-ManagedPipelineMode</span></span>
<span data-ttu-id="63d35-166">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="63d35-166">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="63d35-167">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="63d35-167">-MinTlsVersion</span></span>
<span data-ttu-id="63d35-168">Минимальная версия TLS, необходимая для запросов SSL.</span><span class="sxs-lookup"><span data-stu-id="63d35-168">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="63d35-169">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="63d35-169">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="63d35-170">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63d35-170">-Name</span></span>
<span data-ttu-id="63d35-171">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-171">WebApp Name</span></span>

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

### <span data-ttu-id="63d35-172">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="63d35-172">-NetFrameworkVersion</span></span>
<span data-ttu-id="63d35-173">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="63d35-173">Net Framework Version</span></span>

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

### <span data-ttu-id="63d35-174">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="63d35-174">-NumberOfWorkers</span></span>
<span data-ttu-id="63d35-175">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="63d35-175">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="63d35-176">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="63d35-176">-PhpVersion</span></span>
<span data-ttu-id="63d35-177">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="63d35-177">Php Version</span></span>

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

### <span data-ttu-id="63d35-178">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="63d35-178">-RequestTracingEnabled</span></span>
<span data-ttu-id="63d35-179">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="63d35-179">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="63d35-180">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d35-180">-ResourceGroupName</span></span>
<span data-ttu-id="63d35-181">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="63d35-181">Resource Group Name</span></span>

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

### <span data-ttu-id="63d35-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="63d35-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="63d35-183">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="63d35-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="63d35-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-184">-WebApp</span></span>
<span data-ttu-id="63d35-185">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-185">WebApp Object</span></span>

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

### <span data-ttu-id="63d35-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="63d35-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="63d35-187">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="63d35-187">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="63d35-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d35-188">CommonParameters</span></span>
<span data-ttu-id="63d35-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63d35-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d35-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63d35-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d35-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63d35-191">INPUTS</span></span>

### <span data-ttu-id="63d35-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="63d35-192">System.Int32</span></span>

### <span data-ttu-id="63d35-193">System. String</span><span class="sxs-lookup"><span data-stu-id="63d35-193">System.String</span></span>

### <span data-ttu-id="63d35-194">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="63d35-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63d35-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d35-195">OUTPUTS</span></span>

### <span data-ttu-id="63d35-196">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="63d35-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="63d35-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="63d35-197">NOTES</span></span>
<span data-ttu-id="63d35-198">Ниже приведен командлет, который поможет вам обновить веб-приложение Azure до **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="63d35-198">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="63d35-199">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="63d35-199">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="63d35-200">Замените значения параметров Default-Web-WestUS именем группы ресурсов webapp и ContosoWebApp именем webapp.</span><span class="sxs-lookup"><span data-stu-id="63d35-200">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="63d35-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63d35-201">RELATED LINKS</span></span>

[<span data-ttu-id="63d35-202">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-202">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="63d35-203">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-203">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="63d35-204">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-204">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="63d35-205">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-205">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="63d35-206">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-206">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="63d35-207">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="63d35-207">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="63d35-208">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="63d35-208">New-AzResource</span></span>](./New-AzResource.md)
