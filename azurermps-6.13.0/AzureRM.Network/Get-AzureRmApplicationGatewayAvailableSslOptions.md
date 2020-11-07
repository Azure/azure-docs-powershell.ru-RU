---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAvailableSslOptions.md
ms.openlocfilehash: 157093dc382b4f56ac7759a9b32b42c8b2488d90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734940"
---
# <span data-ttu-id="2004b-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="2004b-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2004b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2004b-102">SYNOPSIS</span></span>
<span data-ttu-id="2004b-103">Получает все доступные параметры SSL для политики SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2004b-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2004b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2004b-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2004b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2004b-105">DESCRIPTION</span></span>
<span data-ttu-id="2004b-106">Командлет **Get-AzureRmApplicationGatewayAvailableSslOptions** получает все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="2004b-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="2004b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2004b-107">EXAMPLES</span></span>

### <span data-ttu-id="2004b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2004b-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="2004b-109">Эти команды возвращают все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="2004b-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="2004b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2004b-110">PARAMETERS</span></span>

### <span data-ttu-id="2004b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2004b-111">-DefaultProfile</span></span>
<span data-ttu-id="2004b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2004b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2004b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2004b-113">CommonParameters</span></span>
<span data-ttu-id="2004b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2004b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2004b-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2004b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2004b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2004b-116">INPUTS</span></span>

### <span data-ttu-id="2004b-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="2004b-117">None</span></span>

## <span data-ttu-id="2004b-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2004b-118">OUTPUTS</span></span>

### <span data-ttu-id="2004b-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="2004b-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2004b-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="2004b-120">NOTES</span></span>

## <span data-ttu-id="2004b-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2004b-121">RELATED LINKS</span></span>
