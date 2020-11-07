---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B80389B9-E143-4E24-A222-E95F691DA2E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementApi.md
ms.openlocfilehash: 95784b084f6d106413c65b840dd73f313a47799e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734287"
---
# <span data-ttu-id="fb108-101">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-101">Get-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="fb108-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb108-102">SYNOPSIS</span></span>
<span data-ttu-id="fb108-103">Возвращает API.</span><span class="sxs-lookup"><span data-stu-id="fb108-103">Gets an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb108-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb108-104">SYNTAX</span></span>

### <span data-ttu-id="fb108-105">Все API (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb108-105">All APIs (Default)</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb108-106">Найти по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fb108-106">Find by ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb108-107">Поиск по имени</span><span class="sxs-lookup"><span data-stu-id="fb108-107">Find by Name</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb108-108">Найти по коду продукта</span><span class="sxs-lookup"><span data-stu-id="fb108-108">Find by product ID</span></span>
```
Get-AzureRmApiManagementApi -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb108-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb108-109">DESCRIPTION</span></span>
<span data-ttu-id="fb108-110">Командлет **Get-AzureRmApiManagementApi** получает один или несколько API для управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="fb108-110">The **Get-AzureRmApiManagementApi** cmdlet gets one or more Azure API Management APIs.</span></span>

## <span data-ttu-id="fb108-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb108-111">EXAMPLES</span></span>

### <span data-ttu-id="fb108-112">Пример 1: получение всех API-интерфейсов управления</span><span class="sxs-lookup"><span data-stu-id="fb108-112">Example 1: Get all management APIs</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext
```

<span data-ttu-id="fb108-113">Эта команда получает все API для заданного контекста.</span><span class="sxs-lookup"><span data-stu-id="fb108-113">This command gets all of the APIs for the specified context.</span></span>

### <span data-ttu-id="fb108-114">Пример 2: получение API управления по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="fb108-114">Example 2: Get a management API by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId $ApiId
```

<span data-ttu-id="fb108-115">Эта команда возвращает API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="fb108-115">This command gets the API with the specified ID.</span></span>

### <span data-ttu-id="fb108-116">Пример 3: получение API-интерфейса управления по имени</span><span class="sxs-lookup"><span data-stu-id="fb108-116">Example 3: Get a management API by name</span></span>
```
PS C:\>Get-AzureRmApiManagementApi -Context $ApiMgmtContext -Name "EchoApi"
```

<span data-ttu-id="fb108-117">Эта команда возвращает API с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="fb108-117">This command gets the API with the specified name.</span></span>

## <span data-ttu-id="fb108-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb108-118">PARAMETERS</span></span>

### <span data-ttu-id="fb108-119">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fb108-119">-ApiId</span></span>
<span data-ttu-id="fb108-120">Указывает идентификатор API для получения.</span><span class="sxs-lookup"><span data-stu-id="fb108-120">Specifies the ID of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb108-121">-Context</span><span class="sxs-lookup"><span data-stu-id="fb108-121">-Context</span></span>
<span data-ttu-id="fb108-122">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="fb108-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="fb108-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fb108-123">-Name</span></span>
<span data-ttu-id="fb108-124">Указывает имя получаемого API.</span><span class="sxs-lookup"><span data-stu-id="fb108-124">Specifies the name of the API to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by Name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb108-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fb108-125">-ProductId</span></span>
<span data-ttu-id="fb108-126">Указывает идентификатор продукта, для которого требуется получить API.</span><span class="sxs-lookup"><span data-stu-id="fb108-126">Specifies the ID of the product for which to get the API.</span></span>

```yaml
Type: System.String
Parameter Sets: Find by product ID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb108-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb108-127">-DefaultProfile</span></span>
<span data-ttu-id="fb108-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb108-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb108-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb108-129">CommonParameters</span></span>
<span data-ttu-id="fb108-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb108-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb108-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb108-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb108-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb108-132">INPUTS</span></span>

## <span data-ttu-id="fb108-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb108-133">OUTPUTS</span></span>

### <span data-ttu-id="fb108-134">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi></span><span class="sxs-lookup"><span data-stu-id="fb108-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi></span></span>

## <span data-ttu-id="fb108-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb108-135">NOTES</span></span>

## <span data-ttu-id="fb108-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb108-136">RELATED LINKS</span></span>

[<span data-ttu-id="fb108-137">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-137">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="fb108-138">Import-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-138">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="fb108-139">New-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-139">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="fb108-140">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-140">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="fb108-141">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="fb108-141">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


