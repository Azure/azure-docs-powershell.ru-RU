---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516614"
---
# <span data-ttu-id="b19ef-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b19ef-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="b19ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b19ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b19ef-103">Возвращает весь или конкретный шлюз управления API.</span><span class="sxs-lookup"><span data-stu-id="b19ef-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="b19ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b19ef-104">SYNTAX</span></span>

### <span data-ttu-id="b19ef-105">GetAllGateways (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b19ef-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b19ef-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="b19ef-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b19ef-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b19ef-107">DESCRIPTION</span></span>
<span data-ttu-id="b19ef-108">Для получения всего или отдельного шлюза управления API возвращается **cmdlet Get-AzApiManagementGateway.**</span><span class="sxs-lookup"><span data-stu-id="b19ef-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="b19ef-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b19ef-109">EXAMPLES</span></span>

### <span data-ttu-id="b19ef-110">Пример 1. Получить все шлюзы</span><span class="sxs-lookup"><span data-stu-id="b19ef-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="b19ef-111">Эта команда возвращает все шлюзы.</span><span class="sxs-lookup"><span data-stu-id="b19ef-111">This command gets all gateways.</span></span>

### <span data-ttu-id="b19ef-112">Пример 2. Получить шлюз по ИД</span><span class="sxs-lookup"><span data-stu-id="b19ef-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="b19ef-113">Эта команда возвращает шлюз 0123456789.</span><span class="sxs-lookup"><span data-stu-id="b19ef-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="b19ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b19ef-114">PARAMETERS</span></span>

### <span data-ttu-id="b19ef-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="b19ef-115">-Context</span></span>
<span data-ttu-id="b19ef-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b19ef-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b19ef-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="b19ef-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b19ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b19ef-118">-DefaultProfile</span></span>
<span data-ttu-id="b19ef-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b19ef-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b19ef-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b19ef-120">-GatewayId</span></span>
<span data-ttu-id="b19ef-121">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="b19ef-121">Identifier of a gateway.</span></span>
<span data-ttu-id="b19ef-122">Если он указан, будет пытаться найти шлюз по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="b19ef-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b19ef-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b19ef-123">CommonParameters</span></span>
<span data-ttu-id="b19ef-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b19ef-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b19ef-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b19ef-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b19ef-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b19ef-126">INPUTS</span></span>

### <span data-ttu-id="b19ef-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b19ef-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b19ef-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b19ef-128">System.String</span></span>

## <span data-ttu-id="b19ef-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b19ef-129">OUTPUTS</span></span>

### <span data-ttu-id="b19ef-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b19ef-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="b19ef-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b19ef-131">NOTES</span></span>

## <span data-ttu-id="b19ef-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b19ef-132">RELATED LINKS</span></span>
