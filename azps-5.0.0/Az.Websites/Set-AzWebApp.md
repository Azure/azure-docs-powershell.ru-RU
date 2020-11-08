---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 2028132e427bdba3fd49c20b9e7944eff90a9aa5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249137"
---
# <span data-ttu-id="7c62f-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-101">Set-AzWebApp</span></span>

## <span data-ttu-id="7c62f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c62f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c62f-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7c62f-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="7c62f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c62f-104">SYNTAX</span></span>

### <span data-ttu-id="7c62f-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="7c62f-105">S1</span></span>
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

### <span data-ttu-id="7c62f-106">S2</span><span class="sxs-lookup"><span data-stu-id="7c62f-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c62f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c62f-107">DESCRIPTION</span></span>
<span data-ttu-id="7c62f-108">Командлет **Set-AzWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="7c62f-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="7c62f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c62f-109">EXAMPLES</span></span>

### <span data-ttu-id="7c62f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7c62f-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="7c62f-111">Эта команда изменяет план appservice, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="7c62f-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="7c62f-112">Воспользуйтесь ссылкой, чтобы узнать больше о том, как изменить план appservice и ограничения, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="7c62f-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="7c62f-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="7c62f-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="7c62f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7c62f-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="7c62f-115">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="7c62f-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="7c62f-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7c62f-116">Example 3</span></span>

