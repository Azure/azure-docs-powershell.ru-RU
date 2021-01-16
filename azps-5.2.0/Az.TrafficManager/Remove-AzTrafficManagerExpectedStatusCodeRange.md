---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402084"
---
# <span data-ttu-id="39305-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="39305-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="39305-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39305-102">SYNOPSIS</span></span>
<span data-ttu-id="39305-103">Удаляет ожидаемый диапазон кода состояния из объекта локального профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="39305-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="39305-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="39305-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39305-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="39305-105">DESCRIPTION</span></span>
<span data-ttu-id="39305-106">Для **удаления диапазона** ожидаемых кодов состояния из локального объекта профиля Azure Traffic Manager удаляется диапазон ожидаемых кодов состояния.</span><span class="sxs-lookup"><span data-stu-id="39305-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="39305-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="39305-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="39305-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="39305-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="39305-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="39305-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="39305-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="39305-110">EXAMPLES</span></span>

### <span data-ttu-id="39305-111">Пример 1. Удаление ожидаемого диапазона кода состояния из профиля</span><span class="sxs-lookup"><span data-stu-id="39305-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="39305-112">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="39305-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="39305-113">Вторая команда удаляет ожидаемый диапазон кода состояния из профиля, храняного в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="39305-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="39305-114">Конечная команда обновляет профиль Диспетчера трафика в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="39305-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="39305-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39305-115">PARAMETERS</span></span>

### <span data-ttu-id="39305-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39305-116">-DefaultProfile</span></span>
<span data-ttu-id="39305-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="39305-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39305-118">-Min</span><span class="sxs-lookup"><span data-stu-id="39305-118">-Min</span></span>
<span data-ttu-id="39305-119">Указывает наименьшее значение в диапазоне кода состояния, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="39305-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="39305-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39305-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="39305-121">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="39305-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="39305-122">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="39305-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="39305-123">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="39305-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="39305-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39305-124">-Confirm</span></span>
<span data-ttu-id="39305-125">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39305-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39305-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39305-126">-WhatIf</span></span>
<span data-ttu-id="39305-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39305-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="39305-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="39305-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39305-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39305-129">CommonParameters</span></span>
<span data-ttu-id="39305-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39305-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39305-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39305-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39305-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="39305-132">INPUTS</span></span>

### <span data-ttu-id="39305-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39305-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="39305-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="39305-134">OUTPUTS</span></span>

### <span data-ttu-id="39305-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39305-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="39305-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="39305-136">NOTES</span></span>

## <span data-ttu-id="39305-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="39305-137">RELATED LINKS</span></span>

[<span data-ttu-id="39305-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="39305-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="39305-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39305-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="39305-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="39305-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
