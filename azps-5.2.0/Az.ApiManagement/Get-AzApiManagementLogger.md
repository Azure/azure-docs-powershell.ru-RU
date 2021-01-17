---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401135"
---
# <span data-ttu-id="39498-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="39498-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="39498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39498-102">SYNOPSIS</span></span>
<span data-ttu-id="39498-103">Получает объекты регистратора управления API.</span><span class="sxs-lookup"><span data-stu-id="39498-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="39498-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39498-104">SYNTAX</span></span>

### <span data-ttu-id="39498-105">GetAllLoggers (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="39498-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39498-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="39498-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39498-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39498-107">DESCRIPTION</span></span>
<span data-ttu-id="39498-108">Для **этого с** его использованием можно получить журнал управления API Azure или все журналы. </span><span class="sxs-lookup"><span data-stu-id="39498-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="39498-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39498-109">EXAMPLES</span></span>

### <span data-ttu-id="39498-110">Пример 1. Получить всех регистраторов</span><span class="sxs-lookup"><span data-stu-id="39498-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="39498-111">Эта команда возвращает всех регистраторов для указанного контекста.</span><span class="sxs-lookup"><span data-stu-id="39498-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="39498-112">Пример 2. Получить определенный журнал</span><span class="sxs-lookup"><span data-stu-id="39498-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="39498-113">Эта команда удаляет регистратор с ИД 123.</span><span class="sxs-lookup"><span data-stu-id="39498-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="39498-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39498-114">PARAMETERS</span></span>

### <span data-ttu-id="39498-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="39498-115">-Context</span></span>
<span data-ttu-id="39498-116">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="39498-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="39498-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39498-117">-DefaultProfile</span></span>
<span data-ttu-id="39498-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39498-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39498-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="39498-119">-LoggerId</span></span>
<span data-ttu-id="39498-120">Определяет ИД конкретного регистратора, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="39498-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="39498-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39498-121">CommonParameters</span></span>
<span data-ttu-id="39498-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39498-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39498-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39498-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39498-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39498-124">INPUTS</span></span>

### <span data-ttu-id="39498-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="39498-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="39498-126">System.String</span><span class="sxs-lookup"><span data-stu-id="39498-126">System.String</span></span>

## <span data-ttu-id="39498-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39498-127">OUTPUTS</span></span>

### <span data-ttu-id="39498-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="39498-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="39498-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39498-129">NOTES</span></span>

## <span data-ttu-id="39498-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39498-130">RELATED LINKS</span></span>

[<span data-ttu-id="39498-131">New-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="39498-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="39498-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="39498-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="39498-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="39498-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


