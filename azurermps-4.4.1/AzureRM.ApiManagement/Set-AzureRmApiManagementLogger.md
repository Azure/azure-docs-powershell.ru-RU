---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B4ADD38-FA22-4C25-9B9C-FD7861883811
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementLogger.md
ms.openlocfilehash: c21c227dd748f28523f4ac616d003e029d19e38f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566342"
---
# <span data-ttu-id="2aba8-101">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2aba8-101">Set-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="2aba8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2aba8-102">SYNOPSIS</span></span>
<span data-ttu-id="2aba8-103">Изменяет средство ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="2aba8-103">Modifies an API Management Logger.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aba8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2aba8-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String> [-Name <String>]
 [-ConnectionString <String>] [-Description <String>] [-IsBuffered] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aba8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aba8-105">DESCRIPTION</span></span>
<span data-ttu-id="2aba8-106">Командлет **Set-AzureRmApiManagementLogger** изменяет параметры **средства ведения журнала** управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2aba8-106">The **Set-AzureRmApiManagementLogger** cmdlet modifies settings of an Azure API Management **Logger**.</span></span>

## <span data-ttu-id="2aba8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2aba8-107">EXAMPLES</span></span>

### <span data-ttu-id="2aba8-108">Пример 1: изменение средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="2aba8-108">Example 1: Modify a logger</span></span>
```
PS C:\>Set-AzureRmApiManagementLogger -Context $ApimContext -LoggerId "Logger123" -Name "ContosoSdkEventHub" -ConnectionString "Endpoint=sb://ContosoSdkEventHubs.servicebus.windows.net/;SharedAccessKeyName=SendKey;SharedAccessKey=<key>" -Description "updated SDK event hub logger" -PassThru
```

<span data-ttu-id="2aba8-109">Эта команда изменяет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="2aba8-109">This command modifies a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="2aba8-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2aba8-110">PARAMETERS</span></span>

### <span data-ttu-id="2aba8-111">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="2aba8-111">-ConnectionString</span></span>
<span data-ttu-id="2aba8-112">Указывает строку подключения к концентраторам событий Azure, которая включает права на отправку политики.</span><span class="sxs-lookup"><span data-stu-id="2aba8-112">Specifies an Azure Event Hubs connection string that includes Send policy rights.</span></span>

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

### <span data-ttu-id="2aba8-113">-Context</span><span class="sxs-lookup"><span data-stu-id="2aba8-113">-Context</span></span>
<span data-ttu-id="2aba8-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2aba8-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2aba8-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="2aba8-115">-Description</span></span>
<span data-ttu-id="2aba8-116">Задает описание.</span><span class="sxs-lookup"><span data-stu-id="2aba8-116">Specifies a description.</span></span>

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

### <span data-ttu-id="2aba8-117">-Буферизация</span><span class="sxs-lookup"><span data-stu-id="2aba8-117">-IsBuffered</span></span>
<span data-ttu-id="2aba8-118">Указывает, что записи в средстве ведения журнала буферизуются перед публикацией.</span><span class="sxs-lookup"><span data-stu-id="2aba8-118">Specifies that the records in the logger are buffered before publishing.</span></span>
<span data-ttu-id="2aba8-119">Когда записи записываются в буфер, они отправляются в концентраторы событий каждые 15 секунд или каждый раз, когда буфер получает 256 КБ сообщений.</span><span class="sxs-lookup"><span data-stu-id="2aba8-119">When records are buffered, they are sent to Event Hubs every 15 seconds, or whenever the buffer receives 256 KB of messages.</span></span>

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

### <span data-ttu-id="2aba8-120">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="2aba8-120">-LoggerId</span></span>
<span data-ttu-id="2aba8-121">Указывает ИД регистратора для обновления.</span><span class="sxs-lookup"><span data-stu-id="2aba8-121">Specifies the ID of the logger to update.</span></span>

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

### <span data-ttu-id="2aba8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2aba8-122">-Name</span></span>
<span data-ttu-id="2aba8-123">Указывает имя сущности концентратора событий на классическом портале Azure.</span><span class="sxs-lookup"><span data-stu-id="2aba8-123">Specifies the entity name of an event hub from Azure classic portal.</span></span>

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

### <span data-ttu-id="2aba8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aba8-124">-PassThru</span></span>
<span data-ttu-id="2aba8-125">Указывает на то, что этот командлет возвращает  **PsApiManagementLogger** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="2aba8-125">Indicates that this cmdlet returns the  **PsApiManagementLogger** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="2aba8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aba8-126">-DefaultProfile</span></span>
<span data-ttu-id="2aba8-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2aba8-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aba8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aba8-128">CommonParameters</span></span>
<span data-ttu-id="2aba8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2aba8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aba8-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aba8-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aba8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2aba8-131">INPUTS</span></span>

## <span data-ttu-id="2aba8-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aba8-132">OUTPUTS</span></span>

### <span data-ttu-id="2aba8-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2aba8-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="2aba8-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2aba8-134">NOTES</span></span>

## <span data-ttu-id="2aba8-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2aba8-135">RELATED LINKS</span></span>

[<span data-ttu-id="2aba8-136">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2aba8-136">Get-AzureRmApiManagementLogger</span></span>](./Get-AzureRmApiManagementLogger.md)

[<span data-ttu-id="2aba8-137">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2aba8-137">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="2aba8-138">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="2aba8-138">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)


