---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075515"
---
# <span data-ttu-id="d730f-101">New-AzureStorSimpleNetworkConfig</span><span class="sxs-lookup"><span data-stu-id="d730f-101">New-AzureStorSimpleNetworkConfig</span></span>

## <span data-ttu-id="d730f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d730f-102">SYNOPSIS</span></span>
<span data-ttu-id="d730f-103">Подготавливает объект конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="d730f-103">Prepares a network configuration object.</span></span>

## <span data-ttu-id="d730f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d730f-104">SYNTAX</span></span>

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d730f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d730f-105">DESCRIPTION</span></span>
<span data-ttu-id="d730f-106">Командлет **New-AzureStorSimpleNetworkConfig** подготавливает объект конфигурации сети для передачи командлету **Set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="d730f-106">The **New-AzureStorSimpleNetworkConfig** cmdlet prepares a network configuration object to pass to the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="d730f-107">Задайте параметры *Controller0IPAddress* и *Controller1IPAddress* только в интерфейсе Data0.</span><span class="sxs-lookup"><span data-stu-id="d730f-107">Set the *Controller0IPAddress* parameter and *Controller1IPAddress* parameter only on the Data0 interface.</span></span>
<span data-ttu-id="d730f-108">Data0 поддерживает только три параметра: *Controller0IPAddress* , *Controller1IPAdress* и *EnableIscsi*.</span><span class="sxs-lookup"><span data-stu-id="d730f-108">Data0 supports only three settings: *Controller0IPAddress* , *Controller1IPAdress* , and *EnableIscsi*.</span></span>

## <span data-ttu-id="d730f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d730f-109">EXAMPLES</span></span>

### <span data-ttu-id="d730f-110">Пример 1: Настройка интерфейса Data0</span><span class="sxs-lookup"><span data-stu-id="d730f-110">Example 1: Configure a Data0 interface</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

<span data-ttu-id="d730f-111">Эта команда создает сетевую конфигурацию для интерфейса Data0.</span><span class="sxs-lookup"><span data-stu-id="d730f-111">This command creates network configuration for the Data0 interface.</span></span>
<span data-ttu-id="d730f-112">Эта команда задает параметры *Controller0IPv4Address* , *Controller1IPv4Address* и *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="d730f-112">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="d730f-113">Этот командлет может настроить Data0 только для этих трех параметров.</span><span class="sxs-lookup"><span data-stu-id="d730f-113">This cmdlet can configure Data0 for only these three parameters.</span></span>

### <span data-ttu-id="d730f-114">Пример 2: Configuren интерфейс, отличный от Data0</span><span class="sxs-lookup"><span data-stu-id="d730f-114">Example 2: Configuren an interface other than Data0 an</span></span>
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

<span data-ttu-id="d730f-115">Эта команда позволяет настроить интерфейс файл1.</span><span class="sxs-lookup"><span data-stu-id="d730f-115">This command configures the Data1 interface.</span></span>

### <span data-ttu-id="d730f-116">Пример 3: изменение конфигурации устройства</span><span class="sxs-lookup"><span data-stu-id="d730f-116">Example 3: Modify a configuration for a device</span></span>
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

<span data-ttu-id="d730f-117">Первая команда создает сетевую конфигурацию для интерфейса Data0.</span><span class="sxs-lookup"><span data-stu-id="d730f-117">The first command creates a network configuration for the Data0 interface.</span></span>
<span data-ttu-id="d730f-118">Эта команда задает параметры *Controller0IPv4Address* , *Controller1IPv4Address* и *EnableIscsi* .</span><span class="sxs-lookup"><span data-stu-id="d730f-118">This command specifies the *Controller0IPv4Address* , *Controller1IPv4Address* , and *EnableIscsi* parameters.</span></span>
<span data-ttu-id="d730f-119">Команда сохраняет результат в переменной $NetworkConfigData 0.</span><span class="sxs-lookup"><span data-stu-id="d730f-119">The command stores the result in the $NetworkConfigData0 variable.</span></span>

