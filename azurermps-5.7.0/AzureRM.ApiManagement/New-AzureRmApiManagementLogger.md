---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: 2929cbd89328d971b47b748d4aa042ade13c1af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563760"
---
# <span data-ttu-id="cea15-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cea15-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="cea15-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cea15-102">SYNOPSIS</span></span>
<span data-ttu-id="cea15-103">Создает средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="cea15-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cea15-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cea15-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cea15-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cea15-105">DESCRIPTION</span></span>
<span data-ttu-id="cea15-106">Командлет **New-AzureRmApiManagementLogger** создает **средство ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="cea15-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="cea15-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cea15-107">EXAMPLES</span></span>

### <span data-ttu-id="cea15-108">Пример 1: создание средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="cea15-108">Example 1: Create a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="cea15-109">Эта команда создает средство ведения журнала с именем ContosoSdkEventHub, используя указанную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="cea15-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="cea15-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cea15-110">PARAMETERS</span></span>

### <span data-ttu-id="cea15-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="cea15-111">-ConnectionString</span></span>
<span data-ttu-id="cea15-112">Указывает строку подключения к концентраторам событий Azure, которая начинается со следующего:</span><span class="sxs-lookup"><span data-stu-id="cea15-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="cea15-113">Ключ с правами отправки в строке соединения должен быть настроен.</span><span class="sxs-lookup"><span data-stu-id="cea15-113">The Key with Send Rights in the connection string must be configured.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea15-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cea15-114">-Context</span></span>
<span data-ttu-id="cea15-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cea15-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea15-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cea15-116">-DefaultProfile</span></span>
<span data-ttu-id="cea15-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cea15-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="cea15-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="cea15-118">-Description</span></span>
<span data-ttu-id="cea15-119">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="cea15-119">Specifies a description.</span></span>

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

### <span data-ttu-id="cea15-120">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="cea15-120">-IsBuffered</span></span>
<span data-ttu-id="cea15-121">Указывает, буферизуются ли записи в средстве ведения журнала перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="cea15-121">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="cea15-122">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="cea15-122">The default value is $True.</span></span>
<span data-ttu-id="cea15-123">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="cea15-123">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="cea15-124">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="cea15-124">-LoggerId</span></span>
<span data-ttu-id="cea15-125">Указывает идентификатор для средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="cea15-125">Specifies an ID for the logger.</span></span>
<span data-ttu-id="cea15-126">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="cea15-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="cea15-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cea15-127">-Name</span></span>
<span data-ttu-id="cea15-128">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="cea15-128">Specifies the entity name of an event hub from Azure classic portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cea15-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cea15-129">CommonParameters</span></span>
<span data-ttu-id="cea15-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cea15-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cea15-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cea15-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cea15-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cea15-132">INPUTS</span></span>

### <span data-ttu-id="cea15-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="cea15-133">None</span></span>
<span data-ttu-id="cea15-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cea15-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cea15-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cea15-135">OUTPUTS</span></span>

### <span data-ttu-id="cea15-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cea15-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="cea15-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="cea15-137">NOTES</span></span>

## <span data-ttu-id="cea15-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cea15-138">RELATED LINKS</span></span>

[<span data-ttu-id="cea15-139">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cea15-139">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cea15-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cea15-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="cea15-141">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="cea15-141">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


