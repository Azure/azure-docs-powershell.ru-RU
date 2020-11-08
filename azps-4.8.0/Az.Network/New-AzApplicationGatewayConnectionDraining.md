---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 679a1311526f7fa5028c83e6571001d14b2ff3f5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244398"
---
# <span data-ttu-id="5fcaa-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5fcaa-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5fcaa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5fcaa-102">SYNOPSIS</span></span>
<span data-ttu-id="5fcaa-103">Создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="5fcaa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5fcaa-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5fcaa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fcaa-105">DESCRIPTION</span></span>
<span data-ttu-id="5fcaa-106">Командлет **New-AzApplicationGatewayConnectionDraining** создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="5fcaa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5fcaa-107">EXAMPLES</span></span>

### <span data-ttu-id="5fcaa-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5fcaa-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="5fcaa-109">Команда создает новую конфигурацию сток подключений с параметром "Enabled" (true), а DrainTimeoutInSec — 42 секунд и сохраняет его в $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="5fcaa-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5fcaa-110">PARAMETERS</span></span>

### <span data-ttu-id="5fcaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fcaa-111">-DefaultProfile</span></span>
<span data-ttu-id="5fcaa-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fcaa-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="5fcaa-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="5fcaa-114">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="5fcaa-115">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="5fcaa-116">-Включено</span><span class="sxs-lookup"><span data-stu-id="5fcaa-116">-Enabled</span></span>
<span data-ttu-id="5fcaa-117">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="5fcaa-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fcaa-118">CommonParameters</span></span>
<span data-ttu-id="5fcaa-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5fcaa-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fcaa-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fcaa-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fcaa-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5fcaa-121">INPUTS</span></span>

### <span data-ttu-id="5fcaa-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="5fcaa-122">None</span></span>

## <span data-ttu-id="5fcaa-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5fcaa-123">OUTPUTS</span></span>

### <span data-ttu-id="5fcaa-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5fcaa-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="5fcaa-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5fcaa-125">NOTES</span></span>

## <span data-ttu-id="5fcaa-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5fcaa-126">RELATED LINKS</span></span>

[<span data-ttu-id="5fcaa-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5fcaa-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5fcaa-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5fcaa-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="5fcaa-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="5fcaa-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

