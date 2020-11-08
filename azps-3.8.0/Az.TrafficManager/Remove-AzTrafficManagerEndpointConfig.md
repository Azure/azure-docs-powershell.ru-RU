---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066735"
---
# <span data-ttu-id="54149-101">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="54149-101">Remove-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="54149-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54149-102">SYNOPSIS</span></span>
<span data-ttu-id="54149-103">Удаляет конечную точку из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="54149-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="54149-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54149-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54149-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54149-105">DESCRIPTION</span></span>
<span data-ttu-id="54149-106">Командлет **Remove-AzTrafficManagerEndpointConfig** удаляет конечную точку из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="54149-106">The **Remove-AzTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="54149-107">Вы можете получить профиль с помощью командлета Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-107">You can get a profile by using the Get-AzTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="54149-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="54149-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="54149-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="54149-110">Чтобы удалить конечную точку и внести изменения в одной операции, используйте командлет Remove-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="54149-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="54149-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54149-111">EXAMPLES</span></span>

### <span data-ttu-id="54149-112">Пример 1: Удаление конечной точки</span><span class="sxs-lookup"><span data-stu-id="54149-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="54149-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="54149-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="54149-114">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="54149-115">Вторая команда удаляет конечную точку Azure с именем Contoso из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="54149-116">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="54149-116">This command changes only the local object.</span></span>

<span data-ttu-id="54149-117">Последняя команда обновляет профиль диспетчера трафика с именем ContosoProfile, чтобы соответствовать локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="54149-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54149-118">PARAMETERS</span></span>

### <span data-ttu-id="54149-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54149-119">-DefaultProfile</span></span>
<span data-ttu-id="54149-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54149-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54149-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="54149-121">-EndpointName</span></span>
<span data-ttu-id="54149-122">Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="54149-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="54149-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54149-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="54149-124">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="54149-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="54149-125">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="54149-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="54149-126">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="54149-126">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="54149-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54149-127">CommonParameters</span></span>
<span data-ttu-id="54149-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54149-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54149-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54149-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54149-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54149-130">INPUTS</span></span>

### <span data-ttu-id="54149-131">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54149-131">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="54149-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54149-132">OUTPUTS</span></span>

### <span data-ttu-id="54149-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54149-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="54149-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="54149-134">NOTES</span></span>

## <span data-ttu-id="54149-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54149-135">RELATED LINKS</span></span>

[<span data-ttu-id="54149-136">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="54149-136">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="54149-137">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54149-137">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="54149-138">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="54149-138">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="54149-139">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="54149-139">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


