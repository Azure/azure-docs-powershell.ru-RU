---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224601"
---
# <span data-ttu-id="ad91b-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ad91b-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="ad91b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad91b-102">SYNOPSIS</span></span>
<span data-ttu-id="ad91b-103">Удаляет конечную точку из локального объекта профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="ad91b-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="ad91b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ad91b-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad91b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad91b-105">DESCRIPTION</span></span>
<span data-ttu-id="ad91b-106">Для удаления конечной точки из локального объекта профиля Azure Traffic Manager удаляется конечная точка **AzTrafficManagerEndpointConfig.**</span><span class="sxs-lookup"><span data-stu-id="ad91b-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="ad91b-107">Вы можете получить профиль с помощью Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ad91b-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="ad91b-108">Этот cmdlet выполняется с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="ad91b-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="ad91b-109">Зафиксировать изменения в профиле диспетчера трафика с помощью Set-AzTrafficManagerProfile управления.</span><span class="sxs-lookup"><span data-stu-id="ad91b-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="ad91b-110">Чтобы удалить конечную точку и зафиксировать изменения за одну операцию, используйте Remove-AzTrafficManagerEndpoint конечную точку.</span><span class="sxs-lookup"><span data-stu-id="ad91b-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="ad91b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ad91b-111">EXAMPLES</span></span>

### <span data-ttu-id="ad91b-112">Пример 1. Удаление конечной точки</span><span class="sxs-lookup"><span data-stu-id="ad91b-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="ad91b-113">Первая команда получает профиль Диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="ad91b-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="ad91b-114">Команда сохраняет локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ad91b-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="ad91b-115">Вторая команда удаляет конечную точку Azure contoso из профиля, храняого в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ad91b-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="ad91b-116">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="ad91b-116">This command changes only the local object.</span></span>

<span data-ttu-id="ad91b-117">Конечная команда обновляет профиль диспетчера трафика с именем ContosoProfile в соответствие с локальным значением в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="ad91b-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="ad91b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad91b-118">PARAMETERS</span></span>

### <span data-ttu-id="ad91b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-119">-DefaultProfile</span></span>
<span data-ttu-id="ad91b-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad91b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad91b-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ad91b-121">-EndpointName</span></span>
<span data-ttu-id="ad91b-122">Указывает имя конечной точки Диспетчера трафика, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad91b-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ad91b-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="ad91b-124">Определяет локальный **объект TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="ad91b-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="ad91b-125">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="ad91b-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="ad91b-126">Чтобы получить объект **TrafficManagerProfile,** используйте Get-AzTrafficManagerProfile..</span><span class="sxs-lookup"><span data-stu-id="ad91b-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="ad91b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad91b-127">CommonParameters</span></span>
<span data-ttu-id="ad91b-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad91b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad91b-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad91b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad91b-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ad91b-130">INPUTS</span></span>

### <span data-ttu-id="ad91b-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ad91b-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad91b-132">OUTPUTS</span></span>

### <span data-ttu-id="ad91b-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="ad91b-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ad91b-134">NOTES</span></span>

## <span data-ttu-id="ad91b-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad91b-135">RELATED LINKS</span></span>

[<span data-ttu-id="ad91b-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="ad91b-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="ad91b-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="ad91b-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="ad91b-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="ad91b-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="ad91b-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


