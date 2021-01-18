---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98516606"
---
# <span data-ttu-id="80838-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="80838-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="80838-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80838-102">SYNOPSIS</span></span>
<span data-ttu-id="80838-103">Ключи существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="80838-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="80838-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80838-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80838-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80838-105">DESCRIPTION</span></span>
<span data-ttu-id="80838-106">Cmdlet **Get-AzApiManagementGatewayKey** получает ключи существующего шлюза</span><span class="sxs-lookup"><span data-stu-id="80838-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="80838-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80838-107">EXAMPLES</span></span>

### <span data-ttu-id="80838-108">Пример 2. Получить шлюз по ИД</span><span class="sxs-lookup"><span data-stu-id="80838-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="80838-109">Эта команда получает ключи для шлюза 0123456789.</span><span class="sxs-lookup"><span data-stu-id="80838-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="80838-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80838-110">PARAMETERS</span></span>

### <span data-ttu-id="80838-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="80838-111">-Context</span></span>
<span data-ttu-id="80838-112">Экземпляр PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="80838-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="80838-113">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="80838-113">This parameter is required.</span></span>

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

### <span data-ttu-id="80838-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80838-114">-DefaultProfile</span></span>
<span data-ttu-id="80838-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80838-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80838-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="80838-116">-GatewayId</span></span>
<span data-ttu-id="80838-117">Идентификатор шлюза.</span><span class="sxs-lookup"><span data-stu-id="80838-117">Gateway identifier.</span></span>
<span data-ttu-id="80838-118">Этот параметр является required(обязательно).</span><span class="sxs-lookup"><span data-stu-id="80838-118">This parameter is required.</span></span>

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

### <span data-ttu-id="80838-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80838-119">CommonParameters</span></span>
<span data-ttu-id="80838-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80838-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80838-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80838-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80838-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80838-122">INPUTS</span></span>

### <span data-ttu-id="80838-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80838-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80838-124">System.String</span><span class="sxs-lookup"><span data-stu-id="80838-124">System.String</span></span>

## <span data-ttu-id="80838-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80838-125">OUTPUTS</span></span>

### <span data-ttu-id="80838-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="80838-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="80838-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80838-127">NOTES</span></span>

## <span data-ttu-id="80838-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80838-128">RELATED LINKS</span></span>
