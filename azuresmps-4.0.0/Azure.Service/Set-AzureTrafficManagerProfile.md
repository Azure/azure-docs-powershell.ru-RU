---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075794"
---
# <span data-ttu-id="b000c-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="b000c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b000c-102">SYNOPSIS</span></span>
<span data-ttu-id="b000c-103">Обновляет свойства профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="b000c-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="b000c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b000c-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b000c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b000c-105">DESCRIPTION</span></span>
<span data-ttu-id="b000c-106">Командлет **Set-AzureTrafficManagerProfile** обновляет свойства профиля диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b000c-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="b000c-107">Для профилей, для которых для параметра *LoadBalancingMethod* задано значение "переход на другой ресурс", вы можете определить порядок отработки отказа конечных точек, добавленных в профиль с помощью командлета Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b000c-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="b000c-108">Дополнительные сведения можно найти в статье пример 3.</span><span class="sxs-lookup"><span data-stu-id="b000c-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="b000c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b000c-109">EXAMPLES</span></span>

### <span data-ttu-id="b000c-110">Пример 1: Настройка TTL для профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="b000c-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="b000c-111">Эта команда задает срок жизни 60 секунд для объекта профиля диспетчера трафика MyTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="b000c-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="b000c-112">Пример 2: Настройка нескольких значений для профиля</span><span class="sxs-lookup"><span data-stu-id="b000c-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="b000c-113">Эта команда получает профиль диспетчера трафика с именем отобразите с помощью командлета **Get-AzureTrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="b000c-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="b000c-114">В профиле используется метод балансировки нагрузки RoundRobin, срок жизни: 30 секунд, протокол монитора HTTP, порт монитора и относительный путь к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="b000c-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="b000c-115">Пример 3: упорядочение конечных точек в требуемый заказ на перемещение</span><span class="sxs-lookup"><span data-stu-id="b000c-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b000c-116">В этом примере показано, как изменить порядок конечных точек, добавленных в отобразите, к нужному заказу на перемещение.</span><span class="sxs-lookup"><span data-stu-id="b000c-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="b000c-117">Первая команда получает объект профиля диспетчера трафика с именем отобразите и сохраняет объект в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="b000c-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="b000c-118">Вторая команда повторно упорядочивает конечные точки из массива конечных точек в том порядке, в котором должна выполняться отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="b000c-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="b000c-119">Последняя команда обновляет профиль диспетчера трафика, хранящийся в $Profile с новым порядком конечных точек.</span><span class="sxs-lookup"><span data-stu-id="b000c-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="b000c-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b000c-120">PARAMETERS</span></span>

### <span data-ttu-id="b000c-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="b000c-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="b000c-122">Указывает метод балансировки нагрузки, используемый для распространения соединения.</span><span class="sxs-lookup"><span data-stu-id="b000c-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="b000c-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b000c-123">Valid values are:</span></span> 

- <span data-ttu-id="b000c-124">Эффективности</span><span class="sxs-lookup"><span data-stu-id="b000c-124">Performance</span></span>
- <span data-ttu-id="b000c-125">Переключения</span><span class="sxs-lookup"><span data-stu-id="b000c-125">Failover</span></span>
- <span data-ttu-id="b000c-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="b000c-126">RoundRobin</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="b000c-127">-MonitorPort</span></span>
<span data-ttu-id="b000c-128">Указывает порт, используемый для отслеживания работоспособности конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b000c-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="b000c-129">Допустимые значения: целочисленные значения больше 0 и меньше или равно 65 535.</span><span class="sxs-lookup"><span data-stu-id="b000c-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="b000c-130">-MonitorProtocol</span></span>
<span data-ttu-id="b000c-131">Указывает протокол для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="b000c-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="b000c-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b000c-132">Valid values are:</span></span> 

- <span data-ttu-id="b000c-133">Через</span><span class="sxs-lookup"><span data-stu-id="b000c-133">Http</span></span>
- <span data-ttu-id="b000c-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="b000c-134">Https</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="b000c-135">-MonitorRelativePath</span></span>
<span data-ttu-id="b000c-136">Указывает путь относительно имени домена конечной точки для проверки состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="b000c-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="b000c-137">Путь должен соответствовать следующим ограничениям:</span><span class="sxs-lookup"><span data-stu-id="b000c-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="b000c-138">Путь должен содержать от 1 до 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="b000c-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="b000c-139">Она должна начинаться с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="b000c-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="b000c-140">Он не должен содержать XML-элементы \<\> .</span><span class="sxs-lookup"><span data-stu-id="b000c-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="b000c-141">Оно должно содержать без двойных косых черт (//).</span><span class="sxs-lookup"><span data-stu-id="b000c-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="b000c-142">Он должен содержать недопустимые escape-символы HTML.</span><span class="sxs-lookup"><span data-stu-id="b000c-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="b000c-143">Например,% XY.</span><span class="sxs-lookup"><span data-stu-id="b000c-143">For example, %XY.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b000c-144">-Name</span></span>
<span data-ttu-id="b000c-145">Указывает имя профиля диспетчера трафика для обновления.</span><span class="sxs-lookup"><span data-stu-id="b000c-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="b000c-146">-Profile</span></span>
<span data-ttu-id="b000c-147">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b000c-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b000c-148">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b000c-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="b000c-150">Указывает объект профиля диспетчера трафика, который вы используете для задания профиля.</span><span class="sxs-lookup"><span data-stu-id="b000c-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-151">-TTL</span><span class="sxs-lookup"><span data-stu-id="b000c-151">-Ttl</span></span>
<span data-ttu-id="b000c-152">Указывает срок жизни (TTL) DNS, который информирует локальных имен DNS о том, сколько времени кэширование DNS-записей.</span><span class="sxs-lookup"><span data-stu-id="b000c-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="b000c-153">Допустимые значения — целое число от 30 до 999 999.</span><span class="sxs-lookup"><span data-stu-id="b000c-153">Valid values are an integer from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b000c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b000c-154">CommonParameters</span></span>
<span data-ttu-id="b000c-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b000c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b000c-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b000c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b000c-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b000c-157">INPUTS</span></span>

## <span data-ttu-id="b000c-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b000c-158">OUTPUTS</span></span>

### <span data-ttu-id="b000c-159">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="b000c-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="b000c-160">Этот командлет создает объект профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="b000c-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="b000c-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="b000c-161">NOTES</span></span>

## <span data-ttu-id="b000c-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b000c-162">RELATED LINKS</span></span>

[<span data-ttu-id="b000c-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b000c-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b000c-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b000c-166">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b000c-167">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b000c-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