<span data-ttu-id="d730f-120">Вторая команда использует командлет **Get-AzureStorSimpleDevice** и командлет **Where-Object** для получения сетевого устройства StorSimple, а затем сохраняет его в переменной $OnlineDevice.</span><span class="sxs-lookup"><span data-stu-id="d730f-120">The second command uses the **Get-AzureStorSimpleDevice** cmdlet and the **Where-Object** core cmdlet to get an online StorSimple device, and then stores it in the $OnlineDevice variable.</span></span>

<span data-ttu-id="d730f-121">Последняя команда изменяет конфигурацию устройства с указанным ИДЕНТИФИКАТОРом устройства с помощью командлета **Set-AzureStorSimpleDevice** .</span><span class="sxs-lookup"><span data-stu-id="d730f-121">The final command modifies the configuration for the device that has the specified device ID by using the **Set-AzureStorSimpleDevice** cmdlet.</span></span>
<span data-ttu-id="d730f-122">В команде используется объект Configuration, созданный текущим командлетом в первой команде.</span><span class="sxs-lookup"><span data-stu-id="d730f-122">The command uses the configuration object that the current cmdlet created in the first command.</span></span>

## <span data-ttu-id="d730f-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d730f-123">PARAMETERS</span></span>

### <span data-ttu-id="d730f-124">-Controller0IPv4Address</span><span class="sxs-lookup"><span data-stu-id="d730f-124">-Controller0IPv4Address</span></span>
<span data-ttu-id="d730f-125">Указывает IPv4-адрес для контроллера 0.</span><span class="sxs-lookup"><span data-stu-id="d730f-125">Specifies the IPv4 address for controller 0.</span></span>
<span data-ttu-id="d730f-126">Указывайте этот параметр только для интерфейса Data0.</span><span class="sxs-lookup"><span data-stu-id="d730f-126">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="d730f-127">-Controller1IPv4Address</span><span class="sxs-lookup"><span data-stu-id="d730f-127">-Controller1IPv4Address</span></span>
<span data-ttu-id="d730f-128">Задает IPv4-адрес для контроллера 1.</span><span class="sxs-lookup"><span data-stu-id="d730f-128">Specifies the IPv4 address for controller 1.</span></span>
<span data-ttu-id="d730f-129">Указывайте этот параметр только для интерфейса Data0.</span><span class="sxs-lookup"><span data-stu-id="d730f-129">Specify this parameter only for the Data0 interface.</span></span>

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

### <span data-ttu-id="d730f-130">-EnableCloud</span><span class="sxs-lookup"><span data-stu-id="d730f-130">-EnableCloud</span></span>
<span data-ttu-id="d730f-131">Указывает, следует ли разрешать интерфейс в облаке.</span><span class="sxs-lookup"><span data-stu-id="d730f-131">Indicates whether to cloud-enable the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-132">-EnableIscsi</span><span class="sxs-lookup"><span data-stu-id="d730f-132">-EnableIscsi</span></span>
<span data-ttu-id="d730f-133">Указывает, следует ли включить в интерфейсе Интернет-SCSI (ISCSI).</span><span class="sxs-lookup"><span data-stu-id="d730f-133">Indicates whether to enable Internet SCSI (ISCSI) for the interface.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d730f-134">-InterfaceAlias</span><span class="sxs-lookup"><span data-stu-id="d730f-134">-InterfaceAlias</span></span>
<span data-ttu-id="d730f-135">Указывает псевдоним интерфейса интерфейса, для которого этот командлет предоставляет параметры.</span><span class="sxs-lookup"><span data-stu-id="d730f-135">Specifies the interface alias of interface for which this cmdlet supplies settings.</span></span>
<span data-ttu-id="d730f-136">Допустимые значения: от Data0 до Data5.</span><span class="sxs-lookup"><span data-stu-id="d730f-136">Valid values are from Data0 to Data5.</span></span>

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

### <span data-ttu-id="d730f-137">-IPv4Address</span><span class="sxs-lookup"><span data-stu-id="d730f-137">-IPv4Address</span></span>
<span data-ttu-id="d730f-138">Задает IPv4-адрес для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d730f-138">Specifies the IPv4 address for the interface.</span></span>

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

### <span data-ttu-id="d730f-139">-IPv4Gateway</span><span class="sxs-lookup"><span data-stu-id="d730f-139">-IPv4Gateway</span></span>
<span data-ttu-id="d730f-140">Указывает IPv4-адрес шлюза.</span><span class="sxs-lookup"><span data-stu-id="d730f-140">Specifies the IPv4 address of a gateway.</span></span>

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

