---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D343
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromProfile.md
ms.openlocfilehash: 1026f5e34c2b8efc17503a81a521a0ceb3d92060
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991836"
---
# <span data-ttu-id="4775a-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-101">Remove-AzTrafficManagerCustomHeaderFromProfile</span></span>

## <span data-ttu-id="4775a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4775a-102">SYNOPSIS</span></span>
<span data-ttu-id="4775a-103">Удаляет пользовательские данные загона из локального объекта профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="4775a-103">Removes custom header information from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="4775a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4775a-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromProfile -Name <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4775a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4775a-105">DESCRIPTION</span></span>
<span data-ttu-id="4775a-106">Cmdlet **Remove-AzTrafficManagerCustomHeaderFromProfile** удаляет пользовательские данные заголовок из локального объекта профиля Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="4775a-106">The **Remove-AzTrafficManagerCustomHeaderFromProfile** cmdlet removes custom header information from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="4775a-107">Вы можете получить профиль с помощью New-AzTrafficManagerProfile или Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4775a-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="4775a-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="4775a-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="4775a-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="4775a-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>

## <span data-ttu-id="4775a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4775a-110">EXAMPLES</span></span>

### <span data-ttu-id="4775a-111">Пример 1. Удаление пользовательских данных загона из профиля</span><span class="sxs-lookup"><span data-stu-id="4775a-111">Example 1: Remove custom header information from a profile</span></span>
```
PS C:\> $TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerProfile $TrafficManagerProfile -Name "host"
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="4775a-112">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="4775a-112">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="4775a-113">Вторая команда удаляет пользовательские данные загона из профиля, храняного в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4775a-113">The second command removes custom header information from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="4775a-114">Конечная команда обновляет профиль Диспетчера трафика в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="4775a-114">The final command updates the profile in Traffic Manager to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="4775a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4775a-115">PARAMETERS</span></span>

### <span data-ttu-id="4775a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-116">-DefaultProfile</span></span>
<span data-ttu-id="4775a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4775a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4775a-118">-Name</span><span class="sxs-lookup"><span data-stu-id="4775a-118">-Name</span></span>
<span data-ttu-id="4775a-119">Указывает имя удаляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="4775a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="4775a-120">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-120">-TrafficManagerProfile</span></span>
<span data-ttu-id="4775a-121">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="4775a-121">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="4775a-122">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="4775a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4775a-123">Чтобы получить объект **TrafficManagerProfile,** воспользуйтесь Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="4775a-123">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="4775a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4775a-124">-Confirm</span></span>
<span data-ttu-id="4775a-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="4775a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4775a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4775a-126">-WhatIf</span></span>
<span data-ttu-id="4775a-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4775a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4775a-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4775a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4775a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4775a-129">CommonParameters</span></span>
<span data-ttu-id="4775a-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4775a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4775a-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4775a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4775a-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4775a-132">INPUTS</span></span>

### <span data-ttu-id="4775a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4775a-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4775a-134">OUTPUTS</span></span>

### <span data-ttu-id="4775a-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="4775a-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4775a-136">NOTES</span></span>

## <span data-ttu-id="4775a-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4775a-137">RELATED LINKS</span></span>

[<span data-ttu-id="4775a-138">Add-AzTrafficManagerCustomHeaderToProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-138">Add-AzTrafficManagerCustomHeaderToProfile</span></span>](./Add-AzTrafficManagerCustomHeaderToProfile.md)

[<span data-ttu-id="4775a-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="4775a-140">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4775a-140">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)
