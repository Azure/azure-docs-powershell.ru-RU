---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 79EE846E-D5BE-4808-BC6F-E3B16A308AB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9d0cd7ef0eacc7ff3e38c4619b60a0bd61f24f1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075566"
---
# <span data-ttu-id="13005-101">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="13005-101">Get-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="13005-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="13005-102">SYNOPSIS</span></span>
<span data-ttu-id="13005-103">Получает тома на устройстве.</span><span class="sxs-lookup"><span data-stu-id="13005-103">Gets volumes on a device.</span></span>

## <span data-ttu-id="13005-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="13005-104">SYNTAX</span></span>

### <span data-ttu-id="13005-105">IdentifyByParentObject</span><span class="sxs-lookup"><span data-stu-id="13005-105">IdentifyByParentObject</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="13005-106">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="13005-106">IdentifyByName</span></span>
```
Get-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="13005-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="13005-107">DESCRIPTION</span></span>
<span data-ttu-id="13005-108">Командлет **Get-AzureStorSimpleDeviceVolume** получает список томов для определенного контейнера тома или тома с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="13005-108">The **Get-AzureStorSimpleDeviceVolume** cmdlet gets a list of volumes for a specified volume container, or volume that has the specified name.</span></span>
<span data-ttu-id="13005-109">Возвращенный объект имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="13005-109">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="13005-110">**AccessType**</span><span class="sxs-lookup"><span data-stu-id="13005-110">**AccessType**</span></span>
- <span data-ttu-id="13005-111">**AcrList**</span><span class="sxs-lookup"><span data-stu-id="13005-111">**AcrList**</span></span>
- <span data-ttu-id="13005-112">**Тип**</span><span class="sxs-lookup"><span data-stu-id="13005-112">**AppType**</span></span>
- <span data-ttu-id="13005-113">**Контейнер содержания**</span><span class="sxs-lookup"><span data-stu-id="13005-113">**DataContainer**</span></span>
- <span data-ttu-id="13005-114">**DataContainerId**</span><span class="sxs-lookup"><span data-stu-id="13005-114">**DataContainerId**</span></span>
- <span data-ttu-id="13005-115">**ИД**</span><span class="sxs-lookup"><span data-stu-id="13005-115">**InstanceId**</span></span>
- <span data-ttu-id="13005-116">**IsBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="13005-116">**IsBackupEnabled**</span></span>
- <span data-ttu-id="13005-117">**IsDefaultBackupEnabled**</span><span class="sxs-lookup"><span data-stu-id="13005-117">**IsDefaultBackupEnabled**</span></span>
- <span data-ttu-id="13005-118">**IsMonitoringEnabled**</span><span class="sxs-lookup"><span data-stu-id="13005-118">**IsMonitoringEnabled**</span></span>
- <span data-ttu-id="13005-119">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="13005-119">**Name**</span></span>
- <span data-ttu-id="13005-120">**Онлайн**</span><span class="sxs-lookup"><span data-stu-id="13005-120">**Online**</span></span>
- <span data-ttu-id="13005-121">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="13005-121">**OperationInProgress**</span></span>
- <span data-ttu-id="13005-122">**SizeInBytes**</span><span class="sxs-lookup"><span data-stu-id="13005-122">**SizeInBytes**</span></span>
- <span data-ttu-id="13005-123">**VSN**</span><span class="sxs-lookup"><span data-stu-id="13005-123">**VSN**</span></span>

## <span data-ttu-id="13005-124">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="13005-124">EXAMPLES</span></span>

### <span data-ttu-id="13005-125">Пример 1: получение томов в указанном контейнере</span><span class="sxs-lookup"><span data-stu-id="13005-125">Example 1: Get volumes in a specified container</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container03" | Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm"
InstanceId             : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c
Name                   : Volume 1 Clone
Online                 : True
SizeInBytes            : 3298534883328
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017214433280-ade42af6-dabb-449d-b66b-4f5d06891d4c

InstanceId             : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe
Name                   : Volume 3 Clone
Online                 : True
SizeInBytes            : 1717986918400
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : BA-1503262017366008684-cf8bb1a3-21e5-4cfc-ba0d-bfe238d77ebe

InstanceId             : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
Name                   : Volume 4
Online                 : True
SizeInBytes            : 1610612736000
AccessType             : ReadWrite
AcrList                : {Linux_XYUSFL719_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-2180be94-36f1-473e-a42b-a3ebd2cdb481
```

