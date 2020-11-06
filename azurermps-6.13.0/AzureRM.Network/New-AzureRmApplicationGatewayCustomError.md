---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaycustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayCustomError.md
ms.openlocfilehash: 9e05684f40223711db7a8a6aaaf1cfb684efced4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567709"
---
# <span data-ttu-id="abd89-101">New-AzureRmApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="abd89-101">New-AzureRmApplicationGatewayCustomError</span></span>

## <span data-ttu-id="abd89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="abd89-102">SYNOPSIS</span></span>
<span data-ttu-id="abd89-103">Создание настраиваемой ошибки с кодом состояния HTTP и URL-адресом настраиваемой страницы ошибок</span><span class="sxs-lookup"><span data-stu-id="abd89-103">Creates a custom error with http status code and custom error page url</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abd89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="abd89-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayCustomError -StatusCode <String> -CustomErrorPageUrl <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="abd89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd89-105">DESCRIPTION</span></span>
<span data-ttu-id="abd89-106">Командлет **New-AzureRmApplicationGatewayCustomError** создает настраиваемое сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="abd89-106">The **New-AzureRmApplicationGatewayCustomError** cmdlet creates a custom error.</span></span>

## <span data-ttu-id="abd89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="abd89-107">EXAMPLES</span></span>

### <span data-ttu-id="abd89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="abd89-108">Example 1</span></span>
```powershell
PS C:\> $customError403Url = "https://mycustomerrorpages.blob.core.windows.net/errorpages/403-another.htm"
PS C:\> $ce = New-AzureRmApplicationGatewayCustomError -StatusCode HttpStatus403 -CustomErrorPageUrl $customError403Url
```

<span data-ttu-id="abd89-109">Эта команда создает настраиваемое сообщение об ошибке с кодом состояния HTTP 403.</span><span class="sxs-lookup"><span data-stu-id="abd89-109">This command creates the custom error of http status code 403.</span></span>

## <span data-ttu-id="abd89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="abd89-110">PARAMETERS</span></span>

### <span data-ttu-id="abd89-111">-CustomErrorPageUrl</span><span class="sxs-lookup"><span data-stu-id="abd89-111">-CustomErrorPageUrl</span></span>
<span data-ttu-id="abd89-112">URL-адрес страницы "ошибка" клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="abd89-112">Error page URL of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd89-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd89-113">-DefaultProfile</span></span>
<span data-ttu-id="abd89-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="abd89-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd89-115">-StatusCode</span><span class="sxs-lookup"><span data-stu-id="abd89-115">-StatusCode</span></span>
<span data-ttu-id="abd89-116">Код состояния ошибки клиента шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="abd89-116">Status code of the application gateway customer error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abd89-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd89-117">CommonParameters</span></span>
<span data-ttu-id="abd89-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="abd89-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="abd89-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abd89-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd89-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="abd89-120">INPUTS</span></span>

### <span data-ttu-id="abd89-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="abd89-121">None</span></span>

## <span data-ttu-id="abd89-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="abd89-122">OUTPUTS</span></span>

### <span data-ttu-id="abd89-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayCustomError</span><span class="sxs-lookup"><span data-stu-id="abd89-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayCustomError</span></span>

## <span data-ttu-id="abd89-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="abd89-124">NOTES</span></span>

## <span data-ttu-id="abd89-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="abd89-125">RELATED LINKS</span></span>
