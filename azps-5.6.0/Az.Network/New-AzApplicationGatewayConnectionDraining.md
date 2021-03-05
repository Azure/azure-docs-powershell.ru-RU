---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b5bfedea118aa3770bac3141d05db379a4655906
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006216"
---
# <span data-ttu-id="62386-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62386-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="62386-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62386-102">SYNOPSIS</span></span>
<span data-ttu-id="62386-103">Создает новую конфигурацию разрядки подключений для back-end HTTP-параметров.</span><span class="sxs-lookup"><span data-stu-id="62386-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="62386-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="62386-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62386-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62386-105">DESCRIPTION</span></span>
<span data-ttu-id="62386-106">С **помощью cmdlet New-AzApplicationGatewayConnectionDraining** создается новая конфигурация разрядки подключения для конечных параметров HTTP.</span><span class="sxs-lookup"><span data-stu-id="62386-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="62386-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="62386-107">EXAMPLES</span></span>

### <span data-ttu-id="62386-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="62386-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="62386-109">Команда создает новую конфигурацию разрядки подключения с включенным подключением с установленным для функции "Истина" и РазрядкаTimeoutInSec 42 секунды и сохраняет его в $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="62386-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="62386-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62386-110">PARAMETERS</span></span>

### <span data-ttu-id="62386-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62386-111">-DefaultProfile</span></span>
<span data-ttu-id="62386-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62386-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62386-113">-DrainTimeoutInsec</span><span class="sxs-lookup"><span data-stu-id="62386-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="62386-114">Разрядка соединения за считанные секунды активна.</span><span class="sxs-lookup"><span data-stu-id="62386-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="62386-115">Допустимыми являются значения от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="62386-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62386-116">-Enabled</span><span class="sxs-lookup"><span data-stu-id="62386-116">-Enabled</span></span>
<span data-ttu-id="62386-117">Включена ли разрядка подключения.</span><span class="sxs-lookup"><span data-stu-id="62386-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62386-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62386-118">CommonParameters</span></span>
<span data-ttu-id="62386-119">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62386-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62386-120">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62386-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62386-121">INPUTS</span><span class="sxs-lookup"><span data-stu-id="62386-121">INPUTS</span></span>

### <span data-ttu-id="62386-122">Нет</span><span class="sxs-lookup"><span data-stu-id="62386-122">None</span></span>

## <span data-ttu-id="62386-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="62386-123">OUTPUTS</span></span>

### <span data-ttu-id="62386-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62386-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="62386-125">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="62386-125">NOTES</span></span>

## <span data-ttu-id="62386-126">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62386-126">RELATED LINKS</span></span>

[<span data-ttu-id="62386-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62386-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="62386-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62386-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="62386-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="62386-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

