---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: AE8E6778-1299-4EC7-BFE0-3FB464AA7BB4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7bea5cbf2b5e10c85aaafa43203c207193040464
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075753"
---
# <span data-ttu-id="9aa1d-101">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="9aa1d-101">Set-AzureStorSimpleDevice</span></span>

## <span data-ttu-id="9aa1d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9aa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa1d-103">Изменяет конфигурацию устройства для устройства.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-103">Changes the device configuration for a device.</span></span>

## <span data-ttu-id="9aa1d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9aa1d-104">SYNTAX</span></span>

### <span data-ttu-id="9aa1d-105">IdentifyByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9aa1d-105">IdentifyByName (Default)</span></span>
```
Set-AzureStorSimpleDevice -DeviceName <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9aa1d-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="9aa1d-106">IdentifyById</span></span>
```
Set-AzureStorSimpleDevice -DeviceId <String> [-NewName <String>] [-TimeZone <TimeZoneInfo>]
 [-SecondaryDnsServer <String>] [-StorSimpleNetworkConfig <NetworkConfig[]>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="9aa1d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa1d-107">DESCRIPTION</span></span>
<span data-ttu-id="9aa1d-108">Командлет **Set-AzureStorSimpleDevice** изменяет конфигурацию устройства для устройства.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-108">The **Set-AzureStorSimpleDevice** cmdlet changes the device configuration for a device.</span></span>
<span data-ttu-id="9aa1d-109">Если вы настраиваете устройство в первый раз, необходимо задать параметры *TimeZone* , *SecondaryDnsServer* и *StorSimpleNetworkConfig* .</span><span class="sxs-lookup"><span data-stu-id="9aa1d-109">If you are setting up a device for the first time, you must specify the *TimeZone* , *SecondaryDnsServer* , and *StorSimpleNetworkConfig* parameters.</span></span>
<span data-ttu-id="9aa1d-110">Необходимо включить конфигурацию сети для Data0 с controller0, controller1 и IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-110">You must include network configuration for Data0 with controller0 and controller1 and IP addresses.</span></span>
<span data-ttu-id="9aa1d-111">Для первой настройки устройства необходим по крайней мере один сетевой интерфейс SCSI (ISCSI) с поддержкой Интернет.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-111">There must be at least one Internet SCSI (ISCSI)-enabled network interface to configure the device for the first time.</span></span>

## <span data-ttu-id="9aa1d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9aa1d-112">EXAMPLES</span></span>

### <span data-ttu-id="9aa1d-113">Пример 1: изменение конфигурации устройства</span><span class="sxs-lookup"><span data-stu-id="9aa1d-113">Example 1: Modify the configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="9aa1d-114">Первая команда создает сетевую конфигурацию для интерфейса Data0.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-114">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="9aa1d-115">Эта команда задает параметры *Controller0IPv4Address* , *Controller1IPv4Address* и *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="9aa1d-115">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="9aa1d-116">Команда сохраняет результат в переменной $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-116">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="9aa1d-117">Вторая команда использует класс **System. TimeZoneInfo** .NET и стандартный синтаксис для получения стандартного тихоокеанское значение часового пояса и сохраняет этот объект в переменной $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-117">The second command uses the **System.TimeZoneInfo** .NET class and standard syntax to get Pacific Standard Time zone, and stores that object in the $TimeZoneInfo variable.</span></span>

<span data-ttu-id="9aa1d-118">Третья команда использует командлет **Get-AzureStorSimpleDevice** и командлет **Where-Object** для получения сетевого устройства StorSimple, а затем сохраняет его в переменной $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-118">The third command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="9aa1d-119">Последняя команда изменяет конфигурацию устройства с указанным ИДЕНТИФИКАТОРом устройства.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-119">The final command modifies the configuration for the device that has the specified device ID.</span></span>
<span data-ttu-id="9aa1d-120">В команде используется объект Configuration, созданный текущим командлетом в первой команде.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-120">The command uses the configuration object that the current cmdlet created in the first command.</span></span>
<span data-ttu-id="9aa1d-121">В команде используется часовой пояс, хранящийся в $TimeZoneInfo.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-121">The command uses the time zone stored in $TimeZoneInfo.</span></span>

### <span data-ttu-id="9aa1d-122">Пример 2: переканальный объект конфигурации для изменения устройства</span><span class="sxs-lookup"><span data-stu-id="9aa1d-122">Example 2: Pipe the configuration object to modify a device</span></span>
```
PS C:\>$TimeZoneInfo = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -TimeZone $TimeZoneInfo -SecondaryDnsServer 10.8.8.8 
VERBOSE: ClientRequestId: fa2f5000-169c-4feb-abbf-23f4b5c837fa_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: fae6a491-919c-44b2-93e0-0c51f202c24b_PS
VERBOSE: ClientRequestId: e1803427-a097-4d58-ab7d-14a4c39fd768_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 9e796c3d-3100-46ab-9a09-0e10c73a296f_PS
VERBOSE: ClientRequestId: 5b4cad96-31f4-4d07-a278-df5af3e06ad4_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: 9061f7df-144f-4f30-858c-045d882ca392_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 2ed2fa9b-8459-4cd6-9a61-5fc25ced2815_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="9aa1d-123">В этом примере выполняется такое же обновление конфигурации, что и в первом примере за исключением того, что последняя команда передает объект конфигурации сети текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-123">This example does the same configuration update as the first example, except that the final command passes the network configuration object to the current cmdlet by using the pipeline operator.</span></span>

### <span data-ttu-id="9aa1d-124">Пример 3: переканальие объекта часового пояса для изменения устройства</span><span class="sxs-lookup"><span data-stu-id="9aa1d-124">Example 3: Pipe the time zone object to modify a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49" 
PS C:\> $OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
PS C:\> $UpdatedDetails = [System.TimeZoneInfo]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" } | Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -NewName "Device22" -SecondaryDnsServer 10.8.8.8 -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: cfc3f3c7-a8b6-462b-96f4-124050b736fe_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 6017b76f-a771-4bf8-901e-14876e0f9962_PS
VERBOSE: ClientRequestId: 59a9275c-9005-4e8a-b68b-efa1e6c27d47_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 08e5142a-b038-4607-8690-0c5a8b948352_PS
VERBOSE: ClientRequestId: 218af244-b8f4-4a4b-817e-8f67e1323f03_PS
VERBOSE: About to configure the device : Device22 ! 
VERBOSE: ClientRequestId: fbd1f32d-1d74-432e-9dc0-90b46674884a_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 981cb941-252c-4898-ba9f-f19e5b8bcaa4_PS
VERBOSE: Successfully updated configuration for device Device22 with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="9aa1d-125">В этом примере выполняется такое же обновление конфигурации, что и в первом примере за исключением того, что последняя команда передает объект часового пояса текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-125">This example does the same configuration update as the first example, except that the final command passes the time zone object to the current cmdlet by using the pipeline operator.</span></span>

## <span data-ttu-id="9aa1d-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9aa1d-126">PARAMETERS</span></span>

### <span data-ttu-id="9aa1d-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9aa1d-127">-DeviceId</span></span>
<span data-ttu-id="9aa1d-128">Указывает ИД экземпляра устройства StorSimple для настройки.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-128">Specifies the instance ID of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa1d-129">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="9aa1d-129">-DeviceName</span></span>
<span data-ttu-id="9aa1d-130">Указывает понятное имя настраиваемого устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-130">Specifies the friendly name of the StorSimple device to configure.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa1d-131">-NewName</span><span class="sxs-lookup"><span data-stu-id="9aa1d-131">-NewName</span></span>
<span data-ttu-id="9aa1d-132">Указывает новое понятное имя устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-132">Specifies the new friendly name of the StorSimple device.</span></span>

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

### <span data-ttu-id="9aa1d-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="9aa1d-133">-Profile</span></span>
<span data-ttu-id="9aa1d-134">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="9aa1d-135">-SecondaryDnsServer</span><span class="sxs-lookup"><span data-stu-id="9aa1d-135">-SecondaryDnsServer</span></span>
<span data-ttu-id="9aa1d-136">Указывает дополнительный DNS-сервер для устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-136">Specifies a secondary DNS server for the StorSimple device.</span></span>

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

### <span data-ttu-id="9aa1d-137">-StorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="9aa1d-137">-StorSimpleNetworkConfig</span></span>
<span data-ttu-id="9aa1d-138">Задает массив объектов конфигурации сети для интерфейсов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-138">Specifies an array of network configuration objectss for interfaces on a device.</span></span>
<span data-ttu-id="9aa1d-139">Чтобы получить объект **NetworkConfig** , используйте командлет New-AzureStorSimpleNetworkConfig.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-139">To obtain a **NetworkConfig** object, use the New-AzureStorSimpleNetworkConfig cmdlet.</span></span>

```yaml
Type: NetworkConfig[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa1d-140">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="9aa1d-140">-TimeZone</span></span>
<span data-ttu-id="9aa1d-141">Указывает часовой пояс для устройства.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-141">Specifies a time zone for the device.</span></span>
<span data-ttu-id="9aa1d-142">Вы можете создать объект **TimeZoneInfo** с помощью метода **GetSystemTimeZone ()** .</span><span class="sxs-lookup"><span data-stu-id="9aa1d-142">You can create a **TimeZoneInfo** object by using the **GetSystemTimeZone()** method.</span></span>
<span data-ttu-id="9aa1d-143">Например, эта команда создает объект сведения о часовом поясе для стандартного тихоокеанское время: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span><span class="sxs-lookup"><span data-stu-id="9aa1d-143">For example, this command creates a time zone information object for Pacific Standard Time: `\[System.TimeZoneInfo\]::GetSystemTimeZones() | where { $_.Id -eq "Pacific Standard Time" }`</span></span>

```yaml
Type: TimeZoneInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa1d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa1d-144">CommonParameters</span></span>
<span data-ttu-id="9aa1d-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa1d-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa1d-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa1d-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9aa1d-147">INPUTS</span></span>

### <span data-ttu-id="9aa1d-148">NetworkConfig, TimeZoneInfo</span><span class="sxs-lookup"><span data-stu-id="9aa1d-148">NetworkConfig, TimeZoneInfo</span></span>
<span data-ttu-id="9aa1d-149">Вы можете передать в этот командлет объект **NetworkConfig** или **TimeZoneInfo** .</span><span class="sxs-lookup"><span data-stu-id="9aa1d-149">You can pipe a **NetworkConfig** object or a **TimeZoneInfo** to this cmdlet.</span></span>

## <span data-ttu-id="9aa1d-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9aa1d-150">OUTPUTS</span></span>

### <span data-ttu-id="9aa1d-151">DeviceDetails</span><span class="sxs-lookup"><span data-stu-id="9aa1d-151">DeviceDetails</span></span>
<span data-ttu-id="9aa1d-152">Этот командлет возвращает обновленные сведения об устройстве для виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="9aa1d-152">This cmdlet returns updated device details for the virtual device.</span></span>

## <span data-ttu-id="9aa1d-153">Пуск</span><span class="sxs-lookup"><span data-stu-id="9aa1d-153">NOTES</span></span>

## <span data-ttu-id="9aa1d-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9aa1d-154">RELATED LINKS</span></span>

[<span data-ttu-id="9aa1d-155">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="9aa1d-155">New-AzureStorSimpleNetworkConfig</span></span>](./New-AzureStorSimpleNetworkConfig.md)

[<span data-ttu-id="9aa1d-156">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="9aa1d-156">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


