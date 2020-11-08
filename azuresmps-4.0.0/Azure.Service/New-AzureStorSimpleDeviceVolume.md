---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 049201C9-590F-47EB-9030-25F80CD8DFA5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f3337556a9d7bd52e5800af5cdbd65b71ab9818
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075523"
---
# <span data-ttu-id="43292-101">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43292-101">New-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="43292-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43292-102">SYNOPSIS</span></span>
<span data-ttu-id="43292-103">Создание тома в указанном контейнере тома.</span><span class="sxs-lookup"><span data-stu-id="43292-103">Creates a volume in a specified volume container.</span></span>

## <span data-ttu-id="43292-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43292-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeContainer <DataContainer> -VolumeName <String>
 -VolumeSizeInBytes <Int64>
 -AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>
 -VolumeAppType <AppType> -Online <Boolean> -EnableDefaultBackup <Boolean> -EnableMonitoring <Boolean>
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="43292-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43292-105">DESCRIPTION</span></span>
<span data-ttu-id="43292-106">Командлет **New-AzureStorSimpleDeviceVolume** создает том в указанном контейнере тома.</span><span class="sxs-lookup"><span data-stu-id="43292-106">The **New-AzureStorSimpleDeviceVolume** cmdlet creates a volume in a specified volume container.</span></span>
<span data-ttu-id="43292-107">Этот командлет связывает каждый том с одной или несколькими записями управления доступом.</span><span class="sxs-lookup"><span data-stu-id="43292-107">This cmdlet associates each volume with one or more access control records.</span></span>
<span data-ttu-id="43292-108">Чтобы получить объекты **AccessControlRecord** , используйте командлет **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="43292-108">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="43292-109">Укажите имя, размер и тип для тома.</span><span class="sxs-lookup"><span data-stu-id="43292-109">Specify a name, size, and AppType for the volume.</span></span>
<span data-ttu-id="43292-110">Кроме того, укажите, нужно ли создавать том через Интернет, следует ли включить резервное копирование по умолчанию и следует ли включить мониторинг.</span><span class="sxs-lookup"><span data-stu-id="43292-110">Also, specify whether to create the volume online, whether to enable default backup, and whether to enable monitoring.</span></span>

## <span data-ttu-id="43292-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43292-111">EXAMPLES</span></span>

### <span data-ttu-id="43292-112">Пример 1: создание тома</span><span class="sxs-lookup"><span data-stu-id="43292-112">Example 1: Create a volume</span></span>
```
PS C:\>$AcrList = Get-AzureStorSimpleAccessControlRecord
PS C:\> Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer07" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Size 2000000000 -AccessControlRecords $AcrList -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False

VERBOSE: ClientRequestId: a29d1a84-1f81-4f20-9130-7adfe45e41fb_PS
VERBOSE: ClientRequestId: 8fa63df1-3f81-4029-a536-b536a70068ad_PS
VERBOSE: ClientRequestId: 964c5744-8bb1-4f70-beda-95ca4c7f3eb6_PS
VERBOSE: ClientRequestId: f09fff3a-54fa-4a0e-93db-b079260ed2dd_PS
VERBOSE: ClientRequestId: 59aa29e3-8044-411a-adae-b64a2681ffed_PS
VERBOSE: ClientRequestId: 0ffd0297-19be-40fe-a64e-6a2947d831b4_PS
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
c3b1ad53-7a51-49d7-ae83-94ff1ff3ab90 for tracking the task's status
VERBOSE: Volume container with name: VolumeContainer07 is found.
```

<span data-ttu-id="43292-113">Первая команда получает записи управления доступом в конфигурации службы StorSimple Manager с помощью командлета **Get-AzureStorSimpleAccessControlRecord** , а затем сохраняет их в переменной $AcrList.</span><span class="sxs-lookup"><span data-stu-id="43292-113">The first command gets the access control records in the StorSimple Manager service configuration by using the **Get-AzureStorSimpleAccessControlRecord** cmdlet, and then stores them in the $AcrList variable.</span></span>

