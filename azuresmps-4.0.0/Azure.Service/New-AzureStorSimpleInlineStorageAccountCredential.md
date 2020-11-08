---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BC68C60C-86E3-4857-95AE-1A915A841F7D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 803bc4006e5be8582183248c22115fcd51862d13
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075517"
---
# <span data-ttu-id="cbe61-101">New-AzureStorSimpleInlineStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cbe61-101">New-AzureStorSimpleInlineStorageAccountCredential</span></span>

## <span data-ttu-id="cbe61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cbe61-102">SYNOPSIS</span></span>
<span data-ttu-id="cbe61-103">Создание учетных данных встроенной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cbe61-103">Creates an inline storage account credential.</span></span>

## <span data-ttu-id="cbe61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cbe61-104">SYNTAX</span></span>

```
New-AzureStorSimpleInlineStorageAccountCredential -StorageAccountName <String> -StorageAccountKey <String>
 [-Endpoint <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="cbe61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbe61-105">DESCRIPTION</span></span>
<span data-ttu-id="cbe61-106">Командлет **New-AzureStorSimpleInlineStorageAccountCredential** создает встроенный объект учетных данных учетной записи службы хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cbe61-106">The **New-AzureStorSimpleInlineStorageAccountCredential** cmdlet creates an inline Azure storage account credential object.</span></span>
<span data-ttu-id="cbe61-107">Этот командлет создает фиктивный объект учетных данных.</span><span class="sxs-lookup"><span data-stu-id="cbe61-107">This cmdlet creates a dummy credential object.</span></span>
<span data-ttu-id="cbe61-108">Вы можете использовать командлет **New-AzureStorSimpleDeviceVolumeContainer** и текущий командлет в той же команде с помощью конвейера Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cbe61-108">You can use the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet and the current cmdlet in the same command by using the Windows PowerShell pipeline.</span></span>
<span data-ttu-id="cbe61-109">Фактический объект учетной записи хранения создается в процессе создания контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="cbe61-109">The actual storage account credential object is created as part of creation of the volume container.</span></span>

## <span data-ttu-id="cbe61-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cbe61-110">EXAMPLES</span></span>

### <span data-ttu-id="cbe61-111">Пример 1: создание встроенных учетных данных учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cbe61-111">Example 1: Create a storage account credential inline</span></span>
```
PS C:\>New-AzureStorSimpleInlineStorageAccountCredential -Name "contoso76" -Key x6o/tpZh8Coo8Tteo0NHLksTOKr/P9Vufo0LZNGdPGVTSUu00/p6ta1w9gRbVBNjzN8aa504kH2zkEsfUme+kw== | New-AzureStorSimpleDeviceVolumeContainer -Name "VolumeContainer_06" -DeviceName Contoso_App3 -BandWidthRate 256 -EncryptionEnabled $True -EncryptionKey "Key22" -WaitForComplete
VERBOSE: ClientRequestId: 535d24d5-1ed8-4759-92b2-dd492f94e23e_PS
VERBOSE: ClientRequestId: f32fc069-96c9-4fd9-a71a-0e62d81f25d8_PS
VERBOSE: ClientRequestId: 4376a931-89f5-448f-92bd-b2f7234244c9_PS
VERBOSE: ClientRequestId: 980109d4-7d76-40d0-ae3c-db539e2cb486_PS
VERBOSE: Encryption in progress... 
VERBOSE: Creating StorageAccountCredential inline
VERBOSE: Found storage account with name : contoso76
VERBOSE: Storage credential verification succeeded. 
VERBOSE: Encryption in progress... 
VERBOSE: ClientRequestId: d4f8a5de-bf81-4773-b6e6-edb034284cf4_PS


JobId        : 2dec64d3-b30d-4d35-adb3-12689b235b79
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your create operation has completed successfully. 
VERBOSE: ClientRequestId: abd4082a-2eda-42ad-8cb3-5864dd2f7d1f_PS
BandwidthRate                   : 256
EncryptionKey                   : SK23I39L7GvoLce7u63TMT/A/V/TW8JXe+PoXKEKzwsr3t/h7tdqV1EpfaK0DGO/qo5b2PLCagFHAxnZEiejg
                                  jtF9TcyK+aLyzEnkqtM+eNRJmgANzJ9C/5L6Ubp+eSWiy+U/pyZygxPrb37e0yFg+qbHV9R9Qi+afBpHD9Gsi
                                  rhURuOc/idWG29eaEifuRzn/zEjvwJ2pEyYLcsuL+ftfRYZom69XO+cRDv5yT3xdNI/dAod/5YUaf1IhJl8wR
                                  cWjqyr00NxlCI03hTgH2sFyTFZWc07S2KI5K5n3rmCL6vGT76SRgNFeUxGz3v06/VoBhdmv9vDfrEz5UkW04d
                                  Qw==
