---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075776"
---
# <span data-ttu-id="27586-101">Start-AzureStorSimpleDeviceFailoverJob</span><span class="sxs-lookup"><span data-stu-id="27586-101">Start-AzureStorSimpleDeviceFailoverJob</span></span>

## <span data-ttu-id="27586-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27586-102">SYNOPSIS</span></span>
<span data-ttu-id="27586-103">Инициирует операцию отработки отказа для групп контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="27586-103">Initiates a failover operation of volume container groups.</span></span>

## <span data-ttu-id="27586-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27586-104">SYNTAX</span></span>

### <span data-ttu-id="27586-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="27586-105">Empty (Default)</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="27586-106">IdentifyById</span><span class="sxs-lookup"><span data-stu-id="27586-106">IdentifyById</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="27586-107">IdentifyByName</span><span class="sxs-lookup"><span data-stu-id="27586-107">IdentifyByName</span></span>
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="27586-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27586-108">DESCRIPTION</span></span>
<span data-ttu-id="27586-109">Командлет **Start-AzureStorSimpleDeviceFailoverJob** инициирует операцию отработки отказа для одной или нескольких групп контейнера тома от одного устройства к другому.</span><span class="sxs-lookup"><span data-stu-id="27586-109">The **Start-AzureStorSimpleDeviceFailoverJob** cmdlet initiates a failover operation of one or more volume container groups from one device to another.</span></span>

## <span data-ttu-id="27586-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27586-110">EXAMPLES</span></span>

