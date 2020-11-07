---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 96a170d302d66ed2fa27d2cd7bdb17fc23cefcd3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730643"
---
# <span data-ttu-id="6393f-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="6393f-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="6393f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6393f-102">SYNOPSIS</span></span>
<span data-ttu-id="6393f-103">Получение удостоверения, назначенного шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="6393f-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="6393f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6393f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6393f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6393f-105">DESCRIPTION</span></span>
<span data-ttu-id="6393f-106">Командлет **Get-AzApplicationGatewayIdentity** получает удостоверение, назначенное шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="6393f-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="6393f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6393f-107">EXAMPLES</span></span>

### <span data-ttu-id="6393f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6393f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="6393f-109">В этом примере показано, как получить удостоверение шлюза приложения из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="6393f-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="6393f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6393f-110">PARAMETERS</span></span>

### <span data-ttu-id="6393f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6393f-111">-ApplicationGateway</span></span>
<span data-ttu-id="6393f-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6393f-112">The applicationGateway</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6393f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6393f-113">-DefaultProfile</span></span>
<span data-ttu-id="6393f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6393f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6393f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6393f-115">CommonParameters</span></span>
<span data-ttu-id="6393f-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6393f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6393f-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6393f-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6393f-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6393f-118">INPUTS</span></span>

### <span data-ttu-id="6393f-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="6393f-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="6393f-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6393f-120">OUTPUTS</span></span>

### <span data-ttu-id="6393f-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="6393f-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="6393f-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="6393f-122">NOTES</span></span>

## <span data-ttu-id="6393f-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6393f-123">RELATED LINKS</span></span>
