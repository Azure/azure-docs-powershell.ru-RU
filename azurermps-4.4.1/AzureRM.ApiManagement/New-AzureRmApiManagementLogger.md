---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D53F56-6E3B-491E-8776-5EBE109FBE3C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementLogger.md
ms.openlocfilehash: c7827f0df8b1baf4bb2fead9df091619751c969c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565726"
---
# <span data-ttu-id="027a7-101">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="027a7-101">New-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="027a7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="027a7-102">SYNOPSIS</span></span>
<span data-ttu-id="027a7-103">Создает средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="027a7-103">Creates an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="027a7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="027a7-104">SYNTAX</span></span>

```
New-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-LoggerId <String>] -Name <String>
 -ConnectionString <String> [-Description <String>] [-IsBuffered <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="027a7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="027a7-105">DESCRIPTION</span></span>
<span data-ttu-id="027a7-106">Командлет **New-AzureRmApiManagementLogger** создает **средство ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="027a7-106">The **New-AzureRmApiManagementLogger** cmdlet creates an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="027a7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="027a7-107">EXAMPLES</span></span>

### <span data-ttu-id="027a7-108">Пример 1: создание средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="027a7-108">Example 1: Create a logger</span></span>
```
PS C:\>New-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "SDK event hub logger"
```

<span data-ttu-id="027a7-109">Эта команда создает средство ведения журнала с именем ContosoSdkEventHub, используя указанную строку подключения.</span><span class="sxs-lookup"><span data-stu-id="027a7-109">This command creates a logger named ContosoSdkEventHub by using the specified connection string.</span></span>

## <span data-ttu-id="027a7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="027a7-110">PARAMETERS</span></span>

### <span data-ttu-id="027a7-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="027a7-111">-ConnectionString</span></span>
<span data-ttu-id="027a7-112">Указывает строку подключения к концентраторам событий Azure, которая начинается со следующего:</span><span class="sxs-lookup"><span data-stu-id="027a7-112">Specifies an Azure Event Hubs connection string that starts with the following:</span></span> 

`Endpoint=endpoint and key from Azure classic portal`

<span data-ttu-id="027a7-113">Ключ с правами отправки в строке соединения должен быть настроен.</span><span class="sxs-lookup"><span data-stu-id="027a7-113">The Key with Send Rights in the connection string must be configured.</span></span>

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

### <span data-ttu-id="027a7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="027a7-114">-Context</span></span>
<span data-ttu-id="027a7-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="027a7-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="027a7-116">-Описание</span><span class="sxs-lookup"><span data-stu-id="027a7-116">-Description</span></span>
<span data-ttu-id="027a7-117">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="027a7-117">Specifies a description.</span></span>

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

### <span data-ttu-id="027a7-118">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="027a7-118">-IsBuffered</span></span>
<span data-ttu-id="027a7-119">Указывает, буферизуются ли записи в средстве ведения журнала перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="027a7-119">Specifies whether the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="027a7-120">Значение по умолчанию — $True.</span><span class="sxs-lookup"><span data-stu-id="027a7-120">The default value is $True.</span></span>
<span data-ttu-id="027a7-121">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="027a7-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="027a7-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="027a7-122">-LoggerId</span></span>
<span data-ttu-id="027a7-123">Указывает идентификатор для средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="027a7-123">Specifies an ID for the logger.</span></span>
<span data-ttu-id="027a7-124">Если идентификатор не указан, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="027a7-124">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="027a7-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="027a7-125">-Name</span></span>
<span data-ttu-id="027a7-126">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="027a7-126">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="027a7-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="027a7-127">-DefaultProfile</span></span>
<span data-ttu-id="027a7-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="027a7-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="027a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="027a7-129">CommonParameters</span></span>
<span data-ttu-id="027a7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="027a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="027a7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="027a7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="027a7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="027a7-132">INPUTS</span></span>

## <span data-ttu-id="027a7-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="027a7-133">OUTPUTS</span></span>

### <span data-ttu-id="027a7-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="027a7-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="027a7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="027a7-135">NOTES</span></span>

## <span data-ttu-id="027a7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="027a7-136">RELATED LINKS</span></span>

[<span data-ttu-id="027a7-137">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="027a7-137">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="027a7-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="027a7-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="027a7-139">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="027a7-139">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