<span data-ttu-id="13005-126">Эта команда получает контейнер томов с именем Container03 на устройстве с именем Contoso63-AppVm с помощью командлета **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="13005-126">This command gets the volume container named Container03 on the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="13005-127">Команда использует оператор конвейера для передачи этого контейнера в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="13005-127">The command uses the pipeline operator to pass that container to the current cmdlet.</span></span>
<span data-ttu-id="13005-128">Этот командлет получает все тома в контейнере для устройства с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="13005-128">That cmdlet gets all the volumes in that container for the device named Contoso63-AppVm.</span></span>

### <span data-ttu-id="13005-129">Пример 2: получение тома с помощью его имени</span><span class="sxs-lookup"><span data-stu-id="13005-129">Example 2: Get a volume by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18"
InstanceId             : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
Name                   : Volume18
Online                 : True
SizeInBytes            : 2748779069440
AccessType             : ReadWrite
AcrList                : {Windows_XYUSFL718-RV_ACR}
AppType                : Invalid
DataContainerId        : 127135b6-92de-4f53-850d-70e1f9a38cbe
IsBackupEnabled        : True
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
VSN                    : SS-VOL-c75e9636-1dcf-43db-92df-3af1ecf3f18a
```

<span data-ttu-id="13005-130">Эта команда получает том с именем Volume18 на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="13005-130">This command gets the volume named Volume18 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="13005-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="13005-131">PARAMETERS</span></span>

### <span data-ttu-id="13005-132">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="13005-132">-DeviceName</span></span>
<span data-ttu-id="13005-133">Указывает имя устройства StorSimple, из которого нужно получить тома.</span><span class="sxs-lookup"><span data-stu-id="13005-133">Specifies the name of the StorSimple device from which to get volumes.</span></span>

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

### <span data-ttu-id="13005-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="13005-134">-Profile</span></span>
<span data-ttu-id="13005-135">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="13005-135">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="13005-136">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="13005-136">-VolumeContainer</span></span>
<span data-ttu-id="13005-137">Указывает контейнер томов, **как объект-контейнер,** включающий тома для получения.</span><span class="sxs-lookup"><span data-stu-id="13005-137">Specifies the volume container, as a **DataContainer** object, that includes the volumes to get.</span></span>
<span data-ttu-id="13005-138">Чтобы получить объект **Contain** , используйте командлет **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="13005-138">To obtain a **DataContainer** , use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: IdentifyByParentObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="13005-139">-Тома</span><span class="sxs-lookup"><span data-stu-id="13005-139">-VolumeName</span></span>
<span data-ttu-id="13005-140">Указывает имя тома, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13005-140">Specifies the name of the volume to get.</span></span>

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="13005-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13005-141">CommonParameters</span></span>
<span data-ttu-id="13005-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="13005-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13005-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="13005-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13005-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="13005-144">INPUTS</span></span>

### <span data-ttu-id="13005-145">Контейнер содержания</span><span class="sxs-lookup"><span data-stu-id="13005-145">DataContainer</span></span>
<span data-ttu-id="13005-146">Этот командлет принимает объект- **контейнер** , содержащий том, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="13005-146">This cmdlet accepts a **DataContainer** object that contains the volume to get.</span></span>

## <span data-ttu-id="13005-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="13005-147">OUTPUTS</span></span>

### <span data-ttu-id="13005-148">VirtualDisk, IList\<VirtualDisk\></span><span class="sxs-lookup"><span data-stu-id="13005-148">VirtualDisk, IList\<VirtualDisk\></span></span>
<span data-ttu-id="13005-149">Этот командлет возвращает объект **VirtualDisk** , если указан параметр "значение *тома* ".</span><span class="sxs-lookup"><span data-stu-id="13005-149">This cmdlet returns a **VirtualDisk** object if you specify the *VolumeName* parameter.</span></span>
<span data-ttu-id="13005-150">Если указан *VolumeContainer* , этот командлет возвращает объект **IList \<VirtualDisk\>** .</span><span class="sxs-lookup"><span data-stu-id="13005-150">If you specify the *VolumeContainer* , this cmdlet returns an **IList\<VirtualDisk\>** object.</span></span>

## <span data-ttu-id="13005-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="13005-151">NOTES</span></span>

## <span data-ttu-id="13005-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="13005-152">RELATED LINKS</span></span>

[<span data-ttu-id="13005-153">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="13005-153">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="13005-154">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="13005-154">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="13005-155">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="13005-155">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="13005-156">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="13005-156">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)


