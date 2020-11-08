---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236459"
---
# <span data-ttu-id="4359d-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4359d-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="4359d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4359d-102">SYNOPSIS</span></span>
<span data-ttu-id="4359d-103">Возвращает объекты средства ведения журнала управления API.</span><span class="sxs-lookup"><span data-stu-id="4359d-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="4359d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4359d-104">SYNTAX</span></span>

### <span data-ttu-id="4359d-105">GetAllLoggers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4359d-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4359d-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="4359d-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4359d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4359d-107">DESCRIPTION</span></span>
<span data-ttu-id="4359d-108">Командлет **Get-AzApiManagementLogger** получает **средство ведения журнала** управления API Azure или все средства ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="4359d-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="4359d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4359d-109">EXAMPLES</span></span>

### <span data-ttu-id="4359d-110">Пример 1: получение всех средств ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4359d-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="4359d-111">Эта команда получает все средства ведения журнала для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="4359d-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="4359d-112">Пример 2: получение определенного средства ведения журнала</span><span class="sxs-lookup"><span data-stu-id="4359d-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="4359d-113">Эта команда удаляет средство ведения журнала с ИДЕНТИФИКАТОРом Logger123.</span><span class="sxs-lookup"><span data-stu-id="4359d-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="4359d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4359d-114">PARAMETERS</span></span>

### <span data-ttu-id="4359d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="4359d-115">-Context</span></span>
<span data-ttu-id="4359d-116">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4359d-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4359d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4359d-117">-DefaultProfile</span></span>
<span data-ttu-id="4359d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4359d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4359d-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="4359d-119">-LoggerId</span></span>
<span data-ttu-id="4359d-120">Указывает идентификатор определенного регистратора, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="4359d-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4359d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4359d-121">CommonParameters</span></span>
<span data-ttu-id="4359d-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4359d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4359d-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4359d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4359d-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4359d-124">INPUTS</span></span>

### <span data-ttu-id="4359d-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4359d-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4359d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4359d-126">System.String</span></span>

## <span data-ttu-id="4359d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4359d-127">OUTPUTS</span></span>

### <span data-ttu-id="4359d-128">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4359d-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="4359d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="4359d-129">NOTES</span></span>

## <span data-ttu-id="4359d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4359d-130">RELATED LINKS</span></span>

[<span data-ttu-id="4359d-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4359d-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="4359d-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4359d-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="4359d-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="4359d-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


