---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066121"
---
# <span data-ttu-id="5a481-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5a481-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="5a481-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a481-102">SYNOPSIS</span></span>
<span data-ttu-id="5a481-103">Добавляет ожидаемый диапазон кодов состояния к локальному объекту профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="5a481-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="5a481-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a481-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5a481-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a481-105">DESCRIPTION</span></span>
<span data-ttu-id="5a481-106">Командлет **Add-AzTrafficManagerExpectedStatusCodeRange** добавляет диапазон ожидаемых кодов состояния в локальный объект профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="5a481-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="5a481-107">Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="5a481-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="5a481-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="5a481-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="5a481-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a481-110">EXAMPLES</span></span>

### <span data-ttu-id="5a481-111">Пример 1: Добавление диапазона кода ожидаемого состояния к профилю</span><span class="sxs-lookup"><span data-stu-id="5a481-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="5a481-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="5a481-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="5a481-113">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="5a481-114">Вторая команда добавляет ожидаемый диапазон кода состояния в профиль, хранящийся в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="5a481-115">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="5a481-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a481-116">PARAMETERS</span></span>

### <span data-ttu-id="5a481-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-117">-DefaultProfile</span></span>
<span data-ttu-id="5a481-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a481-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a481-119">-Max</span><span class="sxs-lookup"><span data-stu-id="5a481-119">-Max</span></span>
<span data-ttu-id="5a481-120">Указывает наибольшее значение в диапазоне кода состояния, которое нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="5a481-120">Specifies the highest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a481-121">— Минимум</span><span class="sxs-lookup"><span data-stu-id="5a481-121">-Min</span></span>
<span data-ttu-id="5a481-122">Указывает наименьшее значение в диапазоне кода состояния, которое нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="5a481-122">Specifies the lowest value in the status code range to be added.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a481-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="5a481-124">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="5a481-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5a481-125">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="5a481-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="5a481-126">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5a481-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a481-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a481-127">-Confirm</span></span>
<span data-ttu-id="5a481-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a481-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a481-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a481-129">-WhatIf</span></span>
<span data-ttu-id="5a481-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a481-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a481-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a481-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a481-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a481-132">CommonParameters</span></span>
<span data-ttu-id="5a481-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a481-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a481-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a481-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a481-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a481-135">INPUTS</span></span>

### <span data-ttu-id="5a481-136">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5a481-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a481-137">OUTPUTS</span></span>

### <span data-ttu-id="5a481-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5a481-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a481-139">NOTES</span></span>

## <span data-ttu-id="5a481-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a481-140">RELATED LINKS</span></span>

[<span data-ttu-id="5a481-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="5a481-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="5a481-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5a481-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5a481-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
