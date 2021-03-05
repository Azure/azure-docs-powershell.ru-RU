---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 8e79fe1a0d0cc1c681c88cb3d5dfdd8d48dfd26b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987258"
---
# <span data-ttu-id="f3113-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f3113-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="f3113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3113-102">SYNOPSIS</span></span>
<span data-ttu-id="f3113-103">Удаляет ожидаемый диапазон кода состояния из объекта локального профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f3113-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f3113-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f3113-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3113-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3113-105">DESCRIPTION</span></span>
<span data-ttu-id="f3113-106">Для **удаления диапазона** ожидаемых кодов состояния из локального объекта профиля Azure Traffic Manager удаляется диапазон ожидаемых кодов состояния.</span><span class="sxs-lookup"><span data-stu-id="f3113-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f3113-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f3113-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f3113-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="f3113-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f3113-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="f3113-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="f3113-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f3113-110">EXAMPLES</span></span>

### <span data-ttu-id="f3113-111">Пример 1. Удаление ожидаемого диапазона кода состояния из профиля</span><span class="sxs-lookup"><span data-stu-id="f3113-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f3113-112">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="f3113-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f3113-113">Вторая команда удаляет ожидаемый диапазон кода состояния из профиля, храняого в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f3113-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f3113-114">Конечная команда обновляет профиль Диспетчера трафика в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f3113-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f3113-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3113-115">PARAMETERS</span></span>

### <span data-ttu-id="f3113-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-116">-DefaultProfile</span></span>
<span data-ttu-id="f3113-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3113-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3113-118">-Min</span><span class="sxs-lookup"><span data-stu-id="f3113-118">-Min</span></span>
<span data-ttu-id="f3113-119">Указывает наименьшее значение в диапазоне кода состояния, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f3113-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="f3113-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="f3113-121">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="f3113-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f3113-122">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="f3113-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f3113-123">Чтобы получить объект **TrafficManagerProfile,** воспользуйтесь Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="f3113-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="f3113-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3113-124">-Confirm</span></span>
<span data-ttu-id="f3113-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f3113-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3113-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3113-126">-WhatIf</span></span>
<span data-ttu-id="f3113-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3113-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3113-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f3113-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3113-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3113-129">CommonParameters</span></span>
<span data-ttu-id="f3113-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3113-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3113-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3113-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3113-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3113-132">INPUTS</span></span>

### <span data-ttu-id="f3113-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f3113-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f3113-134">OUTPUTS</span></span>

### <span data-ttu-id="f3113-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f3113-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f3113-136">NOTES</span></span>

## <span data-ttu-id="f3113-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3113-137">RELATED LINKS</span></span>

[<span data-ttu-id="f3113-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="f3113-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="f3113-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f3113-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f3113-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
