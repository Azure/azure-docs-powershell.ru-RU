---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243573"
---
# <span data-ttu-id="e0bfc-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="e0bfc-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="e0bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="e0bfc-103">Создание объекта PSLoadBalancingSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="e0bfc-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="e0bfc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0bfc-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0bfc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0bfc-105">DESCRIPTION</span></span>
<span data-ttu-id="e0bfc-106">Создание объекта PSLoadBalancingSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="e0bfc-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="e0bfc-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0bfc-107">EXAMPLES</span></span>

### <span data-ttu-id="e0bfc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0bfc-108">Example 1</span></span>
```powershell
PS C:\> New-AzFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="e0bfc-109">Создание объекта PSLoadBalancingSetting для создания передней двери</span><span class="sxs-lookup"><span data-stu-id="e0bfc-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="e0bfc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0bfc-110">PARAMETERS</span></span>

### <span data-ttu-id="e0bfc-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="e0bfc-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="e0bfc-112">Дополнительные задержки в миллисекундах для кеглей попадают в сегмент наименьшей задержки.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="e0bfc-113">Значение по умолчанию — 0</span><span class="sxs-lookup"><span data-stu-id="e0bfc-113">Default value is 0</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0bfc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0bfc-114">-DefaultProfile</span></span>
<span data-ttu-id="e0bfc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0bfc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e0bfc-116">-Name</span></span>
<span data-ttu-id="e0bfc-117">имя параметра health в настройках.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-117">health probe setting name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0bfc-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="e0bfc-118">-SampleSize</span></span>
<span data-ttu-id="e0bfc-119">Количество выборок, которые следует рассмотреть для принятия решений по балансировке нагрузки.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="e0bfc-120">Значение по умолчанию — 4</span><span class="sxs-lookup"><span data-stu-id="e0bfc-120">Default value is 4</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0bfc-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="e0bfc-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="e0bfc-122">Количество выборок в течение примера, которые должны быть успешными, — 2</span><span class="sxs-lookup"><span data-stu-id="e0bfc-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0bfc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0bfc-123">CommonParameters</span></span>
<span data-ttu-id="e0bfc-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0bfc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0bfc-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0bfc-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0bfc-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0bfc-126">INPUTS</span></span>

### <span data-ttu-id="e0bfc-127">Нет</span><span class="sxs-lookup"><span data-stu-id="e0bfc-127">None</span></span>

## <span data-ttu-id="e0bfc-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0bfc-128">OUTPUTS</span></span>

### <span data-ttu-id="e0bfc-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="e0bfc-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="e0bfc-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0bfc-130">NOTES</span></span>

## <span data-ttu-id="e0bfc-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0bfc-131">RELATED LINKS</span></span>

<span data-ttu-id="e0bfc-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="e0bfc-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>
