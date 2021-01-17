---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324550"
---
# <span data-ttu-id="4129f-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4129f-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="4129f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4129f-102">SYNOPSIS</span></span>
<span data-ttu-id="4129f-103">Возвращает весь или конкретный шлюз управления API.</span><span class="sxs-lookup"><span data-stu-id="4129f-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="4129f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4129f-104">SYNTAX</span></span>

### <span data-ttu-id="4129f-105">GetAllGateways (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4129f-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4129f-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="4129f-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4129f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4129f-107">DESCRIPTION</span></span>
<span data-ttu-id="4129f-108">Для получения всего или отдельного шлюза управления API возвращается **cmdlet Get-AzApiManagementGateway.**</span><span class="sxs-lookup"><span data-stu-id="4129f-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="4129f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4129f-109">EXAMPLES</span></span>

### <span data-ttu-id="4129f-110">Пример 1. Получить все шлюзы</span><span class="sxs-lookup"><span data-stu-id="4129f-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="4129f-111">Эта команда возвращает все шлюзы.</span><span class="sxs-lookup"><span data-stu-id="4129f-111">This command gets all gateways.</span></span>

### <span data-ttu-id="4129f-112">Пример 2. Получить шлюз по ИД</span><span class="sxs-lookup"><span data-stu-id="4129f-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="4129f-113">Эта команда возвращает шлюз 0123456789.</span><span class="sxs-lookup"><span data-stu-id="4129f-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="4129f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4129f-114">PARAMETERS</span></span>

### <span data-ttu-id="4129f-115">-Контекст</span><span class="sxs-lookup"><span data-stu-id="4129f-115">-Context</span></span>
<span data-ttu-id="4129f-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4129f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4129f-117">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="4129f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="4129f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4129f-118">-DefaultProfile</span></span>
<span data-ttu-id="4129f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4129f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4129f-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="4129f-120">-GatewayId</span></span>
<span data-ttu-id="4129f-121">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="4129f-121">Identifier of a gateway.</span></span>
<span data-ttu-id="4129f-122">Если он указан, будет пытаться найти шлюз по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="4129f-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="4129f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4129f-123">CommonParameters</span></span>
<span data-ttu-id="4129f-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4129f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4129f-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4129f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4129f-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4129f-126">INPUTS</span></span>

### <span data-ttu-id="4129f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4129f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4129f-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4129f-128">System.String</span></span>

## <span data-ttu-id="4129f-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4129f-129">OUTPUTS</span></span>

### <span data-ttu-id="4129f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="4129f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="4129f-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4129f-131">NOTES</span></span>

## <span data-ttu-id="4129f-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4129f-132">RELATED LINKS</span></span>
