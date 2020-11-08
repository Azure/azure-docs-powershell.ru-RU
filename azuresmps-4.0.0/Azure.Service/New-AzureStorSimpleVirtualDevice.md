---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F16BCE0C-1F2C-4FB7-972D-28BE3CCD96D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: dc41efa1901debf2efabf66f8d27f00da7eafe5f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075511"
---
# <span data-ttu-id="08561-101">New-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="08561-101">New-AzureStorSimpleVirtualDevice</span></span>

## <span data-ttu-id="08561-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="08561-102">SYNOPSIS</span></span>
<span data-ttu-id="08561-103">Создание виртуального устройства StorSimple.</span><span class="sxs-lookup"><span data-stu-id="08561-103">Creates a virtual StorSimple device.</span></span>

## <span data-ttu-id="08561-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="08561-104">SYNTAX</span></span>

### <span data-ttu-id="08561-105">CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08561-105">CreateNewStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 [-StorageAccountName <String>] [-CreateNewStorageAccount] [-PersistAzureVMOnFailrue]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="08561-106">UseExistingStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08561-106">UseExistingStorageAccount</span></span>
```
New-AzureStorSimpleVirtualDevice -VirtualDeviceName <String> -VirtualNetworkName <String> -SubNetName <String>
 -StorageAccountName <String> [-PersistAzureVMOnFailrue] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="08561-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="08561-107">DESCRIPTION</span></span>
<span data-ttu-id="08561-108">Командлет **New-AzureStorSimpleVirtualDevice** создает виртуальное устройство StorSimple.</span><span class="sxs-lookup"><span data-stu-id="08561-108">The **New-AzureStorSimpleVirtualDevice** cmdlet creates a virtual StorSimple device.</span></span>
<span data-ttu-id="08561-109">Укажите имя устройства.</span><span class="sxs-lookup"><span data-stu-id="08561-109">Specify a device name for the device.</span></span>
<span data-ttu-id="08561-110">Укажите сведения о виртуальной сети и подсети для виртуальной сети в той же подписке.</span><span class="sxs-lookup"><span data-stu-id="08561-110">Specify virtual network and subnet details for the virtual network in the same subscription.</span></span>
<span data-ttu-id="08561-111">Geo должен соответствовать географическому элементу, в котором создан ресурс StorSimple.</span><span class="sxs-lookup"><span data-stu-id="08561-111">The geo should match the geo in which the StorSimple resource is created.</span></span>
<span data-ttu-id="08561-112">Чтобы использовать существующую учетную запись хранения для этого виртуального устройства, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="08561-112">To use an existing storage account for this virtual device, specify the name.</span></span>
<span data-ttu-id="08561-113">Чтобы создать новую учетную запись хранения для этого виртуального устройства, укажите параметры *StorageAccountName* и *CreateNewStorageAccount* .</span><span class="sxs-lookup"><span data-stu-id="08561-113">To create a new storage account for this virtual device, specify both the *StorageAccountName* and the *CreateNewStorageAccount* parameters.</span></span>

## <span data-ttu-id="08561-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="08561-114">EXAMPLES</span></span>

### <span data-ttu-id="08561-115">Пример 1: создание виртуального устройства с новой учетной записью и существующей сетью</span><span class="sxs-lookup"><span data-stu-id="08561-115">Example 1: Create a virtual device with a new account and an existing network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "Contosodevice02" -VirtualNetworkName "Saas2vpn" -SubNetName "TenantSubnet" -StorageAccountName "AzureTenant04" -CreateNewStorageAccount
64e4c564-b0ac-44b0-afb4-adf28ac24ad0
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 64e4c564-b0ac-44b0-afb4-adf28ac24ad0 for tracking the job's status
```

<span data-ttu-id="08561-116">Эта команда создает виртуальное устройство, использующее новую учетную запись хранения и существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="08561-116">This command creates a virtual device that uses a new storage account and an existing virtual network.</span></span>

