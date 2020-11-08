---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 39E9BB88-6AD8-4B05-9498-35393E22BA30
online version: ''
schema: 2.0.0
ms.openlocfilehash: 234b1f7fa2719cc1b34e6bcd0b8e8fd340acc4af
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076418"
---
# <span data-ttu-id="6690f-101">Set-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="6690f-101">Set-AzureStorSimpleDeviceVolume</span></span>

## <span data-ttu-id="6690f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6690f-102">SYNOPSIS</span></span>
<span data-ttu-id="6690f-103">Обновляет свойства существующего тома.</span><span class="sxs-lookup"><span data-stu-id="6690f-103">Updates the properties of an existing volume.</span></span>

## <span data-ttu-id="6690f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6690f-104">SYNTAX</span></span>

### <span data-ttu-id="6690f-105">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="6690f-105">IdentifyByName</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -VolumeName <String> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="6690f-106">IdentifyByObject</span><span class="sxs-lookup"><span data-stu-id="6690f-106">IdentifyByObject</span></span>
```
Set-AzureStorSimpleDeviceVolume -DeviceName <String> -Volume <VirtualDisk> [-Online <Boolean>]
 [-VolumeSizeInBytes <Int64>] [-VolumeAppType <AppType>]
 [-AccessControlRecords <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]>]
 [-WaitForComplete] [-NewName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="6690f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6690f-107">DESCRIPTION</span></span>
<span data-ttu-id="6690f-108">Командлет **Set-AzureStorSimpleDeviceVolume** обновляет свойства существующего тома.</span><span class="sxs-lookup"><span data-stu-id="6690f-108">The **Set-AzureStorSimpleDeviceVolume** cmdlet updates the properties of an existing volume.</span></span>
<span data-ttu-id="6690f-109">Этот командлет связывает том с одной или несколькими записями управления доступом.</span><span class="sxs-lookup"><span data-stu-id="6690f-109">This cmdlet associates a volume with one or more access control records.</span></span>
<span data-ttu-id="6690f-110">Чтобы получить объекты **AccessControlRecord** , используйте командлет **Get-AzureStorSimpleAccessControlRecord** .</span><span class="sxs-lookup"><span data-stu-id="6690f-110">To obtain **AccessControlRecord** objects, use the **Get-AzureStorSimpleAccessControlRecord** cmdlet.</span></span>
<span data-ttu-id="6690f-111">Обновите размер или тип тома.</span><span class="sxs-lookup"><span data-stu-id="6690f-111">Update the size or type for the volume.</span></span>
<span data-ttu-id="6690f-112">Кроме того, вы можете изменить способ создания тома через Интернет.</span><span class="sxs-lookup"><span data-stu-id="6690f-112">Also, update whether to create the volume online.</span></span>

## <span data-ttu-id="6690f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6690f-113">EXAMPLES</span></span>

### <span data-ttu-id="6690f-114">Пример 1: Обновление значения Online для тома</span><span class="sxs-lookup"><span data-stu-id="6690f-114">Example 1: Update online value for a volume</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $False
VERBOSE: ClientRequestId: f2869570-ea47-4be7-801e-9c0f22f2600d_PS
VERBOSE: ClientRequestId: c70bb86a-51d3-4390-be17-4d0847641dc3_PS
VERBOSE: ClientRequestId: d20cb5b2-6b3c-4e06-af99-cada28c5e50a_PS
VERBOSE: ClientRequestId: ab6d533e-b55b-4cfb-9c58-9153295e0547_PS
de7000f1-29c7-4102-a375-b52432f9e67e
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
de7000f1-29c7-4102-a375-b52432f9e67e for tracking the task's status
```

<span data-ttu-id="6690f-115">Эта команда обновляет том с именем Volume18, чтобы иметь онлайновую величину $False.</span><span class="sxs-lookup"><span data-stu-id="6690f-115">This command updates the volume named Volume18 to have an online value of $False.</span></span>
<span data-ttu-id="6690f-116">Эта команда запускает задачу, а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="6690f-116">This command starts the task, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="6690f-117">Чтобы просмотреть состояние задачи, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="6690f-117">To see the status of the task, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

