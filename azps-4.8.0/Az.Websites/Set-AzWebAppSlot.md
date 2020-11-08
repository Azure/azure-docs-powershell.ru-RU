---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: 5f465f97ab5f5bec817619709359179acff38043
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244656"
---
# <span data-ttu-id="41a70-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="41a70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41a70-102">SYNOPSIS</span></span>
<span data-ttu-id="41a70-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="41a70-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="41a70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41a70-104">SYNTAX</span></span>

### <span data-ttu-id="41a70-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="41a70-105">S1</span></span>
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

### <span data-ttu-id="41a70-106">S2</span><span class="sxs-lookup"><span data-stu-id="41a70-106">S2</span></span>
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

## <span data-ttu-id="41a70-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a70-107">DESCRIPTION</span></span>
<span data-ttu-id="41a70-108">Командлет **Set-AzWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="41a70-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="41a70-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41a70-109">EXAMPLES</span></span>

### <span data-ttu-id="41a70-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="41a70-110">Example 1</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="41a70-111">Эта команда изменяет план appservice, связанный с Slot001, на webapp ContosoWebApp, связанном с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="41a70-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="41a70-112">Воспользуйтесь ссылкой, чтобы узнать больше о том, как изменить план appservice и ограничения, связанные с ним.</span><span class="sxs-lookup"><span data-stu-id="41a70-112">Use the link to learn more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="41a70-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="41a70-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="41a70-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="41a70-114">Example 2</span></span>
```powershell
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="41a70-115">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="41a70-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

### <span data-ttu-id="41a70-116">Пример 3</span><span class="sxs-lookup"><span data-stu-id="41a70-116">Example 3</span></span>

<span data-ttu-id="41a70-117">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="41a70-117">Modifies an Azure Web App slot.</span></span> <span data-ttu-id="41a70-118">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="41a70-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzWebAppSlot -AppSettings <Hashtable> -Name 'ContosoWebApp' -ResourceGroupName 'Default-Web-WestUS' -Slot 'Slot001'
```

## <span data-ttu-id="41a70-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41a70-119">PARAMETERS</span></span>

### <span data-ttu-id="41a70-120">-AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="41a70-120">-AlwaysOn</span></span>
<span data-ttu-id="41a70-121">Убедитесь, что веб-приложение загружено все время, а не выгружено после его бездействия.</span><span class="sxs-lookup"><span data-stu-id="41a70-121">Ensure web app gets loaded all the time, rather unloaded after been idle.</span></span>

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

### <span data-ttu-id="41a70-122">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="41a70-122">-AppServicePlan</span></span>
<span data-ttu-id="41a70-123">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="41a70-123">App Service Plan Name</span></span>

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

### <span data-ttu-id="41a70-124">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="41a70-124">-AppSettings</span></span>
<span data-ttu-id="41a70-125">Хэш-таблица параметров приложения.</span><span class="sxs-lookup"><span data-stu-id="41a70-125">App Settings HashTable.</span></span> <span data-ttu-id="41a70-126">Существующие параметры приложения будут заменены, а не все параметры, которые не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="41a70-126">Existing App Settings will be replaced, removing any settings that are not provided.</span></span>

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

