---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/set-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Set-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 9536e6250f73270c7700a14406cb24b8e8f31189
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558143"
---
# <span data-ttu-id="9fff6-101">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-101">Set-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="9fff6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9fff6-102">SYNOPSIS</span></span>
<span data-ttu-id="9fff6-103">Обновление профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="9fff6-103">Updates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9fff6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9fff6-104">SYNTAX</span></span>

```
Set-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9fff6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fff6-105">DESCRIPTION</span></span>
<span data-ttu-id="9fff6-106">Командлет **Set-AzureRmTrafficManagerProfile** обновляет профиль диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="9fff6-106">The **Set-AzureRmTrafficManagerProfile** cmdlet updates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9fff6-107">Этот командлет обновляет параметры профиля из локального объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="9fff6-107">This cmdlet updates the settings of the profile from a local profile object.</span></span>
<span data-ttu-id="9fff6-108">Вы можете указать объект профиля с помощью параметра *TrafficManagerProfile* или конвейера.</span><span class="sxs-lookup"><span data-stu-id="9fff6-108">You can specify the profile object either by using the *TrafficManagerProfile* parameter or by using the pipeline.</span></span>

<span data-ttu-id="9fff6-109">Вы можете получить локальный объект, представляющий профиль, с помощью командлета Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9fff6-109">You can obtain a local object that represents a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9fff6-110">Измените объект на локальном компьютере, а затем используйте **Set-AzureRmTrafficManagerProfile** , чтобы зафиксировать изменения.</span><span class="sxs-lookup"><span data-stu-id="9fff6-110">Modify the object locally and then use **Set-AzureRmTrafficManagerProfile** to commit your changes.</span></span>

## <span data-ttu-id="9fff6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9fff6-111">EXAMPLES</span></span>

### <span data-ttu-id="9fff6-112">Пример 1: обновление профиля</span><span class="sxs-lookup"><span data-stu-id="9fff6-112">Example 1: Update a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="9fff6-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9fff6-113">The first command gets an Azure Traffic Manager profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9fff6-114">Команда хранит профиль локально в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9fff6-114">The command stores the profile locally in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="9fff6-115">Вторая команда изменяет этот профиль локально.</span><span class="sxs-lookup"><span data-stu-id="9fff6-115">The second command changes that profile locally.</span></span>
<span data-ttu-id="9fff6-116">Эта команда отключает профиль.</span><span class="sxs-lookup"><span data-stu-id="9fff6-116">This command disables the profile.</span></span>

<span data-ttu-id="9fff6-117">Третья команда обновляет профиль диспетчера трафика с именем ContosoProfile, чтобы соответствовать локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="9fff6-117">The third command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="9fff6-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9fff6-118">PARAMETERS</span></span>

### <span data-ttu-id="9fff6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-119">-DefaultProfile</span></span>
<span data-ttu-id="9fff6-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9fff6-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9fff6-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="9fff6-122">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9fff6-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="9fff6-123">Этот командлет обновляет диспетчер трафика для соответствия этому локальному объекту.</span><span class="sxs-lookup"><span data-stu-id="9fff6-123">This cmdlet updates Traffic Manager to match this local object.</span></span>

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

### <span data-ttu-id="9fff6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fff6-124">CommonParameters</span></span>
<span data-ttu-id="9fff6-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9fff6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fff6-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fff6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fff6-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9fff6-127">INPUTS</span></span>

### <span data-ttu-id="9fff6-128">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-128">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9fff6-129">Этот командлет принимает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9fff6-129">This cmdlet accepts a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9fff6-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9fff6-130">OUTPUTS</span></span>

### <span data-ttu-id="9fff6-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="9fff6-132">Этот командлет возвращает объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="9fff6-132">This cmdlet returns a **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="9fff6-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9fff6-133">NOTES</span></span>

## <span data-ttu-id="9fff6-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9fff6-134">RELATED LINKS</span></span>

[<span data-ttu-id="9fff6-135">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9fff6-135">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9fff6-136">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-136">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9fff6-137">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-137">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9fff6-138">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9fff6-138">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9fff6-139">Remove-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9fff6-139">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)


