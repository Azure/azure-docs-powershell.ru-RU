---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 4166119F-D26A-45A1-B040-D7B2459833D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmWebApp.md
ms.openlocfilehash: 0f8008a2b567bb2cb2b67755d2ea5bb586f0c115
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560404"
---
# <span data-ttu-id="34e8c-101">Set-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-101">Set-AzureRmWebApp</span></span>

## <span data-ttu-id="34e8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="34e8c-103">Изменение веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="34e8c-103">Modifies an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34e8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34e8c-104">SYNTAX</span></span>

### <span data-ttu-id="34e8c-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="34e8c-105">S1</span></span>
```
Set-AzureRmWebApp [[-AppServicePlan] <String>] [[-DefaultDocuments] <String[]>]
 [[-NetFrameworkVersion] <String>] [[-PhpVersion] <String>] [[-RequestTracingEnabled] <Boolean>]
 [[-HttpLoggingEnabled] <Boolean>] [[-DetailedErrorLoggingEnabled] <Boolean>] [[-AppSettings] <Hashtable>]
 [[-ConnectionStrings] <Hashtable>]
 [[-HandlerMappings] <System.Collections.Generic.IList`1[Microsoft.Azure.Management.WebSites.Models.HandlerMapping]>]
 [[-ManagedPipelineMode] <String>] [[-WebSocketsEnabled] <Boolean>] [[-Use32BitWorkerProcess] <Boolean>]
 [[-AutoSwapSlotName] <String>] [-HostNames <String[]>] [-NumberOfWorkers <Int32>]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34e8c-106">S2</span><span class="sxs-lookup"><span data-stu-id="34e8c-106">S2</span></span>
