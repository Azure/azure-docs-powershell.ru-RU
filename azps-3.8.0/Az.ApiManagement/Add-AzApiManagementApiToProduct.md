---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073948"
---
# <span data-ttu-id="4cc3a-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="4cc3a-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="4cc3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4cc3a-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc3a-103">Добавляет API в продукт.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-103">Adds an API to a product.</span></span>

## <span data-ttu-id="4cc3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4cc3a-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc3a-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc3a-106">Командлет **Add-AzApiManagementApiToProduct** добавляет API управления Azure API для продукта.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="4cc3a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4cc3a-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc3a-108">Пример 1: Добавление API для продукта</span><span class="sxs-lookup"><span data-stu-id="4cc3a-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="4cc3a-109">Эта команда добавляет указанный API к указанному продукту.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="4cc3a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4cc3a-110">PARAMETERS</span></span>

### <span data-ttu-id="4cc3a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4cc3a-111">-ApiId</span></span>
<span data-ttu-id="4cc3a-112">Указывает идентификатор API для добавления в продукт.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="4cc3a-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4cc3a-113">-Context</span></span>
<span data-ttu-id="4cc3a-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4cc3a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4cc3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc3a-115">-DefaultProfile</span></span>
<span data-ttu-id="4cc3a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc3a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4cc3a-117">-PassThru</span></span>
<span data-ttu-id="4cc3a-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="4cc3a-118">passthru</span></span>

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

### <span data-ttu-id="4cc3a-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4cc3a-119">-ProductId</span></span>
<span data-ttu-id="4cc3a-120">Указывает идентификатор продукта, в который нужно добавить API.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="4cc3a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc3a-121">CommonParameters</span></span>
<span data-ttu-id="4cc3a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4cc3a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc3a-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cc3a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc3a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4cc3a-124">INPUTS</span></span>

### <span data-ttu-id="4cc3a-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cc3a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cc3a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="4cc3a-126">System.String</span></span>

### <span data-ttu-id="4cc3a-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4cc3a-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4cc3a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4cc3a-128">OUTPUTS</span></span>

### <span data-ttu-id="4cc3a-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cc3a-129">System.Boolean</span></span>

## <span data-ttu-id="4cc3a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="4cc3a-130">NOTES</span></span>

## <span data-ttu-id="4cc3a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4cc3a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4cc3a-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="4cc3a-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


