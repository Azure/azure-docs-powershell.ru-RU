---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 16bb651efd13d42b25509834637faea866678459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733925"
---
# <span data-ttu-id="01f2c-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="01f2c-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="01f2c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01f2c-102">SYNOPSIS</span></span>
<span data-ttu-id="01f2c-103">Добавляет API в продукт.</span><span class="sxs-lookup"><span data-stu-id="01f2c-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f2c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01f2c-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01f2c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01f2c-105">DESCRIPTION</span></span>
<span data-ttu-id="01f2c-106">Командлет **Add-AzureRmApiManagementApiToProduct** добавляет API управления Azure API для продукта.</span><span class="sxs-lookup"><span data-stu-id="01f2c-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="01f2c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01f2c-107">EXAMPLES</span></span>

### <span data-ttu-id="01f2c-108">Пример 1: Добавление API для продукта</span><span class="sxs-lookup"><span data-stu-id="01f2c-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="01f2c-109">Эта команда добавляет указанный API к указанному продукту.</span><span class="sxs-lookup"><span data-stu-id="01f2c-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="01f2c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01f2c-110">PARAMETERS</span></span>

### <span data-ttu-id="01f2c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="01f2c-111">-ApiId</span></span>
<span data-ttu-id="01f2c-112">Указывает идентификатор API для добавления в продукт.</span><span class="sxs-lookup"><span data-stu-id="01f2c-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="01f2c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="01f2c-113">-Context</span></span>
<span data-ttu-id="01f2c-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="01f2c-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="01f2c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f2c-115">-DefaultProfile</span></span>
<span data-ttu-id="01f2c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01f2c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f2c-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01f2c-117">-PassThru</span></span>
<span data-ttu-id="01f2c-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="01f2c-118">passthru</span></span>

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

### <span data-ttu-id="01f2c-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="01f2c-119">-ProductId</span></span>
<span data-ttu-id="01f2c-120">Указывает идентификатор продукта, в который нужно добавить API.</span><span class="sxs-lookup"><span data-stu-id="01f2c-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="01f2c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f2c-121">CommonParameters</span></span>
<span data-ttu-id="01f2c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01f2c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f2c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f2c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f2c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01f2c-124">INPUTS</span></span>

### <span data-ttu-id="01f2c-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01f2c-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01f2c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="01f2c-126">System.String</span></span>

### <span data-ttu-id="01f2c-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="01f2c-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="01f2c-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01f2c-128">OUTPUTS</span></span>

### <span data-ttu-id="01f2c-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01f2c-129">System.Boolean</span></span>

## <span data-ttu-id="01f2c-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="01f2c-130">NOTES</span></span>

## <span data-ttu-id="01f2c-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01f2c-131">RELATED LINKS</span></span>

[<span data-ttu-id="01f2c-132">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="01f2c-132">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


