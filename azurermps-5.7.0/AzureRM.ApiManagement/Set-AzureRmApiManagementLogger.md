---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: 16a60f5f9951aaa40ac8da8584e1c2690206cdb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569088"
---
# <span data-ttu-id="aebe6-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="aebe6-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="aebe6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aebe6-102">SYNOPSIS</span></span>
<span data-ttu-id="aebe6-103">Изменяет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="aebe6-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aebe6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aebe6-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aebe6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aebe6-105">DESCRIPTION</span></span>
<span data-ttu-id="aebe6-106">Командлет **Set-AzureRmApiManagementLogger** изменяет параметры **средства ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="aebe6-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="aebe6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aebe6-107">EXAMPLES</span></span>

### <span data-ttu-id="aebe6-108">Пример 1: изменение средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="aebe6-108">Example 1: Modify a logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="aebe6-109">Эта команда изменяет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="aebe6-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="aebe6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aebe6-110">PARAMETERS</span></span>

### <span data-ttu-id="aebe6-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="aebe6-111">-ConnectionString</span></span>
<span data-ttu-id="aebe6-112">Указывает строку подключения к концентраторам событий Azure, которая включает права на отправку политики.</span><span class="sxs-lookup"><span data-stu-id="aebe6-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="aebe6-113">-Context</span><span class="sxs-lookup"><span data-stu-id="aebe6-113">-Context</span></span>
<span data-ttu-id="aebe6-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="aebe6-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="aebe6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aebe6-115">-DefaultProfile</span></span>
<span data-ttu-id="aebe6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aebe6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="aebe6-117">-Описание</span><span class="sxs-lookup"><span data-stu-id="aebe6-117">-Description</span></span>
<span data-ttu-id="aebe6-118">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="aebe6-118">Specifies a description.</span></span>

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

### <span data-ttu-id="aebe6-119">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="aebe6-119">-IsBuffered</span></span>
<span data-ttu-id="aebe6-120">Указывает, что записи в средстве ведения журнала буферизуются перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="aebe6-120">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="aebe6-121">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="aebe6-121">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aebe6-122">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="aebe6-122">-LoggerId</span></span>
<span data-ttu-id="aebe6-123">Указывает ИД регистратора для обновления.</span><span class="sxs-lookup"><span data-stu-id="aebe6-123">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="aebe6-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="aebe6-124">-Name</span></span>
<span data-ttu-id="aebe6-125">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="aebe6-125">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="aebe6-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aebe6-126">-PassThru</span></span>
<span data-ttu-id="aebe6-127">Указывает на то, что этот командлет возвращает  **PsApiManagementLogger** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="aebe6-127">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aebe6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aebe6-128">CommonParameters</span></span>
<span data-ttu-id="aebe6-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aebe6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aebe6-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aebe6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aebe6-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aebe6-131">INPUTS</span></span>

### <span data-ttu-id="aebe6-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="aebe6-132">None</span></span>
<span data-ttu-id="aebe6-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="aebe6-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aebe6-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aebe6-134">OUTPUTS</span></span>

### <span data-ttu-id="aebe6-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="aebe6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="aebe6-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="aebe6-136">NOTES</span></span>

## <span data-ttu-id="aebe6-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aebe6-137">RELATED LINKS</span></span>

[<span data-ttu-id="aebe6-138">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="aebe6-138">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="aebe6-139">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="aebe6-139">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="aebe6-140">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="aebe6-140">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


