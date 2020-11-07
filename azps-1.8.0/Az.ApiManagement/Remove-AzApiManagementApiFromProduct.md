---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 34631b2f1ac68e5f58c6269fa473dcf3d9103c7f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901690"
---
# <span data-ttu-id="f621c-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="f621c-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="f621c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f621c-102">SYNOPSIS</span></span>
<span data-ttu-id="f621c-103">Удаляет API из продукта.</span><span class="sxs-lookup"><span data-stu-id="f621c-103">Removes an API from a product.</span></span>

## <span data-ttu-id="f621c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f621c-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f621c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f621c-105">DESCRIPTION</span></span>
<span data-ttu-id="f621c-106">Командлет **Remove-AzApiManagementApiFromProduct** удаляет API Azure API Management из продукта.</span><span class="sxs-lookup"><span data-stu-id="f621c-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="f621c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f621c-107">EXAMPLES</span></span>

### <span data-ttu-id="f621c-108">Пример 1: удаление API из продукта</span><span class="sxs-lookup"><span data-stu-id="f621c-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="f621c-109">Этот commnd удаляет указанный API из продукта.</span><span class="sxs-lookup"><span data-stu-id="f621c-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="f621c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f621c-110">PARAMETERS</span></span>

### <span data-ttu-id="f621c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f621c-111">-ApiId</span></span>
<span data-ttu-id="f621c-112">Указывает идентификатор API для удаления из продукта.</span><span class="sxs-lookup"><span data-stu-id="f621c-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="f621c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f621c-113">-Context</span></span>
<span data-ttu-id="f621c-114">Указывает **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f621c-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f621c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f621c-115">-DefaultProfile</span></span>
<span data-ttu-id="f621c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f621c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f621c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f621c-117">-PassThru</span></span>
<span data-ttu-id="f621c-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f621c-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f621c-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f621c-119">-ProductId</span></span>
<span data-ttu-id="f621c-120">Указывает идентификатор продукта, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="f621c-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="f621c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f621c-121">CommonParameters</span></span>
<span data-ttu-id="f621c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f621c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f621c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f621c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f621c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f621c-124">INPUTS</span></span>

### <span data-ttu-id="f621c-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f621c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f621c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f621c-126">System.String</span></span>

### <span data-ttu-id="f621c-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f621c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f621c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f621c-128">OUTPUTS</span></span>

### <span data-ttu-id="f621c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f621c-129">System.Boolean</span></span>

## <span data-ttu-id="f621c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f621c-130">NOTES</span></span>

## <span data-ttu-id="f621c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f621c-131">RELATED LINKS</span></span>

[<span data-ttu-id="f621c-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="f621c-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


