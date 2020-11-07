---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720144"
---
# <span data-ttu-id="42c65-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42c65-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="42c65-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42c65-102">SYNOPSIS</span></span>
<span data-ttu-id="42c65-103">Возвращает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="42c65-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="42c65-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42c65-104">SYNTAX</span></span>

### <span data-ttu-id="42c65-105">GetAllProducts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42c65-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42c65-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="42c65-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42c65-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="42c65-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42c65-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c65-108">DESCRIPTION</span></span>
<span data-ttu-id="42c65-109">Командлет **Get-AzApiManagementProduct** получает список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="42c65-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="42c65-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42c65-110">EXAMPLES</span></span>

### <span data-ttu-id="42c65-111">Пример 1: получение всех продуктов</span><span class="sxs-lookup"><span data-stu-id="42c65-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="42c65-112">Эта команда возвращает все продукты для управления API.</span><span class="sxs-lookup"><span data-stu-id="42c65-112">This command get all API Management products.</span></span>

### <span data-ttu-id="42c65-113">Пример 2: получение продукта по ИДЕНТИФИКАТОРу</span><span class="sxs-lookup"><span data-stu-id="42c65-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="42c65-114">Эта команда получает продукт по управлению API по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="42c65-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="42c65-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42c65-115">PARAMETERS</span></span>

### <span data-ttu-id="42c65-116">-Context</span><span class="sxs-lookup"><span data-stu-id="42c65-116">-Context</span></span>
<span data-ttu-id="42c65-117">Указывает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="42c65-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="42c65-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c65-118">-DefaultProfile</span></span>
<span data-ttu-id="42c65-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42c65-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42c65-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="42c65-120">-ProductId</span></span>
<span data-ttu-id="42c65-121">Указывает идентификатор продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="42c65-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="42c65-122">-Title</span><span class="sxs-lookup"><span data-stu-id="42c65-122">-Title</span></span>
<span data-ttu-id="42c65-123">Указывает название продукта для поиска.</span><span class="sxs-lookup"><span data-stu-id="42c65-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="42c65-124">Если задано значение, командлет попытается получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="42c65-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="42c65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c65-125">CommonParameters</span></span>
<span data-ttu-id="42c65-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42c65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c65-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42c65-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42c65-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42c65-128">INPUTS</span></span>

### <span data-ttu-id="42c65-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="42c65-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="42c65-130">System. String</span><span class="sxs-lookup"><span data-stu-id="42c65-130">System.String</span></span>

## <span data-ttu-id="42c65-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42c65-131">OUTPUTS</span></span>

### <span data-ttu-id="42c65-132">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42c65-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="42c65-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="42c65-133">NOTES</span></span>

## <span data-ttu-id="42c65-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42c65-134">RELATED LINKS</span></span>

[<span data-ttu-id="42c65-135">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42c65-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="42c65-136">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42c65-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="42c65-137">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="42c65-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


