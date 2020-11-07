---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 8676a90e533217fe291e47fce40ffbd43929031a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728146"
---
# <span data-ttu-id="5608f-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="5608f-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="5608f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5608f-102">SYNOPSIS</span></span>
<span data-ttu-id="5608f-103">Добавляет API в продукт.</span><span class="sxs-lookup"><span data-stu-id="5608f-103">Adds an API to a product.</span></span>

## <span data-ttu-id="5608f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5608f-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5608f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5608f-105">DESCRIPTION</span></span>
<span data-ttu-id="5608f-106">Командлет **Add-AzApiManagementApiToProduct** добавляет API управления Azure API для продукта.</span><span class="sxs-lookup"><span data-stu-id="5608f-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="5608f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5608f-107">EXAMPLES</span></span>

### <span data-ttu-id="5608f-108">Пример 1: Добавление API для продукта</span><span class="sxs-lookup"><span data-stu-id="5608f-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="5608f-109">Эта команда добавляет указанный API к указанному продукту.</span><span class="sxs-lookup"><span data-stu-id="5608f-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="5608f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5608f-110">PARAMETERS</span></span>

### <span data-ttu-id="5608f-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5608f-111">-ApiId</span></span>
<span data-ttu-id="5608f-112">Указывает идентификатор API для добавления в продукт.</span><span class="sxs-lookup"><span data-stu-id="5608f-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="5608f-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5608f-113">-Context</span></span>
<span data-ttu-id="5608f-114">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5608f-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5608f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5608f-115">-DefaultProfile</span></span>
<span data-ttu-id="5608f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5608f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5608f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5608f-117">-PassThru</span></span>
<span data-ttu-id="5608f-118">PassThru</span><span class="sxs-lookup"><span data-stu-id="5608f-118">passthru</span></span>

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

### <span data-ttu-id="5608f-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5608f-119">-ProductId</span></span>
<span data-ttu-id="5608f-120">Указывает идентификатор продукта, в который нужно добавить API.</span><span class="sxs-lookup"><span data-stu-id="5608f-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="5608f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5608f-121">CommonParameters</span></span>
<span data-ttu-id="5608f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5608f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5608f-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5608f-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5608f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5608f-124">INPUTS</span></span>

### <span data-ttu-id="5608f-125">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5608f-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5608f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5608f-126">System.String</span></span>

### <span data-ttu-id="5608f-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5608f-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5608f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5608f-128">OUTPUTS</span></span>

### <span data-ttu-id="5608f-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5608f-129">System.Boolean</span></span>

## <span data-ttu-id="5608f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="5608f-130">NOTES</span></span>

## <span data-ttu-id="5608f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5608f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5608f-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="5608f-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


