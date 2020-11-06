---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565753"
---
# <span data-ttu-id="96610-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="96610-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="96610-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96610-102">SYNOPSIS</span></span>
<span data-ttu-id="96610-103">Возвращает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="96610-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96610-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96610-104">SYNTAX</span></span>

### <span data-ttu-id="96610-105">Получить все producst (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96610-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="96610-106">Получить по идентификатору</span><span class="sxs-lookup"><span data-stu-id="96610-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96610-107">Получить по названию</span><span class="sxs-lookup"><span data-stu-id="96610-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96610-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96610-108">DESCRIPTION</span></span>
<span data-ttu-id="96610-109">Командлет **Get-AzureRmApiManagementProduct** получает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="96610-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="96610-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96610-110">EXAMPLES</span></span>

### <span data-ttu-id="96610-111">Пример 1: получение всех продуктов</span><span class="sxs-lookup"><span data-stu-id="96610-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="96610-112">Эта команда возвращает все продукты для управления API.</span><span class="sxs-lookup"><span data-stu-id="96610-112">This command get all API Management products.</span></span>

### <span data-ttu-id="96610-113">Пример 2: получение продукта по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="96610-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="96610-114">Эта команда получает продукт по управлению API по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="96610-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="96610-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96610-115">PARAMETERS</span></span>

### <span data-ttu-id="96610-116">-Context</span><span class="sxs-lookup"><span data-stu-id="96610-116">-Context</span></span>
<span data-ttu-id="96610-117">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="96610-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="96610-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="96610-118">-ProductId</span></span>
<span data-ttu-id="96610-119">Указывает идентификатор продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="96610-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96610-120">-Title</span><span class="sxs-lookup"><span data-stu-id="96610-120">-Title</span></span>
<span data-ttu-id="96610-121">Указывает название продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="96610-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="96610-122">Если задано значение, командлет попытается получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="96610-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96610-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96610-123">-DefaultProfile</span></span>
<span data-ttu-id="96610-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96610-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96610-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96610-125">CommonParameters</span></span>
<span data-ttu-id="96610-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96610-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96610-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96610-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96610-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96610-128">INPUTS</span></span>

## <span data-ttu-id="96610-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96610-129">OUTPUTS</span></span>

### <span data-ttu-id="96610-130">IList<Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="96610-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="96610-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="96610-131">NOTES</span></span>

## <span data-ttu-id="96610-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96610-132">RELATED LINKS</span></span>

[<span data-ttu-id="96610-133">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="96610-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="96610-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="96610-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="96610-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="96610-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


