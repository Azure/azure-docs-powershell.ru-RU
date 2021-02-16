---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212164"
---
# <span data-ttu-id="81f33-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="81f33-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="81f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81f33-102">SYNOPSIS</span></span>
<span data-ttu-id="81f33-103">Удаляет API из продукта.</span><span class="sxs-lookup"><span data-stu-id="81f33-103">Removes an API from a product.</span></span>

## <span data-ttu-id="81f33-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="81f33-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81f33-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="81f33-105">DESCRIPTION</span></span>
<span data-ttu-id="81f33-106">Для удаления из продукта API управления Azure API удаляется cmdlet **Remove-AzApiManagementApiFromProduct.**</span><span class="sxs-lookup"><span data-stu-id="81f33-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="81f33-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="81f33-107">EXAMPLES</span></span>

### <span data-ttu-id="81f33-108">Пример 1. Удаление API из продукта</span><span class="sxs-lookup"><span data-stu-id="81f33-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="81f33-109">Эта команда удаляет указанный API из продукта.</span><span class="sxs-lookup"><span data-stu-id="81f33-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="81f33-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="81f33-110">PARAMETERS</span></span>

### <span data-ttu-id="81f33-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="81f33-111">-ApiId</span></span>
<span data-ttu-id="81f33-112">Определяет ИД API, который нужно удалить из продукта.</span><span class="sxs-lookup"><span data-stu-id="81f33-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="81f33-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="81f33-113">-Context</span></span>
<span data-ttu-id="81f33-114">Указывает **psApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="81f33-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="81f33-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81f33-115">-DefaultProfile</span></span>
<span data-ttu-id="81f33-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="81f33-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81f33-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81f33-117">-PassThru</span></span>
<span data-ttu-id="81f33-118">Указывает на то, что этот $True возвращает значение успешного $False.</span><span class="sxs-lookup"><span data-stu-id="81f33-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="81f33-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="81f33-119">-ProductId</span></span>
<span data-ttu-id="81f33-120">Определяет ИД продукта, из которого нужно удалить API.</span><span class="sxs-lookup"><span data-stu-id="81f33-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="81f33-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81f33-121">CommonParameters</span></span>
<span data-ttu-id="81f33-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81f33-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81f33-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81f33-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81f33-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="81f33-124">INPUTS</span></span>

### <span data-ttu-id="81f33-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="81f33-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="81f33-126">System.String</span><span class="sxs-lookup"><span data-stu-id="81f33-126">System.String</span></span>

### <span data-ttu-id="81f33-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81f33-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81f33-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="81f33-128">OUTPUTS</span></span>

### <span data-ttu-id="81f33-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="81f33-129">System.Boolean</span></span>

## <span data-ttu-id="81f33-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="81f33-130">NOTES</span></span>

## <span data-ttu-id="81f33-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="81f33-131">RELATED LINKS</span></span>

[<span data-ttu-id="81f33-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="81f33-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


