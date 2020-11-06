---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4ba94f0f7633feefc32c0b32d820e8bee9b6d1b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565273"
---
# <span data-ttu-id="98378-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="98378-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98378-102">SYNOPSIS</span></span>
<span data-ttu-id="98378-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="98378-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98378-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98378-104">SYNTAX</span></span>

### <span data-ttu-id="98378-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="98378-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ContainerImageName <String>]
 [-ContainerRegistryUrl <String>] [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-AsJob] [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-Slot] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="98378-106">S2</span><span class="sxs-lookup"><span data-stu-id="98378-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98378-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98378-107">DESCRIPTION</span></span>
<span data-ttu-id="98378-108">Командлет **Set-AzureRmWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="98378-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="98378-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98378-109">EXAMPLES</span></span>

### <span data-ttu-id="98378-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="98378-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="98378-111">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="98378-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="98378-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98378-112">PARAMETERS</span></span>

### <span data-ttu-id="98378-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="98378-113">-AppServicePlan</span></span>
<span data-ttu-id="98378-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="98378-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="98378-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="98378-115">-AppSettings</span></span>
<span data-ttu-id="98378-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="98378-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="98378-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98378-117">-AsJob</span></span>
<span data-ttu-id="98378-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="98378-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="98378-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="98378-119">-AssignIdentity</span></span>
<span data-ttu-id="98378-120">Включение и отключение MSI для существующего слота [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="98378-120">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="98378-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="98378-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="98378-122">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="98378-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="98378-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="98378-123">-ConnectionStrings</span></span>
<span data-ttu-id="98378-124">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="98378-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="98378-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="98378-125">-ContainerImageName</span></span>
<span data-ttu-id="98378-126">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="98378-126">Container Image Name</span></span>

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

### <span data-ttu-id="98378-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="98378-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="98378-128">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="98378-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="98378-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="98378-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="98378-130">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="98378-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="98378-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="98378-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="98378-132">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="98378-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="98378-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="98378-133">-DefaultDocuments</span></span>
<span data-ttu-id="98378-134">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="98378-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="98378-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98378-135">-DefaultProfile</span></span>
<span data-ttu-id="98378-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98378-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98378-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="98378-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="98378-138">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="98378-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="98378-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="98378-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="98378-140">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="98378-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="98378-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="98378-141">-HandlerMappings</span></span>
<span data-ttu-id="98378-142">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="98378-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="98378-143">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="98378-143">-HttpLoggingEnabled</span></span>
<span data-ttu-id="98378-144">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="98378-144">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="98378-145">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="98378-145">-HttpsOnly</span></span>
<span data-ttu-id="98378-146">Включение и отключение перенаправления всего трафика на HTTPS на существующую ячейку</span><span class="sxs-lookup"><span data-stu-id="98378-146">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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

### <span data-ttu-id="98378-147">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="98378-147">-ManagedPipelineMode</span></span>
<span data-ttu-id="98378-148">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="98378-148">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="98378-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98378-149">-Name</span></span>
<span data-ttu-id="98378-150">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="98378-150">WebApp Name</span></span>

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

### <span data-ttu-id="98378-151">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="98378-151">-NetFrameworkVersion</span></span>
<span data-ttu-id="98378-152">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="98378-152">Net Framework Version</span></span>

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

### <span data-ttu-id="98378-153">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="98378-153">-NumberOfWorkers</span></span>
<span data-ttu-id="98378-154">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="98378-154">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="98378-155">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="98378-155">-PhpVersion</span></span>
<span data-ttu-id="98378-156">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="98378-156">Php Version</span></span>

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

### <span data-ttu-id="98378-157">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="98378-157">-RequestTracingEnabled</span></span>
<span data-ttu-id="98378-158">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="98378-158">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="98378-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98378-159">-ResourceGroupName</span></span>
<span data-ttu-id="98378-160">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="98378-160">Resource Group Name</span></span>

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

### <span data-ttu-id="98378-161">-Slot</span><span class="sxs-lookup"><span data-stu-id="98378-161">-Slot</span></span>
<span data-ttu-id="98378-162">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="98378-162">WebApp Slot Name</span></span>

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

### <span data-ttu-id="98378-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="98378-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="98378-164">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="98378-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="98378-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="98378-165">-WebApp</span></span>
<span data-ttu-id="98378-166">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="98378-166">WebApp Object</span></span>

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

### <span data-ttu-id="98378-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="98378-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="98378-168">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="98378-168">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="98378-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98378-169">CommonParameters</span></span>
<span data-ttu-id="98378-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98378-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98378-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98378-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98378-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98378-172">INPUTS</span></span>

### <span data-ttu-id="98378-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="98378-173">System.Int32</span></span>
<span data-ttu-id="98378-174">Параметры: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98378-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="98378-175">System. String</span><span class="sxs-lookup"><span data-stu-id="98378-175">System.String</span></span>

### <span data-ttu-id="98378-176">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="98378-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="98378-177">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="98378-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="98378-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98378-178">OUTPUTS</span></span>

### <span data-ttu-id="98378-179">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="98378-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="98378-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="98378-180">NOTES</span></span>

## <span data-ttu-id="98378-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98378-181">RELATED LINKS</span></span>

[<span data-ttu-id="98378-182">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-182">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-183">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-183">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-184">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-184">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-185">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-185">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-186">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-186">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-187">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="98378-187">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="98378-188">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="98378-188">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
