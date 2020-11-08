---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9D821623-DEF9-49E4-9C44-10643A92A2E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f6690aa45125a0d1b3383b08443234f47a1f7e3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075433"
---
# <span data-ttu-id="74e12-101">Set-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="74e12-101">Set-AzureWebsite</span></span>

## <span data-ttu-id="74e12-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74e12-102">SYNOPSIS</span></span>
<span data-ttu-id="74e12-103">Настройка веб-сайта, работающего в Azure.</span><span class="sxs-lookup"><span data-stu-id="74e12-103">Configures a website running in Azure.</span></span>

## <span data-ttu-id="74e12-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74e12-104">SYNTAX</span></span>

```
Set-AzureWebsite [-NumberOfWorkers <Int32>] [-DefaultDocuments <String[]>] [-NetFrameworkVersion <String>]
 [-PhpVersion <String>] [-RequestTracingEnabled <Boolean>] [-HttpLoggingEnabled <Boolean>]
 [-DetailedErrorLoggingEnabled <Boolean>] [-HostNames <String[]>] [-AppSettings <Hashtable>]
 [-Metadata <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]>]
 [-ConnectionStrings <ConnStringPropertyBag>] [-HandlerMappings <HandlerMapping[]>]
 [-SiteWithConfig <SiteWithConfig>] [-PassThru] [-ManagedPipelineMode <ManagedPipelineMode>]
 [-WebSocketsEnabled <Boolean>]
 [-RoutingRules <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]>]
 [-Use32BitWorkerProcess <Boolean>] [-AutoSwapSlotName <String>]
 [-SlotStickyAppSettingNames <System.Collections.Generic.List`1[System.String]>]
 [-SlotStickyConnectionStringNames <System.Collections.Generic.List`1[System.String]>] [-Name <String>]
 [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="74e12-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e12-105">DESCRIPTION</span></span>
<span data-ttu-id="74e12-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="74e12-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="74e12-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="74e12-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="74e12-108">Командлет **Set-AzureWebsite** настраивает веб-сайт, работающий в Azure.</span><span class="sxs-lookup"><span data-stu-id="74e12-108">The **Set-AzureWebsite** cmdlet configures a website running in Azure.</span></span>

## <span data-ttu-id="74e12-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74e12-109">EXAMPLES</span></span>

### <span data-ttu-id="74e12-110">Пример 1: Включение ведения журнала HTTP для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="74e12-110">Example 1: Enable HTTP logging for a website</span></span>
```
PS C:\> Set-AzureWebsite -HttpLoggingEnabled 1
```

<span data-ttu-id="74e12-111">В этом примере разрешено ведение журнала HTTP.</span><span class="sxs-lookup"><span data-stu-id="74e12-111">This example enables HTTP logging.</span></span>

### <span data-ttu-id="74e12-112">Пример 2: Настройка учетных данных хранилища для веб-сайта</span><span class="sxs-lookup"><span data-stu-id="74e12-112">Example 2: Set storage credentials for a website</span></span>
```
PS C:\> $settings = New-Object Hashtable$settings["AZURE_STORAGE_ACCOUNT"= myaccountname$settings["AZURE_STORAGE_ACCESS_KEY"] = myaccesskeySet-AzureWebsite -AppSettings $settings myWebsite
```

<span data-ttu-id="74e12-113">В этом примере на веб-сайте с именем myWebsite устанавливаются учетные данные хранилища с переменными среды для AZURE_STORAGE_ACCOUNT и AZURE_STORAGE_ACCESS_KEY.</span><span class="sxs-lookup"><span data-stu-id="74e12-113">This example sets storage credentials in a website named myWebsite with environment variables for AZURE_STORAGE_ACCOUNT and AZURE_STORAGE_ACCESS_KEY.</span></span>

## <span data-ttu-id="74e12-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74e12-114">PARAMETERS</span></span>

### <span data-ttu-id="74e12-115">-AppSettings</span><span class="sxs-lookup"><span data-stu-id="74e12-115">-AppSettings</span></span>
<span data-ttu-id="74e12-116">Указывает переменные среды, которые будут использоваться веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="74e12-116">Specifies the environment variables that will be used by the website.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-117">-AutoSwapSlotName</span><span class="sxs-lookup"><span data-stu-id="74e12-117">-AutoSwapSlotName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-118">-ConnectionStrings</span><span class="sxs-lookup"><span data-stu-id="74e12-118">-ConnectionStrings</span></span>
<span data-ttu-id="74e12-119">Указывает строки подключения, используемые веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="74e12-119">Specifies the connection strings used by the website.</span></span>

```yaml
Type: ConnStringPropertyBag
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-120">-DefaultDocuments</span><span class="sxs-lookup"><span data-stu-id="74e12-120">-DefaultDocuments</span></span>
<span data-ttu-id="74e12-121">Указывает документы, которые автоматически отображаются при просмотре веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-121">Specifies the documents that are automatically displayed when browsing the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-122">-DetailedErrorLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="74e12-122">-DetailedErrorLoggingEnabled</span></span>
<span data-ttu-id="74e12-123">Определяет, регистрируются ли подробные ошибки IIS для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-123">Determines whether detailed IIS errors are logged for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-124">-HandlerMappings</span><span class="sxs-lookup"><span data-stu-id="74e12-124">-HandlerMappings</span></span>
<span data-ttu-id="74e12-125">Указывает сопоставления обработчиков, используемые веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="74e12-125">Specifies the handler mappings used by the website.</span></span>

```yaml
Type: HandlerMapping[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="74e12-126">-HostNames</span></span>
<span data-ttu-id="74e12-127">Указывает полные имена узлов, которые можно использовать для доступа к веб-сайту.</span><span class="sxs-lookup"><span data-stu-id="74e12-127">Specifies the fully qualified host names that can be used to access the website.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-128">-HttpLoggingEnabled</span><span class="sxs-lookup"><span data-stu-id="74e12-128">-HttpLoggingEnabled</span></span>
<span data-ttu-id="74e12-129">Определяет, включено ли ведение журнала HTTP для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-129">Determines whether http logging is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-130">-ManagedPipelineMode</span><span class="sxs-lookup"><span data-stu-id="74e12-130">-ManagedPipelineMode</span></span>
<span data-ttu-id="74e12-131">Задает режим управляемого конвейера.</span><span class="sxs-lookup"><span data-stu-id="74e12-131">Specifies the managed pipeline mode.</span></span>

```yaml
Type: ManagedPipelineMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="74e12-132">-Metadata</span></span>
<span data-ttu-id="74e12-133">Задает метаданные для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-133">Specifies the metadata for the website.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.NameValuePair]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-134">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74e12-134">-Name</span></span>
<span data-ttu-id="74e12-135">Указывает имя веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-135">Specifies the name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-136">-NetFrameworkVersion</span><span class="sxs-lookup"><span data-stu-id="74e12-136">-NetFrameworkVersion</span></span>
<span data-ttu-id="74e12-137">Указывает версию платформы .NET Framework, требуемую для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-137">Specifies the version of the .Net Framework required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-138">-NumberOfWorkers</span><span class="sxs-lookup"><span data-stu-id="74e12-138">-NumberOfWorkers</span></span>
<span data-ttu-id="74e12-139">Указывает количество рабочих процессов, на которых запущен веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="74e12-139">Specifies the number of worker processes running the website.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74e12-140">-PassThru</span></span>
<span data-ttu-id="74e12-141">Указывает на то, что этот командлет возвращает **логическое** значение.</span><span class="sxs-lookup"><span data-stu-id="74e12-141">Indicates that this cmdlet returns a **Boolean** value.</span></span>

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

### <span data-ttu-id="74e12-142">-PhpVersion</span><span class="sxs-lookup"><span data-stu-id="74e12-142">-PhpVersion</span></span>
<span data-ttu-id="74e12-143">Указывает версию PHP, требуемую для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-143">Specifies the PHP version required by the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="74e12-144">-Profile</span></span>
<span data-ttu-id="74e12-145">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="74e12-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74e12-146">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="74e12-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-147">-RequestTracingEnabled</span><span class="sxs-lookup"><span data-stu-id="74e12-147">-RequestTracingEnabled</span></span>
<span data-ttu-id="74e12-148">Определяет, включена ли трассировка запросов для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-148">Determines whether request tracing is enabled for the website.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-149">-RoutingRules</span><span class="sxs-lookup"><span data-stu-id="74e12-149">-RoutingRules</span></span>
<span data-ttu-id="74e12-150">Задает правила маршрутизации, используемые для тестирования в производстве.</span><span class="sxs-lookup"><span data-stu-id="74e12-150">Specifies the routing rules to use for testing in production.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.RoutingRule]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-151">-SiteWithConfig</span><span class="sxs-lookup"><span data-stu-id="74e12-151">-SiteWithConfig</span></span>
<span data-ttu-id="74e12-152">Указывает конфигурацию, используемую веб-сайтом.</span><span class="sxs-lookup"><span data-stu-id="74e12-152">Specifies the configuration used by the website.</span></span>

```yaml
Type: SiteWithConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-153">-Slot</span><span class="sxs-lookup"><span data-stu-id="74e12-153">-Slot</span></span>
<span data-ttu-id="74e12-154">Указывает имя гнезда для веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="74e12-154">Specifies the slot name of the website.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-155">-SlotStickyAppSettingNames</span><span class="sxs-lookup"><span data-stu-id="74e12-155">-SlotStickyAppSettingNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-156">-SlotStickyConnectionStringNames</span><span class="sxs-lookup"><span data-stu-id="74e12-156">-SlotStickyConnectionStringNames</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-157">-Use32BitWorkerProcess</span><span class="sxs-lookup"><span data-stu-id="74e12-157">-Use32BitWorkerProcess</span></span>
<span data-ttu-id="74e12-158">Указывает, нужно ли включать 32-разрядный режим.</span><span class="sxs-lookup"><span data-stu-id="74e12-158">Specifies whether to enable 32-bit mode.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-159">-WebSocketsEnabled</span><span class="sxs-lookup"><span data-stu-id="74e12-159">-WebSocketsEnabled</span></span>
<span data-ttu-id="74e12-160">Указывает, нужно ли включать WebSocket.</span><span class="sxs-lookup"><span data-stu-id="74e12-160">Specifies whether to enable WebSockets.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74e12-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e12-161">CommonParameters</span></span>
<span data-ttu-id="74e12-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74e12-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e12-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e12-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e12-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74e12-164">INPUTS</span></span>

## <span data-ttu-id="74e12-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e12-165">OUTPUTS</span></span>

## <span data-ttu-id="74e12-166">Пуск</span><span class="sxs-lookup"><span data-stu-id="74e12-166">NOTES</span></span>

## <span data-ttu-id="74e12-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74e12-167">RELATED LINKS</span></span>

[<span data-ttu-id="74e12-168">Get-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="74e12-168">Get-AzureWebsite</span></span>](./Get-AzureWebsite.md)

[<span data-ttu-id="74e12-169">New-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="74e12-169">New-AzureWebsite</span></span>](./New-AzureWebsite.md)

[<span data-ttu-id="74e12-170">Remove-AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="74e12-170">Remove-AzureWebsite</span></span>](./Remove-AzureWebsite.md)