### <span data-ttu-id="d730f-141">-IPv4Netmask</span><span class="sxs-lookup"><span data-stu-id="d730f-141">-IPv4Netmask</span></span>
<span data-ttu-id="d730f-142">Задает сетевую маску IPv4 для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d730f-142">Specifies the IPv4 netmask for the interface.</span></span>

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

### <span data-ttu-id="d730f-143">-IPv6Gateway</span><span class="sxs-lookup"><span data-stu-id="d730f-143">-IPv6Gateway</span></span>
<span data-ttu-id="d730f-144">Задает шлюз IPv6 для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d730f-144">Specifies the IPv6 gateway for the interface.</span></span>

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

### <span data-ttu-id="d730f-145">-IPv6Prefix</span><span class="sxs-lookup"><span data-stu-id="d730f-145">-IPv6Prefix</span></span>
<span data-ttu-id="d730f-146">Задает префикс IPv6 для интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d730f-146">Specifies the IPv6 prefix for the interface.</span></span>

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

### <span data-ttu-id="d730f-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="d730f-147">-Profile</span></span>
<span data-ttu-id="d730f-148">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="d730f-148">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="d730f-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d730f-149">CommonParameters</span></span>
<span data-ttu-id="d730f-150">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d730f-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d730f-151">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d730f-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d730f-152">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d730f-152">INPUTS</span></span>

### <span data-ttu-id="d730f-153">Ничего</span><span class="sxs-lookup"><span data-stu-id="d730f-153">None</span></span>

## <span data-ttu-id="d730f-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d730f-154">OUTPUTS</span></span>

### <span data-ttu-id="d730f-155">NetworkConfig</span><span class="sxs-lookup"><span data-stu-id="d730f-155">NetworkConfig</span></span>
<span data-ttu-id="d730f-156">Этот командлет возвращает объект NetworkConfig, который включает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="d730f-156">This cmdlet returns a NetworkConfig object that contains the following properties:</span></span> 

- <span data-ttu-id="d730f-157">**IsIscsiEnabled** ( **логическое значение** )</span><span class="sxs-lookup"><span data-stu-id="d730f-157">**IsIscsiEnabled** ( **Boolean** )</span></span> 
- <span data-ttu-id="d730f-158">**IsCloudEnabled** ( **логическое значение** )</span><span class="sxs-lookup"><span data-stu-id="d730f-158">**IsCloudEnabled** ( **Boolean** )</span></span>
- <span data-ttu-id="d730f-159">**Controller0IPv4Address** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-159">**Controller0IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-160">**Controller1IPv4Address** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-160">**Controller1IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-161">**IPv6Gateway** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-161">**IPv6Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-162">**IPv4Gateway** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-162">**IPv4Gateway** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-163">**IPv4Address** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-163">**IPv4Address** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-164">**IPv6Prefix** ( **строка** )</span><span class="sxs-lookup"><span data-stu-id="d730f-164">**IPv6Prefix** ( **String** )</span></span>
- <span data-ttu-id="d730f-165">**IPv4Netmask** ( **IP-адрес** )</span><span class="sxs-lookup"><span data-stu-id="d730f-165">**IPv4Netmask** ( **IPAddress** )</span></span> 
- <span data-ttu-id="d730f-166">**InterfaceAlias** ( **NetInterfaceId** )</span><span class="sxs-lookup"><span data-stu-id="d730f-166">**InterfaceAlias** ( **NetInterfaceId** )</span></span>

## <span data-ttu-id="d730f-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="d730f-167">NOTES</span></span>

## <span data-ttu-id="d730f-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d730f-168">RELATED LINKS</span></span>

[<span data-ttu-id="d730f-169">Set-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="d730f-169">Set-AzureStorSimpleDevice</span></span>](./Set-AzureStorSimpleDevice.md)

[<span data-ttu-id="d730f-170">Get-AzureStorSimpleDevice</span><span class="sxs-lookup"><span data-stu-id="d730f-170">Get-AzureStorSimpleDevice</span></span>](./Get-AzureStorSimpleDevice.md)


