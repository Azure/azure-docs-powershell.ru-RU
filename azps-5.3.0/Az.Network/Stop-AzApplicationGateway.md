---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517889"
---
# <span data-ttu-id="b34a3-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="b34a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34a3-102">SYNOPSIS</span></span>
<span data-ttu-id="b34a3-103">Остановка шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b34a3-103">Stops an application gateway</span></span>

## <span data-ttu-id="b34a3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b34a3-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b34a3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b34a3-105">DESCRIPTION</span></span>
<span data-ttu-id="b34a3-106">Для шлюза приложения прекращается доступ к шлюзу приложения с применением **cmdlet Stop-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="b34a3-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="b34a3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b34a3-107">EXAMPLES</span></span>

### <span data-ttu-id="b34a3-108">Пример 1. Остановка шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="b34a3-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="b34a3-109">Эта команда останавливает хранение шлюза приложения в переменной $AppGw приложения.</span><span class="sxs-lookup"><span data-stu-id="b34a3-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="b34a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b34a3-110">PARAMETERS</span></span>

### <span data-ttu-id="b34a3-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-111">-ApplicationGateway</span></span>
<span data-ttu-id="b34a3-112">Указывает шлюз приложения, который останавливает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b34a3-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="b34a3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b34a3-113">-AsJob</span></span>
<span data-ttu-id="b34a3-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b34a3-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34a3-115">-DefaultProfile</span></span>
<span data-ttu-id="b34a3-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b34a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b34a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34a3-117">CommonParameters</span></span>
<span data-ttu-id="b34a3-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34a3-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b34a3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34a3-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b34a3-120">INPUTS</span></span>

### <span data-ttu-id="b34a3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b34a3-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b34a3-122">OUTPUTS</span></span>

### <span data-ttu-id="b34a3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b34a3-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b34a3-124">NOTES</span></span>

## <span data-ttu-id="b34a3-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b34a3-125">RELATED LINKS</span></span>

[<span data-ttu-id="b34a3-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="b34a3-127">New-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="b34a3-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="b34a3-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="b34a3-130">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b34a3-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


