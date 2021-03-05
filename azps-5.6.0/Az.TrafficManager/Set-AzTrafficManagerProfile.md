---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987213"
---
# <span data-ttu-id="5114d-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="5114d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5114d-102">SYNOPSIS</span></span>
<span data-ttu-id="5114d-103">Обновляет профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="5114d-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="5114d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5114d-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5114d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5114d-105">DESCRIPTION</span></span>
<span data-ttu-id="5114d-106">Cmdlet **Set-AzTrafficManagerProfile** обновляет профиль Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="5114d-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5114d-107">Этот cmdlet обновляет параметры профиля из локального объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="5114d-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="5114d-108">Объект профиля можно указать либо с помощью параметра *TrafficManagerProfile,* либо с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="5114d-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="5114d-109">Вы можете получить локальный объект, который представляет профиль, с помощью Get-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="5114d-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5114d-110">Измените объект локально, а затем с помощью **Set-AzTrafficManagerProfile** зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="5114d-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="5114d-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5114d-111">EXAMPLES</span></span>

### <span data-ttu-id="5114d-112">Пример 1. Обновление профиля</span><span class="sxs-lookup"><span data-stu-id="5114d-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="5114d-113">Первая команда получает профиль Диспетчера трафика Azure с помощью Get-AzTrafficManagerProfile командлета.</span><span class="sxs-lookup"><span data-stu-id="5114d-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5114d-114">Команда сохраняет профиль локально в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5114d-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="5114d-115">Вторая команда изменяет профиль локально.</span><span class="sxs-lookup"><span data-stu-id="5114d-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="5114d-116">Эта команда отключает профиль.</span><span class="sxs-lookup"><span data-stu-id="5114d-116">This command disables the profile.</span></span>

<span data-ttu-id="5114d-117">Третья команда обновляет профиль диспетчера трафика с именем ContosoProfile в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="5114d-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="5114d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5114d-118">PARAMETERS</span></span>

### <span data-ttu-id="5114d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-119">-DefaultProfile</span></span>
<span data-ttu-id="5114d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5114d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5114d-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="5114d-122">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="5114d-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="5114d-123">Этот командлет обновляет диспетчер трафика в связи с этим локальным объектом.</span><span class="sxs-lookup"><span data-stu-id="5114d-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="5114d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5114d-124">CommonParameters</span></span>
<span data-ttu-id="5114d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5114d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5114d-126">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5114d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5114d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5114d-127">INPUTS</span></span>

### <span data-ttu-id="5114d-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5114d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5114d-129">OUTPUTS</span></span>

### <span data-ttu-id="5114d-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="5114d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5114d-131">NOTES</span></span>

## <span data-ttu-id="5114d-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5114d-132">RELATED LINKS</span></span>

[<span data-ttu-id="5114d-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5114d-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5114d-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="5114d-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="5114d-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5114d-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5114d-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5114d-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


