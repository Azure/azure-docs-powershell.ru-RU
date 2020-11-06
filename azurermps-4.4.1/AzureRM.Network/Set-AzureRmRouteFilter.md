---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 56f0c3ec3a69819ad7faa28b10d33a3cf751c48f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562399"
---
# <span data-ttu-id="5d57d-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5d57d-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="5d57d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d57d-102">SYNOPSIS</span></span>
<span data-ttu-id="5d57d-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="5d57d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d57d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d57d-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d57d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d57d-105">DESCRIPTION</span></span>
<span data-ttu-id="5d57d-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="5d57d-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="5d57d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d57d-107">EXAMPLES</span></span>

### <span data-ttu-id="5d57d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d57d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="5d57d-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="5d57d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="5d57d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d57d-110">PARAMETERS</span></span>

### <span data-ttu-id="5d57d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="5d57d-111">-Force</span></span>
<span data-ttu-id="5d57d-112">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="5d57d-112">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="5d57d-113">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5d57d-113">-RouteFilter</span></span>
<span data-ttu-id="5d57d-114">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="5d57d-114">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d57d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d57d-115">-Confirm</span></span>
<span data-ttu-id="5d57d-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5d57d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d57d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d57d-117">-WhatIf</span></span>
<span data-ttu-id="5d57d-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5d57d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5d57d-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5d57d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d57d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d57d-120">-DefaultProfile</span></span>
<span data-ttu-id="5d57d-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d57d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d57d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d57d-122">CommonParameters</span></span>
<span data-ttu-id="5d57d-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d57d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d57d-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d57d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d57d-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d57d-125">INPUTS</span></span>

### <span data-ttu-id="5d57d-126">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5d57d-126">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5d57d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d57d-127">OUTPUTS</span></span>

### <span data-ttu-id="5d57d-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="5d57d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="5d57d-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d57d-129">NOTES</span></span>

## <span data-ttu-id="5d57d-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d57d-130">RELATED LINKS</span></span>

