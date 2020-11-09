---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: e9195a60b06f206a5b3133834f19cfdab68db31b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247413"
---
# <span data-ttu-id="362d6-101">New-AzFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="362d6-101">New-AzFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="362d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="362d6-102">SYNOPSIS</span></span>
<span data-ttu-id="362d6-103">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="362d6-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="362d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="362d6-104">SYNTAX</span></span>

```
New-AzFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="362d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="362d6-105">DESCRIPTION</span></span>
<span data-ttu-id="362d6-106">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="362d6-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="362d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="362d6-107">EXAMPLES</span></span>

### <span data-ttu-id="362d6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="362d6-108">Example 1</span></span>
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

<span data-ttu-id="362d6-109">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="362d6-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="362d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="362d6-110">PARAMETERS</span></span>

### <span data-ttu-id="362d6-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="362d6-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="362d6-112">Дополнительная задержка (в миллисекундах), с которой зонды должны попадать в сегмент минимальной задержки.</span><span class="sxs-lookup"><span data-stu-id="362d6-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="362d6-113">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="362d6-113">Default value is 0</span></span>

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

### <span data-ttu-id="362d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="362d6-114">-DefaultProfile</span></span>
<span data-ttu-id="362d6-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="362d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="362d6-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="362d6-116">-Name</span></span>
<span data-ttu-id="362d6-117">имя параметра проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="362d6-117">health probe setting name.</span></span>

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

### <span data-ttu-id="362d6-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="362d6-118">-SampleSize</span></span>
<span data-ttu-id="362d6-119">Количество примеров для принятия решений об балансировке нагрузки.</span><span class="sxs-lookup"><span data-stu-id="362d6-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="362d6-120">Значение по умолчанию — 4</span><span class="sxs-lookup"><span data-stu-id="362d6-120">Default value is 4</span></span>

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

### <span data-ttu-id="362d6-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="362d6-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="362d6-122">Количество образцов в периоде выборки, которые должны успешно пройти по умолчанию: 2</span><span class="sxs-lookup"><span data-stu-id="362d6-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="362d6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="362d6-123">CommonParameters</span></span>
<span data-ttu-id="362d6-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="362d6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="362d6-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="362d6-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="362d6-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="362d6-126">INPUTS</span></span>

### <span data-ttu-id="362d6-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="362d6-127">None</span></span>

## <span data-ttu-id="362d6-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="362d6-128">OUTPUTS</span></span>

### <span data-ttu-id="362d6-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="362d6-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="362d6-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="362d6-130">NOTES</span></span>

## <span data-ttu-id="362d6-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="362d6-131">RELATED LINKS</span></span>

<span data-ttu-id="362d6-132">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="362d6-132">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)</span></span>