---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563800"
---
# <span data-ttu-id="e51e7-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e51e7-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e51e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e51e7-102">SYNOPSIS</span></span>
<span data-ttu-id="e51e7-103">Возвращает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="e51e7-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e51e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e51e7-104">SYNTAX</span></span>

### <span data-ttu-id="e51e7-105">GetAllProducts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e51e7-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e51e7-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e51e7-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e51e7-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="e51e7-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51e7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e51e7-108">DESCRIPTION</span></span>
<span data-ttu-id="e51e7-109">Командлет **Get-AzureRmApiManagementProduct** получает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="e51e7-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="e51e7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e51e7-110">EXAMPLES</span></span>

### <span data-ttu-id="e51e7-111">Пример 1: получение всех продуктов</span><span class="sxs-lookup"><span data-stu-id="e51e7-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="e51e7-112">Эта команда возвращает все продукты для управления API.</span><span class="sxs-lookup"><span data-stu-id="e51e7-112">This command get all API Management products.</span></span>

### <span data-ttu-id="e51e7-113">Пример 2: получение продукта по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="e51e7-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="e51e7-114">Эта команда получает продукт по управлению API по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="e51e7-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="e51e7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e51e7-115">PARAMETERS</span></span>

### <span data-ttu-id="e51e7-116">-Context</span><span class="sxs-lookup"><span data-stu-id="e51e7-116">-Context</span></span>
<span data-ttu-id="e51e7-117">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e51e7-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e51e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51e7-118">-DefaultProfile</span></span>
<span data-ttu-id="e51e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e51e7-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e51e7-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e51e7-120">-ProductId</span></span>
<span data-ttu-id="e51e7-121">Указывает идентификатор продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="e51e7-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51e7-122">-Title</span><span class="sxs-lookup"><span data-stu-id="e51e7-122">-Title</span></span>
<span data-ttu-id="e51e7-123">Указывает название продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="e51e7-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="e51e7-124">Если задано значение, командлет попытается получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="e51e7-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e51e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51e7-125">CommonParameters</span></span>
<span data-ttu-id="e51e7-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e51e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51e7-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e51e7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51e7-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e51e7-128">INPUTS</span></span>

### <span data-ttu-id="e51e7-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="e51e7-129">None</span></span>
<span data-ttu-id="e51e7-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e51e7-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e51e7-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e51e7-131">OUTPUTS</span></span>

### <span data-ttu-id="e51e7-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e51e7-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="e51e7-133">Сведения о продукте в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="e51e7-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="e51e7-134">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="e51e7-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="e51e7-135">Список продуктов в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="e51e7-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="e51e7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="e51e7-136">NOTES</span></span>

## <span data-ttu-id="e51e7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e51e7-137">RELATED LINKS</span></span>

[<span data-ttu-id="e51e7-138">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e51e7-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e51e7-139">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e51e7-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e51e7-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e51e7-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


