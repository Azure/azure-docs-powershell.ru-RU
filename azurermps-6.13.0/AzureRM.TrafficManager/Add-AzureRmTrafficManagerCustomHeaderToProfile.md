---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: c14854da187101f3b15db178c656005942c1bff0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568822"
---
# <span data-ttu-id="58def-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="58def-101">Add-AzureRmTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="58def-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58def-102">SYNOPSIS</span></span>
<span data-ttu-id="58def-103">Добавляет пользовательские данные заголовка в объект профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="58def-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58def-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58def-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58def-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58def-105">DESCRIPTION</span></span>
<span data-ttu-id="58def-106">Командлет **Add-AzureRmTrafficManagerCustomHeaderToProfile** добавляет сведения о настраиваемом заголовке в локальный объект профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="58def-106">The **Add-AzureRmTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="58def-107">Вы можете получить профиль, используя командлеты New-AzureRmTrafficManagerProfile или Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="58def-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="58def-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="58def-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="58def-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58def-110">EXAMPLES</span></span>

### <span data-ttu-id="58def-111">Пример 1: Добавление сведений о настраиваемом заголовке к профилю</span><span class="sxs-lookup"><span data-stu-id="58def-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="58def-112">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="58def-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="58def-113">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="58def-114">Вторая команда добавляет сведения о настраиваемом заголовке в профиль, хранящийся в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="58def-115">Последняя команда обновляет профиль в диспетчере трафика таким образом, чтобы он соответствовал локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="58def-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58def-116">PARAMETERS</span></span>

### <span data-ttu-id="58def-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58def-117">-DefaultProfile</span></span>
<span data-ttu-id="58def-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58def-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58def-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58def-119">-Name</span></span>
<span data-ttu-id="58def-120">Задает имя добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="58def-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="58def-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58def-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="58def-122">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="58def-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="58def-123">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="58def-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="58def-124">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="58def-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="58def-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="58def-125">-Value</span></span>
<span data-ttu-id="58def-126">Задает значение добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="58def-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="58def-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58def-127">-Confirm</span></span>
<span data-ttu-id="58def-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58def-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58def-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58def-129">-WhatIf</span></span>
<span data-ttu-id="58def-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58def-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58def-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58def-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58def-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58def-132">CommonParameters</span></span>
<span data-ttu-id="58def-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58def-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58def-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58def-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58def-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58def-135">INPUTS</span></span>

### <span data-ttu-id="58def-136">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58def-136">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="58def-137">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="58def-137">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="58def-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58def-138">OUTPUTS</span></span>

### <span data-ttu-id="58def-139">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58def-139">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="58def-140">Этот командлет возвращает модифицированный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="58def-140">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="58def-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="58def-141">NOTES</span></span>

## <span data-ttu-id="58def-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58def-142">RELATED LINKS</span></span>

[<span data-ttu-id="58def-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="58def-143">Remove-AzureRmTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="58def-144">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58def-144">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="58def-145">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="58def-145">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)
