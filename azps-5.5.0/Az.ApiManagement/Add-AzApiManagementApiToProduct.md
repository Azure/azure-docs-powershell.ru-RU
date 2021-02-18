---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239912"
---
# <span data-ttu-id="b4ab5-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="b4ab5-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="b4ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="b4ab5-103">Добавляет API в продукт.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-103">Adds an API to a product.</span></span>

## <span data-ttu-id="b4ab5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b4ab5-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4ab5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="b4ab5-106">Cmdlet **Add-AzApiManagementApiToProduct** добавляет к продукту API управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="b4ab5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b4ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="b4ab5-108">Пример 1. Добавление API в продукт</span><span class="sxs-lookup"><span data-stu-id="b4ab5-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="b4ab5-109">Эта команда добавляет указанный API в указанный продукт.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="b4ab5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b4ab5-110">PARAMETERS</span></span>

### <span data-ttu-id="b4ab5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b4ab5-111">-ApiId</span></span>
<span data-ttu-id="b4ab5-112">Определяет ИД API, который нужно добавить в продукт.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="b4ab5-113">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b4ab5-113">-Context</span></span>
<span data-ttu-id="b4ab5-114">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="b4ab5-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b4ab5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4ab5-115">-DefaultProfile</span></span>
<span data-ttu-id="b4ab5-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b4ab5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b4ab5-117">-PassThru</span></span>
<span data-ttu-id="b4ab5-118">passthru</span><span class="sxs-lookup"><span data-stu-id="b4ab5-118">passthru</span></span>

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

### <span data-ttu-id="b4ab5-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b4ab5-119">-ProductId</span></span>
<span data-ttu-id="b4ab5-120">Определяет ИД продукта, к которому нужно добавить API.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="b4ab5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4ab5-121">CommonParameters</span></span>
<span data-ttu-id="b4ab5-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4ab5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4ab5-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b4ab5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4ab5-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b4ab5-124">INPUTS</span></span>

### <span data-ttu-id="b4ab5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b4ab5-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b4ab5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b4ab5-126">System.String</span></span>

### <span data-ttu-id="b4ab5-127">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b4ab5-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b4ab5-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b4ab5-128">OUTPUTS</span></span>

### <span data-ttu-id="b4ab5-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b4ab5-129">System.Boolean</span></span>

## <span data-ttu-id="b4ab5-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b4ab5-130">NOTES</span></span>

## <span data-ttu-id="b4ab5-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4ab5-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4ab5-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="b4ab5-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