### <span data-ttu-id="6690f-118">Пример 2: изменение значения и типа Online</span><span class="sxs-lookup"><span data-stu-id="6690f-118">Example 2: Modify online value and type</span></span>
```
PS C:\>Set-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "Volume18" -Online $True -VolumeAppType ArchiveVolume 
VERBOSE: ClientRequestId: af42b02a-645e-4801-a2d7-4197511c68cf_PS
VERBOSE: ClientRequestId: 7cb4f3b4-548e-42dc-a38c-0df0911c5206_PS
VERBOSE: ClientRequestId: 7cc706ad-a58f-4939-8e78-cabae8379a51_PS
VERBOSE: ClientRequestId: 6bed21d5-12fc-4a12-a89c-120bdb5636b1_PS
aa977225-af78-4c93-b754-72704afc928f
VERBOSE: The update task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
aa977225-af78-4c93-b754-72704afc928f for tracking the task's status
```

<span data-ttu-id="6690f-119">Эта команда обновляет том с именем Volume18.</span><span class="sxs-lookup"><span data-stu-id="6690f-119">This command updates the volume named Volume18.</span></span>
<span data-ttu-id="6690f-120">Он изменяет тип и изменяет значение параметра *Online* на $true.</span><span class="sxs-lookup"><span data-stu-id="6690f-120">It modifies the type and changes the value of the *Online* parameter to $True.</span></span>

## <span data-ttu-id="6690f-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6690f-121">PARAMETERS</span></span>

### <span data-ttu-id="6690f-122">-AccessControlRecords</span><span class="sxs-lookup"><span data-stu-id="6690f-122">-AccessControlRecords</span></span>
<span data-ttu-id="6690f-123">Указывает список записей контроля доступа, которые нужно связать с томом.</span><span class="sxs-lookup"><span data-stu-id="6690f-123">Specifies a list of access control records to associate with the volume.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.AccessControlRecord]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-124">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="6690f-124">-DeviceName</span></span>
<span data-ttu-id="6690f-125">Указывает имя устройства StorSimple, на котором находится том, на котором нужно обновить том.</span><span class="sxs-lookup"><span data-stu-id="6690f-125">Specifies the name of the StorSimple device on which to update the volume exists.</span></span>

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

### <span data-ttu-id="6690f-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="6690f-126">-InformationAction</span></span>
<span data-ttu-id="6690f-127">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="6690f-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="6690f-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6690f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6690f-129">Продолжал</span><span class="sxs-lookup"><span data-stu-id="6690f-129">Continue</span></span>
- <span data-ttu-id="6690f-130">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="6690f-130">Ignore</span></span>
- <span data-ttu-id="6690f-131">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="6690f-131">Inquire</span></span>
- <span data-ttu-id="6690f-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="6690f-132">SilentlyContinue</span></span>
- <span data-ttu-id="6690f-133">Остановить</span><span class="sxs-lookup"><span data-stu-id="6690f-133">Stop</span></span>
- <span data-ttu-id="6690f-134">Рвать</span><span class="sxs-lookup"><span data-stu-id="6690f-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="6690f-135">-InformationVariable</span></span>
<span data-ttu-id="6690f-136">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="6690f-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-137">-NewName</span><span class="sxs-lookup"><span data-stu-id="6690f-137">-NewName</span></span>
<span data-ttu-id="6690f-138">Указывает новое имя для устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="6690f-138">Specifies a new name for the StorSimple device.</span></span>

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

### <span data-ttu-id="6690f-139">-Online</span><span class="sxs-lookup"><span data-stu-id="6690f-139">-Online</span></span>
<span data-ttu-id="6690f-140">Указывает, находится ли том в сети.</span><span class="sxs-lookup"><span data-stu-id="6690f-140">Specifies whether the volume is online.</span></span>

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

