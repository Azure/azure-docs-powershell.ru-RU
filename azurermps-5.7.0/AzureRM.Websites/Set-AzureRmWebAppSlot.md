---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 717f355326acc4d169bee1e93d98446fa052a5e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733934"
---
# <span data-ttu-id="83849-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="83849-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83849-102">SYNOPSIS</span></span>
<span data-ttu-id="83849-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="83849-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83849-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83849-104">SYNTAX</span></span>

### <span data-ttu-id="83849-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="83849-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83849-106">S2</span><span class="sxs-lookup"><span data-stu-id="83849-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83849-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83849-107">DESCRIPTION</span></span>
<span data-ttu-id="83849-108">Командлет **Set-AzureRmWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="83849-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="83849-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83849-109">EXAMPLES</span></span>

### <span data-ttu-id="83849-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="83849-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="83849-111">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="83849-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="83849-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83849-112">PARAMETERS</span></span>

### <span data-ttu-id="83849-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="83849-113">-AppServicePlan</span></span>
<span data-ttu-id="83849-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="83849-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="83849-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="83849-115">-AppSettings</span></span>
<span data-ttu-id="83849-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="83849-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="83849-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="83849-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="83849-118">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="83849-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="83849-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="83849-119">-ConnectionStrings</span></span>
<span data-ttu-id="83849-120">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="83849-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="83849-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="83849-121">-DefaultDocuments</span></span>
<span data-ttu-id="83849-122">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="83849-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="83849-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83849-123">-DefaultProfile</span></span>
<span data-ttu-id="83849-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83849-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83849-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="83849-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="83849-126">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="83849-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="83849-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="83849-127">-HandlerMappings</span></span>
<span data-ttu-id="83849-128">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="83849-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="83849-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="83849-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="83849-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="83849-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="83849-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="83849-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="83849-132">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="83849-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="83849-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="83849-133">-Name</span></span>
<span data-ttu-id="83849-134">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="83849-134">WebApp Name</span></span>

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

### <span data-ttu-id="83849-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="83849-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="83849-136">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="83849-136">Net Framework Version</span></span>

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

### <span data-ttu-id="83849-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="83849-137">-NumberOfWorkers</span></span>
<span data-ttu-id="83849-138">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="83849-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="83849-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="83849-139">-PhpVersion</span></span>
<span data-ttu-id="83849-140">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="83849-140">Php Version</span></span>

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

### <span data-ttu-id="83849-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="83849-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="83849-142">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="83849-142">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="83849-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83849-143">-ResourceGroupName</span></span>
<span data-ttu-id="83849-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="83849-144">Resource Group Name</span></span>

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

### <span data-ttu-id="83849-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="83849-145">-Slot</span></span>
<span data-ttu-id="83849-146">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="83849-146">WebApp Slot Name</span></span>

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

### <span data-ttu-id="83849-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="83849-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="83849-148">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="83849-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="83849-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="83849-149">-WebApp</span></span>
<span data-ttu-id="83849-150">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="83849-150">WebApp Object</span></span>

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

### <span data-ttu-id="83849-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="83849-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="83849-152">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="83849-152">Web Sockets Enabled Boolean</span></span>

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
### <span data-ttu-id="83849-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="83849-153">-AsJob</span></span>
<span data-ttu-id="83849-154">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="83849-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="83849-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83849-155">CommonParameters</span></span>
<span data-ttu-id="83849-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83849-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83849-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83849-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83849-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83849-158">INPUTS</span></span>

### <span data-ttu-id="83849-159">Int32</span><span class="sxs-lookup"><span data-stu-id="83849-159">Int32</span></span>
<span data-ttu-id="83849-160">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="83849-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="83849-161">Семейств</span><span class="sxs-lookup"><span data-stu-id="83849-161">Site</span></span>
<span data-ttu-id="83849-162">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="83849-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="83849-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83849-163">OUTPUTS</span></span>

## <span data-ttu-id="83849-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="83849-164">NOTES</span></span>

## <span data-ttu-id="83849-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83849-165">RELATED LINKS</span></span>

[<span data-ttu-id="83849-166">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-166">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-167">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-167">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-168">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-168">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-169">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-169">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-170">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-170">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-171">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="83849-171">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="83849-172">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="83849-172">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