<span data-ttu-id="7c62f-117">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="7c62f-117">Modifies an Azure Web App.</span></span> <span data-ttu-id="7c62f-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="7c62f-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebApp -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS'
```

### <span data-ttu-id="7c62f-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="7c62f-119">Example 4</span></span>

<span data-ttu-id="7c62f-120">В следующем примере создается строка подключения с именем myConnectionString для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c62f-120">The following example creates a connection string named myConnectionString for Web App ContosoWebApp.</span></span> <span data-ttu-id="7c62f-121">Это заменяет все существующие строки подключения для веб-приложения ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="7c62f-121">This replaces all existing connection strings for Web App ContosoWebApp.</span></span>

```powershell
$hashtable =  @{myConnectionString = @{Type='MySql';Value='MySql Connection string'}}
Set-AzWebApp -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -ConnectionString $hashtable
```

## <span data-ttu-id="7c62f-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c62f-122">PARAMETERS</span></span>

### <span data-ttu-id="7c62f-123">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="7c62f-123">-AlwaysOn</span></span>
<span data-ttu-id="7c62f-124">Убедитесь, что веб-приложение загружено все время, а не выгружено после его бездействия.</span><span class="sxs-lookup"><span data-stu-id="7c62f-124">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="7c62f-125">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7c62f-125">-AppServicePlan</span></span>
<span data-ttu-id="7c62f-126">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="7c62f-126">App Service Plan Name</span></span>

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

### <span data-ttu-id="7c62f-127">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="7c62f-127">-AppSettings</span></span>
<span data-ttu-id="7c62f-128">Хэш-таблица параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="7c62f-128">App Settings HashTable.</span></span> <span data-ttu-id="7c62f-129">Существующие параметры приложения будут заменены, а не все параметры, которые не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="7c62f-129">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="7c62f-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c62f-130">-AsJob</span></span>
<span data-ttu-id="7c62f-131">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="7c62f-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c62f-132">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7c62f-132">-AssignIdentity</span></span>
<span data-ttu-id="7c62f-133">Включение и отключение MSI для существующих Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="7c62f-133">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="7c62f-134">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="7c62f-134">-AutoSwapSlotName</span></span>
<span data-ttu-id="7c62f-135">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="7c62f-135">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="7c62f-136">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="7c62f-136">-AzureStoragePath</span></span>
<span data-ttu-id="7c62f-137">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="7c62f-137">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="7c62f-138">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="7c62f-138">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="7c62f-139">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="7c62f-139">-ConnectionStrings</span></span>
<span data-ttu-id="7c62f-140">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="7c62f-140">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="7c62f-141">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="7c62f-141">-ContainerImageName</span></span>
<span data-ttu-id="7c62f-142">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="7c62f-142">Container Image Name</span></span>

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

### <span data-ttu-id="7c62f-143">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="7c62f-143">-ContainerRegistryPassword</span></span>
<span data-ttu-id="7c62f-144">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="7c62f-144">Private Container Registry Password</span></span>

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

### <span data-ttu-id="7c62f-145">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="7c62f-145">-ContainerRegistryUrl</span></span>
<span data-ttu-id="7c62f-146">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="7c62f-146">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="7c62f-147">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="7c62f-147">-ContainerRegistryUser</span></span>
<span data-ttu-id="7c62f-148">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="7c62f-148">Private Container Registry Username</span></span>

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

### <span data-ttu-id="7c62f-149">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="7c62f-149">-DefaultDocuments</span></span>
<span data-ttu-id="7c62f-150">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c62f-150">Default Documents String Array</span></span>

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

### <span data-ttu-id="7c62f-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c62f-151">-DefaultProfile</span></span>
<span data-ttu-id="7c62f-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c62f-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c62f-153">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7c62f-153">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="7c62f-154">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="7c62f-154">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="7c62f-155">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="7c62f-155">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="7c62f-156">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="7c62f-156">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="7c62f-157">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="7c62f-157">-FtpsState</span></span>
<span data-ttu-id="7c62f-158">Установка значения состояния FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="7c62f-158">Set the Ftps state value for an app.</span></span> <span data-ttu-id="7c62f-159">Разрешенные значения [AllAllowed | Отключено | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="7c62f-159">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="7c62f-160">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="7c62f-160">-HandlerMappings</span></span>
<span data-ttu-id="7c62f-161">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="7c62f-161">Handler Mappings IList</span></span>

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

### <span data-ttu-id="7c62f-162">-HostName</span><span class="sxs-lookup"><span data-stu-id="7c62f-162">-HostNames</span></span>
<span data-ttu-id="7c62f-163">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-163">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="7c62f-164">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="7c62f-164">-HttpLoggingEnabled</span></span>
<span data-ttu-id="7c62f-165">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="7c62f-165">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="7c62f-166">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="7c62f-166">-HttpsOnly</span></span>
<span data-ttu-id="7c62f-167">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="7c62f-167">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="7c62f-168">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="7c62f-168">-ManagedPipelineMode</span></span>
<span data-ttu-id="7c62f-169">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="7c62f-169">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="7c62f-170">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="7c62f-170">-MinTlsVersion</span></span>
<span data-ttu-id="7c62f-171">Минимальная версия TLS, необходимая для запросов SSL.</span><span class="sxs-lookup"><span data-stu-id="7c62f-171">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="7c62f-172">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="7c62f-172">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="7c62f-173">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c62f-173">-Name</span></span>
<span data-ttu-id="7c62f-174">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-174">WebApp Name</span></span>

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

### <span data-ttu-id="7c62f-175">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="7c62f-175">-NetFrameworkVersion</span></span>
<span data-ttu-id="7c62f-176">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="7c62f-176">Net Framework Version</span></span>

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

### <span data-ttu-id="7c62f-177">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="7c62f-177">-NumberOfWorkers</span></span>
<span data-ttu-id="7c62f-178">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="7c62f-178">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="7c62f-179">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="7c62f-179">-PhpVersion</span></span>
<span data-ttu-id="7c62f-180">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="7c62f-180">Php Version</span></span>

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

### <span data-ttu-id="7c62f-181">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="7c62f-181">-RequestTracingEnabled</span></span>
<span data-ttu-id="7c62f-182">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="7c62f-182">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="7c62f-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c62f-183">-ResourceGroupName</span></span>
<span data-ttu-id="7c62f-184">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c62f-184">Resource Group Name</span></span>

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

### <span data-ttu-id="7c62f-185">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="7c62f-185">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="7c62f-186">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="7c62f-186">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="7c62f-187">-WebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-187">-WebApp</span></span>
<span data-ttu-id="7c62f-188">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-188">WebApp Object</span></span>

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

### <span data-ttu-id="7c62f-189">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="7c62f-189">-WebSocketsEnabled</span></span>
<span data-ttu-id="7c62f-190">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="7c62f-190">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="7c62f-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c62f-191">CommonParameters</span></span>
<span data-ttu-id="7c62f-192">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c62f-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c62f-193">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c62f-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c62f-194">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c62f-194">INPUTS</span></span>

### <span data-ttu-id="7c62f-195">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7c62f-195">System.Int32</span></span>

### <span data-ttu-id="7c62f-196">System. String</span><span class="sxs-lookup"><span data-stu-id="7c62f-196">System.String</span></span>

### <span data-ttu-id="7c62f-197">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="7c62f-197">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c62f-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c62f-198">OUTPUTS</span></span>

### <span data-ttu-id="7c62f-199">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="7c62f-199">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="7c62f-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c62f-200">NOTES</span></span>
<span data-ttu-id="7c62f-201">Ниже приведен командлет, который поможет вам обновить веб-приложение Azure до **DOTNETCORE**</span><span class="sxs-lookup"><span data-stu-id="7c62f-201">Below provided cmdlet will help you to update Azure Web App to **DOTNETCORE**</span></span>

<span data-ttu-id="7c62f-202">$PropertiesObject = @ {"CURRENT_STACK" = "dotnetcore"} New-AzResource-PropertyObject $PropertiesObject-ResourceGroupName "Default-Web-WestUS"-ResourceType Microsoft. Web/Sites/config-ResourceName "ContosoWebApp/Metadata"-ApiVersion 2018-02-01-Force</span><span class="sxs-lookup"><span data-stu-id="7c62f-202">$PropertiesObject = @{ "CURRENT_STACK" =  "dotnetcore" } New-AzResource -PropertyObject $PropertiesObject -ResourceGroupName "Default-Web-WestUS" -ResourceType Microsoft.Web/sites/config -ResourceName "ContosoWebApp/metadata" -ApiVersion 2018-02-01 -Force</span></span>

<span data-ttu-id="7c62f-203">Замените значения параметров Default-Web-WestUS именем группы ресурсов webapp и ContosoWebApp именем webapp.</span><span class="sxs-lookup"><span data-stu-id="7c62f-203">Replace the values of Default-Web-WestUS with your resource group name of the webapp and ContosoWebApp with the webapp name.</span></span>
 
## <span data-ttu-id="7c62f-204">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c62f-204">RELATED LINKS</span></span>

[<span data-ttu-id="7c62f-205">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-205">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="7c62f-206">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-206">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="7c62f-207">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-207">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="7c62f-208">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-208">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="7c62f-209">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-209">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="7c62f-210">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="7c62f-210">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

[<span data-ttu-id="7c62f-211">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="7c62f-211">New-AzResource</span></span>](./New-AzResource.md)
