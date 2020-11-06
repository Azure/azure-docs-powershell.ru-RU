---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: a47f490ae77fc540f3e14708b19dade5ce4e7c3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563919"
---
# <span data-ttu-id="c3341-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="c3341-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c3341-102">SYNOPSIS</span></span>
<span data-ttu-id="c3341-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="c3341-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3341-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c3341-104">SYNTAX</span></span>

### <span data-ttu-id="c3341-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="c3341-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-ContainerImageName <String>] [-ContainerRegistryUrl <String>]
 [-ContainerRegistryUser <String>] [-ContainerRegistryPassword <SecureString>]
 [-EnableContainerContinuousDeployment <Boolean>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob]
 [-AssignIdentity <Boolean>] [-HttpsOnly <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3341-106">S2</span><span class="sxs-lookup"><span data-stu-id="c3341-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c3341-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3341-107">DESCRIPTION</span></span>
<span data-ttu-id="c3341-108">Командлет **Set-AzureRmWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="c3341-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="c3341-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c3341-109">EXAMPLES</span></span>

### <span data-ttu-id="c3341-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c3341-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="c3341-111">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="c3341-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="c3341-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c3341-112">PARAMETERS</span></span>

### <span data-ttu-id="c3341-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="c3341-113">-AppServicePlan</span></span>
<span data-ttu-id="c3341-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="c3341-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="c3341-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="c3341-115">-AppSettings</span></span>
<span data-ttu-id="c3341-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="c3341-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="c3341-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c3341-117">-AsJob</span></span>
<span data-ttu-id="c3341-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c3341-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c3341-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c3341-119">-AssignIdentity</span></span>
<span data-ttu-id="c3341-120">Включение и отключение MSI для существующих Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="c3341-120">Enable/disable MSI on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c3341-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="c3341-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="c3341-122">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="c3341-122">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="c3341-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="c3341-123">-ConnectionStrings</span></span>
<span data-ttu-id="c3341-124">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="c3341-124">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="c3341-125">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="c3341-125">-ContainerImageName</span></span>
<span data-ttu-id="c3341-126">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="c3341-126">Container Image Name</span></span>

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

### <span data-ttu-id="c3341-127">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="c3341-127">-ContainerRegistryPassword</span></span>
<span data-ttu-id="c3341-128">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="c3341-128">Private Container Registry Password</span></span>

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

### <span data-ttu-id="c3341-129">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="c3341-129">-ContainerRegistryUrl</span></span>
<span data-ttu-id="c3341-130">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="c3341-130">Private Container Registry Server Url</span></span>

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

### <span data-ttu-id="c3341-131">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="c3341-131">-ContainerRegistryUser</span></span>
<span data-ttu-id="c3341-132">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="c3341-132">Private Container Registry Username</span></span>

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

### <span data-ttu-id="c3341-133">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="c3341-133">-DefaultDocuments</span></span>
<span data-ttu-id="c3341-134">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c3341-134">Default Documents String Array</span></span>

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

### <span data-ttu-id="c3341-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3341-135">-DefaultProfile</span></span>
<span data-ttu-id="c3341-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c3341-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3341-137">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3341-137">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="c3341-138">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="c3341-138">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="c3341-139">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="c3341-139">-EnableContainerContinuousDeployment</span></span>
<span data-ttu-id="c3341-140">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="c3341-140">Enables/Disables container continuous deployment webhook</span></span>

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

### <span data-ttu-id="c3341-141">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="c3341-141">-HandlerMappings</span></span>
<span data-ttu-id="c3341-142">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="c3341-142">Handler Mappings IList</span></span>

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

### <span data-ttu-id="c3341-143">-HostName</span><span class="sxs-lookup"><span data-stu-id="c3341-143">-HostNames</span></span>
<span data-ttu-id="c3341-144">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-144">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="c3341-145">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3341-145">-HttpLoggingEnabled</span></span>
<span data-ttu-id="c3341-146">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c3341-146">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="c3341-147">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="c3341-147">-HttpsOnly</span></span>
<span data-ttu-id="c3341-148">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="c3341-148">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

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

### <span data-ttu-id="c3341-149">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="c3341-149">-ManagedPipelineMode</span></span>
<span data-ttu-id="c3341-150">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="c3341-150">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="c3341-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c3341-151">-Name</span></span>
<span data-ttu-id="c3341-152">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-152">WebApp Name</span></span>

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

### <span data-ttu-id="c3341-153">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="c3341-153">-NetFrameworkVersion</span></span>
<span data-ttu-id="c3341-154">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="c3341-154">Net Framework Version</span></span>

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

### <span data-ttu-id="c3341-155">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="c3341-155">-NumberOfWorkers</span></span>
<span data-ttu-id="c3341-156">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="c3341-156">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="c3341-157">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="c3341-157">-PhpVersion</span></span>
<span data-ttu-id="c3341-158">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="c3341-158">Php Version</span></span>

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

### <span data-ttu-id="c3341-159">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3341-159">-RequestTracingEnabled</span></span>
<span data-ttu-id="c3341-160">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="c3341-160">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="c3341-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3341-161">-ResourceGroupName</span></span>
<span data-ttu-id="c3341-162">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c3341-162">Resource Group Name</span></span>

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

### <span data-ttu-id="c3341-163">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="c3341-163">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="c3341-164">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="c3341-164">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="c3341-165">-WebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-165">-WebApp</span></span>
<span data-ttu-id="c3341-166">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-166">WebApp Object</span></span>

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

### <span data-ttu-id="c3341-167">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="c3341-167">-WebSocketsEnabled</span></span>
<span data-ttu-id="c3341-168">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="c3341-168">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="c3341-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3341-169">CommonParameters</span></span>
<span data-ttu-id="c3341-170">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c3341-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3341-171">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3341-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3341-172">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c3341-172">INPUTS</span></span>

### <span data-ttu-id="c3341-173">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c3341-173">System.Int32</span></span>
<span data-ttu-id="c3341-174">Параметры: NumberOfWorkers (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3341-174">Parameters: NumberOfWorkers (ByValue)</span></span>

### <span data-ttu-id="c3341-175">System. String</span><span class="sxs-lookup"><span data-stu-id="c3341-175">System.String</span></span>

### <span data-ttu-id="c3341-176">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="c3341-176">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c3341-177">Параметры: WebApp (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3341-177">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="c3341-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c3341-178">OUTPUTS</span></span>

### <span data-ttu-id="c3341-179">Microsoft. Azure. Management. website. Models. site</span><span class="sxs-lookup"><span data-stu-id="c3341-179">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="c3341-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="c3341-180">NOTES</span></span>

## <span data-ttu-id="c3341-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c3341-181">RELATED LINKS</span></span>

[<span data-ttu-id="c3341-182">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-182">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c3341-183">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-183">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c3341-184">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-184">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c3341-185">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-185">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c3341-186">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-186">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="c3341-187">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c3341-187">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
