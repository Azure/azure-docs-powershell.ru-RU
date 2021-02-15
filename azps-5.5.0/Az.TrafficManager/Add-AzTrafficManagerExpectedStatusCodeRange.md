---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: ee249b7e3d811a527a9322e09ba65075883e73b6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232388"
---
# <span data-ttu-id="02b35-101">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="02b35-101">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="02b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02b35-102">SYNOPSIS</span></span>
<span data-ttu-id="02b35-103">Добавляет ожидаемый диапазон кода состояния в локальный объект профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="02b35-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="02b35-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02b35-104">SYNTAX</span></span>

```
Add-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02b35-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02b35-105">DESCRIPTION</span></span>
<span data-ttu-id="02b35-106">Чтобы добавить диапазон ожидаемых кодов состояния в локальный объект профиля Azure Traffic Manager, можно использовать **cmdlet Add-AzTrafficManagerExpectedStatusCodeRange.**</span><span class="sxs-lookup"><span data-stu-id="02b35-106">The **Add-AzTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="02b35-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02b35-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="02b35-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="02b35-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="02b35-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="02b35-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="02b35-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02b35-110">EXAMPLES</span></span>

### <span data-ttu-id="02b35-111">Пример 1. Добавление ожидаемого диапазона кода состояния в профиль</span><span class="sxs-lookup"><span data-stu-id="02b35-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="02b35-112">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="02b35-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="02b35-113">Команда сохраняет локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02b35-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="02b35-114">Вторая команда добавляет ожидаемый диапазон кода состояния в профиль, $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02b35-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="02b35-115">Конечная команда обновляет профиль Диспетчера трафика в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="02b35-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="02b35-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02b35-116">PARAMETERS</span></span>

### <span data-ttu-id="02b35-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-117">-DefaultProfile</span></span>
<span data-ttu-id="02b35-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02b35-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02b35-119">-Max</span><span class="sxs-lookup"><span data-stu-id="02b35-119">-Max</span></span>
<span data-ttu-id="02b35-120">Указывает самое высокое значение в диапазоне кода состояния, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="02b35-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="02b35-121">-Min</span><span class="sxs-lookup"><span data-stu-id="02b35-121">-Min</span></span>
<span data-ttu-id="02b35-122">Указывает наименьшее значение в диапазоне кода состояния, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="02b35-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="02b35-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="02b35-124">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="02b35-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="02b35-125">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="02b35-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="02b35-126">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="02b35-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="02b35-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02b35-127">-Confirm</span></span>
<span data-ttu-id="02b35-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b35-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02b35-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02b35-129">-WhatIf</span></span>
<span data-ttu-id="02b35-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02b35-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02b35-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02b35-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02b35-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02b35-132">CommonParameters</span></span>
<span data-ttu-id="02b35-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02b35-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02b35-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02b35-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02b35-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02b35-135">INPUTS</span></span>

### <span data-ttu-id="02b35-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="02b35-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02b35-137">OUTPUTS</span></span>

### <span data-ttu-id="02b35-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="02b35-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02b35-139">NOTES</span></span>

## <span data-ttu-id="02b35-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02b35-140">RELATED LINKS</span></span>

[<span data-ttu-id="02b35-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="02b35-141">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="02b35-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="02b35-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="02b35-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
