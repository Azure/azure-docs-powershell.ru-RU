---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoorloadbalancingsettingobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoorLoadBalancingSettingObject.md
ms.openlocfilehash: de13a33aeaf60dbd83fcacebb8380bee27c18c46
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560908"
---
# <span data-ttu-id="3a71a-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span><span class="sxs-lookup"><span data-stu-id="3a71a-101">New-AzureRmFrontDoorLoadBalancingSettingObject</span></span>

## <span data-ttu-id="3a71a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3a71a-102">SYNOPSIS</span></span>
<span data-ttu-id="3a71a-103">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3a71a-103">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a71a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3a71a-104">SYNTAX</span></span>

```
New-AzureRmFrontDoorLoadBalancingSettingObject -Name <String> [-SampleSize <Int32>]
 [-SuccessfulSamplesRequired <Int32>] [-AdditionalLatencyInMilliseconds <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a71a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a71a-105">DESCRIPTION</span></span>
<span data-ttu-id="3a71a-106">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3a71a-106">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="3a71a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3a71a-107">EXAMPLES</span></span>

### <span data-ttu-id="3a71a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3a71a-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmFrontDoorLoadBalancingSettingObject -Name "loadbalancingsetting1"


SampleSize                    : 4
AdditionalLatencyMilliseconds : 0
SuccessfulSamplesRequired     : 2
ResourceState                 :
Id                            :
Name                          : loadbalancingsetting1
Type                          :
```

<span data-ttu-id="3a71a-109">Создание объекта PSLoadBalancingSetting для создания передней дверцы</span><span class="sxs-lookup"><span data-stu-id="3a71a-109">Create a PSLoadBalancingSetting object for Front Door creation</span></span>

## <span data-ttu-id="3a71a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3a71a-110">PARAMETERS</span></span>

### <span data-ttu-id="3a71a-111">-AdditionalLatencyInMilliseconds</span><span class="sxs-lookup"><span data-stu-id="3a71a-111">-AdditionalLatencyInMilliseconds</span></span>
<span data-ttu-id="3a71a-112">Дополнительная задержка (в миллисекундах), с которой зонды должны попадать в сегмент минимальной задержки.</span><span class="sxs-lookup"><span data-stu-id="3a71a-112">The additional latency in milliseconds for probes to fall into the lowest latency bucket.</span></span> <span data-ttu-id="3a71a-113">Значение по умолчанию: 0</span><span class="sxs-lookup"><span data-stu-id="3a71a-113">Default value is 0</span></span>

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

### <span data-ttu-id="3a71a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a71a-114">-DefaultProfile</span></span>
<span data-ttu-id="3a71a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3a71a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a71a-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3a71a-116">-Name</span></span>
<span data-ttu-id="3a71a-117">имя параметра проверки работоспособности.</span><span class="sxs-lookup"><span data-stu-id="3a71a-117">health probe setting name.</span></span>

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

### <span data-ttu-id="3a71a-118">-SampleSize</span><span class="sxs-lookup"><span data-stu-id="3a71a-118">-SampleSize</span></span>
<span data-ttu-id="3a71a-119">Количество примеров для принятия решений об балансировке нагрузки.</span><span class="sxs-lookup"><span data-stu-id="3a71a-119">The number of samples to consider for load balancing decisions.</span></span>
<span data-ttu-id="3a71a-120">Значение по умолчанию — 4</span><span class="sxs-lookup"><span data-stu-id="3a71a-120">Default value is 4</span></span>

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

### <span data-ttu-id="3a71a-121">-SuccessfulSamplesRequired</span><span class="sxs-lookup"><span data-stu-id="3a71a-121">-SuccessfulSamplesRequired</span></span>
<span data-ttu-id="3a71a-122">Количество образцов в периоде выборки, которые должны успешно пройти по умолчанию: 2</span><span class="sxs-lookup"><span data-stu-id="3a71a-122">The number of samples within the sample period that must succeed Default value is 2</span></span>

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

### <span data-ttu-id="3a71a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a71a-123">CommonParameters</span></span>
<span data-ttu-id="3a71a-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3a71a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a71a-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a71a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a71a-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3a71a-126">INPUTS</span></span>

### <span data-ttu-id="3a71a-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="3a71a-127">None</span></span>

## <span data-ttu-id="3a71a-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3a71a-128">OUTPUTS</span></span>

### <span data-ttu-id="3a71a-129">Microsoft. Azure. Commands. FrontDoor. Models. PSLoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="3a71a-129">Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting</span></span>

## <span data-ttu-id="3a71a-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3a71a-130">NOTES</span></span>

## <span data-ttu-id="3a71a-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3a71a-131">RELATED LINKS</span></span>

<span data-ttu-id="3a71a-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="3a71a-132">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)</span></span>
