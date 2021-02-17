---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221785"
---
# <span data-ttu-id="8bd5e-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8bd5e-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="8bd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd5e-103">Возвращает список или определенный продукт.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="8bd5e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8bd5e-104">SYNTAX</span></span>

### <span data-ttu-id="8bd5e-105">GetAllProducts (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8bd5e-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bd5e-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="8bd5e-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bd5e-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="8bd5e-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8bd5e-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="8bd5e-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bd5e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bd5e-109">DESCRIPTION</span></span>
<span data-ttu-id="8bd5e-110">Чтобы **получить список или определенный** продукт, можно получить список или конкретный продукт.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="8bd5e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8bd5e-111">EXAMPLES</span></span>

### <span data-ttu-id="8bd5e-112">Пример 1. Получить все продукты</span><span class="sxs-lookup"><span data-stu-id="8bd5e-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="8bd5e-113">Эта команда получит все продукты управления API.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-113">This command get all API Management products.</span></span>

### <span data-ttu-id="8bd5e-114">Пример 2. Получить продукт по ИД</span><span class="sxs-lookup"><span data-stu-id="8bd5e-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="8bd5e-115">Эта команда получит продукт для управления API по ИД.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="8bd5e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8bd5e-116">PARAMETERS</span></span>

### <span data-ttu-id="8bd5e-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8bd5e-117">-ApiId</span></span>
<span data-ttu-id="8bd5e-118">ApiId Api для поиска корреляции продуктов.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="8bd5e-119">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="8bd5e-120">-Контекст</span><span class="sxs-lookup"><span data-stu-id="8bd5e-120">-Context</span></span>
<span data-ttu-id="8bd5e-121">Указывает экземпляр объекта **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8bd5e-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8bd5e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd5e-122">-DefaultProfile</span></span>
<span data-ttu-id="8bd5e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8bd5e-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8bd5e-124">-ProductId</span></span>
<span data-ttu-id="8bd5e-125">Определяет идентификатор продукта, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="8bd5e-126">-Title</span><span class="sxs-lookup"><span data-stu-id="8bd5e-126">-Title</span></span>
<span data-ttu-id="8bd5e-127">Название продукта, который нужно найти.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="8bd5e-128">При этом будет предпринята попытка получить продукт по заголовку.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="8bd5e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd5e-129">CommonParameters</span></span>
<span data-ttu-id="8bd5e-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd5e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd5e-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8bd5e-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd5e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8bd5e-132">INPUTS</span></span>

### <span data-ttu-id="8bd5e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8bd5e-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8bd5e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="8bd5e-134">System.String</span></span>

## <span data-ttu-id="8bd5e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8bd5e-135">OUTPUTS</span></span>

### <span data-ttu-id="8bd5e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8bd5e-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="8bd5e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8bd5e-137">NOTES</span></span>

## <span data-ttu-id="8bd5e-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bd5e-138">RELATED LINKS</span></span>

[<span data-ttu-id="8bd5e-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8bd5e-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="8bd5e-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8bd5e-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="8bd5e-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8bd5e-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


