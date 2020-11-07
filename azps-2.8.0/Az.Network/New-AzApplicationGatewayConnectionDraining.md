---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3401010e1b65dbd0ad24f634c32b06449671419f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902258"
---
# <span data-ttu-id="57e72-101">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="57e72-101">New-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="57e72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="57e72-102">SYNOPSIS</span></span>
<span data-ttu-id="57e72-103">Создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="57e72-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="57e72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="57e72-104">SYNTAX</span></span>

```
New-AzApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e72-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e72-105">DESCRIPTION</span></span>
<span data-ttu-id="57e72-106">Командлет **New-AzApplicationGatewayConnectionDraining** создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="57e72-106">The **New-AzApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="57e72-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="57e72-107">EXAMPLES</span></span>

### <span data-ttu-id="57e72-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="57e72-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="57e72-109">Команда создает новую конфигурацию сток подключений с параметром "Enabled" (true), а DrainTimeoutInSec — 42 секунд и сохраняет его в $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="57e72-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="57e72-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="57e72-110">PARAMETERS</span></span>

### <span data-ttu-id="57e72-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e72-111">-DefaultProfile</span></span>
<span data-ttu-id="57e72-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57e72-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57e72-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="57e72-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="57e72-114">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="57e72-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="57e72-115">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="57e72-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="57e72-116">-Включено</span><span class="sxs-lookup"><span data-stu-id="57e72-116">-Enabled</span></span>
<span data-ttu-id="57e72-117">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="57e72-117">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="57e72-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e72-118">CommonParameters</span></span>
<span data-ttu-id="57e72-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="57e72-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e72-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e72-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e72-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="57e72-121">INPUTS</span></span>

### <span data-ttu-id="57e72-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="57e72-122">None</span></span>

## <span data-ttu-id="57e72-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="57e72-123">OUTPUTS</span></span>

### <span data-ttu-id="57e72-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="57e72-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="57e72-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="57e72-125">NOTES</span></span>

## <span data-ttu-id="57e72-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57e72-126">RELATED LINKS</span></span>

[<span data-ttu-id="57e72-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="57e72-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="57e72-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="57e72-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="57e72-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="57e72-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

