---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: e965f2cdbd9909003a07ea6c6addd198110e456f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909549"
---
# <span data-ttu-id="e1d1a-101">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="e1d1a-101">Remove-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="e1d1a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e1d1a-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d1a-103">Удаление конфигурации перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-103">Removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="e1d1a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e1d1a-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayRedirectConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d1a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d1a-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d1a-106">Командлет **Remove-AzApplicationGatewayRedirectConfiguration** удаляет конфигурацию перенаправления из существующего шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-106">The **Remove-AzApplicationGatewayRedirectConfiguration** cmdlet removes a redirect configuration from an existing Application Gateway.</span></span>

## <span data-ttu-id="e1d1a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e1d1a-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d1a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e1d1a-108">Example 1</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\>$AppGw = Remove-AzApplicationGatewayRedirectConfiguration -ApplicationGateway $AppGw -Name "Redirect01"
```

<span data-ttu-id="e1d1a-109">Первая команда получает шлюз приложения и сохраняет его в переменной $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e1d1a-110">Вторая команда удаляет конфигурацию перенаправления с именем Redirect01 из шлюза приложения, который хранится в $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-110">The second command removes the redirect configuration named Redirect01 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="e1d1a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e1d1a-111">PARAMETERS</span></span>

### <span data-ttu-id="e1d1a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1d1a-112">-ApplicationGateway</span></span>
<span data-ttu-id="e1d1a-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1d1a-113">The applicationGateway</span></span>

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

### <span data-ttu-id="e1d1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d1a-114">-DefaultProfile</span></span>
<span data-ttu-id="e1d1a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d1a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e1d1a-116">-Name</span></span>
<span data-ttu-id="e1d1a-117">Имя конфигурации перенаправления.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-117">The name of the redirect configuration</span></span>

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

### <span data-ttu-id="e1d1a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d1a-118">CommonParameters</span></span>
<span data-ttu-id="e1d1a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e1d1a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d1a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d1a-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d1a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e1d1a-121">INPUTS</span></span>

### <span data-ttu-id="e1d1a-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1d1a-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1d1a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e1d1a-123">OUTPUTS</span></span>

### <span data-ttu-id="e1d1a-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1d1a-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e1d1a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="e1d1a-125">NOTES</span></span>

## <span data-ttu-id="e1d1a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e1d1a-126">RELATED LINKS</span></span>

