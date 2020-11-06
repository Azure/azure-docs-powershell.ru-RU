---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 4bed4b5022292639a5bc55e30fdd8de356dc818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565964"
---
# <span data-ttu-id="31483-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="31483-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="31483-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31483-102">SYNOPSIS</span></span>
<span data-ttu-id="31483-103">Удаляет API из продукта.</span><span class="sxs-lookup"><span data-stu-id="31483-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31483-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31483-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31483-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31483-105">DESCRIPTION</span></span>
<span data-ttu-id="31483-106">Командлет **Remove-AzureRmApiManagementApiFromProduct** удаляет API Azure API Management из продукта.</span><span class="sxs-lookup"><span data-stu-id="31483-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="31483-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31483-107">EXAMPLES</span></span>

### <span data-ttu-id="31483-108">Пример 1: удаление API из продукта</span><span class="sxs-lookup"><span data-stu-id="31483-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="31483-109">Этот commnd удаляет указанный API из продукта.</span><span class="sxs-lookup"><span data-stu-id="31483-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="31483-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31483-110">PARAMETERS</span></span>

### <span data-ttu-id="31483-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="31483-111">-ApiId</span></span>
<span data-ttu-id="31483-112">Указывает идентификатор API для удаления из продукта.</span><span class="sxs-lookup"><span data-stu-id="31483-112">Specifies the ID of the API to remove from the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31483-113">-Context</span><span class="sxs-lookup"><span data-stu-id="31483-113">-Context</span></span>
<span data-ttu-id="31483-114">Указывает **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="31483-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="31483-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31483-115">-DefaultProfile</span></span>
<span data-ttu-id="31483-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="31483-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31483-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31483-117">-PassThru</span></span>
<span data-ttu-id="31483-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="31483-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31483-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="31483-119">-ProductId</span></span>
<span data-ttu-id="31483-120">Указывает идентификатор продукта, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="31483-120">Specifies the ID of the product from which to remove the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31483-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31483-121">CommonParameters</span></span>
<span data-ttu-id="31483-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31483-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31483-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31483-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31483-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31483-124">INPUTS</span></span>

### <span data-ttu-id="31483-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="31483-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="31483-126">System. String</span><span class="sxs-lookup"><span data-stu-id="31483-126">System.String</span></span>

### <span data-ttu-id="31483-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="31483-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="31483-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31483-128">OUTPUTS</span></span>

### <span data-ttu-id="31483-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="31483-129">System.Boolean</span></span>

## <span data-ttu-id="31483-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="31483-130">NOTES</span></span>

## <span data-ttu-id="31483-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31483-131">RELATED LINKS</span></span>

[<span data-ttu-id="31483-132">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="31483-132">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


