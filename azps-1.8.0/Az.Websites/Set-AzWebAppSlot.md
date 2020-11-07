---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: d0bca8fadf9179990eb5901e67ee07a3532a39cb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728293"
---
# <span data-ttu-id="5c105-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="5c105-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c105-102">SYNOPSIS</span></span>
<span data-ttu-id="5c105-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5c105-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="5c105-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c105-104">SYNTAX</span></span>

### <span data-ttu-id="5c105-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="5c105-105">S1</span></span>
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
 [-AzureStoragePath <WebAppAzureStoragePath[]>] [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c105-106">S2</span><span class="sxs-lookup"><span data-stu-id="5c105-106">S2</span></span>
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

## <span data-ttu-id="5c105-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c105-107">DESCRIPTION</span></span>
<span data-ttu-id="5c105-108">Командлет **Set-AzWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="5c105-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="5c105-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c105-109">EXAMPLES</span></span>

### <span data-ttu-id="5c105-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c105-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -AppServicePlan "ContosoPlan"
```

<span data-ttu-id="5c105-111">Эта команда изменяет план appservice, связанный с Slot001, на webapp ContosoWebApp, связанном с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="5c105-111">This command changes the appservice plan associated with the Slot001, on the Webapp ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="5c105-112">Воспользуйтесь ссылкой для learm более подробного изменения плана appservice и ограничений, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="5c105-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>
<span data-ttu-id="5c105-113"> https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span><span class="sxs-lookup"><span data-stu-id="5c105-113">https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan</span></span>

### <span data-ttu-id="5c105-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c105-114">Example 2</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="5c105-115">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="5c105-115">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="5c105-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c105-116">PARAMETERS</span></span>

### <span data-ttu-id="5c105-117">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5c105-117">-AppServicePlan</span></span>
<span data-ttu-id="5c105-118">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="5c105-118">App Service Plan Name</span></span>

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

### <span data-ttu-id="5c105-119">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="5c105-119">-AppSettings</span></span>
<span data-ttu-id="5c105-120">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="5c105-120">App Settings HashTable</span></span>

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

### <span data-ttu-id="5c105-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c105-121">-AsJob</span></span>
<span data-ttu-id="5c105-122">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c105-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c105-123">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="5c105-123">-AssignIdentity</span></span>
<span data-ttu-id="5c105-124">Включение и отключение MSI для существующего слота [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="5c105-124">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="5c105-125">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="5c105-125">-AutoSwapSlotName</span></span>
<span data-ttu-id="5c105-126">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="5c105-126">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="5c105-127">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="5c105-127">-AzureStoragePath</span></span>
<span data-ttu-id="5c105-128">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="5c105-128">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="5c105-129">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="5c105-129">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>

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

### <span data-ttu-id="5c105-130">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="5c105-130">-ConnectionStrings</span></span>
<span data-ttu-id="5c105-131">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="5c105-131">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="5c105-132">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="5c105-132">-ContainerImageName</span></span>
<span data-ttu-id="5c105-133">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="5c105-133">Container Image Name</span></span>

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

### <span data-ttu-id="5c105-134">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="5c105-134">-ContainerRegistryPassword</span></span>
<span data-ttu-id="5c105-135">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="5c105-135">Private Container Registry Password</span></span>

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

### <span data-ttu-id="5c105-136">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="5c105-136">-ContainerRegistryUrl</span></span>
<span data-ttu-id="5c105-137">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="5c105-137">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="5c105-138">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="5c105-138">-ContainerRegistryUser</span></span>
<span data-ttu-id="5c105-139">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="5c105-139">Private Container Registry Username</span></span>

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

### <span data-ttu-id="5c105-140">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="5c105-140">-DefaultDocuments</span></span>
<span data-ttu-id="5c105-141">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5c105-141">Default Documents String Array</span></span>

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

### <span data-ttu-id="5c105-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c105-142">-DefaultProfile</span></span>
<span data-ttu-id="5c105-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c105-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c105-144">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5c105-144">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="5c105-145">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="5c105-145">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="5c105-146">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="5c105-146">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="5c105-147">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="5c105-147">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="5c105-148">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="5c105-148">-HandlerMappings</span></span>
<span data-ttu-id="5c105-149">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="5c105-149">Handler Mappings IList</span></span>

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

### <span data-ttu-id="5c105-150">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="5c105-150">-HttpLoggingEnabled</span></span>
<span data-ttu-id="5c105-151">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="5c105-151">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="5c105-152">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="5c105-152">-HttpsOnly</span></span>
<span data-ttu-id="5c105-153">Включение и отключение перенаправления всего трафика на HTTPS на существующую ячейку</span><span class="sxs-lookup"><span data-stu-id="5c105-153">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="5c105-154">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="5c105-154">-ManagedPipelineMode</span></span>
<span data-ttu-id="5c105-155">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="5c105-155">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="5c105-156">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c105-156">-Name</span></span>
<span data-ttu-id="5c105-157">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="5c105-157">WebApp Name</span></span>

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

### <span data-ttu-id="5c105-158">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="5c105-158">-NetFrameworkVersion</span></span>
<span data-ttu-id="5c105-159">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="5c105-159">Net Framework Version</span></span>

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

### <span data-ttu-id="5c105-160">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="5c105-160">-NumberOfWorkers</span></span>
<span data-ttu-id="5c105-161">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="5c105-161">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="5c105-162">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="5c105-162">-PhpVersion</span></span>
<span data-ttu-id="5c105-163">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="5c105-163">Php Version</span></span>

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

### <span data-ttu-id="5c105-164">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="5c105-164">-RequestTracingEnabled</span></span>
<span data-ttu-id="5c105-165">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="5c105-165">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="5c105-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c105-166">-ResourceGroupName</span></span>
<span data-ttu-id="5c105-167">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5c105-167">Resource Group Name</span></span>

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

### <span data-ttu-id="5c105-168">-Slot</span><span class="sxs-lookup"><span data-stu-id="5c105-168">-Slot</span></span>
<span data-ttu-id="5c105-169">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="5c105-169">WebApp Slot Name</span></span>

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

### <span data-ttu-id="5c105-170">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="5c105-170">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="5c105-171">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="5c105-171">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="5c105-172">-WebApp</span><span class="sxs-lookup"><span data-stu-id="5c105-172">-WebApp</span></span>
<span data-ttu-id="5c105-173">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="5c105-173">WebApp Object</span></span>

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

### <span data-ttu-id="5c105-174">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="5c105-174">-WebSocketsEnabled</span></span>
<span data-ttu-id="5c105-175">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="5c105-175">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="5c105-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c105-176">CommonParameters</span></span>
<span data-ttu-id="5c105-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c105-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c105-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c105-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c105-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c105-179">INPUTS</span></span>

### <span data-ttu-id="5c105-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="5c105-180">System.Int32</span></span>

### <span data-ttu-id="5c105-181">System. String</span><span class="sxs-lookup"><span data-stu-id="5c105-181">System.String</span></span>

### <span data-ttu-id="5c105-182">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="5c105-182">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5c105-183">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c105-183">OUTPUTS</span></span>

### <span data-ttu-id="5c105-184">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="5c105-184">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="5c105-185">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c105-185">NOTES</span></span>

## <span data-ttu-id="5c105-186">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c105-186">RELATED LINKS</span></span>

[<span data-ttu-id="5c105-187">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-187">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="5c105-188">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-188">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="5c105-189">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-189">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="5c105-190">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-190">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="5c105-191">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-191">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="5c105-192">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="5c105-192">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="5c105-193">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="5c105-193">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
