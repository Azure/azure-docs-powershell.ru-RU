---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilter.md
ms.openlocfilehash: 5dc2b6a9650cdf4110858edf1b061f69adac48f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732918"
---
# <span data-ttu-id="3dc1b-101">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3dc1b-101">Set-AzureRmRouteFilter</span></span>

## <span data-ttu-id="3dc1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dc1b-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc1b-103">{Заполнение кратких описаний}</span><span class="sxs-lookup"><span data-stu-id="3dc1b-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dc1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dc1b-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilter -RouteFilter <PSRouteFilter> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc1b-105">DESCRIPTION</span></span>
<span data-ttu-id="3dc1b-106">{Заполнение в описании}}</span><span class="sxs-lookup"><span data-stu-id="3dc1b-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="3dc1b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dc1b-107">EXAMPLES</span></span>

### <span data-ttu-id="3dc1b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3dc1b-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="3dc1b-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="3dc1b-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="3dc1b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dc1b-110">PARAMETERS</span></span>

### <span data-ttu-id="3dc1b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc1b-111">-AsJob</span></span>
<span data-ttu-id="3dc1b-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3dc1b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dc1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc1b-113">-DefaultProfile</span></span>
<span data-ttu-id="3dc1b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc1b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dc1b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="3dc1b-115">-Force</span></span>
<span data-ttu-id="3dc1b-116">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="3dc1b-116">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="3dc1b-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3dc1b-117">-RouteFilter</span></span>
<span data-ttu-id="3dc1b-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="3dc1b-118">The RouteFilter</span></span>

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

### <span data-ttu-id="3dc1b-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc1b-119">-Confirm</span></span>
<span data-ttu-id="3dc1b-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc1b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc1b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc1b-121">-WhatIf</span></span>
<span data-ttu-id="3dc1b-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc1b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dc1b-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dc1b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc1b-124">CommonParameters</span></span>
<span data-ttu-id="3dc1b-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dc1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc1b-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dc1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc1b-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dc1b-127">INPUTS</span></span>

### <span data-ttu-id="3dc1b-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3dc1b-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>
<span data-ttu-id="3dc1b-129">Параметры: RouteFilter (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3dc1b-129">Parameters: RouteFilter (ByValue)</span></span>

## <span data-ttu-id="3dc1b-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc1b-130">OUTPUTS</span></span>

### <span data-ttu-id="3dc1b-131">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="3dc1b-131">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="3dc1b-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dc1b-132">NOTES</span></span>

## <span data-ttu-id="3dc1b-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dc1b-133">RELATED LINKS</span></span>
