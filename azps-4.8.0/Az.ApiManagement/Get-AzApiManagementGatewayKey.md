---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079897"
---
# <span data-ttu-id="3284a-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3284a-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="3284a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3284a-102">SYNOPSIS</span></span>
<span data-ttu-id="3284a-103">Возвращает ключи существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="3284a-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="3284a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3284a-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3284a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3284a-105">DESCRIPTION</span></span>
<span data-ttu-id="3284a-106">Командлет **Get-AzApiManagementGatewayKey** получает ключи из существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="3284a-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="3284a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3284a-107">EXAMPLES</span></span>

### <span data-ttu-id="3284a-108">Пример 2: получение шлюза с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="3284a-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="3284a-109">Эта команда возвращает клавиши для шлюза "0123456789".</span><span class="sxs-lookup"><span data-stu-id="3284a-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="3284a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3284a-110">PARAMETERS</span></span>

### <span data-ttu-id="3284a-111">-Context</span><span class="sxs-lookup"><span data-stu-id="3284a-111">-Context</span></span>
<span data-ttu-id="3284a-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="3284a-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="3284a-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3284a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="3284a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3284a-114">-DefaultProfile</span></span>
<span data-ttu-id="3284a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3284a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3284a-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="3284a-116">-GatewayId</span></span>
<span data-ttu-id="3284a-117">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="3284a-117">Gateway identifier.</span></span>
<span data-ttu-id="3284a-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="3284a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="3284a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3284a-119">CommonParameters</span></span>
<span data-ttu-id="3284a-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3284a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3284a-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3284a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3284a-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3284a-122">INPUTS</span></span>

### <span data-ttu-id="3284a-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3284a-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3284a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="3284a-124">System.String</span></span>

## <span data-ttu-id="3284a-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3284a-125">OUTPUTS</span></span>

### <span data-ttu-id="3284a-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="3284a-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="3284a-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3284a-127">NOTES</span></span>

## <span data-ttu-id="3284a-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3284a-128">RELATED LINKS</span></span>
