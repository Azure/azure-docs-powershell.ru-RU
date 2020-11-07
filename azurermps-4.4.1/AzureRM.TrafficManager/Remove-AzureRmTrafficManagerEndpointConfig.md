---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4f936569b5a3c7b3ba63a471aedd6828ef6f36d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732050"
---
# <span data-ttu-id="10d04-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="10d04-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="10d04-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10d04-102">SYNOPSIS</span></span>
<span data-ttu-id="10d04-103">Удаляет конечную точку из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="10d04-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10d04-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10d04-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d04-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10d04-105">DESCRIPTION</span></span>
<span data-ttu-id="10d04-106">Командлет **Remove-AzureRmTrafficManagerEndpointConfig** удаляет конечную точку из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="10d04-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="10d04-107">Вы можете получить профиль с помощью командлета Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="10d04-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="10d04-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="10d04-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="10d04-110">Чтобы удалить конечную точку и внести изменения в одной операции, используйте командлет Remove-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="10d04-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="10d04-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10d04-111">EXAMPLES</span></span>

### <span data-ttu-id="10d04-112">Пример 1: Удаление конечной точки</span><span class="sxs-lookup"><span data-stu-id="10d04-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="10d04-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="10d04-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="10d04-114">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="10d04-115">Вторая команда удаляет конечную точку Azure с именем Contoso из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="10d04-116">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="10d04-116">This command changes only the local object.</span></span>

<span data-ttu-id="10d04-117">Последняя команда обновляет профиль диспетчера трафика с именем ContosoProfile, чтобы соответствовать локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="10d04-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10d04-118">PARAMETERS</span></span>

### <span data-ttu-id="10d04-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="10d04-119">-EndpointName</span></span>
<span data-ttu-id="10d04-120">Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10d04-120">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="10d04-121">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-121">-TrafficManagerProfile</span></span>
<span data-ttu-id="10d04-122">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="10d04-122">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="10d04-123">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="10d04-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="10d04-124">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-124">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="10d04-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-125">-DefaultProfile</span></span>
<span data-ttu-id="10d04-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10d04-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10d04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d04-127">CommonParameters</span></span>
<span data-ttu-id="10d04-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10d04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d04-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d04-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d04-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10d04-130">INPUTS</span></span>

### <span data-ttu-id="10d04-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="10d04-132">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="10d04-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="10d04-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10d04-133">OUTPUTS</span></span>

### <span data-ttu-id="10d04-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="10d04-135">Этот командлет возвращает модифицированный объект TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="10d04-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="10d04-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="10d04-136">NOTES</span></span>

## <span data-ttu-id="10d04-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10d04-137">RELATED LINKS</span></span>

[<span data-ttu-id="10d04-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="10d04-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="10d04-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="10d04-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="10d04-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="10d04-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="10d04-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


