---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: b1d38cf748adfc2fb9909fd33e5a4406bf293f13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564748"
---
# <span data-ttu-id="aaadf-101">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="aaadf-101">New-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="aaadf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aaadf-102">SYNOPSIS</span></span>
<span data-ttu-id="aaadf-103">Создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaadf-103">Creates a new connection draining configuration for back-end HTTP settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aaadf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aaadf-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayConnectionDraining -Enabled <Boolean> -DrainTimeoutInSec <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaadf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaadf-105">DESCRIPTION</span></span>
<span data-ttu-id="aaadf-106">Командлет **New-AzureRmApplicationGatewayConnectionDraining** создает новую конфигурацию сток подключений для параметров HTTP для веб-сервер.</span><span class="sxs-lookup"><span data-stu-id="aaadf-106">The **New-AzureRmApplicationGatewayConnectionDraining** cmdlet creates a new connection draining configuration for back-end HTTP settings.</span></span>

## <span data-ttu-id="aaadf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aaadf-107">EXAMPLES</span></span>

### <span data-ttu-id="aaadf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="aaadf-108">Example 1</span></span>
```
PS C:\> $connectionDraining = New-AzureRmApplicationGatewayConnectionDraining -Enabled $True -DrainTimeoutInSec 42
```

<span data-ttu-id="aaadf-109">Команда создает новую конфигурацию сток подключений с параметром "Enabled" (true), а DrainTimeoutInSec — 42 секунд и сохраняет его в $connectionDraining.</span><span class="sxs-lookup"><span data-stu-id="aaadf-109">The command creates a new connection draining configuration with Enabled set to True and DrainTimeoutInSec set to 42 seconds and stores it in $connectionDraining.</span></span>

## <span data-ttu-id="aaadf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aaadf-110">PARAMETERS</span></span>

### <span data-ttu-id="aaadf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaadf-111">-DefaultProfile</span></span>
<span data-ttu-id="aaadf-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aaadf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaadf-113">-DrainTimeoutInSec</span><span class="sxs-lookup"><span data-stu-id="aaadf-113">-DrainTimeoutInSec</span></span>
<span data-ttu-id="aaadf-114">Число секунд, в течение которого сток подключений является активным.</span><span class="sxs-lookup"><span data-stu-id="aaadf-114">The number of seconds connection draining is active.</span></span>
<span data-ttu-id="aaadf-115">Допустимые значения: от 1 секунды до 3600 секунд.</span><span class="sxs-lookup"><span data-stu-id="aaadf-115">Acceptable values are from 1 second to 3600 seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-116">-Включено</span><span class="sxs-lookup"><span data-stu-id="aaadf-116">-Enabled</span></span>
<span data-ttu-id="aaadf-117">Включена ли сток подключений.</span><span class="sxs-lookup"><span data-stu-id="aaadf-117">Whether connection draining is enabled or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaadf-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaadf-118">CommonParameters</span></span>
<span data-ttu-id="aaadf-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aaadf-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaadf-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaadf-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaadf-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aaadf-121">INPUTS</span></span>

### <span data-ttu-id="aaadf-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="aaadf-122">None</span></span>

## <span data-ttu-id="aaadf-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaadf-123">OUTPUTS</span></span>

### <span data-ttu-id="aaadf-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="aaadf-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="aaadf-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="aaadf-125">NOTES</span></span>

## <span data-ttu-id="aaadf-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaadf-126">RELATED LINKS</span></span>

[<span data-ttu-id="aaadf-127">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="aaadf-127">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="aaadf-128">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="aaadf-128">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>](./Remove-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="aaadf-129">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="aaadf-129">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

