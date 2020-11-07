---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: FA868206-D8B0-4868-A1D1-D3F96BF3ADCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebAppSlot.md
ms.openlocfilehash: 4780deac3d335060d5a3d7e262a61184b2e0c3b4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732048"
---
# <span data-ttu-id="3456c-101">Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-101">Set-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="3456c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3456c-102">SYNOPSIS</span></span>
<span data-ttu-id="3456c-103">Изменение слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3456c-103">Modifies an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3456c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3456c-104">SYNTAX</span></span>

### <span data-ttu-id="3456c-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="3456c-105">S1</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-ResourceGroupName] <String> [-Name] <String>
 [-Slot] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3456c-106">S2</span><span class="sxs-lookup"><span data-stu-id="3456c-106">S2</span></span>
```
Set-AzureRmWebAppSlot [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [-AutoSwapSlotName <String>] [-NumberOfWorkers <Int32>] [-WebApp] <Site>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3456c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3456c-107">DESCRIPTION</span></span>
<span data-ttu-id="3456c-108">Командлет **Set-AzureRmWebApp** задает слот веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="3456c-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App Slot.</span></span>

## <span data-ttu-id="3456c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3456c-109">EXAMPLES</span></span>

### <span data-ttu-id="3456c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3456c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -Slot "Slot001" -HttpLoggingEnabled $true
```

<span data-ttu-id="3456c-111">Эта команда устанавливает для HttpLoggingEnabled значение true для слота Slot001, относящегося к веб-приложению ContosoWebApp, связанному с группой ресурсов по умолчанию-веб-WestUS</span><span class="sxs-lookup"><span data-stu-id="3456c-111">This command sets HttpLoggingEnabled to true for Slot Slot001 pertaining to Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="3456c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3456c-112">PARAMETERS</span></span>

### <span data-ttu-id="3456c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3456c-113">-AppServicePlan</span></span>
<span data-ttu-id="3456c-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="3456c-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="3456c-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="3456c-115">-AppSettings</span></span>
<span data-ttu-id="3456c-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="3456c-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="3456c-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="3456c-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="3456c-118">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="3456c-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="3456c-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="3456c-119">-ConnectionStrings</span></span>
<span data-ttu-id="3456c-120">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="3456c-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="3456c-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="3456c-121">-DefaultDocuments</span></span>
<span data-ttu-id="3456c-122">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="3456c-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="3456c-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3456c-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="3456c-124">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="3456c-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="3456c-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="3456c-125">-HandlerMappings</span></span>
<span data-ttu-id="3456c-126">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="3456c-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="3456c-127">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="3456c-127">-HttpLoggingEnabled</span></span>
<span data-ttu-id="3456c-128">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="3456c-128">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="3456c-129">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="3456c-129">-ManagedPipelineMode</span></span>
<span data-ttu-id="3456c-130">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="3456c-130">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="3456c-131">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3456c-131">-Name</span></span>
<span data-ttu-id="3456c-132">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="3456c-132">WebApp Name</span></span>

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

### <span data-ttu-id="3456c-133">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="3456c-133">-NetFrameworkVersion</span></span>
<span data-ttu-id="3456c-134">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="3456c-134">Net Framework Version</span></span>

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

### <span data-ttu-id="3456c-135">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="3456c-135">-NumberOfWorkers</span></span>
<span data-ttu-id="3456c-136">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="3456c-136">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="3456c-137">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="3456c-137">-PhpVersion</span></span>
<span data-ttu-id="3456c-138">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="3456c-138">Php Version</span></span>

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

### <span data-ttu-id="3456c-139">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="3456c-139">-RequestTracingEnabled</span></span>
<span data-ttu-id="3456c-140">Трассировка запросов с включенным логическим значением</span><span class="sxs-lookup"><span data-stu-id="3456c-140">Request Tracing Enabled Boolean</span></span>

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

### <span data-ttu-id="3456c-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3456c-141">-ResourceGroupName</span></span>
<span data-ttu-id="3456c-142">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="3456c-142">Resource Group Name</span></span>

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

### <span data-ttu-id="3456c-143">-Slot</span><span class="sxs-lookup"><span data-stu-id="3456c-143">-Slot</span></span>
<span data-ttu-id="3456c-144">Название гнезда WebApp</span><span class="sxs-lookup"><span data-stu-id="3456c-144">WebApp Slot Name</span></span>

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

### <span data-ttu-id="3456c-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="3456c-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="3456c-146">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="3456c-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="3456c-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="3456c-147">-WebApp</span></span>
<span data-ttu-id="3456c-148">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="3456c-148">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3456c-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="3456c-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="3456c-150">Для веб-сокетов включена логическая переменная</span><span class="sxs-lookup"><span data-stu-id="3456c-150">Web Sockets Enabled Boolean</span></span>

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

### <span data-ttu-id="3456c-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3456c-151">-DefaultProfile</span></span>
<span data-ttu-id="3456c-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3456c-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3456c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3456c-153">CommonParameters</span></span>
<span data-ttu-id="3456c-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3456c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3456c-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3456c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3456c-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3456c-156">INPUTS</span></span>

### <span data-ttu-id="3456c-157">Int32</span><span class="sxs-lookup"><span data-stu-id="3456c-157">Int32</span></span>
<span data-ttu-id="3456c-158">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3456c-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="3456c-159">Семейств</span><span class="sxs-lookup"><span data-stu-id="3456c-159">Site</span></span>
<span data-ttu-id="3456c-160">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3456c-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="3456c-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3456c-161">OUTPUTS</span></span>

## <span data-ttu-id="3456c-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="3456c-162">NOTES</span></span>

## <span data-ttu-id="3456c-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3456c-163">RELATED LINKS</span></span>

[<span data-ttu-id="3456c-164">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-164">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-165">New-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-165">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-166">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-166">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-167">Restarting-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-167">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-168">Start-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-168">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-169">Остановить-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="3456c-169">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="3456c-170">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="3456c-170">Get-AzureRmAppServicePlan</span></span>](./Get-AzureRmAppServicePlan.md)
