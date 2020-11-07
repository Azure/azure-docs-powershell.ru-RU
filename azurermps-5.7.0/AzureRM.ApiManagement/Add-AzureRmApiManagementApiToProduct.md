---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733066"
---
# <span data-ttu-id="d1d25-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="d1d25-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="d1d25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1d25-102">SYNOPSIS</span></span>
<span data-ttu-id="d1d25-103">Добавляет API в продукт.</span><span class="sxs-lookup"><span data-stu-id="d1d25-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1d25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1d25-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1d25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1d25-105">DESCRIPTION</span></span>
<span data-ttu-id="d1d25-106">Командлет **Add-AzureRmApiManagementApiToProduct** добавляет API управления Azure API для продукта.</span><span class="sxs-lookup"><span data-stu-id="d1d25-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="d1d25-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1d25-107">EXAMPLES</span></span>

### <span data-ttu-id="d1d25-108">Пример 1: Добавление API для продукта</span><span class="sxs-lookup"><span data-stu-id="d1d25-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="d1d25-109">Эта команда добавляет указанный API к указанному продукту.</span><span class="sxs-lookup"><span data-stu-id="d1d25-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="d1d25-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1d25-110">PARAMETERS</span></span>

### <span data-ttu-id="d1d25-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d1d25-111">-ApiId</span></span>
<span data-ttu-id="d1d25-112">Указывает идентификатор API для добавления в продукт.</span><span class="sxs-lookup"><span data-stu-id="d1d25-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d25-113">-Context</span><span class="sxs-lookup"><span data-stu-id="d1d25-113">-Context</span></span>
<span data-ttu-id="d1d25-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d1d25-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d1d25-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1d25-115">-DefaultProfile</span></span>
<span data-ttu-id="d1d25-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1d25-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1d25-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d1d25-117">-PassThru</span></span>
<span data-ttu-id="d1d25-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="d1d25-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d25-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d1d25-119">-ProductId</span></span>
<span data-ttu-id="d1d25-120">Указывает идентификатор продукта, в который нужно добавить API.</span><span class="sxs-lookup"><span data-stu-id="d1d25-120">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1d25-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1d25-121">CommonParameters</span></span>
<span data-ttu-id="d1d25-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1d25-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1d25-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1d25-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1d25-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1d25-124">INPUTS</span></span>

### <span data-ttu-id="d1d25-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="d1d25-125">None</span></span>
<span data-ttu-id="d1d25-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="d1d25-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d1d25-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1d25-127">OUTPUTS</span></span>

### <span data-ttu-id="d1d25-128">Значением</span><span class="sxs-lookup"><span data-stu-id="d1d25-128">Boolean</span></span>

## <span data-ttu-id="d1d25-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1d25-129">NOTES</span></span>

## <span data-ttu-id="d1d25-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1d25-130">RELATED LINKS</span></span>

[<span data-ttu-id="d1d25-131">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="d1d25-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


