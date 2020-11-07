---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzWebAppSlot.md
ms.openlocfilehash: b6cb41e49695fa7fd9fa0efdefdbefb2b23229a5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910565"
---
# <span data-ttu-id="86f2d-101">Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-101">Set-AzWebAppSlot</span></span>

## <span data-ttu-id="86f2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="86f2d-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="86f2d-103">Modifies an Azure Web App slot.</span></span>

## <span data-ttu-id="86f2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86f2d-104">SYNTAX</span></span>

### <span data-ttu-id="86f2d-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="86f2d-105">S1</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [[-AssignIdentity] <Boolean>] [[HttpsOnly] <Boolean>] [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="86f2d-106">S2</span><span class="sxs-lookup"><span data-stu-id="86f2d-106">S2</span></span>
```
Set-AzWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86f2d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="86f2d-108">Командлет **Set-AzWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="86f2d-108">The **Set-AzWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="86f2d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86f2d-109">EXAMPLES</span></span>

### <span data-ttu-id="86f2d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="86f2d-110">Example 1</span></span>
```
PS C:\> Set-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="86f2d-111">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="86f2d-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="86f2d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86f2d-112">PARAMETERS</span></span>

### <span data-ttu-id="86f2d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="86f2d-113">-AppServicePlan</span></span>
<span data-ttu-id="86f2d-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="86f2d-114">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="86f2d-115">-AppSettings</span></span>
<span data-ttu-id="86f2d-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="86f2d-116">App Settings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="86f2d-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="86f2d-118">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="86f2d-118">Destination slot name for auto swap</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="86f2d-119">-ConnectionStrings</span></span>
<span data-ttu-id="86f2d-120">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="86f2d-120">Connection Strings HashTable</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="86f2d-121">-DefaultDocuments</span></span>
<span data-ttu-id="86f2d-122">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="86f2d-122">Default Documents String Array</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f2d-123">-DefaultProfile</span></span>
<span data-ttu-id="86f2d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86f2d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="86f2d-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="86f2d-126">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="86f2d-126">Detailed Error Logging Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="86f2d-127">-HandlerMappings</span></span>
<span data-ttu-id="86f2d-128">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="86f2d-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="86f2d-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="86f2d-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="86f2d-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="86f2d-130">HttpLoggingEnabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="86f2d-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="86f2d-132">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="86f2d-132">Managed Pipeline Mode Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Classic, Integrated

Required: False
Position: 13
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86f2d-133">-Name</span></span>
<span data-ttu-id="86f2d-134">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="86f2d-134">WebApp Name</span></span>

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

### <span data-ttu-id="86f2d-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="86f2d-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="86f2d-136">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="86f2d-136">Net Framework Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="86f2d-137">-NumberOfWorkers</span></span>
<span data-ttu-id="86f2d-138">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="86f2d-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="86f2d-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="86f2d-139">-PhpVersion</span></span>
<span data-ttu-id="86f2d-140">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="86f2d-140">Php Version</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="86f2d-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="86f2d-142">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="86f2d-142">Request Tracing Enabled Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86f2d-143">-ResourceGroupName</span></span>
<span data-ttu-id="86f2d-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="86f2d-144">Resource Group Name</span></span>

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

### <span data-ttu-id="86f2d-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="86f2d-145">-Slot</span></span>
<span data-ttu-id="86f2d-146">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="86f2d-146">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="86f2d-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="86f2d-148">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="86f2d-148">Use 32-bit Worker Process Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f2d-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="86f2d-149">-WebApp</span></span>
<span data-ttu-id="86f2d-150">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="86f2d-150">WebApp Object</span></span>

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

### <span data-ttu-id="86f2d-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="86f2d-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="86f2d-152">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="86f2d-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="86f2d-153">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="86f2d-153">-HttpsOnly</span></span>
<span data-ttu-id="86f2d-154">Включение и отключение перенаправления всего трафика на HTTPS на существующую ячейку</span><span class="sxs-lookup"><span data-stu-id="86f2d-154">Enable/disable redirecting all traffic to HTTPS on an existing slot</span></span>

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
### <span data-ttu-id="86f2d-155">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="86f2d-155">-AssignIdentity</span></span>
<span data-ttu-id="86f2d-156">Включение и отключение MSI для существующего слота [Предварительная версия]</span><span class="sxs-lookup"><span data-stu-id="86f2d-156">Enable/disable MSI on an existing slot [PREVIEW]</span></span>

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

### <span data-ttu-id="86f2d-157">-AsJob</span><span class="sxs-lookup"><span data-stu-id="86f2d-157">-AsJob</span></span>
<span data-ttu-id="86f2d-158">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="86f2d-158">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="86f2d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f2d-159">CommonParameters</span></span>
<span data-ttu-id="86f2d-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86f2d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f2d-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86f2d-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f2d-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86f2d-162">INPUTS</span></span>

### <span data-ttu-id="86f2d-163">Int32</span><span class="sxs-lookup"><span data-stu-id="86f2d-163">Int32</span></span>
<span data-ttu-id="86f2d-164">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="86f2d-164">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="86f2d-165">Семейств</span><span class="sxs-lookup"><span data-stu-id="86f2d-165">Site</span></span>
<span data-ttu-id="86f2d-166">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="86f2d-166">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="86f2d-167">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f2d-167">OUTPUTS</span></span>

## <span data-ttu-id="86f2d-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="86f2d-168">NOTES</span></span>

## <span data-ttu-id="86f2d-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86f2d-169">RELATED LINKS</span></span>

[<span data-ttu-id="86f2d-170">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-170">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-171">New-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-171">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-172">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-172">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-173">Restarting-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-173">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-174">Start-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-174">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-175">Остановить-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="86f2d-175">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="86f2d-176">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="86f2d-176">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)
