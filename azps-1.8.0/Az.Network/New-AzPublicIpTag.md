---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpubliciptag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPublicIpTag.md
ms.openlocfilehash: 7e4bfae0479d4f37f6a73c8e07239112267ac182
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730285"
---
# <span data-ttu-id="83e9f-101">New-AzPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="83e9f-101">New-AzPublicIpTag</span></span>

## <span data-ttu-id="83e9f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="83e9f-103">Создание тега IP.</span><span class="sxs-lookup"><span data-stu-id="83e9f-103">Creates an IP Tag.</span></span>

## <span data-ttu-id="83e9f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83e9f-104">SYNTAX</span></span>

```
New-AzPublicIpTag -IpTagType <String> -Tag <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83e9f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83e9f-105">DESCRIPTION</span></span>
<span data-ttu-id="83e9f-106">Командлет **New-AzPublicIpTag** создает тег IP.</span><span class="sxs-lookup"><span data-stu-id="83e9f-106">The **New-AzPublicIpTag** cmdlet creates a IP Tag.</span></span>

## <span data-ttu-id="83e9f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83e9f-107">EXAMPLES</span></span>

### <span data-ttu-id="83e9f-108">1: создание нового тега IP</span><span class="sxs-lookup"><span data-stu-id="83e9f-108">1: Create a new IP Tag</span></span>
```
$ipTag = New-AzPublicIpTag -IpTagType $ipTagType -Tag $tag
```

<span data-ttu-id="83e9f-109">Эта команда создает новый тег IP с tagtype, например "FirstPartyUsage", и тег Like "/SQL".</span><span class="sxs-lookup"><span data-stu-id="83e9f-109">This command creates a new IP Tag with the Tagtype like "FirstPartyUsage" and tag like "/Sql".</span></span> <span data-ttu-id="83e9f-110">Используется для создания publicIpAddress с этими конкретными тегами для выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="83e9f-110">This is used in publicIpAddress creation with these specific tags for allocation.</span></span>

## <span data-ttu-id="83e9f-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83e9f-111">PARAMETERS</span></span>

### <span data-ttu-id="83e9f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e9f-112">-DefaultProfile</span></span>
<span data-ttu-id="83e9f-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83e9f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83e9f-114">-IpTagType</span><span class="sxs-lookup"><span data-stu-id="83e9f-114">-IpTagType</span></span>
<span data-ttu-id="83e9f-115">Пример типа IpTag: FirstPartyUsage</span><span class="sxs-lookup"><span data-stu-id="83e9f-115">IpTag type Example:FirstPartyUsage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: FirstPartyUsage, NetworkDomain

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-116">-Тег</span><span class="sxs-lookup"><span data-stu-id="83e9f-116">-Tag</span></span>
<span data-ttu-id="83e9f-117">Пример значения IpTag:/SQL</span><span class="sxs-lookup"><span data-stu-id="83e9f-117">IpTag value Example:/Sql</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="83e9f-118">-Confirm</span></span>
<span data-ttu-id="83e9f-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="83e9f-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e9f-120">-WhatIf</span></span>
<span data-ttu-id="83e9f-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="83e9f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e9f-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="83e9f-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83e9f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e9f-123">CommonParameters</span></span>
<span data-ttu-id="83e9f-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83e9f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e9f-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83e9f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e9f-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83e9f-126">INPUTS</span></span>

### <span data-ttu-id="83e9f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="83e9f-127">System.String</span></span>

## <span data-ttu-id="83e9f-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83e9f-128">OUTPUTS</span></span>

### <span data-ttu-id="83e9f-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpTag</span><span class="sxs-lookup"><span data-stu-id="83e9f-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpTag</span></span>

## <span data-ttu-id="83e9f-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="83e9f-130">NOTES</span></span>

## <span data-ttu-id="83e9f-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83e9f-131">RELATED LINKS</span></span>
