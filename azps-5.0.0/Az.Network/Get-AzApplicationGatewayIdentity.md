---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIdentity.md
ms.openlocfilehash: 2ba4a6c0f625941daf34b6754a3df856b8554075
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249996"
---
# <span data-ttu-id="009cf-101">Get-AzApplicationGatewayIdentity</span><span class="sxs-lookup"><span data-stu-id="009cf-101">Get-AzApplicationGatewayIdentity</span></span>

## <span data-ttu-id="009cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="009cf-102">SYNOPSIS</span></span>
<span data-ttu-id="009cf-103">Получение удостоверения, назначенного шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="009cf-103">Get identity assigned to the application gateway.</span></span>

## <span data-ttu-id="009cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="009cf-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIdentity -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="009cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="009cf-105">DESCRIPTION</span></span>
<span data-ttu-id="009cf-106">Командлет **Get-AzApplicationGatewayIdentity** получает удостоверение, назначенное шлюзу приложений.</span><span class="sxs-lookup"><span data-stu-id="009cf-106">The **Get-AzApplicationGatewayIdentity** cmdlet gets identity assigned to the application gateway.</span></span>

## <span data-ttu-id="009cf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="009cf-107">EXAMPLES</span></span>

### <span data-ttu-id="009cf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="009cf-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $identity = Get-AzApplicationGatewayIdentity -ApplicationGateway $gw
```

<span data-ttu-id="009cf-109">В этом примере показано, как получить удостоверение шлюза приложения из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="009cf-109">This examples shows how to get application gateway identity from Application Gateway.</span></span>

## <span data-ttu-id="009cf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="009cf-110">PARAMETERS</span></span>

### <span data-ttu-id="009cf-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="009cf-111">-ApplicationGateway</span></span>
<span data-ttu-id="009cf-112">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="009cf-112">The applicationGateway</span></span>

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

### <span data-ttu-id="009cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="009cf-113">-DefaultProfile</span></span>
<span data-ttu-id="009cf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="009cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="009cf-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="009cf-115">CommonParameters</span></span>
<span data-ttu-id="009cf-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="009cf-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="009cf-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="009cf-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="009cf-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="009cf-118">INPUTS</span></span>

### <span data-ttu-id="009cf-119">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="009cf-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="009cf-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="009cf-120">OUTPUTS</span></span>

### <span data-ttu-id="009cf-121">Microsoft. Azure. Commands. Network. Models. PSManagedServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="009cf-121">Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity</span></span>

## <span data-ttu-id="009cf-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="009cf-122">NOTES</span></span>

## <span data-ttu-id="009cf-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="009cf-123">RELATED LINKS</span></span>