### <span data-ttu-id="41a70-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41a70-127">-AsJob</span></span>
<span data-ttu-id="41a70-128">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="41a70-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41a70-129">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="41a70-129">-AssignIdentity</span></span>
<span data-ttu-id="41a70-130">Включение и отключение MSI для существующего слота [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="41a70-130">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="41a70-131">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="41a70-131">-AutoSwapSlotName</span></span>
<span data-ttu-id="41a70-132">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="41a70-132">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="41a70-133">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="41a70-133">-AzureStoragePath</span></span>
<span data-ttu-id="41a70-134">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="41a70-134">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="41a70-135">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="41a70-135">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="41a70-136">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="41a70-136">-ConnectionStrings</span></span>
<span data-ttu-id="41a70-137">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="41a70-137">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="41a70-138">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="41a70-138">-ContainerImageName</span></span>
<span data-ttu-id="41a70-139">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="41a70-139">Container Image Name</span></span>

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

### <span data-ttu-id="41a70-140">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="41a70-140">-ContainerRegistryPassword</span></span>
<span data-ttu-id="41a70-141">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="41a70-141">Private Container Registry Password</span></span>

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

### <span data-ttu-id="41a70-142">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="41a70-142">-ContainerRegistryUrl</span></span>
<span data-ttu-id="41a70-143">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="41a70-143">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="41a70-144">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="41a70-144">-ContainerRegistryUser</span></span>
<span data-ttu-id="41a70-145">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="41a70-145">Private Container Registry Username</span></span>

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

### <span data-ttu-id="41a70-146">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="41a70-146">-DefaultDocuments</span></span>
<span data-ttu-id="41a70-147">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="41a70-147">Default Documents String Array</span></span>

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

### <span data-ttu-id="41a70-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a70-148">-DefaultProfile</span></span>
<span data-ttu-id="41a70-149">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41a70-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41a70-150">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="41a70-150">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="41a70-151">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="41a70-151">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="41a70-152">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="41a70-152">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="41a70-153">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="41a70-153">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="41a70-154">-FtpsState</span><span class="sxs-lookup"><span data-stu-id="41a70-154">-FtpsState</span></span>
<span data-ttu-id="41a70-155">Установка значения состояния FTPS для приложения.</span><span class="sxs-lookup"><span data-stu-id="41a70-155">Set the Ftps state value for an app.</span></span> <span data-ttu-id="41a70-156">Разрешенные значения [AllAllowed | Отключено | FtpsOnly].</span><span class="sxs-lookup"><span data-stu-id="41a70-156">Allowed Values [AllAllowed | Disabled | FtpsOnly].</span></span>

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

### <span data-ttu-id="41a70-157">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="41a70-157">-HandlerMappings</span></span>
<span data-ttu-id="41a70-158">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="41a70-158">Handler Mappings IList</span></span>

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

### <span data-ttu-id="41a70-159">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="41a70-159">-HttpLoggingEnabled</span></span>
<span data-ttu-id="41a70-160">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="41a70-160">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="41a70-161">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="41a70-161">-HttpsOnly</span></span>
<span data-ttu-id="41a70-162">Включение и отключение перенаправления всего трафика на HTTPS на существующую ячейку</span><span class="sxs-lookup"><span data-stu-id="41a70-162">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="41a70-163">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="41a70-163">-ManagedPipelineMode</span></span>
<span data-ttu-id="41a70-164">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="41a70-164">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="41a70-165">-MinTlsVersion</span><span class="sxs-lookup"><span data-stu-id="41a70-165">-MinTlsVersion</span></span>
<span data-ttu-id="41a70-166">Минимальная версия TLS, необходимая для запросов SSL.</span><span class="sxs-lookup"><span data-stu-id="41a70-166">The minimum version of TLS required for SSL requests.</span></span> <span data-ttu-id="41a70-167">Разрешенные значения [1,0 | 1,1 | 1,2].</span><span class="sxs-lookup"><span data-stu-id="41a70-167">Allowed Values [1.0 | 1.1 | 1.2].</span></span>

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

### <span data-ttu-id="41a70-168">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="41a70-168">-Name</span></span>
<span data-ttu-id="41a70-169">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="41a70-169">WebApp Name</span></span>

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

### <span data-ttu-id="41a70-170">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="41a70-170">-NetFrameworkVersion</span></span>
<span data-ttu-id="41a70-171">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="41a70-171">Net Framework Version</span></span>

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

### <span data-ttu-id="41a70-172">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="41a70-172">-NumberOfWorkers</span></span>
<span data-ttu-id="41a70-173">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="41a70-173">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="41a70-174">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="41a70-174">-PhpVersion</span></span>
<span data-ttu-id="41a70-175">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="41a70-175">Php Version</span></span>

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

### <span data-ttu-id="41a70-176">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="41a70-176">-RequestTracingEnabled</span></span>
<span data-ttu-id="41a70-177">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="41a70-177">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="41a70-178">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41a70-178">-ResourceGroupName</span></span>
<span data-ttu-id="41a70-179">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="41a70-179">Resource Group Name</span></span>

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

### <span data-ttu-id="41a70-180">-Slot</span><span class="sxs-lookup"><span data-stu-id="41a70-180">-Slot</span></span>
<span data-ttu-id="41a70-181">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="41a70-181">WebApp Slot Name</span></span>

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

### <span data-ttu-id="41a70-182">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="41a70-182">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="41a70-183">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="41a70-183">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="41a70-184">-WebApp</span><span class="sxs-lookup"><span data-stu-id="41a70-184">-WebApp</span></span>
<span data-ttu-id="41a70-185">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="41a70-185">WebApp Object</span></span>

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

### <span data-ttu-id="41a70-186">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="41a70-186">-WebSocketsEnabled</span></span>
<span data-ttu-id="41a70-187">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="41a70-187">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="41a70-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a70-188">CommonParameters</span></span>
<span data-ttu-id="41a70-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41a70-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a70-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41a70-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a70-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41a70-191">INPUTS</span></span>

### <span data-ttu-id="41a70-192">System. Int32</span><span class="sxs-lookup"><span data-stu-id="41a70-192">System.Int32</span></span>

### <span data-ttu-id="41a70-193">System. String</span><span class="sxs-lookup"><span data-stu-id="41a70-193">System.String</span></span>

### <span data-ttu-id="41a70-194">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="41a70-194">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41a70-195">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41a70-195">OUTPUTS</span></span>

### <span data-ttu-id="41a70-196">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="41a70-196">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="41a70-197">Пуск</span><span class="sxs-lookup"><span data-stu-id="41a70-197">NOTES</span></span>

## <span data-ttu-id="41a70-198">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41a70-198">RELATED LINKS</span></span>

[<span data-ttu-id="41a70-199">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-199">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="41a70-200">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-200">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="41a70-201">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-201">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="41a70-202">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-202">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="41a70-203">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-203">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="41a70-204">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="41a70-204">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="41a70-205">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="41a70-205">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