### <span data-ttu-id="6690f-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="6690f-141">-Profile</span></span>
<span data-ttu-id="6690f-142">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="6690f-142">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="6690f-143">-Volume</span><span class="sxs-lookup"><span data-stu-id="6690f-143">-Volume</span></span>
<span data-ttu-id="6690f-144">Указывает имя тома для обновления.</span><span class="sxs-lookup"><span data-stu-id="6690f-144">Specifies the name of the volume to update.</span></span>

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-145">-VolumeAppType</span><span class="sxs-lookup"><span data-stu-id="6690f-145">-VolumeAppType</span></span>
<span data-ttu-id="6690f-146">Указывает, нужно ли обновлять том на основной или архивный.</span><span class="sxs-lookup"><span data-stu-id="6690f-146">Specifies whether to update the volume to be a primary or archive volume.</span></span>
<span data-ttu-id="6690f-147">Допустимые значения: PrimaryVolume и ArchiveVolume.</span><span class="sxs-lookup"><span data-stu-id="6690f-147">Valid values are: PrimaryVolume and ArchiveVolume.</span></span>

```yaml
Type: AppType
Parameter Sets: (All)
Aliases: AppType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-148">-Тома</span><span class="sxs-lookup"><span data-stu-id="6690f-148">-VolumeName</span></span>
<span data-ttu-id="6690f-149">Указывает имя тома для обновления.</span><span class="sxs-lookup"><span data-stu-id="6690f-149">Specifies the name of the volume to update.</span></span>

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

### <span data-ttu-id="6690f-150">-VolumeSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6690f-150">-VolumeSizeInBytes</span></span>
<span data-ttu-id="6690f-151">Задает обновленный размер тома (в байтах).</span><span class="sxs-lookup"><span data-stu-id="6690f-151">Specifies the updated size, in bytes, for the volume.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: SizeInBytes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6690f-152">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="6690f-152">-WaitForComplete</span></span>
<span data-ttu-id="6690f-153">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6690f-153">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="6690f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6690f-154">CommonParameters</span></span>
<span data-ttu-id="6690f-155">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6690f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6690f-156">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6690f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6690f-157">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6690f-157">INPUTS</span></span>

### <span data-ttu-id="6690f-158">Список\<AccessControlRecord\></span><span class="sxs-lookup"><span data-stu-id="6690f-158">List\<AccessControlRecord\></span></span>
<span data-ttu-id="6690f-159">Этот командлет принимает список объектов **AccessControlRecord** , которые нужно связать с томом.</span><span class="sxs-lookup"><span data-stu-id="6690f-159">This cmdlet accepts a list of **AccessControlRecord** objects to associate to a volume.</span></span>

## <span data-ttu-id="6690f-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6690f-160">OUTPUTS</span></span>

### <span data-ttu-id="6690f-161">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="6690f-161">TaskStatusInfo</span></span>
<span data-ttu-id="6690f-162">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="6690f-162">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="6690f-163">Пуск</span><span class="sxs-lookup"><span data-stu-id="6690f-163">NOTES</span></span>

## <span data-ttu-id="6690f-164">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6690f-164">RELATED LINKS</span></span>

[<span data-ttu-id="6690f-165">Get-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="6690f-165">Get-AzureStorSimpleDeviceVolume</span></span>](./Get-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="6690f-166">New-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="6690f-166">New-AzureStorSimpleDeviceVolume</span></span>](./New-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="6690f-167">Remove-AzureStorSimpleDeviceVolume</span><span class="sxs-lookup"><span data-stu-id="6690f-167">Remove-AzureStorSimpleDeviceVolume</span></span>](./Remove-AzureStorSimpleDeviceVolume.md)

[<span data-ttu-id="6690f-168">Get-AzureStorSimpleAccessControlRecord</span><span class="sxs-lookup"><span data-stu-id="6690f-168">Get-AzureStorSimpleAccessControlRecord</span></span>](./Get-AzureStorSimpleAccessControlRecord.md)

[<span data-ttu-id="6690f-169">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="6690f-169">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


