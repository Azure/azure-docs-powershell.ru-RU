---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPublicIpTag.md
ms.openlocfilehash: 56352ff165d2e7dcbf5386e713028fae5c991d8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568566"
---
# <span data-ttu-id="658ee-101">New-AzureRmPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="658ee-101">New-AzureRmPublicIpTag</span></span>

## <span data-ttu-id="658ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="658ee-102">SYNOPSIS</span></span>
<span data-ttu-id="658ee-103">Создание тега IP.</span><span class="sxs-lookup"><span data-stu-id="658ee-103">Creates an IP Tag.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="658ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="658ee-104">SYNTAX</span></span>

```
New-AzureRmPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="658ee-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="658ee-105">DESCRIPTION</span></span>
<span data-ttu-id="658ee-106">Командлет **New-AzureRmPublicIpTag** создает тег IP.</span><span class="sxs-lookup"><span data-stu-id="658ee-106">The **New-AzureRmPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="658ee-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="658ee-107">EXAMPLES</span></span>

### <span data-ttu-id="658ee-108">1: создание нового тега IP</span><span class="sxs-lookup"><span data-stu-id="658ee-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzureRmPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="658ee-109">Эта команда создает новый тег IP с tagtype, например "FirstPartyUsage", и тег Like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="658ee-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="658ee-110">Используется для создания publicIpAddress с этими конкретными тегами для выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="658ee-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="658ee-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="658ee-111">PARAMETERS</span></span>

### <span data-ttu-id="658ee-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658ee-112">-DefaultProfile</span></span>
<span data-ttu-id="658ee-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="658ee-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="658ee-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="658ee-114">-IpTagType</span></span>
<span data-ttu-id="658ee-115">Пример типа IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="658ee-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658ee-116">-Тег</span><span class="sxs-lookup"><span data-stu-id="658ee-116">-Tag</span></span>
<span data-ttu-id="658ee-117">Пример значения IpTag:/SQL</span><span class="sxs-lookup"><span data-stu-id="658ee-117">IpTag value Example:/Sql</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="658ee-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="658ee-118">-Confirm</span></span>
<span data-ttu-id="658ee-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="658ee-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="658ee-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658ee-120">-WhatIf</span></span>
<span data-ttu-id="658ee-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="658ee-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658ee-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="658ee-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="658ee-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="658ee-123">INPUTS</span></span>

### <span data-ttu-id="658ee-124">System. String</span><span class="sxs-lookup"><span data-stu-id="658ee-124">System.String</span></span>


## <span data-ttu-id="658ee-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="658ee-125">OUTPUTS</span></span>

### <span data-ttu-id="658ee-126">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="658ee-126">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>


## <span data-ttu-id="658ee-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="658ee-127">NOTES</span></span>

## <span data-ttu-id="658ee-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="658ee-128">RELATED LINKS</span></span>

