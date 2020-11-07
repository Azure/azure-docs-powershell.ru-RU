---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayavailablessloptions
schema: 2.0.0
ms.openlocfilehash: 023b2a43114fe47b50956e7f4626a75706e914f5
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913853"
---
# <span data-ttu-id="4b5d3-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4b5d3-101">Get-AzureRmApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4b5d3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b5d3-102">SYNOPSIS</span></span>
<span data-ttu-id="4b5d3-103">Получает все доступные параметры SSL для политики SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="4b5d3-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b5d3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b5d3-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayAvailableSslOptions [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b5d3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b5d3-105">DESCRIPTION</span></span>
<span data-ttu-id="4b5d3-106">Командлет **Get-AzureRmApplicationGatewayAvailableSslOptions** получает все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="4b5d3-106">The **Get-AzureRmApplicationGatewayAvailableSslOptions** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="4b5d3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b5d3-107">EXAMPLES</span></span>

### <span data-ttu-id="4b5d3-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b5d3-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzureRmApplicationGatewayAvailableSslOptions
```

<span data-ttu-id="4b5d3-109">Эти команды возвращают все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="4b5d3-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="4b5d3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b5d3-110">PARAMETERS</span></span>

### <span data-ttu-id="4b5d3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b5d3-111">-DefaultProfile</span></span>
<span data-ttu-id="4b5d3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b5d3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b5d3-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b5d3-113">CommonParameters</span></span>
<span data-ttu-id="4b5d3-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b5d3-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b5d3-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b5d3-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b5d3-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b5d3-116">INPUTS</span></span>

### <span data-ttu-id="4b5d3-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="4b5d3-117">None</span></span>

## <span data-ttu-id="4b5d3-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b5d3-118">OUTPUTS</span></span>

### <span data-ttu-id="4b5d3-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="4b5d3-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="4b5d3-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b5d3-120">NOTES</span></span>

## <span data-ttu-id="4b5d3-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b5d3-121">RELATED LINKS</span></span>

