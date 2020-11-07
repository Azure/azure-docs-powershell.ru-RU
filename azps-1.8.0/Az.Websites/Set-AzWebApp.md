---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/set-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Set-AzWebApp.md
ms.openlocfilehash: 7fb1118d612aae7cf5495f0743550510088e5dbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728298"
---
# <span data-ttu-id="a961d-101">Set-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-101">Set-AzWebApp</span></span>



## <span data-ttu-id="a961d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a961d-102">SYNOPSIS</span></span>

<span data-ttu-id="a961d-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="a961d-103">Modifies an Azure Web App.</span></span>



## <span data-ttu-id="a961d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a961d-104">SYNTAX</span></span>



### <span data-ttu-id="a961d-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a961d-105">S1</span></span>

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



### <span data-ttu-id="a961d-106">S2</span><span class="sxs-lookup"><span data-stu-id="a961d-106">S2</span></span>

```

Set-AzWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>] [-NumberOfWorkers <Int32>]

 [-AsJob] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]

```



## <span data-ttu-id="a961d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a961d-107">DESCRIPTION</span></span>

<span data-ttu-id="a961d-108">Командлет **Set-AzWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="a961d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App.</span></span>



## <span data-ttu-id="a961d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a961d-109">EXAMPLES</span></span>



### <span data-ttu-id="a961d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a961d-110">Example 1</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -AppServicePlan "ContosoPlan"

```



<span data-ttu-id="a961d-111">Эта команда изменяет план appservice, связанный с веб-приложением ContosoWebApp, связанным с группой ресурсов по умолчанию — Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a961d-111">This command changes the appservice plan associated with the Web App ContosoWebApp associated with the resource group Default-Web-WestUS.</span></span> <span data-ttu-id="a961d-112">Воспользуйтесь ссылкой для learm более подробного изменения плана appservice и ограничений, связанных с ним.</span><span class="sxs-lookup"><span data-stu-id="a961d-112">Use the link to learm more about changing the appservice plan and constraints associated with it.</span></span>

https://docs.microsoft.com/en-us/azure/app-service/app-service-plan-manage#move-an-app-to-another-app-service-plan


### <span data-ttu-id="a961d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a961d-113">Example 2</span></span>

```

PS C:\> Set-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true

