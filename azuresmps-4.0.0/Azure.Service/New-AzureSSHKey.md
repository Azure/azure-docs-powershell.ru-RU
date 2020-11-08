---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075982"
---
# <span data-ttu-id="3486c-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="3486c-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="3486c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3486c-102">SYNOPSIS</span></span>
<span data-ttu-id="3486c-103">Создание объекта ключа SSH для вставки существующего сертификата в новые виртуальные машины Azure на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="3486c-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="3486c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3486c-104">SYNTAX</span></span>

### <span data-ttu-id="3486c-105">пары</span><span class="sxs-lookup"><span data-stu-id="3486c-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3486c-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="3486c-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3486c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3486c-107">DESCRIPTION</span></span>
<span data-ttu-id="3486c-108">Командлет **New-AzureSSHKey** создает объект ключа SSH для сертификата, который уже добавлен в Azure.</span><span class="sxs-lookup"><span data-stu-id="3486c-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="3486c-109">Этот объект ключа SSH может затем использоваться с помощью **New-AzureProvisioningConfig** при создании объекта конфигурации для новой виртуальной машины с помощью **New-AzureVM** или при создании новой виртуальной машины с помощью **New-AzureQuickVM**.</span><span class="sxs-lookup"><span data-stu-id="3486c-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="3486c-110">При включении в сценарий создания виртуальной машины на новую виртуальную машину добавляется указанный открытый ключ SSH или пара ключей.</span><span class="sxs-lookup"><span data-stu-id="3486c-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="3486c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3486c-111">EXAMPLES</span></span>

### <span data-ttu-id="3486c-112">Пример 1: создание объекта параметров сертификата</span><span class="sxs-lookup"><span data-stu-id="3486c-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="3486c-113">Эта команда создает объект параметра сертификата для существующего сертификата и сохраняет объект в переменной для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="3486c-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="3486c-114">Пример 2: Добавление сертификата в службу</span><span class="sxs-lookup"><span data-stu-id="3486c-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="3486c-115">Эта команда добавляет сертификат в службу Azure, а затем создает новую виртуальную машину Linux, использующую сертификат.</span><span class="sxs-lookup"><span data-stu-id="3486c-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="3486c-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3486c-116">PARAMETERS</span></span>

### <span data-ttu-id="3486c-117">-Отпечаток пальца</span><span class="sxs-lookup"><span data-stu-id="3486c-117">-Fingerprint</span></span>
<span data-ttu-id="3486c-118">Указывает отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="3486c-118">Specifies the fingerprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3486c-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3486c-119">-InformationAction</span></span>
<span data-ttu-id="3486c-120">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="3486c-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3486c-121">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="3486c-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3486c-122">Продолжал</span><span class="sxs-lookup"><span data-stu-id="3486c-122">Continue</span></span>
- <span data-ttu-id="3486c-123">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="3486c-123">Ignore</span></span>
- <span data-ttu-id="3486c-124">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="3486c-124">Inquire</span></span>
- <span data-ttu-id="3486c-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3486c-125">SilentlyContinue</span></span>
- <span data-ttu-id="3486c-126">Остановить</span><span class="sxs-lookup"><span data-stu-id="3486c-126">Stop</span></span>
- <span data-ttu-id="3486c-127">Рвать</span><span class="sxs-lookup"><span data-stu-id="3486c-127">Suspend</span></span>

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

### <span data-ttu-id="3486c-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3486c-128">-InformationVariable</span></span>
<span data-ttu-id="3486c-129">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="3486c-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3486c-130">-Пару ключей</span><span class="sxs-lookup"><span data-stu-id="3486c-130">-KeyPair</span></span>
<span data-ttu-id="3486c-131">Указывает на то, что этот командлет создает объект для вставки пары ключей SSH в новую конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3486c-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3486c-132">-Path</span><span class="sxs-lookup"><span data-stu-id="3486c-132">-Path</span></span>
<span data-ttu-id="3486c-133">Указывает путь для хранения открытого ключа SSH или пары ключей.</span><span class="sxs-lookup"><span data-stu-id="3486c-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3486c-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="3486c-134">-PublicKey</span></span>
<span data-ttu-id="3486c-135">Указывает на то, что этот командлет создает объект для вставки открытого ключа SSH в новую конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3486c-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3486c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3486c-136">CommonParameters</span></span>
<span data-ttu-id="3486c-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3486c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3486c-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3486c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3486c-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3486c-139">INPUTS</span></span>

## <span data-ttu-id="3486c-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3486c-140">OUTPUTS</span></span>

## <span data-ttu-id="3486c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="3486c-141">NOTES</span></span>

## <span data-ttu-id="3486c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3486c-142">RELATED LINKS</span></span>

[<span data-ttu-id="3486c-143">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="3486c-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="3486c-144">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="3486c-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="3486c-145">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="3486c-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="3486c-146">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="3486c-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


