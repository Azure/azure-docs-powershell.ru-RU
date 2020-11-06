---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 7a037b107f3d72a000c2f69c8de507a4f414e283
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563171"
---
# <span data-ttu-id="664bc-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="664bc-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="664bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="664bc-102">SYNOPSIS</span></span>
<span data-ttu-id="664bc-103">Изменяет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="664bc-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="664bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="664bc-104">SYNTAX</span></span>

### <span data-ttu-id="664bc-105">EventHubLoggerSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="664bc-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="664bc-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="664bc-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-InstrumentationKey <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="664bc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="664bc-107">DESCRIPTION</span></span>
<span data-ttu-id="664bc-108">Командлет **Set-AzureRmApiManagementLogger** изменяет параметры **средства ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="664bc-108">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="664bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="664bc-109">EXAMPLES</span></span>

### <span data-ttu-id="664bc-110">Пример 1: изменение средства ведения журнала EventHub</span><span class="sxs-lookup"><span data-stu-id="664bc-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="664bc-111">Эта команда изменяет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="664bc-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="664bc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="664bc-112">PARAMETERS</span></span>

### <span data-ttu-id="664bc-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="664bc-113">-ConnectionString</span></span>
<span data-ttu-id="664bc-114">Указывает строку подключения к концентраторам событий Azure, которая включает права на отправку политики.</span><span class="sxs-lookup"><span data-stu-id="664bc-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-115">-Context</span><span class="sxs-lookup"><span data-stu-id="664bc-115">-Context</span></span>
<span data-ttu-id="664bc-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="664bc-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="664bc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="664bc-117">-DefaultProfile</span></span>
<span data-ttu-id="664bc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="664bc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="664bc-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="664bc-119">-Description</span></span>
<span data-ttu-id="664bc-120">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="664bc-120">Specifies a description.</span></span>

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

### <span data-ttu-id="664bc-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="664bc-121">-InstrumentationKey</span></span>
<span data-ttu-id="664bc-122">Ключ инструментирования для Application Insights.</span><span class="sxs-lookup"><span data-stu-id="664bc-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="664bc-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="664bc-123">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationInsightsLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-124">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="664bc-124">-IsBuffered</span></span>
<span data-ttu-id="664bc-125">Указывает, что записи в средстве ведения журнала буферизуются перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="664bc-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="664bc-126">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="664bc-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="664bc-127">-LoggerId</span></span>
<span data-ttu-id="664bc-128">Указывает ИД регистратора для обновления.</span><span class="sxs-lookup"><span data-stu-id="664bc-128">Specifies the ID of the logger to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="664bc-129">-Name</span></span>
<span data-ttu-id="664bc-130">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="664bc-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubLoggerSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="664bc-131">-PassThru</span></span>
<span data-ttu-id="664bc-132">Указывает на то, что этот командлет возвращает  **PsApiManagementLogger** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="664bc-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="664bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="664bc-133">CommonParameters</span></span>
<span data-ttu-id="664bc-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="664bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="664bc-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="664bc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="664bc-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="664bc-136">INPUTS</span></span>

### <span data-ttu-id="664bc-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="664bc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="664bc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="664bc-138">System.String</span></span>

### <span data-ttu-id="664bc-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="664bc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="664bc-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="664bc-140">OUTPUTS</span></span>

### <span data-ttu-id="664bc-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="664bc-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="664bc-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="664bc-142">NOTES</span></span>

## <span data-ttu-id="664bc-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="664bc-143">RELATED LINKS</span></span>

[<span data-ttu-id="664bc-144">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="664bc-144">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="664bc-145">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="664bc-145">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="664bc-146">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="664bc-146">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


