---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: 10b17f60ae100004c23a16f341924de6de11b0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556980"
---
# <span data-ttu-id="f260e-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f260e-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="f260e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f260e-102">SYNOPSIS</span></span>
<span data-ttu-id="f260e-103">Возвращает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="f260e-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f260e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f260e-104">SYNTAX</span></span>

### <span data-ttu-id="f260e-105">GetAllProducts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f260e-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f260e-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="f260e-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f260e-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="f260e-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f260e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f260e-108">DESCRIPTION</span></span>
<span data-ttu-id="f260e-109">Командлет **Get-AzureRmApiManagementProduct** получает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="f260e-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="f260e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f260e-110">EXAMPLES</span></span>

### <span data-ttu-id="f260e-111">Пример 1: получение всех продуктов</span><span class="sxs-lookup"><span data-stu-id="f260e-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="f260e-112">Эта команда возвращает все продукты для управления API.</span><span class="sxs-lookup"><span data-stu-id="f260e-112">This command get all API Management products.</span></span>

### <span data-ttu-id="f260e-113">Пример 2: получение продукта по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="f260e-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f260e-114">Эта команда получает продукт по управлению API по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="f260e-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="f260e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f260e-115">PARAMETERS</span></span>

### <span data-ttu-id="f260e-116">-Context</span><span class="sxs-lookup"><span data-stu-id="f260e-116">-Context</span></span>
<span data-ttu-id="f260e-117">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f260e-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f260e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f260e-118">-DefaultProfile</span></span>
<span data-ttu-id="f260e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f260e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f260e-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f260e-120">-ProductId</span></span>
<span data-ttu-id="f260e-121">Указывает идентификатор продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="f260e-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="f260e-122">-Title</span><span class="sxs-lookup"><span data-stu-id="f260e-122">-Title</span></span>
<span data-ttu-id="f260e-123">Указывает название продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="f260e-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="f260e-124">Если задано значение, командлет попытается получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="f260e-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="f260e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f260e-125">CommonParameters</span></span>
<span data-ttu-id="f260e-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f260e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f260e-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f260e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f260e-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f260e-128">INPUTS</span></span>

### <span data-ttu-id="f260e-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f260e-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f260e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f260e-130">System.String</span></span>

## <span data-ttu-id="f260e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f260e-131">OUTPUTS</span></span>

### <span data-ttu-id="f260e-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f260e-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="f260e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f260e-133">NOTES</span></span>

## <span data-ttu-id="f260e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f260e-134">RELATED LINKS</span></span>

[<span data-ttu-id="f260e-135">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f260e-135">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f260e-136">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f260e-136">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="f260e-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f260e-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


