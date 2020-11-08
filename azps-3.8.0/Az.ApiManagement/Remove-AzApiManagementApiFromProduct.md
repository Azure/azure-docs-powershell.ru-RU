---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072904"
---
# <span data-ttu-id="8e646-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="8e646-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="8e646-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e646-102">SYNOPSIS</span></span>
<span data-ttu-id="8e646-103">Удаляет API из продукта.</span><span class="sxs-lookup"><span data-stu-id="8e646-103">Removes an API from a product.</span></span>

## <span data-ttu-id="8e646-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e646-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e646-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e646-105">DESCRIPTION</span></span>
<span data-ttu-id="8e646-106">Командлет **Remove-AzApiManagementApiFromProduct** удаляет API Azure API Management из продукта.</span><span class="sxs-lookup"><span data-stu-id="8e646-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="8e646-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e646-107">EXAMPLES</span></span>

### <span data-ttu-id="8e646-108">Пример 1: удаление API из продукта</span><span class="sxs-lookup"><span data-stu-id="8e646-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="8e646-109">Эта команда удаляет указанный API из продукта.</span><span class="sxs-lookup"><span data-stu-id="8e646-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="8e646-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e646-110">PARAMETERS</span></span>

### <span data-ttu-id="8e646-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8e646-111">-ApiId</span></span>
<span data-ttu-id="8e646-112">Указывает идентификатор API для удаления из продукта.</span><span class="sxs-lookup"><span data-stu-id="8e646-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="8e646-113">-Context</span><span class="sxs-lookup"><span data-stu-id="8e646-113">-Context</span></span>
<span data-ttu-id="8e646-114">Указывает **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="8e646-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="8e646-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e646-115">-DefaultProfile</span></span>
<span data-ttu-id="8e646-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e646-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e646-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e646-117">-PassThru</span></span>
<span data-ttu-id="8e646-118">Указывает на то, что этот командлет возвращает значение $True, если оно прошло успешно, или $False, в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8e646-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="8e646-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8e646-119">-ProductId</span></span>
<span data-ttu-id="8e646-120">Указывает идентификатор продукта, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="8e646-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="8e646-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e646-121">CommonParameters</span></span>
<span data-ttu-id="8e646-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e646-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e646-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e646-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e646-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e646-124">INPUTS</span></span>

### <span data-ttu-id="8e646-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e646-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e646-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8e646-126">System.String</span></span>

### <span data-ttu-id="8e646-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e646-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8e646-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e646-128">OUTPUTS</span></span>

### <span data-ttu-id="8e646-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e646-129">System.Boolean</span></span>

## <span data-ttu-id="8e646-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e646-130">NOTES</span></span>

## <span data-ttu-id="8e646-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e646-131">RELATED LINKS</span></span>

[<span data-ttu-id="8e646-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="8e646-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


