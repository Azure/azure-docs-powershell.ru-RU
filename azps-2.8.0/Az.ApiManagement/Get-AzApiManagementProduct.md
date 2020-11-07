---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9ad3c6b149e58bcd81ec8ce9c15ddc27fff85878
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728099"
---
# <span data-ttu-id="9b16b-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9b16b-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="9b16b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b16b-102">SYNOPSIS</span></span>
<span data-ttu-id="9b16b-103">Возвращает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="9b16b-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="9b16b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b16b-104">SYNTAX</span></span>

### <span data-ttu-id="9b16b-105">GetAllProducts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b16b-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b16b-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="9b16b-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b16b-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="9b16b-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b16b-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="9b16b-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b16b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b16b-109">DESCRIPTION</span></span>
<span data-ttu-id="9b16b-110">Командлет **Get-AzApiManagementProduct** получает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="9b16b-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="9b16b-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b16b-111">EXAMPLES</span></span>

### <span data-ttu-id="9b16b-112">Пример 1: получение всех продуктов</span><span class="sxs-lookup"><span data-stu-id="9b16b-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="9b16b-113">Эта команда возвращает все продукты для управления API.</span><span class="sxs-lookup"><span data-stu-id="9b16b-113">This command get all API Management products.</span></span>

### <span data-ttu-id="9b16b-114">Пример 2: получение продукта по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="9b16b-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="9b16b-115">Эта команда получает продукт по управлению API по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="9b16b-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="9b16b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b16b-116">PARAMETERS</span></span>

### <span data-ttu-id="9b16b-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9b16b-117">-ApiId</span></span>
<span data-ttu-id="9b16b-118">ApiId API для поиска соответствующих продуктов.</span><span class="sxs-lookup"><span data-stu-id="9b16b-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="9b16b-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9b16b-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b16b-120">-Context</span><span class="sxs-lookup"><span data-stu-id="9b16b-120">-Context</span></span>
<span data-ttu-id="9b16b-121">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9b16b-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b16b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b16b-122">-DefaultProfile</span></span>
<span data-ttu-id="9b16b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b16b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b16b-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9b16b-124">-ProductId</span></span>
<span data-ttu-id="9b16b-125">Указывает идентификатор продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="9b16b-125">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b16b-126">-Title</span><span class="sxs-lookup"><span data-stu-id="9b16b-126">-Title</span></span>
<span data-ttu-id="9b16b-127">Указывает название продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="9b16b-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="9b16b-128">Если задано значение, командлет попытается получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="9b16b-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b16b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b16b-129">CommonParameters</span></span>
<span data-ttu-id="9b16b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b16b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b16b-131">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b16b-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b16b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b16b-132">INPUTS</span></span>

### <span data-ttu-id="9b16b-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9b16b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9b16b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9b16b-134">System.String</span></span>

## <span data-ttu-id="9b16b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b16b-135">OUTPUTS</span></span>

### <span data-ttu-id="9b16b-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9b16b-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="9b16b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b16b-137">NOTES</span></span>

## <span data-ttu-id="9b16b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b16b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9b16b-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9b16b-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="9b16b-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9b16b-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="9b16b-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9b16b-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


