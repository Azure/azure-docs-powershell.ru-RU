---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: ba979a12584d526ba7e3a36d13c44b51704b44f6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913604"
---
# <span data-ttu-id="6d49f-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="6d49f-101">Remove-AzureRmApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="6d49f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d49f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d49f-103">Удаление конфигурации перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6d49f-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d49f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d49f-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d49f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d49f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d49f-106">Командлет **Remove-AzureRmApplicationGatewayRedirectConfiguration** удаляет конфигурацию перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6d49f-106">The **Remove-AzureRmApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="6d49f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d49f-107">EXAMPLES</span></span>

### <span data-ttu-id="6d49f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d49f-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzureRmApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="6d49f-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6d49f-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="6d49f-110">Вторая команда удаляет конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="6d49f-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="6d49f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d49f-111">PARAMETERS</span></span>

### <span data-ttu-id="6d49f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d49f-112">-ApplicationGateway</span></span>
<span data-ttu-id="6d49f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d49f-113">The applicationGateway</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d49f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d49f-114">-DefaultProfile</span></span>
<span data-ttu-id="6d49f-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d49f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d49f-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d49f-116">-Name</span></span>
<span data-ttu-id="6d49f-117">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="6d49f-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="6d49f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d49f-118">CommonParameters</span></span>
<span data-ttu-id="6d49f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d49f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d49f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d49f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d49f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d49f-121">INPUTS</span></span>

### <span data-ttu-id="6d49f-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d49f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d49f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d49f-123">OUTPUTS</span></span>

### <span data-ttu-id="6d49f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6d49f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6d49f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d49f-125">NOTES</span></span>

## <span data-ttu-id="6d49f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d49f-126">RELATED LINKS</span></span>