InstanceId                      : a72bf4bb-0f0a-4ec2-a8b1-c4548825f522
IsDefault                       : False
IsEncryptionEnabled             : True
Name                            : VolumneContainer_06
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 0
```

<span data-ttu-id="cbe61-112">Эта команда создает встроенные учетные данные учетной записи хранения, а затем передает ее командлету **New-AzureStorSimpleDeviceVolumeContainer** с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="cbe61-112">This command creates a storage account credential inline, and then passes it to the **New-AzureStorSimpleDeviceVolumeContainer** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="cbe61-113">Этот контейнер использует фиктивные учетные данные для создания контейнера тома.</span><span class="sxs-lookup"><span data-stu-id="cbe61-113">That container uses the dummy credential to create a volume container.</span></span>

## <span data-ttu-id="cbe61-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cbe61-114">PARAMETERS</span></span>

### <span data-ttu-id="cbe61-115">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="cbe61-115">-Endpoint</span></span>
<span data-ttu-id="cbe61-116">Указывает конечную точку хранилища Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cbe61-116">Specifies the Azure storage endpoint for the storage account.</span></span>

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

### <span data-ttu-id="cbe61-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="cbe61-117">-Profile</span></span>
<span data-ttu-id="cbe61-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cbe61-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cbe61-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cbe61-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cbe61-120">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cbe61-120">-StorageAccountKey</span></span>
<span data-ttu-id="cbe61-121">Задает ключ учетной записи хранения в формате обычного текста.</span><span class="sxs-lookup"><span data-stu-id="cbe61-121">Specifies the account key of the storage account in plain text.</span></span>
<span data-ttu-id="cbe61-122">Ключ передается в зашифрованном формате.</span><span class="sxs-lookup"><span data-stu-id="cbe61-122">The key is transferred in encrypted format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Key

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbe61-123">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cbe61-123">-StorageAccountName</span></span>
<span data-ttu-id="cbe61-124">Указывает имя существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cbe61-124">Specifies the name of an existing storage account.</span></span>

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

### <span data-ttu-id="cbe61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbe61-125">CommonParameters</span></span>
<span data-ttu-id="cbe61-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cbe61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbe61-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbe61-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbe61-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cbe61-128">INPUTS</span></span>

### <span data-ttu-id="cbe61-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="cbe61-129">None</span></span>

## <span data-ttu-id="cbe61-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cbe61-130">OUTPUTS</span></span>

### <span data-ttu-id="cbe61-131">StorageAccountCredentialResponse</span><span class="sxs-lookup"><span data-stu-id="cbe61-131">StorageAccountCredentialResponse</span></span>
<span data-ttu-id="cbe61-132">Этот командлет возвращает объект **CloudType** , который включает следующие поля:</span><span class="sxs-lookup"><span data-stu-id="cbe61-132">This cmdlet returns a **CloudType** object, which contains the following fields:</span></span> 

- <span data-ttu-id="cbe61-133">**HostName (имя узла** ).</span><span class="sxs-lookup"><span data-stu-id="cbe61-133">**Hostname**.</span></span>
<span data-ttu-id="cbe61-134">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-134">**String**.</span></span> 
- <span data-ttu-id="cbe61-135">**InstanceId**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-135">**InstanceId**.</span></span>
<span data-ttu-id="cbe61-136">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-136">**String**.</span></span> 
- <span data-ttu-id="cbe61-137">**По умолчанию**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-137">**IsDefault**.</span></span>
<span data-ttu-id="cbe61-138">**Логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-138">**Boolean**.</span></span> 
- <span data-ttu-id="cbe61-139">**Расположение**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-139">**Location**.</span></span>
<span data-ttu-id="cbe61-140">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-140">**String**.</span></span> 
- <span data-ttu-id="cbe61-141">**Вход**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-141">**Login**.</span></span>
<span data-ttu-id="cbe61-142">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-142">**String**.</span></span> 
- <span data-ttu-id="cbe61-143">**Name (имя** ).</span><span class="sxs-lookup"><span data-stu-id="cbe61-143">**Name**.</span></span>
<span data-ttu-id="cbe61-144">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-144">**String**.</span></span> 
- <span data-ttu-id="cbe61-145">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-145">**OperationInProgress**.</span></span>
<span data-ttu-id="cbe61-146">**OperationInProgress**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-146">**OperationInProgress**.</span></span> 
- <span data-ttu-id="cbe61-147">**Password (пароль** ).</span><span class="sxs-lookup"><span data-stu-id="cbe61-147">**Password**.</span></span>
<span data-ttu-id="cbe61-148">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-148">**String**.</span></span> 
- <span data-ttu-id="cbe61-149">**PasswordEncryptionCertThumbprint**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-149">**PasswordEncryptionCertThumbprint**.</span></span>
<span data-ttu-id="cbe61-150">**String**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-150">**String**.</span></span> 
- <span data-ttu-id="cbe61-151">**UseSSL**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-151">**UseSSL**.</span></span>
<span data-ttu-id="cbe61-152">**Логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-152">**Boolean**.</span></span> 
- <span data-ttu-id="cbe61-153">**VolumeCount**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-153">**VolumeCount**.</span></span>
<span data-ttu-id="cbe61-154">**Целое число**.</span><span class="sxs-lookup"><span data-stu-id="cbe61-154">**Integer**.</span></span>

## <span data-ttu-id="cbe61-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="cbe61-155">NOTES</span></span>

## <span data-ttu-id="cbe61-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cbe61-156">RELATED LINKS</span></span>

[<span data-ttu-id="cbe61-157">New-AzureStorSimpleStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="cbe61-157">New-AzureStorSimpleStorageAccountCredential</span></span>](./New-AzureStorSimpleStorageAccountCredential.md)

[<span data-ttu-id="cbe61-158">New-AzureStorSimpleDeviceVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="cbe61-158">New-AzureStorSimpleDeviceVolumeContainer</span></span>](./New-AzureStorSimpleDeviceVolumeContainer.md)


