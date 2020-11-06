---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D340
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagerexpectedstatuscoderange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerExpectedStatusCodeRange.md
ms.openlocfilehash: 32a00a6dce3d6a370f7b7f79f05794a312277a09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556451"
---
# <span data-ttu-id="971cf-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="971cf-101">Add-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>

## <span data-ttu-id="971cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="971cf-102">SYNOPSIS</span></span>
<span data-ttu-id="971cf-103">Добавляет ожидаемый диапазон кодов состояния к локальному объекту профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="971cf-103">Adds an expected status code range to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="971cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="971cf-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerExpectedStatusCodeRange -Min <Int32> -Max <Int32>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="971cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="971cf-105">DESCRIPTION</span></span>
<span data-ttu-id="971cf-106">Командлет **Add-AzureRmTrafficManagerExpectedStatusCodeRange** добавляет диапазон ожидаемых кодов состояния в локальный объект профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="971cf-106">The **Add-AzureRmTrafficManagerExpectedStatusCodeRange** cmdlet adds a range of expected status codes to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="971cf-107">Вы можете получить профиль, используя командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="971cf-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="971cf-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="971cf-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="971cf-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="971cf-110">EXAMPLES</span></span>

### <span data-ttu-id="971cf-111">Пример 1: Добавление диапазона кода ожидаемого состояния к профилю</span><span class="sxs-lookup"><span data-stu-id="971cf-111">Example 1: Add an expected status code range to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerExpectedStatusCodeRange -TrafficManagerProfile $TrafficManagerProfile -Min 200 -Max 499
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="971cf-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="971cf-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="971cf-113">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="971cf-114">Вторая команда добавляет ожидаемый диапазон кода состояния в профиль, хранящийся в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-114">The second command adds an expected status code range to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="971cf-115">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="971cf-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="971cf-116">PARAMETERS</span></span>

### <span data-ttu-id="971cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-117">-DefaultProfile</span></span>
<span data-ttu-id="971cf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="971cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="971cf-119">-Max</span><span class="sxs-lookup"><span data-stu-id="971cf-119">-Max</span></span>
<span data-ttu-id="971cf-120">Указывает наибольшее значение в диапазоне кода состояния, которое нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="971cf-120">Specifies the highest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="971cf-121">— Минимум</span><span class="sxs-lookup"><span data-stu-id="971cf-121">-Min</span></span>
<span data-ttu-id="971cf-122">Указывает наименьшее значение в диапазоне кода состояния, которое нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="971cf-122">Specifies the lowest value in the status code range to be added.</span></span>

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

### <span data-ttu-id="971cf-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="971cf-124">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="971cf-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="971cf-125">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="971cf-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="971cf-126">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="971cf-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="971cf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="971cf-127">-Confirm</span></span>
<span data-ttu-id="971cf-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="971cf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="971cf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="971cf-129">-WhatIf</span></span>
<span data-ttu-id="971cf-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="971cf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="971cf-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="971cf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="971cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="971cf-132">CommonParameters</span></span>
<span data-ttu-id="971cf-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="971cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="971cf-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="971cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="971cf-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="971cf-135">INPUTS</span></span>

### <span data-ttu-id="971cf-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="971cf-137">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="971cf-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="971cf-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="971cf-138">OUTPUTS</span></span>

### <span data-ttu-id="971cf-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="971cf-140">Этот командлет возвращает модифицированный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="971cf-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="971cf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="971cf-141">NOTES</span></span>

## <span data-ttu-id="971cf-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="971cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="971cf-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="971cf-143">Remove-AzureRmTrafficManagerExpectedStatusCodeRange</span></span>](./Remove-AzureRmTrafficManagerExpectedStatusCodeRange.md)

[<span data-ttu-id="971cf-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="971cf-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="971cf-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
