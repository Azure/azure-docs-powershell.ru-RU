---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: ca03b95748203546fb8d9235cb7822a4dde359a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568734"
---
# <span data-ttu-id="d580f-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d580f-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d580f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d580f-102">SYNOPSIS</span></span>
<span data-ttu-id="d580f-103">Создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="d580f-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d580f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d580f-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d580f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d580f-105">DESCRIPTION</span></span>
<span data-ttu-id="d580f-106">Командлет **New-AzureRmApplicationGatewayConnectionDraining** создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="d580f-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="d580f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d580f-107">EXAMPLES</span></span>

### <span data-ttu-id="d580f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d580f-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="d580f-109">Команда создает новую конфигурацию сток подключений с параметром "Enabled" (true), а DrainTimeoutInSec — 42 секунд и сохраняет его в $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="d580f-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="d580f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d580f-110">PARAMETERS</span></span>

### <span data-ttu-id="d580f-111">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="d580f-111">-DrainTimeoutInSec</span></span>
<span data-ttu-id="d580f-112">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="d580f-112">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="d580f-113">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="d580f-113">Acceptable values are from 1 second to 3600 seconds.</span></span>

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

### <span data-ttu-id="d580f-114">-Включено</span><span class="sxs-lookup"><span data-stu-id="d580f-114">-Enabled</span></span>
<span data-ttu-id="d580f-115">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="d580f-115">Whether connection draining is enabled or not.</span></span>

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

### <span data-ttu-id="d580f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d580f-116">-DefaultProfile</span></span>
<span data-ttu-id="d580f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d580f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d580f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d580f-118">CommonParameters</span></span>
<span data-ttu-id="d580f-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d580f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d580f-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d580f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d580f-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d580f-121">INPUTS</span></span>

### <span data-ttu-id="d580f-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="d580f-122">None</span></span>

## <span data-ttu-id="d580f-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d580f-123">OUTPUTS</span></span>

### <span data-ttu-id="d580f-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d580f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="d580f-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d580f-125">NOTES</span></span>

## <span data-ttu-id="d580f-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d580f-126">RELATED LINKS</span></span>

[<span data-ttu-id="d580f-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d580f-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d580f-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d580f-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="d580f-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="d580f-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

