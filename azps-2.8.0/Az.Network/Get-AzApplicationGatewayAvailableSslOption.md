---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayavailablessloption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: 04a24ee5148782f4a15aa5b93ffb937ad312ccfb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903038"
---
# <span data-ttu-id="a16e0-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="a16e0-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="a16e0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a16e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a16e0-103">Получает все доступные параметры SSL для политики SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="a16e0-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="a16e0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a16e0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a16e0-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a16e0-106">Командлет **Get-AzApplicationGatewayAvailableSslOption** получает все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="a16e0-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="a16e0-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a16e0-107">EXAMPLES</span></span>

### <span data-ttu-id="a16e0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a16e0-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="a16e0-109">Эти команды возвращают все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="a16e0-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="a16e0-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a16e0-110">PARAMETERS</span></span>

### <span data-ttu-id="a16e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16e0-111">-DefaultProfile</span></span>
<span data-ttu-id="a16e0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a16e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a16e0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16e0-113">CommonParameters</span></span>
<span data-ttu-id="a16e0-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a16e0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16e0-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a16e0-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16e0-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a16e0-116">INPUTS</span></span>

### <span data-ttu-id="a16e0-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="a16e0-117">None</span></span>

## <span data-ttu-id="a16e0-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a16e0-118">OUTPUTS</span></span>

### <span data-ttu-id="a16e0-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="a16e0-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="a16e0-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="a16e0-120">NOTES</span></span>

## <span data-ttu-id="a16e0-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a16e0-121">RELATED LINKS</span></span>
