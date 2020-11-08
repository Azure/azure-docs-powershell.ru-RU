---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244643"
---
# <span data-ttu-id="bb162-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="bb162-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="bb162-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb162-102">SYNOPSIS</span></span>
<span data-ttu-id="bb162-103">Возвращает все или конкретные шлюзы управления API.</span><span class="sxs-lookup"><span data-stu-id="bb162-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="bb162-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb162-104">SYNTAX</span></span>

### <span data-ttu-id="bb162-105">GetAllGateways (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bb162-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bb162-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="bb162-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb162-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb162-107">DESCRIPTION</span></span>
<span data-ttu-id="bb162-108">Командлет **Get-AzApiManagementGateway** получает все или определенные шлюзы управления API.</span><span class="sxs-lookup"><span data-stu-id="bb162-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="bb162-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb162-109">EXAMPLES</span></span>

### <span data-ttu-id="bb162-110">Пример 1: получение всех шлюзов</span><span class="sxs-lookup"><span data-stu-id="bb162-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="bb162-111">Эта команда получает все шлюзы.</span><span class="sxs-lookup"><span data-stu-id="bb162-111">This command gets all gateways.</span></span>

### <span data-ttu-id="bb162-112">Пример 2: получение шлюза с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="bb162-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="bb162-113">Эта команда возвращает шлюз 0123456789.</span><span class="sxs-lookup"><span data-stu-id="bb162-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="bb162-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb162-114">PARAMETERS</span></span>

### <span data-ttu-id="bb162-115">-Context</span><span class="sxs-lookup"><span data-stu-id="bb162-115">-Context</span></span>
<span data-ttu-id="bb162-116">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bb162-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bb162-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="bb162-117">This parameter is required.</span></span>

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

### <span data-ttu-id="bb162-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb162-118">-DefaultProfile</span></span>
<span data-ttu-id="bb162-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb162-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb162-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="bb162-120">-GatewayId</span></span>
<span data-ttu-id="bb162-121">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="bb162-121">Identifier of a gateway.</span></span>
<span data-ttu-id="bb162-122">Если задано значение, это попытается найти шлюз по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="bb162-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="bb162-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb162-123">CommonParameters</span></span>
<span data-ttu-id="bb162-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb162-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb162-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bb162-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb162-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb162-126">INPUTS</span></span>

### <span data-ttu-id="bb162-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bb162-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bb162-128">System. String</span><span class="sxs-lookup"><span data-stu-id="bb162-128">System.String</span></span>

## <span data-ttu-id="bb162-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb162-129">OUTPUTS</span></span>

### <span data-ttu-id="bb162-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="bb162-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="bb162-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb162-131">NOTES</span></span>

## <span data-ttu-id="bb162-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb162-132">RELATED LINKS</span></span>