```



<span data-ttu-id="a961d-114">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="a961d-114">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>



## <span data-ttu-id="a961d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a961d-115">PARAMETERS</span></span>



### <span data-ttu-id="a961d-116">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a961d-116">-AppServicePlan</span></span>

<span data-ttu-id="a961d-117">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a961d-117">App Service Plan Name</span></span>



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



### <span data-ttu-id="a961d-118">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="a961d-118">-AppSettings</span></span>

<span data-ttu-id="a961d-119">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="a961d-119">App Settings HashTable</span></span>



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



### <span data-ttu-id="a961d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a961d-120">-AsJob</span></span>

<span data-ttu-id="a961d-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a961d-121">Run cmdlet in the background</span></span>



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



### <span data-ttu-id="a961d-122">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a961d-122">-AssignIdentity</span></span>

<span data-ttu-id="a961d-123">Включение и отключение MSI для существующих Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="a961d-123">Enable/disable MSI on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="a961d-124">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="a961d-124">-AutoSwapSlotName</span></span>

<span data-ttu-id="a961d-125">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="a961d-125">Destination slot name for auto swap</span></span>



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



### <span data-ttu-id="a961d-126">-AzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a961d-126">-AzureStoragePath</span></span>

<span data-ttu-id="a961d-127">Хранилище Azure, которое нужно подключить к веб-приложению для контейнера.</span><span class="sxs-lookup"><span data-stu-id="a961d-127">Azure Storage to mount inside a Web App for Container.</span></span> <span data-ttu-id="a961d-128">Создание ИТ с помощью New-AzureRmWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="a961d-128">Use New-AzureRmWebAppAzureStoragePath to create it</span></span>



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



### <span data-ttu-id="a961d-129">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="a961d-129">-ConnectionStrings</span></span>

<span data-ttu-id="a961d-130">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="a961d-130">Connection Strings HashTable</span></span>



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



### <span data-ttu-id="a961d-131">-ContainerImageName</span><span class="sxs-lookup"><span data-stu-id="a961d-131">-ContainerImageName</span></span>

<span data-ttu-id="a961d-132">Имя изображения контейнера</span><span class="sxs-lookup"><span data-stu-id="a961d-132">Container Image Name</span></span>



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



### <span data-ttu-id="a961d-133">-ContainerRegistryPassword</span><span class="sxs-lookup"><span data-stu-id="a961d-133">-ContainerRegistryPassword</span></span>

<span data-ttu-id="a961d-134">Пароль закрытого контейнера в реестре</span><span class="sxs-lookup"><span data-stu-id="a961d-134">Private Container Registry Password</span></span>



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



### <span data-ttu-id="a961d-135">-ContainerRegistryUrl</span><span class="sxs-lookup"><span data-stu-id="a961d-135">-ContainerRegistryUrl</span></span>

<span data-ttu-id="a961d-136">URL-адрес сервера реестра закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="a961d-136">Private Container Registry Server Url</span></span>



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



### <span data-ttu-id="a961d-137">-ContainerRegistryUser</span><span class="sxs-lookup"><span data-stu-id="a961d-137">-ContainerRegistryUser</span></span>

<span data-ttu-id="a961d-138">Имя пользователя в реестре для закрытого контейнера</span><span class="sxs-lookup"><span data-stu-id="a961d-138">Private Container Registry Username</span></span>



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



### <span data-ttu-id="a961d-139">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="a961d-139">-DefaultDocuments</span></span>

<span data-ttu-id="a961d-140">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a961d-140">Default Documents String Array</span></span>



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



### <span data-ttu-id="a961d-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a961d-141">-DefaultProfile</span></span>

<span data-ttu-id="a961d-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a961d-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>



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



### <span data-ttu-id="a961d-143">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a961d-143">-DetailedErrorLoggingEnabled</span></span>

<span data-ttu-id="a961d-144">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="a961d-144">Detailed Error Logging Enabled Boolean</span></span>



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



### <span data-ttu-id="a961d-145">-EnableContainerContinuousDeployment</span><span class="sxs-lookup"><span data-stu-id="a961d-145">-EnableContainerContinuousDeployment</span></span>

<span data-ttu-id="a961d-146">Включение и отключение веб-перехватчика непрерывного развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="a961d-146">Enables/Disables container continuous deployment webhook</span></span>



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



### <span data-ttu-id="a961d-147">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="a961d-147">-HandlerMappings</span></span>

<span data-ttu-id="a961d-148">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="a961d-148">Handler Mappings IList</span></span>



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



### <span data-ttu-id="a961d-149">-HostName</span><span class="sxs-lookup"><span data-stu-id="a961d-149">-HostNames</span></span>

<span data-ttu-id="a961d-150">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-150">WebApp HostNames String Array</span></span>



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



### <span data-ttu-id="a961d-151">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="a961d-151">-HttpLoggingEnabled</span></span>

<span data-ttu-id="a961d-152">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a961d-152">HttpLoggingEnabled Boolean</span></span>



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



### <span data-ttu-id="a961d-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="a961d-153">-HttpsOnly</span></span>

<span data-ttu-id="a961d-154">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="a961d-154">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>



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



### <span data-ttu-id="a961d-155">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="a961d-155">-ManagedPipelineMode</span></span>

<span data-ttu-id="a961d-156">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="a961d-156">Managed Pipeline Mode Name</span></span>



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



### <span data-ttu-id="a961d-157">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a961d-157">-Name</span></span>

<span data-ttu-id="a961d-158">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-158">WebApp Name</span></span>



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



### <span data-ttu-id="a961d-159">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="a961d-159">-NetFrameworkVersion</span></span>

<span data-ttu-id="a961d-160">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="a961d-160">Net Framework Version</span></span>



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



### <span data-ttu-id="a961d-161">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="a961d-161">-NumberOfWorkers</span></span>

<span data-ttu-id="a961d-162">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="a961d-162">The number of workers to be allocated</span></span>



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



### <span data-ttu-id="a961d-163">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="a961d-163">-PhpVersion</span></span>

<span data-ttu-id="a961d-164">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="a961d-164">Php Version</span></span>



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



### <span data-ttu-id="a961d-165">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="a961d-165">-RequestTracingEnabled</span></span>

<span data-ttu-id="a961d-166">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="a961d-166">Request Tracing Enabled</span></span>



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



### <span data-ttu-id="a961d-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a961d-167">-ResourceGroupName</span></span>

<span data-ttu-id="a961d-168">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a961d-168">Resource Group Name</span></span>



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



### <span data-ttu-id="a961d-169">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="a961d-169">-Use32BitWorkerProcess</span></span>

<span data-ttu-id="a961d-170">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="a961d-170">Use 32-bit Worker Process Boolean</span></span>



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



### <span data-ttu-id="a961d-171">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-171">-WebApp</span></span>

<span data-ttu-id="a961d-172">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-172">WebApp Object</span></span>



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



### <span data-ttu-id="a961d-173">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="a961d-173">-WebSocketsEnabled</span></span>

<span data-ttu-id="a961d-174">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="a961d-174">WebSocketsEnabled Boolean</span></span>



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



### <span data-ttu-id="a961d-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a961d-175">CommonParameters</span></span>

<span data-ttu-id="a961d-176">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a961d-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a961d-177">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a961d-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>



## <span data-ttu-id="a961d-178">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a961d-178">INPUTS</span></span>



### <span data-ttu-id="a961d-179">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a961d-179">System.Int32</span></span>



### <span data-ttu-id="a961d-180">System. String</span><span class="sxs-lookup"><span data-stu-id="a961d-180">System.String</span></span>



### <span data-ttu-id="a961d-181">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="a961d-181">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="a961d-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a961d-182">OUTPUTS</span></span>



### <span data-ttu-id="a961d-183">Microsoft. Azure. Commands. Apps. PSSite</span><span class="sxs-lookup"><span data-stu-id="a961d-183">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>



## <span data-ttu-id="a961d-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="a961d-184">NOTES</span></span>



## <span data-ttu-id="a961d-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a961d-185">RELATED LINKS</span></span>



[<span data-ttu-id="a961d-186">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-186">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



[<span data-ttu-id="a961d-187">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-187">New-AzWebApp</span></span>](./New-AzWebApp.md)



[<span data-ttu-id="a961d-188">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-188">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)



[<span data-ttu-id="a961d-189">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-189">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)



[<span data-ttu-id="a961d-190">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-190">Start-AzWebApp</span></span>](./Start-AzWebApp.md)



[<span data-ttu-id="a961d-191">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a961d-191">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)

