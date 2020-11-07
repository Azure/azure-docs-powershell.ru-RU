---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728381"
---
# <span data-ttu-id="79eb4-101">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-101">Set-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="79eb4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79eb4-102">SYNOPSIS</span></span>
<span data-ttu-id="79eb4-103">Обновление профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="79eb4-103">Updates a Traffic Manager profile.</span></span>

## <span data-ttu-id="79eb4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79eb4-104">SYNTAX</span></span>

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79eb4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79eb4-105">DESCRIPTION</span></span>
<span data-ttu-id="79eb4-106">Командлет **Set-AzTrafficManagerProfile** обновляет профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="79eb4-106">The **Set-AzTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="79eb4-107">Этот командлет обновляет параметры профиля из локального объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="79eb4-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="79eb4-108">Вы можете указать объект профиля с помощью параметра *TrafficManagerProfile* или конвейера.</span><span class="sxs-lookup"><span data-stu-id="79eb4-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="79eb4-109">Вы можете получить локальный объект, представляющий профиль, с помощью командлета Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="79eb4-109">You can obtain a local object that represents a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="79eb4-110">Измените объект на локальном компьютере, а затем используйте **Set-AzTrafficManagerProfile** , чтобы зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="79eb4-110">Modify the object locally and then use **Set-AzTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="79eb4-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79eb4-111">EXAMPLES</span></span>

### <span data-ttu-id="79eb4-112">Пример 1: обновление профиля</span><span class="sxs-lookup"><span data-stu-id="79eb4-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="79eb4-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="79eb4-113">The first command gets an Azure Traffic Manager profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="79eb4-114">Команда хранит профиль локально в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="79eb4-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="79eb4-115">Вторая команда изменяет этот профиль локально.</span><span class="sxs-lookup"><span data-stu-id="79eb4-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="79eb4-116">Эта команда отключает профиль.</span><span class="sxs-lookup"><span data-stu-id="79eb4-116">This command disables the profile.</span></span>

<span data-ttu-id="79eb4-117">Третья команда обновляет профиль диспетчера трафика с именем ContosoProfile, чтобы соответствовать локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="79eb4-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="79eb4-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79eb4-118">PARAMETERS</span></span>

### <span data-ttu-id="79eb4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-119">-DefaultProfile</span></span>
<span data-ttu-id="79eb4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79eb4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79eb4-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="79eb4-122">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="79eb4-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="79eb4-123">Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.</span><span class="sxs-lookup"><span data-stu-id="79eb4-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="79eb4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79eb4-124">CommonParameters</span></span>
<span data-ttu-id="79eb4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79eb4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79eb4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79eb4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79eb4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79eb4-127">INPUTS</span></span>

### <span data-ttu-id="79eb4-128">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-128">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="79eb4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79eb4-129">OUTPUTS</span></span>

### <span data-ttu-id="79eb4-130">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-130">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="79eb4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="79eb4-131">NOTES</span></span>

## <span data-ttu-id="79eb4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79eb4-132">RELATED LINKS</span></span>

[<span data-ttu-id="79eb4-133">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="79eb4-133">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="79eb4-134">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-134">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="79eb4-135">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-135">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="79eb4-136">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="79eb4-136">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="79eb4-137">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="79eb4-137">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)


