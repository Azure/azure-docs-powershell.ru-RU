---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075563"
---
# <span data-ttu-id="ef089-101">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ef089-101">Get-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="ef089-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef089-102">SYNOPSIS</span></span>
<span data-ttu-id="ef089-103">Получает контейнеры томов на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ef089-103">Gets volume containers on a device.</span></span>

## <span data-ttu-id="ef089-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef089-104">SYNTAX</span></span>

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ef089-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef089-105">DESCRIPTION</span></span>
<span data-ttu-id="ef089-106">Командлет **Get-AzureStorSimpleDeviceVolumeContainer** получает список контейнеров томов на устройстве или контейнер томов с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="ef089-106">The **Get-AzureStorSimpleDeviceVolumeContainer** cmdlet gets a list of volume containers on a device, or volume container that has the specified name.</span></span>
<span data-ttu-id="ef089-107">Возвращенный объект имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="ef089-107">The returned object contains the following properties:</span></span> 

- <span data-ttu-id="ef089-108">**BandwidthRate**</span><span class="sxs-lookup"><span data-stu-id="ef089-108">**BandwidthRate**</span></span>
- <span data-ttu-id="ef089-109">**EncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="ef089-109">**EncryptionKey**</span></span>
- <span data-ttu-id="ef089-110">**ИД**</span><span class="sxs-lookup"><span data-stu-id="ef089-110">**InstanceId**</span></span>
- <span data-ttu-id="ef089-111">**Default (по умолчанию)**</span><span class="sxs-lookup"><span data-stu-id="ef089-111">**IsDefault**</span></span>
- <span data-ttu-id="ef089-112">**IsEncryptionEnabled**</span><span class="sxs-lookup"><span data-stu-id="ef089-112">**IsEncryptionEnabled**</span></span>
- <span data-ttu-id="ef089-113">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="ef089-113">**Name**</span></span>
- <span data-ttu-id="ef089-114">**OperationInProgress**</span><span class="sxs-lookup"><span data-stu-id="ef089-114">**OperationInProgress**</span></span>
- <span data-ttu-id="ef089-115">**Принадлежал**</span><span class="sxs-lookup"><span data-stu-id="ef089-115">**Owned**</span></span>
- <span data-ttu-id="ef089-116">**PrimaryStorageAccountCredential**</span><span class="sxs-lookup"><span data-stu-id="ef089-116">**PrimaryStorageAccountCredential**</span></span>
- <span data-ttu-id="ef089-117">**SecretsEncryptionThumbprint**</span><span class="sxs-lookup"><span data-stu-id="ef089-117">**SecretsEncryptionThumbprint**</span></span>
- <span data-ttu-id="ef089-118">**VolumeCount**</span><span class="sxs-lookup"><span data-stu-id="ef089-118">**VolumeCount**</span></span>

## <span data-ttu-id="ef089-119">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef089-119">EXAMPLES</span></span>

### <span data-ttu-id="ef089-120">Пример 1: получение всех контейнеров на устройстве</span><span class="sxs-lookup"><span data-stu-id="ef089-120">Example 1: Get all the containers on a device</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

<span data-ttu-id="ef089-121">Эта команда получает список контейнеров томов на устройстве с именем 8600-Bravo 001.</span><span class="sxs-lookup"><span data-stu-id="ef089-121">This command gets a list of the volume containers on the device named 8600-Bravo 001.</span></span>

### <span data-ttu-id="ef089-122">Пример 2: получение контейнера с использованием его имени</span><span class="sxs-lookup"><span data-stu-id="ef089-122">Example 2: Get a container by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

<span data-ttu-id="ef089-123">Эта команда получает контейнер томов с именем Container08 на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="ef089-123">This command gets the volume container named Container08 on the device named Contoso63-AppVm.</span></span>

## <span data-ttu-id="ef089-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef089-124">PARAMETERS</span></span>

### <span data-ttu-id="ef089-125">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="ef089-125">-DeviceName</span></span>
<span data-ttu-id="ef089-126">Указывает имя устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="ef089-126">Specifies the name of a StorSimple device.</span></span>
<span data-ttu-id="ef089-127">Этот командлет получает контейнеры томов на устройстве, указанном этим параметром.</span><span class="sxs-lookup"><span data-stu-id="ef089-127">This cmdlet gets volume containers from the device that this parameter specifies.</span></span>

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

### <span data-ttu-id="ef089-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef089-128">-Profile</span></span>
<span data-ttu-id="ef089-129">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="ef089-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="ef089-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="ef089-130">-VolumeContainerName</span></span>
<span data-ttu-id="ef089-131">Указывает имя контейнера тома, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ef089-131">Specifies the name of the volume container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef089-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef089-132">CommonParameters</span></span>
<span data-ttu-id="ef089-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef089-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef089-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef089-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef089-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef089-135">INPUTS</span></span>

### <span data-ttu-id="ef089-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="ef089-136">None</span></span>

## <span data-ttu-id="ef089-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef089-137">OUTPUTS</span></span>

### <span data-ttu-id="ef089-138">Контейнер содержания, IList\<DataContainer\></span><span class="sxs-lookup"><span data-stu-id="ef089-138">DataContainer, IList\<DataContainer\></span></span>
<span data-ttu-id="ef089-139">Этот командлет возвращает объект- **контейнер** , если указан параметр *VolumeContainerName* .</span><span class="sxs-lookup"><span data-stu-id="ef089-139">This cmdlet returns a **DataContainer** object, if you specify the *VolumeContainerName* parameter.</span></span>
<span data-ttu-id="ef089-140">Если этот параметр не указан, этот командлет возвращает объект **IList \<DataContainer\>** .</span><span class="sxs-lookup"><span data-stu-id="ef089-140">If you do not specify that parameter, this cmdlet returns an **IList\<DataContainer\>** object.</span></span>

## <span data-ttu-id="ef089-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef089-141">NOTES</span></span>

## <span data-ttu-id="ef089-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef089-142">RELATED LINKS</span></span>

[<span data-ttu-id="ef089-143">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ef089-143">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="ef089-144">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="ef089-144">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


