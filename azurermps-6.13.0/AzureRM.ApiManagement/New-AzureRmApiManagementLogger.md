---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 04119d70f1cf3ae01b1d74e24cb2e030eecaa46b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731995"
---
# <span data-ttu-id="61744-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61744-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="61744-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61744-102">SYNOPSIS</span></span>
<span data-ttu-id="61744-103">Создает средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="61744-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61744-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61744-104">SYNTAX</span></span>

### <span data-ttu-id="61744-105">EventHubLoggerSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="61744-105">EventHubLoggerSet (Default)</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61744-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="61744-106">ApplicationInsightsLoggerSet</span></span>
```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>]
 -InstrumentationKey <String> [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61744-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61744-107">DESCRIPTION</span></span>
<span data-ttu-id="61744-108">Командлет **New-AzureRmApiManagementLogger** создает **средство ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="61744-108">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="61744-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61744-109">EXAMPLES</span></span>

### <span data-ttu-id="61744-110">Пример 1: создание средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="61744-110">Example 1: Create a logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="61744-111">Эта команда создает средство ведения журнала с именем ContosoSdkEventHub, используя указанную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="61744-111">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="61744-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61744-112">PARAMETERS</span></span>

### <span data-ttu-id="61744-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="61744-113">-ConnectionString</span></span>
<span data-ttu-id="61744-114">Указывает строку подключения к концентраторам событий Azure, которая начинается со следующего: `Endpoint=endpoint and key from Azure classic portal`</span><span class="sxs-lookup"><span data-stu-id="61744-114">Specifies an Azure Event Hubs connection string that starts with the following: `Endpoint=endpoint and key from Azure classic portal`</span></span>
<span data-ttu-id="61744-115">Ключ с правами отправки в строке соединения должен быть настроен.</span><span class="sxs-lookup"><span data-stu-id="61744-115">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-116">-Context</span><span class="sxs-lookup"><span data-stu-id="61744-116">-Context</span></span>
<span data-ttu-id="61744-117">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="61744-117">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61744-118">-DefaultProfile</span></span>
<span data-ttu-id="61744-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61744-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61744-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="61744-120">-Description</span></span>
<span data-ttu-id="61744-121">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="61744-121">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-122">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="61744-122">-InstrumentationKey</span></span>
<span data-ttu-id="61744-123">Ключ инструментирования для Application Insights.</span><span class="sxs-lookup"><span data-stu-id="61744-123">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="61744-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="61744-124">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-125">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="61744-125">-IsBuffered</span></span>
<span data-ttu-id="61744-126">Указывает, буферизуются ли записи в средстве ведения журнала перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="61744-126">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="61744-127">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="61744-127">The default value is $True.</span></span>
<span data-ttu-id="61744-128">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="61744-128">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-129">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="61744-129">-LoggerId</span></span>
<span data-ttu-id="61744-130">Указывает идентификатор для средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="61744-130">Specifies an ID for the logger.</span></span>
<span data-ttu-id="61744-131">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="61744-131">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61744-132">-Name</span></span>
<span data-ttu-id="61744-133">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="61744-133">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61744-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61744-134">CommonParameters</span></span>
<span data-ttu-id="61744-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61744-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61744-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61744-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61744-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61744-137">INPUTS</span></span>

### <span data-ttu-id="61744-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="61744-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="61744-139">System. String</span><span class="sxs-lookup"><span data-stu-id="61744-139">System.String</span></span>

### <span data-ttu-id="61744-140">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="61744-140">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="61744-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61744-141">OUTPUTS</span></span>

### <span data-ttu-id="61744-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61744-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="61744-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="61744-143">NOTES</span></span>

## <span data-ttu-id="61744-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61744-144">RELATED LINKS</span></span>

[<span data-ttu-id="61744-145">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61744-145">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="61744-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61744-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="61744-147">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="61744-147">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


