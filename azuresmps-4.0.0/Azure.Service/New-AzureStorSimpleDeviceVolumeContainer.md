---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5605F11E-EEA0-4C32-8445-2E001D56BC47
online version: ''
schema: 2.0.0
ms.openlocfilehash: e364692858cf190b48b61f4d38fbf483d229ffb7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075520"
---
# <span data-ttu-id="19bf5-101">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="19bf5-101">New-AzureStorSimpleDeviceVolumeContainer</span></span>

## <span data-ttu-id="19bf5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="19bf5-103">Создание контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="19bf5-103">Creates a volume container.</span></span>

## <span data-ttu-id="19bf5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19bf5-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> -VolumeContainerName <String>
 -PrimaryStorageAccountCredential <StorageAccountCredentialResponse> -BandWidthRateInMbps <Int32>
 [-EncryptionEnabled <Boolean>] [-EncryptionKey <String>] [-WaitForComplete] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="19bf5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="19bf5-106">Командлет **New-AzureStorSimpleDeviceVolumeContainer** создает контейнер томов.</span><span class="sxs-lookup"><span data-stu-id="19bf5-106">The **New-AzureStorSimpleDeviceVolumeContainer** cmdlet creates a volume container.</span></span>
<span data-ttu-id="19bf5-107">Вы должны связать учетные данные учетной записи хранения с новым контейнером тома.</span><span class="sxs-lookup"><span data-stu-id="19bf5-107">You must associate a storage account credential with the new volume container.</span></span>
<span data-ttu-id="19bf5-108">Чтобы получить учетные данные учетной записи хранения, используйте командлет **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="19bf5-108">To obtain a storage account credential, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

## <span data-ttu-id="19bf5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19bf5-109">EXAMPLES</span></span>

### <span data-ttu-id="19bf5-110">Пример 1: создание контейнера</span><span class="sxs-lookup"><span data-stu-id="19bf5-110">Example 1: Create a container</span></span>
```
PS C:\>Get-AzureStorSimpleStorageAccountCredential -StorageAccountName "ContosoAccount" | New-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08" -BandWidthRateInMbps 256
VERBOSE: ClientRequestId: 96a4ccd4-f2a9-4820-8bc8-e6b7b56dce0d_PS
VERBOSE: ClientRequestId: 90be20db-098a-4f2b-a6da-9da6f533a846_PS
VERBOSE: ClientRequestId: 410fd33a-8fa3-4ae5-a1bf-1b6da9b34ffc_PS
VERBOSE: Storage Access Credential with name ContosoAccount found! 
VERBOSE: ClientRequestId: 0a6d1008-ba1f-43b2-a424-9c86be2fb83b_PS
VERBOSE: ClientRequestId: 08f0d657-a130-4a25-8090-270c58b479dc_PS
VERBOSE: ClientRequestId: 0f3e894a-b031-467c-a258-41b74c89cf18_PS
5b192120-9df0-40ed-b75e-b4e728bd37ef
VERBOSE: The create task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
5b192120-9df0-40ed-b75e-b4e728bd37ef for tracking the task's status
```

<span data-ttu-id="19bf5-111">Эта команда получает учетные данные учетной записи хранения для учетной записи с именем ContosoAccount с помощью командлета **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="19bf5-111">This command gets the storage account credential for the account named ContosoAccount by using the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>
<span data-ttu-id="19bf5-112">Команда передает учетные данные текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="19bf5-112">The command passes the credential to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="19bf5-113">Этот командлет использует учетные данные из этого командлета для создания контейнера с именем Container08 на устройстве с именем Contoso63-AppVm.</span><span class="sxs-lookup"><span data-stu-id="19bf5-113">This cmdlet uses the credential from that cmdlet to create the container named Container08 on the device named Contoso63-AppVm.</span></span>
<span data-ttu-id="19bf5-114">Эта команда запускает задание, а затем возвращает объект **TaskResponse** .</span><span class="sxs-lookup"><span data-stu-id="19bf5-114">This command starts the job, and then returns a **TaskResponse** object.</span></span>
<span data-ttu-id="19bf5-115">Чтобы просмотреть состояние задания, используйте командлет **Get-AzureStorSimpleTask** .</span><span class="sxs-lookup"><span data-stu-id="19bf5-115">To see the status of the job, use the **Get-AzureStorSimpleTask** cmdlet.</span></span>

## <span data-ttu-id="19bf5-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19bf5-116">PARAMETERS</span></span>

