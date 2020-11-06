---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D344
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 0971a4b8d485c1590794de6f1b6c2d4d9d21da4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558152"
---
# <span data-ttu-id="c56c4-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="c56c4-101">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="c56c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c56c4-102">SYNOPSIS</span></span>
<span data-ttu-id="c56c4-103">Удаляет ожидаемый диапазон кодов состояния из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="c56c4-103">Removes an expected status code range from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c56c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c56c4-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c56c4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c56c4-105">DESCRIPTION</span></span>
<span data-ttu-id="c56c4-106">Командлет **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** удаляет диапазон ожидаемых кодов состояния из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="c56c4-106">The **Remove-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet removes a range of expected status codes from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="c56c4-107">Вы можете получить профиль, используя командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c56c4-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="c56c4-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="c56c4-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="c56c4-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c56c4-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="c56c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c56c4-110">EXAMPLES</span></span>

### <span data-ttu-id="c56c4-111">Пример 1: удаление ожидаемого диапазона кодов состояния из профиля</span><span class="sxs-lookup"><span data-stu-id="c56c4-111">Example 1: Remove an expected status code range from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="c56c4-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c56c4-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="c56c4-113">Вторая команда удаляет ожидаемый диапазон кода состояния из профиля, который хранится в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c56c4-113">The second command removes an expected status code range from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="c56c4-114">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c56c4-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="c56c4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c56c4-115">PARAMETERS</span></span>

### <span data-ttu-id="c56c4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-116">-DefaultProfile</span></span>
<span data-ttu-id="c56c4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c56c4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c56c4-118">— Минимум</span><span class="sxs-lookup"><span data-stu-id="c56c4-118">-Min</span></span>
<span data-ttu-id="c56c4-119">Указывает наименьшее значение в диапазоне кода состояния, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c56c4-119">Specifies the lowest value in the status code range to be removed.</span></span>

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

### <span data-ttu-id="c56c4-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="c56c4-121">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c56c4-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="c56c4-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="c56c4-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c56c4-123">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="c56c4-123">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="c56c4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c56c4-124">-Confirm</span></span>
<span data-ttu-id="c56c4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c56c4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c56c4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c56c4-126">-WhatIf</span></span>
<span data-ttu-id="c56c4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c56c4-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c56c4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c56c4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c56c4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c56c4-129">CommonParameters</span></span>
<span data-ttu-id="c56c4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c56c4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c56c4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c56c4-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c56c4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c56c4-132">INPUTS</span></span>

### <span data-ttu-id="c56c4-133">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-133">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c56c4-134">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="c56c4-134">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="c56c4-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c56c4-135">OUTPUTS</span></span>

### <span data-ttu-id="c56c4-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="c56c4-137">Этот командлет возвращает модифицированный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="c56c4-137">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="c56c4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="c56c4-138">NOTES</span></span>

## <span data-ttu-id="c56c4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c56c4-139">RELATED LINKS</span></span>

[<span data-ttu-id="c56c4-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="c56c4-140">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Add-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="c56c4-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="c56c4-142">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c56c4-142">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
