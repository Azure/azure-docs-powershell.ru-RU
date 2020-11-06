---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 413d03723ee2acdc162c1f1f5501d90156e16069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569096"
---
# <span data-ttu-id="a8822-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="a8822-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="a8822-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8822-102">SYNOPSIS</span></span>
<span data-ttu-id="a8822-103">Удаляет API из продукта.</span><span class="sxs-lookup"><span data-stu-id="a8822-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8822-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8822-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8822-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8822-105">DESCRIPTION</span></span>
<span data-ttu-id="a8822-106">Командлет **Remove-AzureRmApiManagementApiFromProduct** удаляет API Azure API Management из продукта.</span><span class="sxs-lookup"><span data-stu-id="a8822-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="a8822-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8822-107">EXAMPLES</span></span>

### <span data-ttu-id="a8822-108">Пример 1: удаление API из продукта</span><span class="sxs-lookup"><span data-stu-id="a8822-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="a8822-109">Этот commnd удаляет указанный API из продукта.</span><span class="sxs-lookup"><span data-stu-id="a8822-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="a8822-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8822-110">PARAMETERS</span></span>

### <span data-ttu-id="a8822-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a8822-111">-ApiId</span></span>
<span data-ttu-id="a8822-112">Указывает идентификатор API для удаления из продукта.</span><span class="sxs-lookup"><span data-stu-id="a8822-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="a8822-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a8822-113">-Context</span></span>
<span data-ttu-id="a8822-114">Указывает **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="a8822-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a8822-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8822-115">-DefaultProfile</span></span>
<span data-ttu-id="a8822-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a8822-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="a8822-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8822-117">-PassThru</span></span>
<span data-ttu-id="a8822-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a8822-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="a8822-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a8822-119">-ProductId</span></span>
<span data-ttu-id="a8822-120">Указывает идентификатор продукта, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="a8822-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="a8822-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8822-121">CommonParameters</span></span>
<span data-ttu-id="a8822-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8822-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8822-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8822-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8822-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8822-124">INPUTS</span></span>

### <span data-ttu-id="a8822-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="a8822-125">None</span></span>
<span data-ttu-id="a8822-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a8822-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a8822-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8822-127">OUTPUTS</span></span>

### <span data-ttu-id="a8822-128">логических</span><span class="sxs-lookup"><span data-stu-id="a8822-128">bool</span></span>

## <span data-ttu-id="a8822-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8822-129">NOTES</span></span>

## <span data-ttu-id="a8822-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8822-130">RELATED LINKS</span></span>

[<span data-ttu-id="a8822-131">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="a8822-131">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


