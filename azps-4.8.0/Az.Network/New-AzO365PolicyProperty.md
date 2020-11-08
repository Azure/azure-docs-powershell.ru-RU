---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244818"
---
# <span data-ttu-id="f0938-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="f0938-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="f0938-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f0938-102">SYNOPSIS</span></span>
<span data-ttu-id="f0938-103">Создание объекта политики передачи трафика в Office 365.</span><span class="sxs-lookup"><span data-stu-id="f0938-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="f0938-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f0938-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0938-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0938-105">DESCRIPTION</span></span>
<span data-ttu-id="f0938-106">Создание политики Office 365 для использования с командлетами New-AzVpnSite и Update-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="f0938-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="f0938-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f0938-107">EXAMPLES</span></span>

### <span data-ttu-id="f0938-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0938-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="f0938-109">Создание политики трафика Office 365 с разрешенными помещениями для разрешения и оптимизации категории трафика.</span><span class="sxs-lookup"><span data-stu-id="f0938-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="f0938-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f0938-110">PARAMETERS</span></span>

### <span data-ttu-id="f0938-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="f0938-111">-Allow</span></span>
<span data-ttu-id="f0938-112">Выступающий трафик категории Allowed.</span><span class="sxs-lookup"><span data-stu-id="f0938-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="f0938-113">-Default</span><span class="sxs-lookup"><span data-stu-id="f0938-113">-Default</span></span>
<span data-ttu-id="f0938-114">Изменяйте трафик по категориям по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f0938-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="f0938-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0938-115">-DefaultProfile</span></span>
<span data-ttu-id="f0938-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0938-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0938-117">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="f0938-117">-Optimize</span></span>
<span data-ttu-id="f0938-118">Выступающий трафик оптимизации категории.</span><span class="sxs-lookup"><span data-stu-id="f0938-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="f0938-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0938-119">CommonParameters</span></span>
<span data-ttu-id="f0938-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f0938-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0938-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0938-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0938-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f0938-122">INPUTS</span></span>

### <span data-ttu-id="f0938-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f0938-123">None</span></span>

## <span data-ttu-id="f0938-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0938-124">OUTPUTS</span></span>

### <span data-ttu-id="f0938-125">Microsoft. Azure. Commands. Network. Models. PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="f0938-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="f0938-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f0938-126">NOTES</span></span>

## <span data-ttu-id="f0938-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0938-127">RELATED LINKS</span></span>
