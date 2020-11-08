---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: f2175583aaaf3af04120e22e32db79d7b20f1e30
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079512"
---
# <span data-ttu-id="d4fe4-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="d4fe4-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="d4fe4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d4fe4-102">SYNOPSIS</span></span>
<span data-ttu-id="d4fe4-103">Получает все доступные параметры SSL для политики SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="d4fe4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d4fe4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4fe4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4fe4-105">DESCRIPTION</span></span>
<span data-ttu-id="d4fe4-106">Командлет **Get-AzApplicationGatewayAvailableSslOption** получает все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="d4fe4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d4fe4-107">EXAMPLES</span></span>

### <span data-ttu-id="d4fe4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4fe4-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="d4fe4-109">Эти команды возвращают все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="d4fe4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d4fe4-110">PARAMETERS</span></span>

### <span data-ttu-id="d4fe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4fe4-111">-DefaultProfile</span></span>
<span data-ttu-id="d4fe4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4fe4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4fe4-113">CommonParameters</span></span>
<span data-ttu-id="d4fe4-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4fe4-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4fe4-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4fe4-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d4fe4-116">INPUTS</span></span>

### <span data-ttu-id="d4fe4-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="d4fe4-117">None</span></span>

## <span data-ttu-id="d4fe4-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4fe4-118">OUTPUTS</span></span>

### <span data-ttu-id="d4fe4-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="d4fe4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="d4fe4-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="d4fe4-120">NOTES</span></span>

## <span data-ttu-id="d4fe4-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4fe4-121">RELATED LINKS</span></span>