### <span data-ttu-id="08561-117">Пример 2: создание виртуального устройства с существующей учетной записью и виртуальной сетью</span><span class="sxs-lookup"><span data-stu-id="08561-117">Example 2: Create a virtual device with an existing account and virtual network</span></span>
```
PS C:\>New-AzureStorSimpleVirtualDevice -VirtualDeviceName "ContosoDevice07" -VirtualNetworkName "Saas2vpn" -SubNetName TenantSubnet -StorageAccountName azurecisbvtdnd
2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf
VERBOSE: The create job is triggered successfully. Please use the command Get-AzureStorSimpleJob -InstanceId 2a18a3b7-1ec6-481d-b95d-66ba8f67ceaf for tracking the job's status
```

<span data-ttu-id="08561-118">Эта команда создает виртуальное устройство, которое использует существующую учетную запись хранения и существующую виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="08561-118">This command creates a virtual device that uses an existing storage account and an existing virtual network.</span></span>

## <span data-ttu-id="08561-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="08561-119">PARAMETERS</span></span>

### <span data-ttu-id="08561-120">-CreateNewStorageAccount</span><span class="sxs-lookup"><span data-stu-id="08561-120">-CreateNewStorageAccount</span></span>
<span data-ttu-id="08561-121">Указывает на то, что этот командлет создает новую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="08561-121">Indicates that this cmdlet creates a new storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08561-122">-PersistAzureVMOnFailrue</span><span class="sxs-lookup"><span data-stu-id="08561-122">-PersistAzureVMOnFailrue</span></span>
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

### <span data-ttu-id="08561-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="08561-123">-Profile</span></span>
<span data-ttu-id="08561-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="08561-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="08561-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="08561-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="08561-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="08561-126">-StorageAccountName</span></span>
<span data-ttu-id="08561-127">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="08561-127">Specifies the name of a storage account.</span></span>

```yaml
Type: String
Parameter Sets: CreateNewStorageAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UseExistingStorageAccount
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08561-128">-SubNetName</span><span class="sxs-lookup"><span data-stu-id="08561-128">-SubNetName</span></span>
<span data-ttu-id="08561-129">Указывает имя виртуальной подсети.</span><span class="sxs-lookup"><span data-stu-id="08561-129">Specifies the name of a virtual subnet.</span></span>

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

### <span data-ttu-id="08561-130">-VirtualDeviceName</span><span class="sxs-lookup"><span data-stu-id="08561-130">-VirtualDeviceName</span></span>
<span data-ttu-id="08561-131">Указывает имя виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="08561-131">Specifies a name for the virtual device.</span></span>

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

### <span data-ttu-id="08561-132">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="08561-132">-VirtualNetworkName</span></span>
<span data-ttu-id="08561-133">Указывает имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="08561-133">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: VNetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08561-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08561-134">CommonParameters</span></span>
<span data-ttu-id="08561-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="08561-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08561-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08561-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08561-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="08561-137">INPUTS</span></span>

## <span data-ttu-id="08561-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="08561-138">OUTPUTS</span></span>

### <span data-ttu-id="08561-139">Подстрок</span><span class="sxs-lookup"><span data-stu-id="08561-139">String</span></span>
<span data-ttu-id="08561-140">Этот командлет возвращает идентификатор задания, которое создает виртуальное устройство.</span><span class="sxs-lookup"><span data-stu-id="08561-140">This cmdlet returns the ID of the job that creates the virtual device.</span></span>
<span data-ttu-id="08561-141">Этот идентификатор можно использовать для отслеживания хода выполнения с помощью командлета Get-AzureStorSimpleJob.</span><span class="sxs-lookup"><span data-stu-id="08561-141">You can use this ID to track the progress using the Get-AzureStorSimpleJob cmdlet.</span></span>

## <span data-ttu-id="08561-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="08561-142">NOTES</span></span>

## <span data-ttu-id="08561-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="08561-143">RELATED LINKS</span></span>

[<span data-ttu-id="08561-144">Get-AzureStorSimpleJob</span><span class="sxs-lookup"><span data-stu-id="08561-144">Get-AzureStorSimpleJob</span></span>](./Get-AzureStorSimpleJob.md)

[<span data-ttu-id="08561-145">Set-AzureStorSimpleVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="08561-145">Set-AzureStorSimpleVirtualDevice</span></span>](./Set-AzureStorSimpleVirtualDevice.md)


