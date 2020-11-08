---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: ed1e073757eb2fc1b63a6ffd799c55ad1ffaf748
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072601"
---
# <span data-ttu-id="2b55f-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="2b55f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b55f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b55f-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2b55f-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="2b55f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b55f-104">SYNTAX</span></span>

### <span data-ttu-id="2b55f-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="2b55f-105">S1</span></span>
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

### <span data-ttu-id="2b55f-106">S2</span><span class="sxs-lookup"><span data-stu-id="2b55f-106">S2</span></span>
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

## <span data-ttu-id="2b55f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b55f-107">DESCRIPTION</span></span>
<span data-ttu-id="2b55f-108">Командлет **Set-AzWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="2b55f-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="2b55f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b55f-109">EXAMPLES</span></span>

### <span data-ttu-id="2b55f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2b55f-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="2b55f-111">Эта команда изменяет план appservice, связанный с Slot001, на webapp ContosoWebApp, связанном с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="2b55f-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="2b55f-112">Воспользуйтесь ссылкой, чтобы узнать больше о том, как изменить план appservice и ограничения, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="2b55f-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="2b55f-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="2b55f-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="2b55f-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2b55f-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="2b55f-115">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="2b55f-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="2b55f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b55f-116">PARAMETERS</span></span>

### <span data-ttu-id="2b55f-117">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="2b55f-117">-AlwaysOn</span></span>
<span data-ttu-id="2b55f-118">Убедитесь, что веб-приложение загружено все время, а не выгружено после его бездействия.</span><span class="sxs-lookup"><span data-stu-id="2b55f-118">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="2b55f-119">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b55f-119">-AppServicePlan</span></span>
<span data-ttu-id="2b55f-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="2b55f-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="2b55f-121">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="2b55f-121">-AppSettings</span></span>
<span data-ttu-id="2b55f-122">Хэш-таблица параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="2b55f-122">App Settings HashTable.</span></span> <span data-ttu-id="2b55f-123">Существующие параметры приложения будут заменены, а не все параметры, которые не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="2b55f-123">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="2b55f-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b55f-124">-AsJob</span></span>
<span data-ttu-id="2b55f-125">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2b55f-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2b55f-126">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2b55f-126">-AssignIdentity</span></span>
<span data-ttu-id="2b55f-127">Включение и отключение MSI для существующего слота [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="2b55f-127">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="2b55f-128">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="2b55f-128">-AutoSwapSlotName</span></span>
<span data-ttu-id="2b55f-129">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="2b55f-129">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="2b55f-130">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="2b55f-130">-AzureStoragePath</span></span>
<span data-ttu-id="2b55f-131">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="2b55f-131">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="2b55f-132">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="2b55f-132">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="2b55f-133">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="2b55f-133">-ConnectionStrings</span></span>
<span data-ttu-id="2b55f-134">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="2b55f-134">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="2b55f-135">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="2b55f-135">-ContainerImageName</span></span>
<span data-ttu-id="2b55f-136">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="2b55f-136">Container Image Name</span></span>

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

### <span data-ttu-id="2b55f-137">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="2b55f-137">-ContainerRegistryPassword</span></span>
<span data-ttu-id="2b55f-138">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="2b55f-138">Private Container Registry Password</span></span>

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

### <span data-ttu-id="2b55f-139">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="2b55f-139">-ContainerRegistryUrl</span></span>
<span data-ttu-id="2b55f-140">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="2b55f-140">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="2b55f-141">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="2b55f-141">-ContainerRegistryUser</span></span>
<span data-ttu-id="2b55f-142">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="2b55f-142">Private Container Registry Username</span></span>

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

### <span data-ttu-id="2b55f-143">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="2b55f-143">-DefaultDocuments</span></span>
<span data-ttu-id="2b55f-144">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="2b55f-144">Default Documents String Array</span></span>

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

### <span data-ttu-id="2b55f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b55f-145">-DefaultProfile</span></span>
<span data-ttu-id="2b55f-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b55f-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b55f-147">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b55f-147">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="2b55f-148">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="2b55f-148">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="2b55f-149">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="2b55f-149">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="2b55f-150">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="2b55f-150">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="2b55f-151">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="2b55f-151">-FtpsState</span></span>
<span data-ttu-id="2b55f-152">Установка значения состояния FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="2b55f-152">Set the Ftps state value for an app.</span></span> <span data-ttu-id="2b55f-153">Разрешенные значения [AllAllowed | Отключено | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="2b55f-153">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="2b55f-154">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="2b55f-154">-HandlerMappings</span></span>
<span data-ttu-id="2b55f-155">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="2b55f-155">Handler Mappings IList</span></span>

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

### <span data-ttu-id="2b55f-156">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b55f-156">-HttpLoggingEnabled</span></span>
<span data-ttu-id="2b55f-157">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="2b55f-157">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="2b55f-158">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="2b55f-158">-HttpsOnly</span></span>
<span data-ttu-id="2b55f-159">Включение и отключение перенаправления всего трафика на HTTPS на существующую ячейку</span><span class="sxs-lookup"><span data-stu-id="2b55f-159">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="2b55f-160">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="2b55f-160">-ManagedPipelineMode</span></span>
<span data-ttu-id="2b55f-161">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="2b55f-161">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="2b55f-162">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2b55f-162">-MinTlsVersion</span></span>
<span data-ttu-id="2b55f-163">Минимальная версия TLS, необходимая для запросов SSL.</span><span class="sxs-lookup"><span data-stu-id="2b55f-163">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="2b55f-164">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="2b55f-164">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="2b55f-165">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b55f-165">-Name</span></span>
<span data-ttu-id="2b55f-166">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="2b55f-166">WebApp Name</span></span>

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

### <span data-ttu-id="2b55f-167">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="2b55f-167">-NetFrameworkVersion</span></span>
<span data-ttu-id="2b55f-168">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2b55f-168">Net Framework Version</span></span>

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

### <span data-ttu-id="2b55f-169">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="2b55f-169">-NumberOfWorkers</span></span>
<span data-ttu-id="2b55f-170">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="2b55f-170">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="2b55f-171">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="2b55f-171">-PhpVersion</span></span>
<span data-ttu-id="2b55f-172">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="2b55f-172">Php Version</span></span>

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

### <span data-ttu-id="2b55f-173">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="2b55f-173">-RequestTracingEnabled</span></span>
<span data-ttu-id="2b55f-174">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="2b55f-174">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="2b55f-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b55f-175">-ResourceGroupName</span></span>
<span data-ttu-id="2b55f-176">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="2b55f-176">Resource Group Name</span></span>

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

### <span data-ttu-id="2b55f-177">-Slot</span><span class="sxs-lookup"><span data-stu-id="2b55f-177">-Slot</span></span>
<span data-ttu-id="2b55f-178">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="2b55f-178">WebApp Slot Name</span></span>

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

### <span data-ttu-id="2b55f-179">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="2b55f-179">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="2b55f-180">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="2b55f-180">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="2b55f-181">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2b55f-181">-WebApp</span></span>
<span data-ttu-id="2b55f-182">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="2b55f-182">WebApp Object</span></span>

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

### <span data-ttu-id="2b55f-183">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="2b55f-183">-WebSocketsEnabled</span></span>
<span data-ttu-id="2b55f-184">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="2b55f-184">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="2b55f-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b55f-185">CommonParameters</span></span>
<span data-ttu-id="2b55f-186">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b55f-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b55f-187">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b55f-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b55f-188">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b55f-188">INPUTS</span></span>

### <span data-ttu-id="2b55f-189">System. Int32</span><span class="sxs-lookup"><span data-stu-id="2b55f-189">System.Int32</span></span>

### <span data-ttu-id="2b55f-190">System. String</span><span class="sxs-lookup"><span data-stu-id="2b55f-190">System.String</span></span>

### <span data-ttu-id="2b55f-191">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="2b55f-191">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2b55f-192">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b55f-192">OUTPUTS</span></span>

### <span data-ttu-id="2b55f-193">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="2b55f-193">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2b55f-194">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b55f-194">NOTES</span></span>

## <span data-ttu-id="2b55f-195">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b55f-195">RELATED LINKS</span></span>

[<span data-ttu-id="2b55f-196">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-196">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-197">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-197">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-198">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-198">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-199">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-199">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-200">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-200">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-201">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="2b55f-201">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="2b55f-202">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="2b55f-202">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
