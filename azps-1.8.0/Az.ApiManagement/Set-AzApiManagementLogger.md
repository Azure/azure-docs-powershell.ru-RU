---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementLogger.md
ms.openlocfilehash: 4c7f4b4f308d04c6f9c82e70f9fbe0598bd4a9fb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901570"
---
# <span data-ttu-id="2d109-101">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2d109-101">Set-AzApiManagementLogger</span></span>

## <span data-ttu-id="2d109-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d109-102">SYNOPSIS</span></span>
<span data-ttu-id="2d109-103">Изменяет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="2d109-103">Modifies an API Management Logger.</span></span>

## <span data-ttu-id="2d109-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d109-104">SYNTAX</span></span>

### <span data-ttu-id="2d109-105">EventHubLoggerSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d109-105">EventHubLoggerSet (Default)</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d109-106">ApplicationInsightsLoggerSet</span><span class="sxs-lookup"><span data-stu-id="2d109-106">ApplicationInsightsLoggerSet</span></span>
```
Set-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-InstrumentationKey <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d109-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d109-107">DESCRIPTION</span></span>
<span data-ttu-id="2d109-108">Командлет **Set-AzApiManagementLogger** изменяет параметры **средства ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2d109-108">The **Set-AzApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="2d109-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d109-109">EXAMPLES</span></span>

### <span data-ttu-id="2d109-110">Пример 1: изменение средства ведения журнала EventHub</span><span class="sxs-lookup"><span data-stu-id="2d109-110">Example 1: Modify EventHub logger</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="2d109-111">Эта команда изменяет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="2d109-111">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="2d109-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d109-112">PARAMETERS</span></span>

### <span data-ttu-id="2d109-113">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2d109-113">-ConnectionString</span></span>
<span data-ttu-id="2d109-114">Указывает строку подключения к концентраторам событий Azure, которая включает права на отправку политики.</span><span class="sxs-lookup"><span data-stu-id="2d109-114">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="2d109-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2d109-115">-Context</span></span>
<span data-ttu-id="2d109-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2d109-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2d109-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d109-117">-DefaultProfile</span></span>
<span data-ttu-id="2d109-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d109-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d109-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="2d109-119">-Description</span></span>
<span data-ttu-id="2d109-120">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="2d109-120">Specifies a description.</span></span>

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

### <span data-ttu-id="2d109-121">-InstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="2d109-121">-InstrumentationKey</span></span>
<span data-ttu-id="2d109-122">Ключ инструментирования для Application Insights.</span><span class="sxs-lookup"><span data-stu-id="2d109-122">Instrumentation Key of the application Insights.</span></span> <span data-ttu-id="2d109-123">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2d109-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="2d109-124">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="2d109-124">-IsBuffered</span></span>
<span data-ttu-id="2d109-125">Указывает, что записи в средстве ведения журнала буферизуются перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="2d109-125">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="2d109-126">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="2d109-126">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="2d109-127">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="2d109-127">-LoggerId</span></span>
<span data-ttu-id="2d109-128">Указывает ИД регистратора для обновления.</span><span class="sxs-lookup"><span data-stu-id="2d109-128">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="2d109-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d109-129">-Name</span></span>
<span data-ttu-id="2d109-130">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="2d109-130">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="2d109-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2d109-131">-PassThru</span></span>
<span data-ttu-id="2d109-132">Указывает на то, что этот командлет возвращает  **PsApiManagementLogger** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2d109-132">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2d109-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d109-133">CommonParameters</span></span>
<span data-ttu-id="2d109-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d109-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d109-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d109-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d109-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d109-136">INPUTS</span></span>

### <span data-ttu-id="2d109-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2d109-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2d109-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2d109-138">System.String</span></span>

### <span data-ttu-id="2d109-139">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d109-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d109-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d109-140">OUTPUTS</span></span>

### <span data-ttu-id="2d109-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2d109-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="2d109-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d109-142">NOTES</span></span>

## <span data-ttu-id="2d109-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d109-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d109-144">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2d109-144">Get-AzApiManagementLogger</span></span>](./Get-AzApiManagementLogger.md)

[<span data-ttu-id="2d109-145">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2d109-145">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="2d109-146">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2d109-146">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)


