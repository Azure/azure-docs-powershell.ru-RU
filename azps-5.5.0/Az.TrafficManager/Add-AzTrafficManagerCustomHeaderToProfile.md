---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToProfile.md
ms.openlocfilehash: b90e83a403be59f5c454c0c055f0fe4719c3116f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241600"
---
# <span data-ttu-id="03ece-101">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-101">Add-AzTrafficManagerCustomHeaderToProfile</span></span>

## <span data-ttu-id="03ece-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03ece-102">SYNOPSIS</span></span>
<span data-ttu-id="03ece-103">Добавляет пользовательские сведения о загонах в локальный объект профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="03ece-103">Adds custom header information to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="03ece-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="03ece-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToProfile -Name <String> -Value <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="03ece-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03ece-105">DESCRIPTION</span></span>
<span data-ttu-id="03ece-106">Cmdlet **Add-AzTrafficManagerCustomHeaderToProfile** добавляет сведения настраиваемого заголовок в локальный объект профиля Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="03ece-106">The **Add-AzTrafficManagerCustomHeaderToProfile** cmdlet adds custom header information to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="03ece-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="03ece-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="03ece-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="03ece-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="03ece-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="03ece-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="03ece-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="03ece-110">EXAMPLES</span></span>

### <span data-ttu-id="03ece-111">Пример 1. Добавление пользовательских данных в профиль</span><span class="sxs-lookup"><span data-stu-id="03ece-111">Example 1: Add custom header information to a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerCustomHeaderToProfile -TrafficManagerProfile $TrafficManagerProfile -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="03ece-112">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="03ece-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="03ece-113">Команда сохраняет локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="03ece-113">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>
<span data-ttu-id="03ece-114">Вторая команда добавляет пользовательские сведения о заглавных $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="03ece-114">The second command adds custom header information to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="03ece-115">Конечная команда обновляет профиль Диспетчера трафика в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="03ece-115">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="03ece-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03ece-116">PARAMETERS</span></span>

### <span data-ttu-id="03ece-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-117">-DefaultProfile</span></span>
<span data-ttu-id="03ece-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03ece-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03ece-119">-Name</span><span class="sxs-lookup"><span data-stu-id="03ece-119">-Name</span></span>
<span data-ttu-id="03ece-120">Определяет имя добавляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="03ece-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="03ece-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="03ece-122">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="03ece-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="03ece-123">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="03ece-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="03ece-124">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="03ece-124">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="03ece-125">-Значение</span><span class="sxs-lookup"><span data-stu-id="03ece-125">-Value</span></span>
<span data-ttu-id="03ece-126">Определяет значение добавляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="03ece-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="03ece-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03ece-127">-Confirm</span></span>
<span data-ttu-id="03ece-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="03ece-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03ece-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03ece-129">-WhatIf</span></span>
<span data-ttu-id="03ece-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03ece-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03ece-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="03ece-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03ece-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03ece-132">CommonParameters</span></span>
<span data-ttu-id="03ece-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03ece-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03ece-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03ece-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03ece-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="03ece-135">INPUTS</span></span>

### <span data-ttu-id="03ece-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="03ece-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="03ece-137">OUTPUTS</span></span>

### <span data-ttu-id="03ece-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="03ece-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="03ece-139">NOTES</span></span>

## <span data-ttu-id="03ece-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03ece-140">RELATED LINKS</span></span>

[<span data-ttu-id="03ece-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-141">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>](./Remove-AzTrafficManagerCustomHeaderFromProfile.md)

[<span data-ttu-id="03ece-142">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-142">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="03ece-143">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="03ece-143">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
