---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 7944328c7cac37d88cf18d715cbb7a893eacc683
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563231"
---
# <span data-ttu-id="86795-101">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="86795-101">Remove-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="86795-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86795-102">SYNOPSIS</span></span>
<span data-ttu-id="86795-103">Удаляет конечную точку из объекта профиля локального диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="86795-103">Removes an endpoint from a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86795-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86795-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="86795-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86795-105">DESCRIPTION</span></span>
<span data-ttu-id="86795-106">Командлет **Remove-AzureRmTrafficManagerEndpointConfig** удаляет конечную точку из локального объекта профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="86795-106">The **Remove-AzureRmTrafficManagerEndpointConfig** cmdlet removes an endpoint from a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="86795-107">Вы можете получить профиль с помощью командлета Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-107">You can get a profile by using the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

<span data-ttu-id="86795-108">Этот командлет работает с объектом локального профиля.</span><span class="sxs-lookup"><span data-stu-id="86795-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="86795-109">Зафиксируйте изменения в профиле диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="86795-110">Чтобы удалить конечную точку и внести изменения в одной операции, используйте командлет Remove-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="86795-110">To remove an endpoint and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="86795-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86795-111">EXAMPLES</span></span>

### <span data-ttu-id="86795-112">Пример 1: Удаление конечной точки</span><span class="sxs-lookup"><span data-stu-id="86795-112">Example 1: Remove an endpoint</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -Type AzureEndpoints -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="86795-113">Первая команда получает профиль диспетчера трафика Azure с помощью командлета **Get-AzureRmTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="86795-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="86795-114">Команда хранит локальный профиль в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="86795-115">Вторая команда удаляет конечную точку Azure с именем Contoso из профиля, хранящегося в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-115">The second command removes an Azure endpoint named contoso from the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="86795-116">Эта команда изменяет только локальный объект.</span><span class="sxs-lookup"><span data-stu-id="86795-116">This command changes only the local object.</span></span>

<span data-ttu-id="86795-117">Последняя команда обновляет профиль диспетчера трафика с именем ContosoProfile, чтобы соответствовать локальному значению в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-117">The final command updates the Traffic Manager profile named ContosoProfile to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="86795-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86795-118">PARAMETERS</span></span>

### <span data-ttu-id="86795-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86795-119">-DefaultProfile</span></span>
<span data-ttu-id="86795-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86795-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86795-121">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="86795-121">-EndpointName</span></span>
<span data-ttu-id="86795-122">Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="86795-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86795-123">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86795-123">-TrafficManagerProfile</span></span>
<span data-ttu-id="86795-124">Указывает локальный объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="86795-124">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="86795-125">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="86795-125">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="86795-126">Чтобы получить объект **TrafficManagerProfile** , используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-126">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86795-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86795-127">CommonParameters</span></span>
<span data-ttu-id="86795-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86795-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86795-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86795-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86795-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86795-130">INPUTS</span></span>

### <span data-ttu-id="86795-131">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86795-131">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="86795-132">Этот командлет принимает объект **TrafficManagerProfile** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="86795-132">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="86795-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86795-133">OUTPUTS</span></span>

### <span data-ttu-id="86795-134">Microsoft. Azure. Commands. Network. TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86795-134">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="86795-135">Этот командлет возвращает модифицированный объект TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="86795-135">This cmdlet returns a modified TrafficManagerProfile object.</span></span>

## <span data-ttu-id="86795-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="86795-136">NOTES</span></span>

## <span data-ttu-id="86795-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86795-137">RELATED LINKS</span></span>

[<span data-ttu-id="86795-138">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="86795-138">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="86795-139">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86795-139">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="86795-140">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86795-140">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="86795-141">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="86795-141">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


