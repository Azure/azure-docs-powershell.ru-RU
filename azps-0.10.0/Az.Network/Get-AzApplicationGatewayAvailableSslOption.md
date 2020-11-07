---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-AzApplicationGatewayAvailableSslOption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayAvailableSslOption.md
ms.openlocfilehash: e0fa27a99a8a2d00819d558b42218b9405a5f039
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910109"
---
# <span data-ttu-id="2dbe4-101">Get-AzApplicationGatewayAvailableSslOption</span><span class="sxs-lookup"><span data-stu-id="2dbe4-101">Get-AzApplicationGatewayAvailableSslOption</span></span>

## <span data-ttu-id="2dbe4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dbe4-102">SYNOPSIS</span></span>
<span data-ttu-id="2dbe4-103">Получает все доступные параметры SSL для политики SSL для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="2dbe4-103">Gets all available ssl options for ssl policy for Application Gateway.</span></span>

## <span data-ttu-id="2dbe4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dbe4-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAvailableSslOption [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2dbe4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dbe4-105">DESCRIPTION</span></span>
<span data-ttu-id="2dbe4-106">Командлет **Get-AzApplicationGatewayAvailableSslOption** получает все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="2dbe4-106">The **Get-AzApplicationGatewayAvailableSslOption** cmdlet gets all available ssl options for ssl policy</span></span>

## <span data-ttu-id="2dbe4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dbe4-107">EXAMPLES</span></span>

### <span data-ttu-id="2dbe4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2dbe4-108">Example 1</span></span>
```
PS C:\>$sslOptions = Get-AzApplicationGatewayAvailableSslOption
```

<span data-ttu-id="2dbe4-109">Эти команды возвращают все доступные параметры SSL для политики SSL.</span><span class="sxs-lookup"><span data-stu-id="2dbe4-109">This commands returns all available ssl options for ssl policy.</span></span>

## <span data-ttu-id="2dbe4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dbe4-110">PARAMETERS</span></span>

### <span data-ttu-id="2dbe4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dbe4-111">-DefaultProfile</span></span>
<span data-ttu-id="2dbe4-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dbe4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dbe4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dbe4-113">CommonParameters</span></span>
<span data-ttu-id="2dbe4-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dbe4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dbe4-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dbe4-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dbe4-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dbe4-116">INPUTS</span></span>

### <span data-ttu-id="2dbe4-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="2dbe4-117">None</span></span>

## <span data-ttu-id="2dbe4-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dbe4-118">OUTPUTS</span></span>

### <span data-ttu-id="2dbe4-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAvailableSslOptions</span><span class="sxs-lookup"><span data-stu-id="2dbe4-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAvailableSslOptions</span></span>

## <span data-ttu-id="2dbe4-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dbe4-120">NOTES</span></span>

## <span data-ttu-id="2dbe4-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dbe4-121">RELATED LINKS</span></span>

