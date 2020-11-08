---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076376"
---
# <span data-ttu-id="3aa0a-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa0a-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3aa0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3aa0a-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa0a-103">Добавляет конечную точку в профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="3aa0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3aa0a-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3aa0a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa0a-105">DESCRIPTION</span></span>
<span data-ttu-id="3aa0a-106">Командлет **Add-AzureTrafficManagerEndpoint** добавляет конечную точку в профиль диспетчера трафика Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="3aa0a-107">После того как вы добавите конечную точку, передайте результат командлету **Set-AzureTrafficManagerProfile** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3aa0a-108">Этот командлет подключается к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="3aa0a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3aa0a-109">EXAMPLES</span></span>

### <span data-ttu-id="3aa0a-110">Пример 1: Добавление конечной точки к профилю</span><span class="sxs-lookup"><span data-stu-id="3aa0a-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="3aa0a-111">Первая команда использует командлет **Get-AzureTrafficManagerProfile** для получения профиля с именем ContosoProfile, а затем сохраняет его в переменной $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="3aa0a-112">Вторая команда добавляет конечную точку в профиль диспетчера трафика, хранящийся в $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="3aa0a-113">Конечная точка имеет доменное имя Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="3aa0a-114">Команда также указывает, включена ли она и тип.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="3aa0a-115">Команда передает объект Profile командлету **Set-AzureTrafficManagerProfile** для подключения к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="3aa0a-116">Пример 2: Добавление конечной точки с указанным расположением и весовым коэффициентом</span><span class="sxs-lookup"><span data-stu-id="3aa0a-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="3aa0a-117">Эта команда добавляет конечную точку в профиль диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="3aa0a-118">Конечная точка имеет доменное имя Contoso02App.couldapp.net.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="3aa0a-119">Команда также указывает, включена ли она и тип.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="3aa0a-120">В команде также указывается плотность и расположение конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="3aa0a-121">Команда передает объект Profile для **настройки** подключения к Azure, чтобы сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="3aa0a-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3aa0a-122">PARAMETERS</span></span>

### <span data-ttu-id="3aa0a-123">-ИмяДомена</span><span class="sxs-lookup"><span data-stu-id="3aa0a-123">-DomainName</span></span>
<span data-ttu-id="3aa0a-124">Указывает доменное имя конечной точки, которую нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="3aa0a-125">-Location</span><span class="sxs-lookup"><span data-stu-id="3aa0a-125">-Location</span></span>
<span data-ttu-id="3aa0a-126">Указывает расположение конечной точки, которую добавляет командлет.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="3aa0a-127">Это должно быть расположение Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-127">This must be an Azure location.</span></span>

<span data-ttu-id="3aa0a-128">Этот параметр должен содержать значения для конечных точек типа any или Type "TrafficManager" в профиле, для которого в методе балансировки нагрузки установлено значение "производительность".</span><span class="sxs-lookup"><span data-stu-id="3aa0a-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="3aa0a-129">Возможные значения — имена областей Azure, как указано в https://azure.microsoft.com/regions/ .</span><span class="sxs-lookup"><span data-stu-id="3aa0a-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="3aa0a-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="3aa0a-130">-MinChildEndpoints</span></span>
<span data-ttu-id="3aa0a-131">Указывает минимальное количество конечных точек, в которых должен быть подключен вложенный профиль для этой конечной точки, чтобы она считалась в сети.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="3aa0a-132">-Profile</span><span class="sxs-lookup"><span data-stu-id="3aa0a-132">-Profile</span></span>
<span data-ttu-id="3aa0a-133">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3aa0a-134">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3aa0a-135">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="3aa0a-135">-Status</span></span>
<span data-ttu-id="3aa0a-136">Указывает состояние конечной точки наблюдения.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="3aa0a-137">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3aa0a-137">Valid values are:</span></span> 

- <span data-ttu-id="3aa0a-138">Включаем</span><span class="sxs-lookup"><span data-stu-id="3aa0a-138">Enabled</span></span>
- <span data-ttu-id="3aa0a-139">Отключает</span><span class="sxs-lookup"><span data-stu-id="3aa0a-139">Disabled</span></span>

<span data-ttu-id="3aa0a-140">Если вы задаете значение Enabled, диспетчер трафика отслеживает конечную точку, а метод балансировки нагрузки считает это при управлении трафиком.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="3aa0a-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3aa0a-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="3aa0a-142">Указывает объект профиля диспетчера трафика, к которому нужно добавить конечную точку.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

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

### <span data-ttu-id="3aa0a-143">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3aa0a-143">-Type</span></span>
<span data-ttu-id="3aa0a-144">Указывает тип конечной точки.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="3aa0a-145">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3aa0a-145">Valid values are:</span></span> 

- <span data-ttu-id="3aa0a-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="3aa0a-146">CloudService</span></span>
- <span data-ttu-id="3aa0a-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="3aa0a-147">AzureWebsite</span></span>
- <span data-ttu-id="3aa0a-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="3aa0a-148">TrafficManager</span></span>

- <span data-ttu-id="3aa0a-149">Необходимые</span><span class="sxs-lookup"><span data-stu-id="3aa0a-149">Any</span></span> 

<span data-ttu-id="3aa0a-150">Если конечная точка AzureWebsite более одной, конечные точки должны находиться в разных центрах обработки данных.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="3aa0a-151">-Weight</span><span class="sxs-lookup"><span data-stu-id="3aa0a-151">-Weight</span></span>
<span data-ttu-id="3aa0a-152">Задает вес конечной точки, добавляемой командлетом.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="3aa0a-153">Допустимый диапазон значений для этого параметра: \[ 1, 1000 \] .</span><span class="sxs-lookup"><span data-stu-id="3aa0a-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="3aa0a-154">Этот параметр используется только для политик балансировки нагрузки RoundRobin.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="3aa0a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa0a-155">CommonParameters</span></span>
<span data-ttu-id="3aa0a-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa0a-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa0a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa0a-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3aa0a-158">INPUTS</span></span>

## <span data-ttu-id="3aa0a-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa0a-159">OUTPUTS</span></span>

### <span data-ttu-id="3aa0a-160">Microsoft. WindowsAzure. Commands. Utilities. TrafficManager. Models. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="3aa0a-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="3aa0a-161">Этот командлет создает объект профиля диспетчера трафика, содержащий сведения об обновленном профиле.</span><span class="sxs-lookup"><span data-stu-id="3aa0a-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="3aa0a-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="3aa0a-162">NOTES</span></span>

## <span data-ttu-id="3aa0a-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aa0a-163">RELATED LINKS</span></span>

[<span data-ttu-id="3aa0a-164">Remove-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa0a-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="3aa0a-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3aa0a-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="3aa0a-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3aa0a-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3aa0a-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3aa0a-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