```
Set-AzureRmWebApp [[-Use32BitWorkerProcess] <Boolean>] [[-AutoSwapSlotName] <String>]
 [-NumberOfWorkers <Int32>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34e8c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="34e8c-108">Командлет **Set-AzureRmWebApp** задает веб-приложение Azure.</span><span class="sxs-lookup"><span data-stu-id="34e8c-108">The **Set-AzureRmWebApp** cmdlet sets an Azure Web App.</span></span>

## <span data-ttu-id="34e8c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="34e8c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34e8c-110">Example 1</span></span>
```
PS C:\> Set-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -HttpLoggingEnabled $true
```

<span data-ttu-id="34e8c-111">Эта команда устанавливает для HttpLoggingEnabled значение true для веб-приложения ContosoWebApp, связанного с группой ресурсов по умолчанию — Web-WestUS</span><span class="sxs-lookup"><span data-stu-id="34e8c-111">This command sets HttpLoggingEnabled to true for Web App ContosoWebApp associated with the resource group Default-Web-WestUS</span></span>

## <span data-ttu-id="34e8c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34e8c-112">PARAMETERS</span></span>

### <span data-ttu-id="34e8c-113">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="34e8c-113">-AppServicePlan</span></span>
<span data-ttu-id="34e8c-114">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="34e8c-114">App Service Plan Name</span></span>

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

### <span data-ttu-id="34e8c-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="34e8c-115">-AppSettings</span></span>
<span data-ttu-id="34e8c-116">Хэш-таблица параметров приложения</span><span class="sxs-lookup"><span data-stu-id="34e8c-116">App Settings HashTable</span></span>

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

### <span data-ttu-id="34e8c-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="34e8c-117">-AutoSwapSlotName</span></span>
<span data-ttu-id="34e8c-118">Имя конечной ячейки для автоматического переключения</span><span class="sxs-lookup"><span data-stu-id="34e8c-118">Destination slot name for auto swap</span></span>

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

### <span data-ttu-id="34e8c-119">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="34e8c-119">-ConnectionStrings</span></span>
<span data-ttu-id="34e8c-120">Хэш-таблица со строками соединения</span><span class="sxs-lookup"><span data-stu-id="34e8c-120">Connection Strings HashTable</span></span>

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

### <span data-ttu-id="34e8c-121">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="34e8c-121">-DefaultDocuments</span></span>
<span data-ttu-id="34e8c-122">Массив строк документов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="34e8c-122">Default Documents String Array</span></span>

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

### <span data-ttu-id="34e8c-123">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34e8c-123">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="34e8c-124">Подробное ведение журнала ошибок включено (логический)</span><span class="sxs-lookup"><span data-stu-id="34e8c-124">Detailed Error Logging Enabled Boolean</span></span>

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

### <span data-ttu-id="34e8c-125">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="34e8c-125">-HandlerMappings</span></span>
<span data-ttu-id="34e8c-126">Сопоставленные обработчики IList</span><span class="sxs-lookup"><span data-stu-id="34e8c-126">Handler Mappings IList</span></span>

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

### <span data-ttu-id="34e8c-127">-HostName</span><span class="sxs-lookup"><span data-stu-id="34e8c-127">-HostNames</span></span>
<span data-ttu-id="34e8c-128">Массив строк HostNames WebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-128">WebApp HostNames String Array</span></span>

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

### <span data-ttu-id="34e8c-129">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="34e8c-129">-HttpLoggingEnabled</span></span>
<span data-ttu-id="34e8c-130">HttpLoggingEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="34e8c-130">HttpLoggingEnabled Boolean</span></span>

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

### <span data-ttu-id="34e8c-131">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="34e8c-131">-ManagedPipelineMode</span></span>
<span data-ttu-id="34e8c-132">Имя режима управляемого конвейера</span><span class="sxs-lookup"><span data-stu-id="34e8c-132">Managed Pipeline Mode Name</span></span>

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

### <span data-ttu-id="34e8c-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="34e8c-133">-Name</span></span>
<span data-ttu-id="34e8c-134">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-134">WebApp Name</span></span>

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

### <span data-ttu-id="34e8c-135">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="34e8c-135">-NetFrameworkVersion</span></span>
<span data-ttu-id="34e8c-136">Версия .NET Framework</span><span class="sxs-lookup"><span data-stu-id="34e8c-136">Net Framework Version</span></span>

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

### <span data-ttu-id="34e8c-137">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="34e8c-137">-NumberOfWorkers</span></span>
<span data-ttu-id="34e8c-138">Количество назначаемых работников</span><span class="sxs-lookup"><span data-stu-id="34e8c-138">The number of workers to be allocated</span></span>

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

### <span data-ttu-id="34e8c-139">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="34e8c-139">-PhpVersion</span></span>
<span data-ttu-id="34e8c-140">Версия PHP</span><span class="sxs-lookup"><span data-stu-id="34e8c-140">Php Version</span></span>

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

### <span data-ttu-id="34e8c-141">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="34e8c-141">-RequestTracingEnabled</span></span>
<span data-ttu-id="34e8c-142">Включена трассировка запросов</span><span class="sxs-lookup"><span data-stu-id="34e8c-142">Request Tracing Enabled</span></span>

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

### <span data-ttu-id="34e8c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e8c-143">-ResourceGroupName</span></span>
<span data-ttu-id="34e8c-144">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="34e8c-144">Resource Group Name</span></span>

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

### <span data-ttu-id="34e8c-145">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="34e8c-145">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="34e8c-146">Использование логического рабочего процесса 32-bit</span><span class="sxs-lookup"><span data-stu-id="34e8c-146">Use 32-bit Worker Process Boolean</span></span>

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

### <span data-ttu-id="34e8c-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-147">-WebApp</span></span>
<span data-ttu-id="34e8c-148">Объект WebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-148">WebApp Object</span></span>

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

### <span data-ttu-id="34e8c-149">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="34e8c-149">-WebSocketsEnabled</span></span>
<span data-ttu-id="34e8c-150">WebSocketsEnabled Boolean</span><span class="sxs-lookup"><span data-stu-id="34e8c-150">WebSocketsEnabled Boolean</span></span>

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

### <span data-ttu-id="34e8c-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e8c-151">-DefaultProfile</span></span>
<span data-ttu-id="34e8c-152">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34e8c-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34e8c-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e8c-153">CommonParameters</span></span>
<span data-ttu-id="34e8c-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34e8c-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e8c-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34e8c-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e8c-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34e8c-156">INPUTS</span></span>

### <span data-ttu-id="34e8c-157">Int32</span><span class="sxs-lookup"><span data-stu-id="34e8c-157">Int32</span></span>
<span data-ttu-id="34e8c-158">Параметр "NumberOfWorkers" принимает значение типа Int32 из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34e8c-158">Parameter 'NumberOfWorkers' accepts value of type 'Int32' from the pipeline</span></span>

### <span data-ttu-id="34e8c-159">Семейств</span><span class="sxs-lookup"><span data-stu-id="34e8c-159">Site</span></span>
<span data-ttu-id="34e8c-160">Параметр "WebApp" принимает значение типа "сайт" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="34e8c-160">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="34e8c-161">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34e8c-161">OUTPUTS</span></span>

## <span data-ttu-id="34e8c-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="34e8c-162">NOTES</span></span>

## <span data-ttu-id="34e8c-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34e8c-163">RELATED LINKS</span></span>

[<span data-ttu-id="34e8c-164">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-164">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="34e8c-165">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-165">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="34e8c-166">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-166">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="34e8c-167">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-167">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="34e8c-168">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-168">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="34e8c-169">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="34e8c-169">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)
