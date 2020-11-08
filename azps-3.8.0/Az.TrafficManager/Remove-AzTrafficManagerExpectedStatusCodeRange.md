---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: fdada94847fdf2f83141f7cca63da61ead6fcd2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072600"
---
# <span data-ttu-id="fd8b7-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="fd8b7-101">Remove-AzTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="fd8b7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd8b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fd8b7-103">Удаляет ожидаемый диапазон кодов состояния из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="fd8b7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd8b7-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd8b7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8b7-105">DESCRIPTION</span></span>
<span data-ttu-id="fd8b7-106">Командлет **Remove-AzTrafficManagerExpectedStatusCodeRange** удаляет диапазон ожидаемых кодов состояния из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-106">The **Remove-AzTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="fd8b7-107">Вы можете получить профиль, используя командлеты New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="fd8b7-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="fd8b7-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="fd8b7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd8b7-110">EXAMPLES</span></span>

### <span data-ttu-id="fd8b7-111">Пример 1: удаление ожидаемого диапазона кодов состояния из профиля</span><span class="sxs-lookup"><span data-stu-id="fd8b7-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="fd8b7-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="fd8b7-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="fd8b7-113">Вторая команда удаляет ожидаемый диапазон кода состояния из профиля, который хранится в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="fd8b7-114">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="fd8b7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd8b7-115">PARAMETERS</span></span>

### <span data-ttu-id="fd8b7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-116">-DefaultProfile</span></span>
<span data-ttu-id="fd8b7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd8b7-118">— Минимум</span><span class="sxs-lookup"><span data-stu-id="fd8b7-118">-Min</span></span>
<span data-ttu-id="fd8b7-119">Указывает наименьшее значение в диапазоне кода состояния, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="fd8b7-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="fd8b7-121">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="fd8b7-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="fd8b7-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="fd8b7-123">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="fd8b7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd8b7-124">-Confirm</span></span>
<span data-ttu-id="fd8b7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd8b7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd8b7-126">-WhatIf</span></span>
<span data-ttu-id="fd8b7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd8b7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd8b7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd8b7-129">CommonParameters</span></span>
<span data-ttu-id="fd8b7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd8b7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd8b7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd8b7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd8b7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd8b7-132">INPUTS</span></span>

### <span data-ttu-id="fd8b7-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fd8b7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd8b7-134">OUTPUTS</span></span>

### <span data-ttu-id="fd8b7-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="fd8b7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd8b7-136">NOTES</span></span>

## <span data-ttu-id="fd8b7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd8b7-137">RELATED LINKS</span></span>

[<span data-ttu-id="fd8b7-138">Add-AzTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="fd8b7-138">Add-AzTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="fd8b7-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="fd8b7-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="fd8b7-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
