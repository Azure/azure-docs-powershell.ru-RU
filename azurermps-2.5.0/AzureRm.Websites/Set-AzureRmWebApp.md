---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: d722c378e246fa175741c91092d99415275f094e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913706"
---
# <span data-ttu-id="34315-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="34315-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34315-102">SYNOPSIS</span></span>
<span data-ttu-id="34315-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="34315-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34315-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34315-104">SYNTAX</span></span>

### <span data-ttu-id="34315-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="34315-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>] [-AsJob] [[-AssignIdentity] <Boolean>]
 [[-HttpsOnly] <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="34315-106">S2</span><span class="sxs-lookup"><span data-stu-id="34315-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-AsJob] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34315-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34315-107">DESCRIPTION</span></span>
<span data-ttu-id="34315-108">Командлет **Set-AzureRmWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="34315-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="34315-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34315-109">EXAMPLES</span></span>

### <span data-ttu-id="34315-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34315-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="34315-111">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="34315-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="34315-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34315-112">PARAMETERS</span></span>

### <span data-ttu-id="34315-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="34315-113">-AppServicePlan</span></span>
<span data-ttu-id="34315-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="34315-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="34315-115">-AppSettings</span></span>
<span data-ttu-id="34315-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="34315-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34315-117">-AsJob</span></span>
<span data-ttu-id="34315-118">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="34315-118">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-119">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="34315-119">-AssignIdentity</span></span>
<span data-ttu-id="34315-120">Включение и отключение MSI для существующих Azure webapp или functionapp [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="34315-120">Enable/disable MSI on an existing azure webapp or functionapp [PREVIEW]</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-121">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="34315-121">-AutoSwapSlotName</span></span>
<span data-ttu-id="34315-122">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="34315-122">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-123">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="34315-123">-ConnectionStrings</span></span>
<span data-ttu-id="34315-124">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="34315-124">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: S1
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-125">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="34315-125">-DefaultDocuments</span></span>
<span data-ttu-id="34315-126">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="34315-126">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34315-127">-DefaultProfile</span></span>
<span data-ttu-id="34315-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34315-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-129">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34315-129">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="34315-130">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="34315-130">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-131">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="34315-131">-HandlerMappings</span></span>
<span data-ttu-id="34315-132">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="34315-132">Handler Mappings IList</span></span>

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

### <span data-ttu-id="34315-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="34315-133">-HostNames</span></span>
<span data-ttu-id="34315-134">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="34315-134">WebApp HostNames String Array</span></span>

```yaml
Type: String[]
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-135">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34315-135">-HttpLoggingEnabled</span></span>
<span data-ttu-id="34315-136">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="34315-136">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-137">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="34315-137">-HttpsOnly</span></span>
<span data-ttu-id="34315-138">Включение и отключение перенаправления всего трафика на HTTPS для существующей службы Azure webapp или functionapp</span><span class="sxs-lookup"><span data-stu-id="34315-138">Enable/disable redirecting all traffic to HTTPS on an existing azure webapp or functionapp</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-139">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="34315-139">-ManagedPipelineMode</span></span>
<span data-ttu-id="34315-140">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="34315-140">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34315-141">-Name</span></span>
<span data-ttu-id="34315-142">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="34315-142">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34315-143">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="34315-143">-NetFrameworkVersion</span></span>
<span data-ttu-id="34315-144">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="34315-144">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-145">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="34315-145">-NumberOfWorkers</span></span>
<span data-ttu-id="34315-146">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="34315-146">The number of workers to be allocated</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34315-147">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="34315-147">-PhpVersion</span></span>
<span data-ttu-id="34315-148">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="34315-148">Php Version</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-149">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="34315-149">-RequestTracingEnabled</span></span>
<span data-ttu-id="34315-150">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="34315-150">Request Tracing Enabled</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34315-151">-ResourceGroupName</span></span>
<span data-ttu-id="34315-152">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="34315-152">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-153">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="34315-153">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="34315-154">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="34315-154">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-155">-WebApp</span><span class="sxs-lookup"><span data-stu-id="34315-155">-WebApp</span></span>
<span data-ttu-id="34315-156">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="34315-156">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34315-157">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="34315-157">-WebSocketsEnabled</span></span>
<span data-ttu-id="34315-158">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="34315-158">WebSocketsEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34315-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34315-159">CommonParameters</span></span>
<span data-ttu-id="34315-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34315-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34315-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34315-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34315-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34315-162">INPUTS</span></span>

### <span data-ttu-id="34315-163">Int32</span><span class="sxs-lookup"><span data-stu-id="34315-163">Int32</span></span>
<span data-ttu-id="34315-164">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34315-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="34315-165">Семейств</span><span class="sxs-lookup"><span data-stu-id="34315-165">Site</span></span>
<span data-ttu-id="34315-166">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34315-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="34315-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34315-167">OUTPUTS</span></span>

## <span data-ttu-id="34315-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="34315-168">NOTES</span></span>

## <span data-ttu-id="34315-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34315-169">RELATED LINKS</span></span>

[<span data-ttu-id="34315-170">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-170">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="34315-171">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-171">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="34315-172">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-172">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="34315-173">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-173">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="34315-174">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-174">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="34315-175">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34315-175">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