<span data-ttu-id="43292-114">Вторая команда получает контейнер томов с именем VolumeContainer07 для устройства с именем Contoso63-AppVm с помощью командлета **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="43292-114">The second command gets the volume container named VolumeContainer07 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="43292-115">Команда передает этот контейнер текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="43292-115">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43292-116">Этот командлет создает том.</span><span class="sxs-lookup"><span data-stu-id="43292-116">This cmdlet creates the volume.</span></span>
<span data-ttu-id="43292-117">Команда задает имя тома, размер и записи управления доступом, хранящиеся в $AcrList.</span><span class="sxs-lookup"><span data-stu-id="43292-117">The command specifies the name for the volume, the size, and the access control records stored in $AcrList.</span></span>
<span data-ttu-id="43292-118">Эта команда запускает задание, а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="43292-118">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="43292-119">Чтобы просмотреть состояние задания, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="43292-119">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="43292-120">Пример 2: создание тома без доступа к элементу управления Controlaccess элемента управления recordsaccess</span><span class="sxs-lookup"><span data-stu-id="43292-120">Example 2: Create a volume without Access Controlaccess control recordsaccess control</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "VolumeContainer01" | New-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume22" -Size 2000000000 -AccessControlRecords @() -VolumeAppType PrimaryVolume -Online $True -EnableDefaultBackup $False -EnableMonitoring $False -WaitForComplete
VERBOSE: ClientRequestId: 3f359790-7e1f-48e7-acf8-ecabba850966_PS
VERBOSE: ClientRequestId: 2723ebcf-cd72-47bb-99b5-0c099d45641b_PS
VERBOSE: ClientRequestId: e605091f-dd63-42a7-bda2-24753cbc1f9a_PS
VERBOSE: ClientRequestId: b3fd08c3-67c5-4309-9591-15d92c360469_PS
VERBOSE: ClientRequestId: 15a024a3-b0c9-4f83-9c34-0ed8b95d024b_PS
VERBOSE: ClientRequestId: c13f92f9-aea1-40dd-af80-3affe273adbe_PS


TaskId       : ceef657e-390e-4f7a-aab7-669a29c29e7f
TaskResult   : Succeeded
TaskStatus   : Completed
ErrorCode    : 
ErrorMessage : 
TaskSteps    : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The task created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: 1d79febf-f752-4255-af2d-230d40773bc6_PS
AccessType             : NoAccess
AcrIdList              : {}
AcrList                : {}
AppType                : PrimaryVolume
DataContainer          : Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainer
DataContainerId        : 68b63d15-6aa5-4e69-9f9d-4a0bc607d6e9
InstanceId             : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd
InternalInstanceId     : 
IsBackupEnabled        : False
IsDefaultBackupEnabled : False
IsMonitoringEnabled    : False
Name                   : Volume22
Online                 : True
OperationInProgress    : None
SizeInBytes            : 2000000000
VSN                    : SS-VOL-d73b7eec-76fc-4310-b347-69b160de8cdd

