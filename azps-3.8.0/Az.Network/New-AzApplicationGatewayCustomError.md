---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayCustomError.md
ms.openlocfilehash: 162e9a5cd869b6ea50e6d72dc7041ab14dc9a8e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074835"
---
# <span data-ttu-id="13efa-101">New-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-101">New-AzApplicationGatewayCustomError</span></span>

## <span data-ttu-id="13efa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13efa-102">SYNOPSIS</span></span>
<span data-ttu-id="13efa-103">Создание настраиваемой ошибки с кодом состояния HTTP и URL-адресом настраиваемой страницы ошибок</span><span class="sxs-lookup"><span data-stu-id="13efa-103">Creates a custom error with http status code and custom error page url</span></span> 

## <span data-ttu-id="13efa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13efa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13efa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13efa-105">DESCRIPTION</span></span>
<span data-ttu-id="13efa-106">Командлет **New-AzApplicationGatewayCustomError** создает настраиваемое сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="13efa-106">The **New-AzApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="13efa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13efa-107">EXAMPLES</span></span>

### <span data-ttu-id="13efa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="13efa-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="13efa-109">Эта команда создает настраиваемое сообщение об ошибке с кодом состояния HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="13efa-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="13efa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13efa-110">PARAMETERS</span></span>

### <span data-ttu-id="13efa-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="13efa-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="13efa-112">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="13efa-112">Error page URL of the application gateway customer error.</span></span>

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

### <span data-ttu-id="13efa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13efa-113">-DefaultProfile</span></span>
<span data-ttu-id="13efa-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="13efa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13efa-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="13efa-115">-StatusCode</span></span>
<span data-ttu-id="13efa-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="13efa-116">Status code of the application gateway customer error.</span></span>

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

### <span data-ttu-id="13efa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13efa-117">CommonParameters</span></span>
<span data-ttu-id="13efa-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13efa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13efa-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13efa-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13efa-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13efa-120">INPUTS</span></span>

### <span data-ttu-id="13efa-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="13efa-121">None</span></span>

## <span data-ttu-id="13efa-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13efa-122">OUTPUTS</span></span>

### <span data-ttu-id="13efa-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="13efa-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="13efa-124">NOTES</span></span>

## <span data-ttu-id="13efa-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13efa-125">RELATED LINKS</span></span>

[<span data-ttu-id="13efa-126">Add-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-126">Add-AzApplicationGatewayCustomError</span></span>](./Add-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="13efa-127">Get-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-127">Get-AzApplicationGatewayCustomError</span></span>](./Get-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="13efa-128">Remove-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-128">Remove-AzApplicationGatewayCustomError</span></span>](./Remove-AzApplicationGatewayCustomError.md)

[<span data-ttu-id="13efa-129">Set-AzApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="13efa-129">Set-AzApplicationGatewayCustomError</span></span>](./Set-AzApplicationGatewayCustomError.md)
