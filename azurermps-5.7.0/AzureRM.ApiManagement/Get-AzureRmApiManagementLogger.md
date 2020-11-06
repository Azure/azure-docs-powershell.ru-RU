---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementLogger.md
ms.openlocfilehash: bcfcd052d2278fa39bc310a5c1927457a1b0fcd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567018"
---
# <span data-ttu-id="e1f49-101">Get-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e1f49-101">Get-AzureRmApiManagementLogger</span></span>

## <span data-ttu-id="e1f49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1f49-102">SYNOPSIS</span></span>
<span data-ttu-id="e1f49-103">Возвращает объекты средства ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="e1f49-103">Gets API Management Logger objects.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1f49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1f49-104">SYNTAX</span></span>

### <span data-ttu-id="e1f49-105">GetAllLoggers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e1f49-105">GetAllLoggers (Default)</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e1f49-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="e1f49-106">GetByLoggerId</span></span>
```
Get-AzureRmApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1f49-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f49-107">DESCRIPTION</span></span>
<span data-ttu-id="e1f49-108">Командлет **Get-AzureRmApiManagementLogger** получает **средство ведения журнала** управления API Azure или все средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="e1f49-108">The **Get-AzureRmApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="e1f49-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1f49-109">EXAMPLES</span></span>

### <span data-ttu-id="e1f49-110">Пример 1: получение всех средств ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e1f49-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext
```

<span data-ttu-id="e1f49-111">Эта команда получает все средства ведения журнала для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="e1f49-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="e1f49-112">Пример 2: получение определенного средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="e1f49-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="e1f49-113">Эта команда удаляет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="e1f49-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="e1f49-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1f49-114">PARAMETERS</span></span>

### <span data-ttu-id="e1f49-115">-Context</span><span class="sxs-lookup"><span data-stu-id="e1f49-115">-Context</span></span>
<span data-ttu-id="e1f49-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e1f49-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e1f49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1f49-117">-DefaultProfile</span></span>
<span data-ttu-id="e1f49-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1f49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e1f49-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="e1f49-119">-LoggerId</span></span>
<span data-ttu-id="e1f49-120">Указывает идентификатор определенного регистратора, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="e1f49-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByLoggerId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1f49-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1f49-121">CommonParameters</span></span>
<span data-ttu-id="e1f49-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1f49-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1f49-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1f49-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1f49-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1f49-124">INPUTS</span></span>

### <span data-ttu-id="e1f49-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="e1f49-125">None</span></span>
<span data-ttu-id="e1f49-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e1f49-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1f49-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1f49-127">OUTPUTS</span></span>

### <span data-ttu-id="e1f49-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e1f49-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>
<span data-ttu-id="e1f49-129">Подробные сведения о средстве ведения журнала, настроенном в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="e1f49-129">The detail of the Logger configured in API Management service.</span></span>

### <span data-ttu-id="e1f49-130">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger></span><span class="sxs-lookup"><span data-stu-id="e1f49-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger></span></span>
<span data-ttu-id="e1f49-131">Список средств ведения журнала, настроенных в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="e1f49-131">The list of Loggers configured in API Management service.</span></span>

## <span data-ttu-id="e1f49-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1f49-132">NOTES</span></span>

## <span data-ttu-id="e1f49-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1f49-133">RELATED LINKS</span></span>

[<span data-ttu-id="e1f49-134">New-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e1f49-134">New-AzureRmApiManagementLogger</span></span>](./New-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e1f49-135">Remove-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e1f49-135">Remove-AzureRmApiManagementLogger</span></span>](./Remove-AzureRmApiManagementLogger.md)

[<span data-ttu-id="e1f49-136">Set-AzureRmApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="e1f49-136">Set-AzureRmApiManagementLogger</span></span>](./Set-AzureRmApiManagementLogger.md)


