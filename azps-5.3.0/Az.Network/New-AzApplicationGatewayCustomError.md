---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421927"
---
# <span data-ttu-id="f977b-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f977b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f977b-102">SYNOPSIS</span></span>
<span data-ttu-id="f977b-103">Создает настраиваемую ошибку с кодом состояния http и URL-адресом страницы настраиваемой ошибки</span><span class="sxs-lookup"><span data-stu-id="f977b-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="f977b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f977b-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f977b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f977b-105">DESCRIPTION</span></span>
<span data-ttu-id="f977b-106">Для создания пользовательской ошибки будет создаваться новый **cmdlet New-AzApplicationGatewayCustomError.**</span><span class="sxs-lookup"><span data-stu-id="f977b-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="f977b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f977b-107">EXAMPLES</span></span>

### <span data-ttu-id="f977b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f977b-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="f977b-109">Эта команда создает настраиваемую ошибку http-кода состояния 403.</span><span class="sxs-lookup"><span data-stu-id="f977b-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="f977b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f977b-110">PARAMETERS</span></span>

### <span data-ttu-id="f977b-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="f977b-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="f977b-112">URL-адрес страницы ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f977b-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f977b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f977b-113">-DefaultProfile</span></span>
<span data-ttu-id="f977b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f977b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f977b-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="f977b-115">-StatusCode</span></span>
<span data-ttu-id="f977b-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f977b-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f977b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f977b-117">CommonParameters</span></span>
<span data-ttu-id="f977b-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f977b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f977b-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f977b-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f977b-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f977b-120">INPUTS</span></span>

### <span data-ttu-id="f977b-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f977b-121">None</span></span>

## <span data-ttu-id="f977b-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f977b-122">OUTPUTS</span></span>

### <span data-ttu-id="f977b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="f977b-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f977b-124">NOTES</span></span>

## <span data-ttu-id="f977b-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f977b-125">RELATED LINKS</span></span>

[<span data-ttu-id="f977b-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f977b-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f977b-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="f977b-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="f977b-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
