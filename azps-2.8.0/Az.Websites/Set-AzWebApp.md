---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 4e4e842605b883b97d408d36929bedc5fef21e4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907258"
---
# <span data-ttu-id="62670-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-101">Set-AzWebApp</span></span>

## <span data-ttu-id="62670-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62670-102">SYNOPSIS</span></span>
<span data-ttu-id="62670-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="62670-103">Modifies an Azure Web App.</span></span>

## <span data-ttu-id="62670-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62670-104">SYNTAX</span></span>

### <span data-ttu-id="62670-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="62670-105">S1</span></span>
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
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62670-106">S2</span><span class="sxs-lookup"><span data-stu-id="62670-106">S2</span></span>
```
Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]
 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62670-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62670-107">DESCRIPTION</span></span>
<span data-ttu-id="62670-108">Командлет **Set-AzWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="62670-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="62670-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62670-109">EXAMPLES</span></span>

### <span data-ttu-id="62670-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62670-110">Example 1</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="62670-111">Эта команда изменяет план appservice, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="62670-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="62670-112">Воспользуйтесь ссылкой, чтобы узнать больше о том, как изменить план appservice и ограничения, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="62670-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="62670-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="62670-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="62670-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="62670-114">Example 2</span></span>
```
PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="62670-115">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="62670-115">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="62670-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62670-116">PARAMETERS</span></span>

### <span data-ttu-id="62670-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="62670-117">-AppServicePlan</span></span>
<span data-ttu-id="62670-118">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="62670-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="62670-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="62670-119">-AppSettings</span></span>
<span data-ttu-id="62670-120">Хэш-таблица параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="62670-120">App Settings HashTable.</span></span> <span data-ttu-id="62670-121">Существующие параметры приложения будут заменены, а не все параметры, которые не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="62670-121">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="62670-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62670-122">-AsJob</span></span>
<span data-ttu-id="62670-123">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="62670-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62670-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="62670-124">-AssignIdentity</span></span>
<span data-ttu-id="62670-125">Включение и отключение MSI для существующих Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="62670-125">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="62670-126">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="62670-126">-AutoSwapSlotName</span></span>
<span data-ttu-id="62670-127">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="62670-127">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="62670-128">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="62670-128">-AzureStoragePath</span></span>
<span data-ttu-id="62670-129">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="62670-129">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="62670-130">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="62670-130">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="62670-131">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="62670-131">-ConnectionStrings</span></span>
<span data-ttu-id="62670-132">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="62670-132">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="62670-133">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="62670-133">-ContainerImageName</span></span>
<span data-ttu-id="62670-134">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="62670-134">Container Image Name</span></span>

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

### <span data-ttu-id="62670-135">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="62670-135">-ContainerRegistryPassword</span></span>
<span data-ttu-id="62670-136">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="62670-136">Private Container Registry Password</span></span>

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

### <span data-ttu-id="62670-137">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="62670-137">-ContainerRegistryUrl</span></span>
<span data-ttu-id="62670-138">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="62670-138">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="62670-139">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="62670-139">-ContainerRegistryUser</span></span>
<span data-ttu-id="62670-140">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="62670-140">Private Container Registry Username</span></span>

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

### <span data-ttu-id="62670-141">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="62670-141">-DefaultDocuments</span></span>
<span data-ttu-id="62670-142">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="62670-142">Default Documents String Array</span></span>

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

### <span data-ttu-id="62670-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62670-143">-DefaultProfile</span></span>
<span data-ttu-id="62670-144">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62670-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62670-145">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="62670-145">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="62670-146">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="62670-146">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="62670-147">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="62670-147">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="62670-148">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="62670-148">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="62670-149">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="62670-149">-HandlerMappings</span></span>
<span data-ttu-id="62670-150">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="62670-150">Handler Mappings IList</span></span>

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

### <span data-ttu-id="62670-151">-HostName</span><span class="sxs-lookup"><span data-stu-id="62670-151">-HostNames</span></span>
<span data-ttu-id="62670-152">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="62670-152">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="62670-153">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="62670-153">-HttpLoggingEnabled</span></span>
<span data-ttu-id="62670-154">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="62670-154">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="62670-155">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="62670-155">-HttpsOnly</span></span>
<span data-ttu-id="62670-156">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="62670-156">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="62670-157">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="62670-157">-ManagedPipelineMode</span></span>
<span data-ttu-id="62670-158">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="62670-158">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="62670-159">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="62670-159">-Name</span></span>
<span data-ttu-id="62670-160">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="62670-160">WebApp Name</span></span>

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

### <span data-ttu-id="62670-161">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="62670-161">-NetFrameworkVersion</span></span>
<span data-ttu-id="62670-162">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="62670-162">Net Framework Version</span></span>

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

### <span data-ttu-id="62670-163">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="62670-163">-NumberOfWorkers</span></span>
<span data-ttu-id="62670-164">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="62670-164">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="62670-165">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="62670-165">-PhpVersion</span></span>
<span data-ttu-id="62670-166">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="62670-166">Php Version</span></span>

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

### <span data-ttu-id="62670-167">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="62670-167">-RequestTracingEnabled</span></span>
<span data-ttu-id="62670-168">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="62670-168">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="62670-169">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62670-169">-ResourceGroupName</span></span>
<span data-ttu-id="62670-170">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="62670-170">Resource Group Name</span></span>

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

### <span data-ttu-id="62670-171">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="62670-171">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="62670-172">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="62670-172">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="62670-173">-WebApp</span><span class="sxs-lookup"><span data-stu-id="62670-173">-WebApp</span></span>
<span data-ttu-id="62670-174">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="62670-174">WebApp Object</span></span>

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

### <span data-ttu-id="62670-175">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="62670-175">-WebSocketsEnabled</span></span>
<span data-ttu-id="62670-176">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="62670-176">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="62670-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62670-177">CommonParameters</span></span>
<span data-ttu-id="62670-178">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62670-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62670-179">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62670-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62670-180">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62670-180">INPUTS</span></span>

### <span data-ttu-id="62670-181">System. Int32</span><span class="sxs-lookup"><span data-stu-id="62670-181">System.Int32</span></span>

### <span data-ttu-id="62670-182">System. String</span><span class="sxs-lookup"><span data-stu-id="62670-182">System.String</span></span>

### <span data-ttu-id="62670-183">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="62670-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="62670-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62670-184">OUTPUTS</span></span>

### <span data-ttu-id="62670-185">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="62670-185">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="62670-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="62670-186">NOTES</span></span>

## <span data-ttu-id="62670-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62670-187">RELATED LINKS</span></span>

[<span data-ttu-id="62670-188">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-188">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="62670-189">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-189">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="62670-190">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-190">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="62670-191">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-191">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="62670-192">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-192">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="62670-193">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="62670-193">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)
