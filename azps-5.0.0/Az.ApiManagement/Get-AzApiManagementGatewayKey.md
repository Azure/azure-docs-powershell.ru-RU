---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315410"
---
# <span data-ttu-id="db294-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="db294-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="db294-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db294-102">SYNOPSIS</span></span>
<span data-ttu-id="db294-103">Возвращает ключи существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="db294-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="db294-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db294-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db294-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db294-105">DESCRIPTION</span></span>
<span data-ttu-id="db294-106">Командлет **Get-AzApiManagementGatewayKey** получает ключи из существующего шлюза.</span><span class="sxs-lookup"><span data-stu-id="db294-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="db294-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db294-107">EXAMPLES</span></span>

### <span data-ttu-id="db294-108">Пример 2: получение шлюза с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="db294-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="db294-109">Эта команда возвращает клавиши для шлюза "0123456789".</span><span class="sxs-lookup"><span data-stu-id="db294-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="db294-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db294-110">PARAMETERS</span></span>

### <span data-ttu-id="db294-111">-Context</span><span class="sxs-lookup"><span data-stu-id="db294-111">-Context</span></span>
<span data-ttu-id="db294-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="db294-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db294-113">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="db294-113">This parameter is required.</span></span>

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

### <span data-ttu-id="db294-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db294-114">-DefaultProfile</span></span>
<span data-ttu-id="db294-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db294-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db294-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="db294-116">-GatewayId</span></span>
<span data-ttu-id="db294-117">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="db294-117">Gateway identifier.</span></span>
<span data-ttu-id="db294-118">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="db294-118">This parameter is required.</span></span>

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

### <span data-ttu-id="db294-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db294-119">CommonParameters</span></span>
<span data-ttu-id="db294-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db294-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db294-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db294-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db294-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db294-122">INPUTS</span></span>

### <span data-ttu-id="db294-123">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db294-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db294-124">System. String</span><span class="sxs-lookup"><span data-stu-id="db294-124">System.String</span></span>

## <span data-ttu-id="db294-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db294-125">OUTPUTS</span></span>

### <span data-ttu-id="db294-126">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="db294-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="db294-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="db294-127">NOTES</span></span>

## <span data-ttu-id="db294-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db294-128">RELATED LINKS</span></span>