### <span data-ttu-id="27586-111">Пример 1: запуск задания отработки отказа для именованного устройства и именованного целевого устройства</span><span class="sxs-lookup"><span data-stu-id="27586-111">Example 1: Start a failover job for a named device and named target device</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="27586-112">Эта команда получает контейнеры отказоустойчивого тома для устройства с именем ChewD_App7 с помощью командлета **Get-AzureStorSimpleFailoverVolumeContainers** .</span><span class="sxs-lookup"><span data-stu-id="27586-112">This command gets the failover volume containers for the device named ChewD_App7 by using the **Get-AzureStorSimpleFailoverVolumeContainers** cmdlet.</span></span>
<span data-ttu-id="27586-113">Команда передает результаты в командлет **Where-Object** , в результате чего удаляются контейнеры со значением, отличным от $true для свойства **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="27586-113">The command passes the results to the **Where-Object** cmdlet, which drops those containers that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="27586-114">Для получения дополнительных сведений введите `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="27586-114">For more information, type `Get-Help Where-Object`.</span></span>
<span data-ttu-id="27586-115">Текущий командлет запускает задания отработки отказа для оставшихся контейнеров отказоустойчивого тома.</span><span class="sxs-lookup"><span data-stu-id="27586-115">The current cmdlet starts failover jobs for the remaining failover volume containers.</span></span>
<span data-ttu-id="27586-116">Команда задает имя устройства и имя оконечного устройства.</span><span class="sxs-lookup"><span data-stu-id="27586-116">The command specifies the device name and target device name.</span></span>
<span data-ttu-id="27586-117">Команда возвращает идентификатор экземпляра задания, с которого начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="27586-117">The command returns the instance ID of the job that the cmdlet starts.</span></span>

### <span data-ttu-id="27586-118">Пример 2: начало задания отработки отказа для устройства и оконечного устройства, указанного ИДЕНТИФИКАТОРом</span><span class="sxs-lookup"><span data-stu-id="27586-118">Example 2: Start a failover job for a device and target device specified by ID</span></span>
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

<span data-ttu-id="27586-119">Эта команда получает контейнеры отказоустойчивого тома для устройства с именем ChewD_App7 с помощью **Get-AzureStorSimpleFailoverVolumeContainers**.</span><span class="sxs-lookup"><span data-stu-id="27586-119">This command gets the failover volume containers for the device named ChewD_App7 by using **Get-AzureStorSimpleFailoverVolumeContainers**.</span></span>
<span data-ttu-id="27586-120">Команда передает результаты в **Where-Object** , которая удаляет эти containters со значением, отличным от $true для свойства **IsDCGroupEligibleForDR** .</span><span class="sxs-lookup"><span data-stu-id="27586-120">The command passes the results to **Where-Object** , which drops those containters that have a value other than $True for the **IsDCGroupEligibleForDR** property.</span></span>
<span data-ttu-id="27586-121">Командлет передает результаты командлету **Select-Object** , выбирающему первый объект, передаваемый в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="27586-121">The cmdlet passes the results to the **Select-Object** cmdlet, which selects the first object to pass to the current cmdlet.</span></span>
<span data-ttu-id="27586-122">Для получения дополнительных сведений введите `Get-Help Select-Object` .</span><span class="sxs-lookup"><span data-stu-id="27586-122">For more information, type `Get-Help Select-Object`.</span></span>
<span data-ttu-id="27586-123">Текущий командлет запускает задания отработки отказа для выбранного контейнера отказоустойчивого тома.</span><span class="sxs-lookup"><span data-stu-id="27586-123">The current cmdlet starts failover jobs for the selected failover volume container.</span></span>
<span data-ttu-id="27586-124">Команда задает идентификатор устройства и идентификатор целевого устройства.</span><span class="sxs-lookup"><span data-stu-id="27586-124">The command specifies the device ID and target device ID.</span></span>
<span data-ttu-id="27586-125">Команда возвращает идентификатор экземпляра задания, с которого начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="27586-125">The command returns the instance ID of the job that the cmdlet starts.</span></span>

## <span data-ttu-id="27586-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27586-126">PARAMETERS</span></span>

### <span data-ttu-id="27586-127">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="27586-127">-DeviceId</span></span>
<span data-ttu-id="27586-128">Указывает ИД экземпляра устройства StorSimple, на котором находятся группы контейнеров тома.</span><span class="sxs-lookup"><span data-stu-id="27586-128">Specifies the instance ID of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="27586-129">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="27586-129">-DeviceName</span></span>
<span data-ttu-id="27586-130">Указывает имя устройства StorSimple, на котором находятся группы контейнеров тома.</span><span class="sxs-lookup"><span data-stu-id="27586-130">Specifies the name of the StorSimple device on which the volume container groups exist.</span></span>

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

### <span data-ttu-id="27586-131">-Force</span><span class="sxs-lookup"><span data-stu-id="27586-131">-Force</span></span>
<span data-ttu-id="27586-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="27586-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="27586-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="27586-133">-Profile</span></span>
<span data-ttu-id="27586-134">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="27586-134">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="27586-135">-TargetDeviceId</span><span class="sxs-lookup"><span data-stu-id="27586-135">-TargetDeviceId</span></span>
<span data-ttu-id="27586-136">Указывает идентификатор экземпляра устройства StorSimple, которому этот командлет не проходит группы контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="27586-136">Specifies the instance ID of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="27586-137">-TargetDeviceName</span><span class="sxs-lookup"><span data-stu-id="27586-137">-TargetDeviceName</span></span>
<span data-ttu-id="27586-138">Указывает имя устройства StorSimple, для которого этот командлет не проходит группы контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="27586-138">Specifies the name of the StorSimple device to which this cmdlet fails over the volume container groups.</span></span>

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

### <span data-ttu-id="27586-139">-VolumecontainerGroups</span><span class="sxs-lookup"><span data-stu-id="27586-139">-VolumecontainerGroups</span></span>
<span data-ttu-id="27586-140">Указывает список групп контейнеров томов, на которые не передается этот командлет на другое устройство.</span><span class="sxs-lookup"><span data-stu-id="27586-140">Specifies the list of volume container groups that this cmdlet fails over to another device.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27586-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27586-141">CommonParameters</span></span>
<span data-ttu-id="27586-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27586-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27586-143">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27586-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27586-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27586-144">INPUTS</span></span>

### <span data-ttu-id="27586-145">Список\<DataContainerGroup\></span><span class="sxs-lookup"><span data-stu-id="27586-145">List\<DataContainerGroup\></span></span>
<span data-ttu-id="27586-146">Вы можете передать в этот командлет список групп контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="27586-146">You can pipe a list of volume container groups to this cmdlet.</span></span>

## <span data-ttu-id="27586-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27586-147">OUTPUTS</span></span>

### <span data-ttu-id="27586-148">Подстрок</span><span class="sxs-lookup"><span data-stu-id="27586-148">String</span></span>

## <span data-ttu-id="27586-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="27586-149">NOTES</span></span>

## <span data-ttu-id="27586-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27586-150">RELATED LINKS</span></span>

[<span data-ttu-id="27586-151">Get-AzureStorSimpleFailoverVolumeContainers</span><span class="sxs-lookup"><span data-stu-id="27586-151">Get-AzureStorSimpleFailoverVolumeContainers</span></span>](./Get-AzureStorSimpleFailoverVolumeContainers.md)