### <span data-ttu-id="19bf5-117">-BandWidthRateInMbps</span><span class="sxs-lookup"><span data-stu-id="19bf5-117">-BandWidthRateInMbps</span></span>
<span data-ttu-id="19bf5-118">Указывает частоту пропускной способности в мегабит в секунду (Мбит/с).</span><span class="sxs-lookup"><span data-stu-id="19bf5-118">Specifies the bandwidth rate in megabits per second (Mbps).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CloudBandwidthInMbps

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bf5-119">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="19bf5-119">-DeviceName</span></span>
<span data-ttu-id="19bf5-120">Указывает имя устройства StorSimple, на котором нужно создать контейнер томов.</span><span class="sxs-lookup"><span data-stu-id="19bf5-120">Specifies the name of the StorSimple device on which to create the volume container.</span></span>

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

### <span data-ttu-id="19bf5-121">-EncryptionEnabled</span><span class="sxs-lookup"><span data-stu-id="19bf5-121">-EncryptionEnabled</span></span>
<span data-ttu-id="19bf5-122">Указывает, следует ли включить шифрование.</span><span class="sxs-lookup"><span data-stu-id="19bf5-122">Indicates whether to enable encryption.</span></span>

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

### <span data-ttu-id="19bf5-123">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="19bf5-123">-EncryptionKey</span></span>
<span data-ttu-id="19bf5-124">Задает ключ шифрования.</span><span class="sxs-lookup"><span data-stu-id="19bf5-124">Specifies the encryption key.</span></span>

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

### <span data-ttu-id="19bf5-125">-PrimaryStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="19bf5-125">-PrimaryStorageAccountCredential</span></span>
<span data-ttu-id="19bf5-126">Задает учетные данные как объект **StorageAccountCredential** для связи с новым контейнером тома.</span><span class="sxs-lookup"><span data-stu-id="19bf5-126">Specifies the credential, as a **StorageAccountCredential** object, to associate with the new volume container.</span></span>
<span data-ttu-id="19bf5-127">Чтобы получить объект **StorageAccountCredential** , используйте командлет **Get-AzureStorSimpleStorageAccountCredential** .</span><span class="sxs-lookup"><span data-stu-id="19bf5-127">To obtain a **StorageAccountCredential** object, use the **Get-AzureStorSimpleStorageAccountCredential** cmdlet.</span></span>

```yaml
Type: StorageAccountCredentialResponse
Parameter Sets: (All)
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19bf5-128">-Profile</span><span class="sxs-lookup"><span data-stu-id="19bf5-128">-Profile</span></span>
<span data-ttu-id="19bf5-129">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="19bf5-129">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="19bf5-130">-VolumeContainerName</span><span class="sxs-lookup"><span data-stu-id="19bf5-130">-VolumeContainerName</span></span>
<span data-ttu-id="19bf5-131">Указывает имя создаваемого контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="19bf5-131">Specifies the name of the volume container to create.</span></span>

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

### <span data-ttu-id="19bf5-132">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="19bf5-132">-WaitForComplete</span></span>
<span data-ttu-id="19bf5-133">Указывает на то, что этот командлет ожидает завершения операции до того, как она возвратит управление на консоль Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="19bf5-133">Indicates that this cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="19bf5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bf5-134">CommonParameters</span></span>
<span data-ttu-id="19bf5-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19bf5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bf5-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19bf5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bf5-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19bf5-137">INPUTS</span></span>

### <span data-ttu-id="19bf5-138">StorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="19bf5-138">StorageAccountCredential</span></span>
<span data-ttu-id="19bf5-139">Этот командлет принимает объект **PrimaryStorageAccountCredential** для связи с контейнером тома.</span><span class="sxs-lookup"><span data-stu-id="19bf5-139">This cmdlet accepts a **PrimaryStorageAccountCredential** object to associate with the volume container.</span></span>

## <span data-ttu-id="19bf5-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19bf5-140">OUTPUTS</span></span>

### <span data-ttu-id="19bf5-141">TaskStatusInfo</span><span class="sxs-lookup"><span data-stu-id="19bf5-141">TaskStatusInfo</span></span>
<span data-ttu-id="19bf5-142">Этот командлет возвращает объект **TaskStatusInfo** , если указан параметр *WaitForComplete* .</span><span class="sxs-lookup"><span data-stu-id="19bf5-142">This cmdlet returns a **TaskStatusInfo** object, if you specify the *WaitForComplete* parameter.</span></span>

## <span data-ttu-id="19bf5-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="19bf5-143">NOTES</span></span>

## <span data-ttu-id="19bf5-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19bf5-144">RELATED LINKS</span></span>

[<span data-ttu-id="19bf5-145">Get-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="19bf5-145">Get-AzureStorSimpleDeviceVolumeContainer</span></span>](./Get-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="19bf5-146">Remove-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="19bf5-146">Remove-AzureStorSimpleDeviceVolumeContainer</span></span>](./Remove-AzureStorSimpleDeviceVolumeContainer.md)

[<span data-ttu-id="19bf5-147">Get-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="19bf5-147">Get-AzureStorSimpleStorageAccountCredential</span></span>](./Get-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="19bf5-148">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="19bf5-148">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)


