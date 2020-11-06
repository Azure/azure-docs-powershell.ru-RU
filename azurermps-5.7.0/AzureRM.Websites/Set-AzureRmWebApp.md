---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/set-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 3587c7a725386976a04a9dc9922b3b0a16eb9362
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567855"
---
# <span data-ttu-id="4335d-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="4335d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4335d-102">SYNOPSIS</span></span>
<span data-ttu-id="4335d-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="4335d-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4335d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4335d-104">SYNTAX</span></span>

### <span data-ttu-id="4335d-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="4335d-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4335d-106">S2</span><span class="sxs-lookup"><span data-stu-id="4335d-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4335d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4335d-107">DESCRIPTION</span></span>
<span data-ttu-id="4335d-108">Командлет **Set-AzureRmWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="4335d-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="4335d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4335d-109">EXAMPLES</span></span>

### <span data-ttu-id="4335d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4335d-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="4335d-111">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="4335d-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="4335d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4335d-112">PARAMETERS</span></span>

### <span data-ttu-id="4335d-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="4335d-113">-AppServicePlan</span></span>
<span data-ttu-id="4335d-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="4335d-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="4335d-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="4335d-115">-AppSettings</span></span>
<span data-ttu-id="4335d-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="4335d-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="4335d-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="4335d-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="4335d-118">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="4335d-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="4335d-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="4335d-119">-ConnectionStrings</span></span>
<span data-ttu-id="4335d-120">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="4335d-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="4335d-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="4335d-121">-DefaultDocuments</span></span>
<span data-ttu-id="4335d-122">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="4335d-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="4335d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4335d-123">-DefaultProfile</span></span>
<span data-ttu-id="4335d-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4335d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4335d-125">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4335d-125">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="4335d-126">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="4335d-126">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="4335d-127">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="4335d-127">-HandlerMappings</span></span>
<span data-ttu-id="4335d-128">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="4335d-128">Handler Mappings IList</span></span>

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

### <span data-ttu-id="4335d-129">-HostName</span><span class="sxs-lookup"><span data-stu-id="4335d-129">-HostNames</span></span>
<span data-ttu-id="4335d-130">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-130">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="4335d-131">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="4335d-131">-HttpLoggingEnabled</span></span>
<span data-ttu-id="4335d-132">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="4335d-132">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="4335d-133">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="4335d-133">-ManagedPipelineMode</span></span>
<span data-ttu-id="4335d-134">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="4335d-134">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="4335d-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4335d-135">-Name</span></span>
<span data-ttu-id="4335d-136">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-136">WebApp Name</span></span>

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

### <span data-ttu-id="4335d-137">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="4335d-137">-NetFrameworkVersion</span></span>
<span data-ttu-id="4335d-138">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="4335d-138">Net Framework Version</span></span>

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

### <span data-ttu-id="4335d-139">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="4335d-139">-NumberOfWorkers</span></span>
<span data-ttu-id="4335d-140">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="4335d-140">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="4335d-141">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="4335d-141">-PhpVersion</span></span>
<span data-ttu-id="4335d-142">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="4335d-142">Php Version</span></span>

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

### <span data-ttu-id="4335d-143">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="4335d-143">-RequestTracingEnabled</span></span>
<span data-ttu-id="4335d-144">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="4335d-144">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="4335d-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4335d-145">-ResourceGroupName</span></span>
<span data-ttu-id="4335d-146">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="4335d-146">Resource Group Name</span></span>

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

### <span data-ttu-id="4335d-147">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="4335d-147">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="4335d-148">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="4335d-148">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="4335d-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-149">-WebApp</span></span>
<span data-ttu-id="4335d-150">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-150">WebApp Object</span></span>

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

### <span data-ttu-id="4335d-151">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="4335d-151">-WebSocketsEnabled</span></span>
<span data-ttu-id="4335d-152">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="4335d-152">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="4335d-153">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4335d-153">-AsJob</span></span>
<span data-ttu-id="4335d-154">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4335d-154">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4335d-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4335d-155">CommonParameters</span></span>
<span data-ttu-id="4335d-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4335d-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4335d-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4335d-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4335d-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4335d-158">INPUTS</span></span>

### <span data-ttu-id="4335d-159">Int32</span><span class="sxs-lookup"><span data-stu-id="4335d-159">Int32</span></span>
<span data-ttu-id="4335d-160">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4335d-160">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="4335d-161">Семейств</span><span class="sxs-lookup"><span data-stu-id="4335d-161">Site</span></span>
<span data-ttu-id="4335d-162">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4335d-162">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="4335d-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4335d-163">OUTPUTS</span></span>

## <span data-ttu-id="4335d-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="4335d-164">NOTES</span></span>

## <span data-ttu-id="4335d-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4335d-165">RELATED LINKS</span></span>

[<span data-ttu-id="4335d-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="4335d-167">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-167">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="4335d-168">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-168">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="4335d-169">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-169">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="4335d-170">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-170">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="4335d-171">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="4335d-171">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