VERBOSE: Volume container with name: VolumeContainer01 is found.
```

<span data-ttu-id="43292-121">Эта команда получает контейнер томов с именем VolumeContainer01 для устройства с именем Contoso63-AppVm с помощью командлета **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="43292-121">This command gets the volume container named VolumeContainer01 for the device named Contoso63-AppVm by using the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>
<span data-ttu-id="43292-122">Команда передает этот контейнер текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="43292-122">The command passes that container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="43292-123">Этот командлет создает том.</span><span class="sxs-lookup"><span data-stu-id="43292-123">This cmdlet creates the volume.</span></span>
<span data-ttu-id="43292-124">Команда задает имя тома, его размер и пустое значение для записей управления доступом.</span><span class="sxs-lookup"><span data-stu-id="43292-124">The command specifies the name for the volume, the size, and an empty value for access control records.</span></span>
<span data-ttu-id="43292-125">Эта команда задает параметр *WaitForComplete* , поэтому он возвращает **TaskStatusInfo** после создания тома.</span><span class="sxs-lookup"><span data-stu-id="43292-125">This command specifies the *WaitForComplete* parameter, so it returns a **TaskStatusInfo** after it creates the volume.</span></span>

<span data-ttu-id="43292-126">Поскольку в команде не указаны записи управления доступом, этот том недоступен.</span><span class="sxs-lookup"><span data-stu-id="43292-126">Because the command specifies no access control records, this volume cannot be accessed.</span></span>
<span data-ttu-id="43292-127">Вы можете добавить доступ позже с помощью командлета **Set-AzureStorSimpleDeviceVolume** .</span><span class="sxs-lookup"><span data-stu-id="43292-127">You can add access, later, by using **Set-AzureStorSimpleDeviceVolume** cmdlet.</span></span>

## <span data-ttu-id="43292-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43292-128">PARAMETERS</span></span>

### <span data-ttu-id="43292-129">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="43292-129">-AccessControlRecords</span></span>
<span data-ttu-id="43292-130">Указывает список записей контроля доступа, которые нужно связать с томом.</span><span class="sxs-lookup"><span data-stu-id="43292-130">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43292-131">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="43292-131">-DeviceName</span></span>
<span data-ttu-id="43292-132">Указывает имя устройства StorSimple, на котором нужно создать том.</span><span class="sxs-lookup"><span data-stu-id="43292-132">Specifies the name of the StorSimple device on which to create the volume.</span></span>

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

### <span data-ttu-id="43292-133">-EnableDefaultBackup</span><span class="sxs-lookup"><span data-stu-id="43292-133">-EnableDefaultBackup</span></span>
<span data-ttu-id="43292-134">Указывает, следует ли включить резервное копирование по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="43292-134">Specifies whether to enable default backup for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-135">-EnableMonitoring</span><span class="sxs-lookup"><span data-stu-id="43292-135">-EnableMonitoring</span></span>
<span data-ttu-id="43292-136">Указывает, следует ли включить мониторинг для тома.</span><span class="sxs-lookup"><span data-stu-id="43292-136">Specifies whether to enable monitoring for the volume.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-137">-Online</span><span class="sxs-lookup"><span data-stu-id="43292-137">-Online</span></span>
<span data-ttu-id="43292-138">Указывает, нужно ли создавать том через Интернет.</span><span class="sxs-lookup"><span data-stu-id="43292-138">Specifies whether to create the volume online.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="43292-139">-Profile</span></span>
<span data-ttu-id="43292-140">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="43292-140">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="43292-141">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="43292-141">-VolumeAppType</span></span>
<span data-ttu-id="43292-142">Указывает, нужно ли создавать основной или архивированный том.</span><span class="sxs-lookup"><span data-stu-id="43292-142">Specifies whether to create a primary or archive volume.</span></span>
<span data-ttu-id="43292-143">Допустимые значения: PrimaryVolume и ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="43292-143">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-144">-VolumeContainer</span><span class="sxs-lookup"><span data-stu-id="43292-144">-VolumeContainer</span></span>
<span data-ttu-id="43292-145">Определяет контейнер, как объект **содержания** , в котором нужно создать том.</span><span class="sxs-lookup"><span data-stu-id="43292-145">Specifies the container, as a **DataContainer** object, in which to create the volume.</span></span>
<span data-ttu-id="43292-146">Чтобы получить объект **VirtualDisk** , используйте командлет **Get-AzureStorSimpleDeviceVolumeContainer** .</span><span class="sxs-lookup"><span data-stu-id="43292-146">To obtain a **VirtualDisk** object, use the **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet.</span></span>

```yaml
Type: DataContainer
Parameter Sets: (All)
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43292-147">-Тома</span><span class="sxs-lookup"><span data-stu-id="43292-147">-VolumeName</span></span>
<span data-ttu-id="43292-148">Задает имя для нового тома.</span><span class="sxs-lookup"><span data-stu-id="43292-148">Specifies a name for the new volume.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-149">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="43292-149">-VolumeSizeInBytes</span></span>
<span data-ttu-id="43292-150">Указывает размер тома в байтах.</span><span class="sxs-lookup"><span data-stu-id="43292-150">Specifies the volume size in bytes.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-151">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="43292-151">-WaitForComplete</span></span>
<span data-ttu-id="43292-152">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="43292-152">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43292-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43292-153">CommonParameters</span></span>
<span data-ttu-id="43292-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43292-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43292-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43292-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43292-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43292-156">INPUTS</span></span>

### <span data-ttu-id="43292-157">Контейнер содержания, список\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="43292-157">DataContainer, List\<AccessControlRecord\></span></span>
<span data-ttu-id="43292-158">Этот командлет принимает объект- **контейнер** данных и список объектов **AccessControlRecord** для нового тома.</span><span class="sxs-lookup"><span data-stu-id="43292-158">This cmdlet accepts a **DataContainer** object and a list of **AccessControlRecord** objects for the new volume.</span></span>

## <span data-ttu-id="43292-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43292-159">OUTPUTS</span></span>

### <span data-ttu-id="43292-160">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="43292-160">TaskStatusInfo</span></span>
<span data-ttu-id="43292-161">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="43292-161">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="43292-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="43292-162">NOTES</span></span>

## <span data-ttu-id="43292-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43292-163">RELATED LINKS</span></span>

[<span data-ttu-id="43292-164">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43292-164">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43292-165">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43292-165">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43292-166">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="43292-166">Set-AzureStorSimpleDeviceVolume</span></span>](./Set-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="43292-167">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="43292-167">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="43292-168">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="43292-168">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="43292-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="43292-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


