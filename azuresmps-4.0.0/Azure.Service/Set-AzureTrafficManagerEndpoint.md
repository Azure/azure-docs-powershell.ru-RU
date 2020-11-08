---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075434"
---
# <span data-ttu-id="381ba-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="381ba-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="381ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="381ba-102">SYNOPSIS</span></span>
<span data-ttu-id="381ba-103">Обновляет свойства конечной точки в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="381ba-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="381ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="381ba-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="381ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="381ba-105">DESCRIPTION</span></span>
<span data-ttu-id="381ba-106">Командлет **Set-AzureTrafficManagerEndpoint** обновляет свойства конечной точки в профиле диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="381ba-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="381ba-107">Если конечная точка не существует в текущем профиле, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="381ba-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="381ba-108">После того как вы добавите конечную точку, передайте результат командлету **Set-AzureTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="381ba-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="381ba-109">Этот командлет подключается к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="381ba-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="381ba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="381ba-110">EXAMPLES</span></span>

### <span data-ttu-id="381ba-111">Пример 1: обновление конечной точки для профиля</span><span class="sxs-lookup"><span data-stu-id="381ba-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="381ba-112">Первая команда использует командлет **Get-AzureTrafficManagerProfile** для получения профиля с именем ContosoProfile, а затем сохраняет его в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="381ba-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="381ba-113">Вторая команда обновляет конечную точку в профиле диспетчера трафика, который хранится в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="381ba-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="381ba-114">Конечная точка имеет доменное имя ContosoApp02.cloudapp.net.</span><span class="sxs-lookup"><span data-stu-id="381ba-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="381ba-115">Команда также задает состояние, тип, толщину и расположение конечной точки.</span><span class="sxs-lookup"><span data-stu-id="381ba-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="381ba-116">Команда передает модифицированный профиль в командлет **Set-AzureTrafficManagerProfile** для подключения к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="381ba-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="381ba-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="381ba-117">PARAMETERS</span></span>

### <span data-ttu-id="381ba-118">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="381ba-118">-DomainName</span></span>
<span data-ttu-id="381ba-119">Указывает доменное имя конечной точки, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="381ba-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="381ba-120">-Location</span><span class="sxs-lookup"><span data-stu-id="381ba-120">-Location</span></span>
<span data-ttu-id="381ba-121">Указывает расположение конечной точки, которую добавляет командлет.</span><span class="sxs-lookup"><span data-stu-id="381ba-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="381ba-122">Это должно быть расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="381ba-122">This must be an Azure location.</span></span>

<span data-ttu-id="381ba-123">Этот параметр должен содержать значения для конечных точек типа any или Type "TrafficManager" в профиле, для которого в методе балансировки нагрузки установлено значение "производительность".</span><span class="sxs-lookup"><span data-stu-id="381ba-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="381ba-124">Возможные значения — имена областей Azure, как указано в  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="381ba-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="381ba-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="381ba-125">-MinChildEndpoints</span></span>
<span data-ttu-id="381ba-126">Указывает минимальное количество конечных точек, в которых должен быть подключен вложенный профиль для этой конечной точки, чтобы она считалась в сети.</span><span class="sxs-lookup"><span data-stu-id="381ba-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="381ba-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="381ba-127">-Profile</span></span>
<span data-ttu-id="381ba-128">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="381ba-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="381ba-129">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="381ba-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="381ba-130">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="381ba-130">-Status</span></span>
<span data-ttu-id="381ba-131">Указывает состояние конечной точки наблюдения.</span><span class="sxs-lookup"><span data-stu-id="381ba-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="381ba-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="381ba-132">Valid values are:</span></span> 

- <span data-ttu-id="381ba-133">Включаем</span><span class="sxs-lookup"><span data-stu-id="381ba-133">Enabled</span></span>
- <span data-ttu-id="381ba-134">Отключает</span><span class="sxs-lookup"><span data-stu-id="381ba-134">Disabled</span></span>

<span data-ttu-id="381ba-135">Если вы задаете значение Enabled, диспетчер трафика отслеживает конечную точку, а метод балансировки нагрузки считает это при управлении трафиком.</span><span class="sxs-lookup"><span data-stu-id="381ba-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="381ba-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="381ba-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="381ba-137">Указывает объект профиля диспетчера трафика, для которого нужно изменить конечную точку.</span><span class="sxs-lookup"><span data-stu-id="381ba-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="381ba-138">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="381ba-138">-Type</span></span>
<span data-ttu-id="381ba-139">Указывает тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="381ba-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="381ba-140">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="381ba-140">Valid values are:</span></span> 

- <span data-ttu-id="381ba-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="381ba-141">CloudService</span></span>
- <span data-ttu-id="381ba-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="381ba-142">AzureWebsite</span></span>
- <span data-ttu-id="381ba-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="381ba-143">TrafficManager</span></span>

- <span data-ttu-id="381ba-144">Необходимые</span><span class="sxs-lookup"><span data-stu-id="381ba-144">Any</span></span> 

<span data-ttu-id="381ba-145">Если конечная точка AzureWebsite более одной, конечные точки должны находиться в разных центрах обработки данных.</span><span class="sxs-lookup"><span data-stu-id="381ba-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="381ba-146">-Weight</span><span class="sxs-lookup"><span data-stu-id="381ba-146">-Weight</span></span>
<span data-ttu-id="381ba-147">Задает вес конечной точки, добавляемой командлетом.</span><span class="sxs-lookup"><span data-stu-id="381ba-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="381ba-148">Допустимый диапазон значений для этого параметра: \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="381ba-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="381ba-149">Этот параметр используется только для политик балансировки нагрузки RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="381ba-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="381ba-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="381ba-150">CommonParameters</span></span>
<span data-ttu-id="381ba-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="381ba-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="381ba-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="381ba-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="381ba-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="381ba-153">INPUTS</span></span>

## <span data-ttu-id="381ba-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="381ba-154">OUTPUTS</span></span>

### <span data-ttu-id="381ba-155">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="381ba-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="381ba-156">Этот командлет создает объект профиля диспетчера трафика, содержащий сведения об обновленном профиле.</span><span class="sxs-lookup"><span data-stu-id="381ba-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="381ba-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="381ba-157">NOTES</span></span>

## <span data-ttu-id="381ba-158">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="381ba-158">RELATED LINKS</span></span>

[<span data-ttu-id="381ba-159">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="381ba-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="381ba-160">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="381ba-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="381ba-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="381ba-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="381ba-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="381ba-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


