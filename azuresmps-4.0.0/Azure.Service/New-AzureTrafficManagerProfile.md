---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076202"
---
# <span data-ttu-id="da0cd-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="da0cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="da0cd-102">SYNOPSIS</span></span>
<span data-ttu-id="da0cd-103">Создание профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="da0cd-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="da0cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="da0cd-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="da0cd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="da0cd-105">DESCRIPTION</span></span>
<span data-ttu-id="da0cd-106">Командлет **New-AzureTrafficManagerProfile** создает профиль диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="da0cd-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="da0cd-107">После создания профиля, в котором вы установили для *LoadBalancingMethod* значение "переход на другой ресурс", вы можете определить порядок отработки отказа конечных точек, добавленных в профиль с помощью командлета Add-AzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="da0cd-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="da0cd-108">Дополнительные сведения можно найти в статье пример 2.</span><span class="sxs-lookup"><span data-stu-id="da0cd-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="da0cd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="da0cd-109">EXAMPLES</span></span>

### <span data-ttu-id="da0cd-110">Пример 1: Создание профиля диспетчера трафика</span><span class="sxs-lookup"><span data-stu-id="da0cd-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="da0cd-111">Эта команда создает профиль диспетчера трафика с именем отобразите в указанном домене диспетчера трафика с помощью метода балансировки нагрузки циклической загрузки, срок жизни 30 секунд, протокол наблюдения HTTP, мониторинг порта 80 и с указанным путем.</span><span class="sxs-lookup"><span data-stu-id="da0cd-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="da0cd-112">Пример 2: упорядочение конечных точек в требуемый заказ на перемещение</span><span class="sxs-lookup"><span data-stu-id="da0cd-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="da0cd-113">В этом примере показано, как изменить порядок конечных точек, добавленных в отобразите, к нужному заказу на перемещение.</span><span class="sxs-lookup"><span data-stu-id="da0cd-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="da0cd-114">Первая команда получает объект профиля диспетчера трафика с именем отобразите и сохраняет объект в переменной $Profile.</span><span class="sxs-lookup"><span data-stu-id="da0cd-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="da0cd-115">Вторая команда повторно упорядочивает конечные точки из массива конечных точек в том порядке, в котором должна выполняться отработка отказа.</span><span class="sxs-lookup"><span data-stu-id="da0cd-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="da0cd-116">Последняя команда обновляет профиль диспетчера трафика, хранящийся в $Profile с новым порядком конечных точек.</span><span class="sxs-lookup"><span data-stu-id="da0cd-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="da0cd-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="da0cd-117">PARAMETERS</span></span>

### <span data-ttu-id="da0cd-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="da0cd-118">-DomainName</span></span>
<span data-ttu-id="da0cd-119">Задает доменное имя профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="da0cd-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="da0cd-120">Это должен быть поддомен trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="da0cd-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="da0cd-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="da0cd-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="da0cd-122">Указывает метод балансировки нагрузки, используемый для распространения соединения.</span><span class="sxs-lookup"><span data-stu-id="da0cd-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="da0cd-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="da0cd-123">Valid values are:</span></span> 

- <span data-ttu-id="da0cd-124">Эффективности</span><span class="sxs-lookup"><span data-stu-id="da0cd-124">Performance</span></span>
- <span data-ttu-id="da0cd-125">Переключения</span><span class="sxs-lookup"><span data-stu-id="da0cd-125">Failover</span></span>
- <span data-ttu-id="da0cd-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="da0cd-126">RoundRobin</span></span>

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

### <span data-ttu-id="da0cd-127">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="da0cd-127">-MonitorPort</span></span>
<span data-ttu-id="da0cd-128">Указывает порт, используемый для отслеживания работоспособности конечной точки.</span><span class="sxs-lookup"><span data-stu-id="da0cd-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="da0cd-129">Допустимые значения: целочисленные значения больше 0 и меньше или равно 65 535.</span><span class="sxs-lookup"><span data-stu-id="da0cd-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0cd-130">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="da0cd-130">-MonitorProtocol</span></span>
<span data-ttu-id="da0cd-131">Указывает протокол для наблюдения за работоспособностью конечной точки.</span><span class="sxs-lookup"><span data-stu-id="da0cd-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="da0cd-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="da0cd-132">Valid values are:</span></span> 

- <span data-ttu-id="da0cd-133">Через</span><span class="sxs-lookup"><span data-stu-id="da0cd-133">Http</span></span>

- <span data-ttu-id="da0cd-134">Протокол</span><span class="sxs-lookup"><span data-stu-id="da0cd-134">Https</span></span>

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

### <span data-ttu-id="da0cd-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="da0cd-135">-MonitorRelativePath</span></span>
<span data-ttu-id="da0cd-136">Указывает путь относительно имени домена конечной точки для проверки состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="da0cd-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="da0cd-137">Путь должен соответствовать следующим ограничениям:</span><span class="sxs-lookup"><span data-stu-id="da0cd-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="da0cd-138">Путь должен содержать от 1 до 1000 символов.</span><span class="sxs-lookup"><span data-stu-id="da0cd-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="da0cd-139">Она должна начинаться с косой черты (/).</span><span class="sxs-lookup"><span data-stu-id="da0cd-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="da0cd-140">Он не должен содержать XML-элементы \<\> .</span><span class="sxs-lookup"><span data-stu-id="da0cd-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="da0cd-141">Оно должно содержать без двойных косых черт (//).</span><span class="sxs-lookup"><span data-stu-id="da0cd-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="da0cd-142">Он должен содержать недопустимые escape-символы HTML.</span><span class="sxs-lookup"><span data-stu-id="da0cd-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="da0cd-143">Например,% XY.</span><span class="sxs-lookup"><span data-stu-id="da0cd-143">For example, %XY.</span></span>

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

### <span data-ttu-id="da0cd-144">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="da0cd-144">-Name</span></span>
<span data-ttu-id="da0cd-145">Указывает имя создаваемого профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="da0cd-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da0cd-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="da0cd-146">-Profile</span></span>
<span data-ttu-id="da0cd-147">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="da0cd-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="da0cd-148">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="da0cd-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da0cd-149">-TTL</span><span class="sxs-lookup"><span data-stu-id="da0cd-149">-Ttl</span></span>
<span data-ttu-id="da0cd-150">Указывает срок жизни (TTL) DNS, который информирует локальных имен DNS о том, сколько времени кэширование DNS-записей.</span><span class="sxs-lookup"><span data-stu-id="da0cd-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="da0cd-151">Допустимые значения — целые числа от 30 до 999 999.</span><span class="sxs-lookup"><span data-stu-id="da0cd-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="da0cd-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da0cd-152">CommonParameters</span></span>
<span data-ttu-id="da0cd-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="da0cd-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da0cd-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da0cd-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da0cd-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="da0cd-155">INPUTS</span></span>

## <span data-ttu-id="da0cd-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="da0cd-156">OUTPUTS</span></span>

### <span data-ttu-id="da0cd-157">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="da0cd-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="da0cd-158">Этот командлет создает объект профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="da0cd-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="da0cd-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="da0cd-159">NOTES</span></span>

## <span data-ttu-id="da0cd-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="da0cd-160">RELATED LINKS</span></span>

[<span data-ttu-id="da0cd-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da0cd-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da0cd-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da0cd-164">Remove-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="da0cd-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="da0cd-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


