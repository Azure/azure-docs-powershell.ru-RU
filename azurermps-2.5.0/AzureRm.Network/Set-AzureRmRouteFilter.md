---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
ms.openlocfilehash: 895819175f9fe4215d926d57c55307bbb4c75ab3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914758"
---
# <span data-ttu-id="9550d-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9550d-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="9550d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9550d-102">SYNOPSIS</span></span>
<span data-ttu-id="9550d-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="9550d-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9550d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9550d-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9550d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9550d-105">DESCRIPTION</span></span>
<span data-ttu-id="9550d-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="9550d-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="9550d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9550d-107">EXAMPLES</span></span>

### <span data-ttu-id="9550d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9550d-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="9550d-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="9550d-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="9550d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9550d-110">PARAMETERS</span></span>

### <span data-ttu-id="9550d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9550d-111">-AsJob</span></span>
<span data-ttu-id="9550d-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9550d-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9550d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9550d-113">-DefaultProfile</span></span>
<span data-ttu-id="9550d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9550d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9550d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9550d-115">-Force</span></span>
<span data-ttu-id="9550d-116">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="9550d-116">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9550d-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9550d-117">-RouteFilter</span></span>
<span data-ttu-id="9550d-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="9550d-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9550d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9550d-119">-Confirm</span></span>
<span data-ttu-id="9550d-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9550d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9550d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9550d-121">-WhatIf</span></span>
<span data-ttu-id="9550d-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9550d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9550d-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9550d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9550d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9550d-124">CommonParameters</span></span>
<span data-ttu-id="9550d-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9550d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9550d-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9550d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9550d-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9550d-127">INPUTS</span></span>

### <span data-ttu-id="9550d-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9550d-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9550d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9550d-129">OUTPUTS</span></span>

### <span data-ttu-id="9550d-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="9550d-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="9550d-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="9550d-131">NOTES</span></span>

## <span data-ttu-id="9550d-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9550d-132">RELATED LINKS</span></span>

