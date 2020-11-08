---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075909"
---
# <span data-ttu-id="072f0-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="072f0-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="072f0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="072f0-102">SYNOPSIS</span></span>
<span data-ttu-id="072f0-103">Настройка и создание виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="072f0-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="072f0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="072f0-104">SYNTAX</span></span>

### <span data-ttu-id="072f0-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="072f0-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="072f0-106">Linux</span><span class="sxs-lookup"><span data-stu-id="072f0-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="072f0-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="072f0-107">DESCRIPTION</span></span>
<span data-ttu-id="072f0-108">Командлет **New-AzureQuickVM** настраивает и создает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="072f0-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="072f0-109">Этот командлет может развернуть виртуальную машину в существующей службе Azure.</span><span class="sxs-lookup"><span data-stu-id="072f0-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="072f0-110">Этот командлет также может создать службу Azure, на которой размещена новая виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="072f0-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="072f0-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="072f0-111">EXAMPLES</span></span>

### <span data-ttu-id="072f0-112">Пример 1: создание виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="072f0-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="072f0-113">Эта команда создает виртуальную машину под управлением операционной системы Windows в существующей службе.</span><span class="sxs-lookup"><span data-stu-id="072f0-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="072f0-114">Командлет выдает виртуальную машину на указанном изображении.</span><span class="sxs-lookup"><span data-stu-id="072f0-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="072f0-115">Команда задает параметр *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="072f0-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="072f0-116">Таким образом, командлет ждет запуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="072f0-117">Пример 2: создание виртуальной машины, использующей сертификаты</span><span class="sxs-lookup"><span data-stu-id="072f0-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="072f0-118">Первая команда получает сертификаты из хранилища и сохраняет их в переменной $certs.</span><span class="sxs-lookup"><span data-stu-id="072f0-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="072f0-119">Вторая команда создает виртуальную машину, которая запускает операционную систему Windows в существующей службе из образа.</span><span class="sxs-lookup"><span data-stu-id="072f0-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="072f0-120">По умолчанию на виртуальной машине включен прослушиватель сети WinRM HTTPS.</span><span class="sxs-lookup"><span data-stu-id="072f0-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="072f0-121">Команда задает параметр *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="072f0-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="072f0-122">Таким образом, командлет ждет запуска виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="072f0-123">Команда отправляет сертификат WinRM и X509Certificates на размещенную службу.</span><span class="sxs-lookup"><span data-stu-id="072f0-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="072f0-124">Пример 3: создание виртуальной машины под управлением операционной системы Linux</span><span class="sxs-lookup"><span data-stu-id="072f0-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="072f0-125">Эта команда создает виртуальную машину, которая запускает операционную систему Linux из образа.</span><span class="sxs-lookup"><span data-stu-id="072f0-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="072f0-126">Эта команда создает службу для размещения новой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="072f0-127">Команда задает расположение службы.</span><span class="sxs-lookup"><span data-stu-id="072f0-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="072f0-128">Пример 4: создание виртуальной машины и создание службы для размещения новой виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="072f0-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="072f0-129">Первая команда получает расположения с помощью командлета **Get-AzureLocation** , а затем сохраняет их в переменной массива $Locations.</span><span class="sxs-lookup"><span data-stu-id="072f0-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="072f0-130">Вторая команда получает доступные изображения с помощью командлета **Get-AzureVMImage** , а затем сохраняет их в переменной массива $Images.</span><span class="sxs-lookup"><span data-stu-id="072f0-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="072f0-131">В последней команде создается большая виртуальная машина с именем VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="072f0-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="072f0-132">Виртуальная машина запускает операционную систему Windows.</span><span class="sxs-lookup"><span data-stu-id="072f0-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="072f0-133">Оно основано на одном из изображений в $Images.</span><span class="sxs-lookup"><span data-stu-id="072f0-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="072f0-134">Команда создает службу с именем ContosoService03 для новой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="072f0-135">Служба находится в папке $Locations.</span><span class="sxs-lookup"><span data-stu-id="072f0-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="072f0-136">Пример 5: создание виртуальной машины с зарезервированным IP-именем</span><span class="sxs-lookup"><span data-stu-id="072f0-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="072f0-137">Первая команда получает расположения, а затем сохраняет их в переменной массива $Locations.</span><span class="sxs-lookup"><span data-stu-id="072f0-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="072f0-138">Вторая команда получает доступные изображения, а затем сохраняет их в переменной массива $Images.</span><span class="sxs-lookup"><span data-stu-id="072f0-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="072f0-139">Последняя команда создает виртуальную машину с именем VirtualMachine27 на основе одного из изображений в $Images.</span><span class="sxs-lookup"><span data-stu-id="072f0-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="072f0-140">Команда создает службу в месте $Locations.</span><span class="sxs-lookup"><span data-stu-id="072f0-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="072f0-141">Виртуальная машина имеет зарезервированное имя IP-адреса, ранее сохраненное в переменной $ipName.</span><span class="sxs-lookup"><span data-stu-id="072f0-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="072f0-142">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="072f0-142">PARAMETERS</span></span>

### <span data-ttu-id="072f0-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="072f0-143">-AdminUsername</span></span>
<span data-ttu-id="072f0-144">Указывает имя пользователя учетной записи администратора, которую этот командлет создает на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="072f0-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="072f0-145">-AffinityGroup</span></span>
<span data-ttu-id="072f0-146">Указывает территориальную группу для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="072f0-147">Укажите этот параметр или параметр *Location* только в том случае, если этот командлет создает службу Azure для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="072f0-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="072f0-148">-AvailabilitySetName</span></span>
<span data-ttu-id="072f0-149">Указывает имя группы доступности, в которой этот командлет создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="072f0-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="072f0-150">-Сертификаты</span><span class="sxs-lookup"><span data-stu-id="072f0-150">-Certificates</span></span>
<span data-ttu-id="072f0-151">Указывает список сертификатов, используемых этим командлетом для создания службы.</span><span class="sxs-lookup"><span data-stu-id="072f0-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="072f0-152">-CustomDataFile</span></span>
<span data-ttu-id="072f0-153">Указывает файл данных для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="072f0-154">Этот командлет кодирует содержимое файла в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="072f0-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="072f0-155">Файл должен быть менее 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="072f0-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="072f0-156">Если гостевая операционная система является операционной системой Windows, этот командлет сохраняет эти данные как двоичный файл с именем%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="072f0-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="072f0-157">Если гостевая операционная система — Linux, этот командлет передает данные с помощью файла ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="072f0-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="072f0-158">При установке файл копируется в каталог/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="072f0-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="072f0-159">Агент также сохраняет данные в кодировке Base64 в/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="072f0-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="072f0-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="072f0-160">-DisableGuestAgent</span></span>
<span data-ttu-id="072f0-161">Указывает на то, что этот командлет отключает Гостевой агент "инфраструктура как службу (IaaS)".</span><span class="sxs-lookup"><span data-stu-id="072f0-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="072f0-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="072f0-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="072f0-163">Указывает на то, что этот командлет отключает удаленное управление Windows (WinRM) на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="072f0-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="072f0-164">По умолчанию служба WinRM включена по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="072f0-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="072f0-165">-DnsSettings</span></span>
<span data-ttu-id="072f0-166">Указывает массив объектов DNS-серверов, которые определяют параметры DNS для нового развертывания.</span><span class="sxs-lookup"><span data-stu-id="072f0-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="072f0-167">Чтобы создать объект **DnsServer** , используйте командлет **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="072f0-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="072f0-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="072f0-169">Указывает на то, что этот командлет включает WinRM через HTTP.</span><span class="sxs-lookup"><span data-stu-id="072f0-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="072f0-170">-HostCaching</span></span>
<span data-ttu-id="072f0-171">Задает режим кэширования узла для диска с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="072f0-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="072f0-172">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="072f0-172">Valid values are:</span></span> 

- <span data-ttu-id="072f0-173">Чтения</span><span class="sxs-lookup"><span data-stu-id="072f0-173">ReadOnly</span></span>
- <span data-ttu-id="072f0-174">Операцию</span><span class="sxs-lookup"><span data-stu-id="072f0-174">ReadWrite</span></span>

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

### <span data-ttu-id="072f0-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="072f0-175">-ImageName</span></span>
<span data-ttu-id="072f0-176">Указывает имя образа диска, используемого этим командлетом для создания диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="072f0-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

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

### <span data-ttu-id="072f0-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="072f0-177">-InformationAction</span></span>
<span data-ttu-id="072f0-178">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="072f0-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="072f0-179">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="072f0-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="072f0-180">Продолжал</span><span class="sxs-lookup"><span data-stu-id="072f0-180">Continue</span></span>
- <span data-ttu-id="072f0-181">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="072f0-181">Ignore</span></span>
- <span data-ttu-id="072f0-182">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="072f0-182">Inquire</span></span>
- <span data-ttu-id="072f0-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="072f0-183">SilentlyContinue</span></span>
- <span data-ttu-id="072f0-184">Остановить</span><span class="sxs-lookup"><span data-stu-id="072f0-184">Stop</span></span>
- <span data-ttu-id="072f0-185">Рвать</span><span class="sxs-lookup"><span data-stu-id="072f0-185">Suspend</span></span>

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

### <span data-ttu-id="072f0-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="072f0-186">-InformationVariable</span></span>
<span data-ttu-id="072f0-187">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="072f0-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="072f0-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="072f0-188">-InstanceSize</span></span>
<span data-ttu-id="072f0-189">Задает размер экземпляра.</span><span class="sxs-lookup"><span data-stu-id="072f0-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="072f0-190">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="072f0-190">Valid values are:</span></span> 

- <span data-ttu-id="072f0-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="072f0-191">ExtraSmall</span></span>
- <span data-ttu-id="072f0-192">Малого</span><span class="sxs-lookup"><span data-stu-id="072f0-192">Small</span></span>
- <span data-ttu-id="072f0-193">Канал</span><span class="sxs-lookup"><span data-stu-id="072f0-193">Medium</span></span>
- <span data-ttu-id="072f0-194">Достаточ</span><span class="sxs-lookup"><span data-stu-id="072f0-194">Large</span></span>
- <span data-ttu-id="072f0-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="072f0-195">ExtraLarge</span></span>
- <span data-ttu-id="072f0-196">Ячейк</span><span class="sxs-lookup"><span data-stu-id="072f0-196">A5</span></span>
- <span data-ttu-id="072f0-197">A6</span><span class="sxs-lookup"><span data-stu-id="072f0-197">A6</span></span>
- <span data-ttu-id="072f0-198">Ответ</span><span class="sxs-lookup"><span data-stu-id="072f0-198">A7</span></span>
- <span data-ttu-id="072f0-199">A8</span><span class="sxs-lookup"><span data-stu-id="072f0-199">A8</span></span>
- <span data-ttu-id="072f0-200">A9</span><span class="sxs-lookup"><span data-stu-id="072f0-200">A9</span></span>
- <span data-ttu-id="072f0-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="072f0-201">Basic_A0</span></span>
- <span data-ttu-id="072f0-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="072f0-202">Basic_A1</span></span>
- <span data-ttu-id="072f0-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="072f0-203">Basic_A2</span></span>
- <span data-ttu-id="072f0-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="072f0-204">Basic_A3</span></span>
- <span data-ttu-id="072f0-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="072f0-205">Basic_A4</span></span>
- <span data-ttu-id="072f0-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="072f0-206">Standard_D1</span></span>
- <span data-ttu-id="072f0-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="072f0-207">Standard_D2</span></span>
- <span data-ttu-id="072f0-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="072f0-208">Standard_D3</span></span>
- <span data-ttu-id="072f0-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="072f0-209">Standard_D4</span></span>
- <span data-ttu-id="072f0-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="072f0-210">Standard_D11</span></span>
- <span data-ttu-id="072f0-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="072f0-211">Standard_D12</span></span>
- <span data-ttu-id="072f0-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="072f0-212">Standard_D13</span></span>
- <span data-ttu-id="072f0-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="072f0-213">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="072f0-214">-Linux</span></span>
<span data-ttu-id="072f0-215">Указывает на то, что этот командлет создает виртуальную машину на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="072f0-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="072f0-216">-LinuxUser</span></span>
<span data-ttu-id="072f0-217">Указывает имя пользователя административной учетной записи Linux, которое этот командлет создает на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="072f0-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-218">-Location</span><span class="sxs-lookup"><span data-stu-id="072f0-218">-Location</span></span>
<span data-ttu-id="072f0-219">Указывает центр обработки данных Azure, на котором размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="072f0-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="072f0-220">Если указать этот параметр, командлет создает службу Azure в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="072f0-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="072f0-221">Указывайте этот параметр или параметр *AffinityGroup* только в том случае, если этот командлет создает службу Azure для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="072f0-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="072f0-222">-MediaLocation</span></span>
<span data-ttu-id="072f0-223">Указывает место хранения Azure, где этот командлет создает диски виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="072f0-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="072f0-224">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="072f0-224">-Name</span></span>
<span data-ttu-id="072f0-225">Указывает имя виртуальной машины, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="072f0-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="072f0-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="072f0-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="072f0-227">Указывает на то, что эта конфигурация не отправляет закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="072f0-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="072f0-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="072f0-229">Указывает на то, что этот командлет не добавляет конечную точку WinRM для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-230">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="072f0-230">-Password</span></span>
<span data-ttu-id="072f0-231">Указывает пароль учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="072f0-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="072f0-232">-Profile</span><span class="sxs-lookup"><span data-stu-id="072f0-232">-Profile</span></span>
<span data-ttu-id="072f0-233">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="072f0-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="072f0-234">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="072f0-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="072f0-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="072f0-235">-ReservedIPName</span></span>
<span data-ttu-id="072f0-236">Задает зарезервированное имя IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="072f0-236">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="072f0-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="072f0-238">Указывает полное доменное имя для обратного поиска DNS.</span><span class="sxs-lookup"><span data-stu-id="072f0-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="072f0-239">-ServiceName</span></span>
<span data-ttu-id="072f0-240">Указывает имя новой или существующей службы Azure, к которой этот командлет добавляет новую виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="072f0-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="072f0-241">Если указана новая служба, этот командлет создаст ее.</span><span class="sxs-lookup"><span data-stu-id="072f0-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="072f0-242">Чтобы создать новую службу, необходимо указать *Расположение* или параметр *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="072f0-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="072f0-243">Если указана существующая служба, не указывайте *Location* или *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="072f0-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

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

### <span data-ttu-id="072f0-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="072f0-244">-SSHKeyPairs</span></span>
<span data-ttu-id="072f0-245">Задает пары ключей SSH.</span><span class="sxs-lookup"><span data-stu-id="072f0-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="072f0-246">-SSHPublicKeys</span></span>
<span data-ttu-id="072f0-247">Указывает открытые ключи SSH.</span><span class="sxs-lookup"><span data-stu-id="072f0-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="072f0-248">-SubnetNames</span></span>
<span data-ttu-id="072f0-249">Указывает массив имен подсети для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="072f0-250">-VNetName</span></span>
<span data-ttu-id="072f0-251">Указывает имя виртуальной сети для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="072f0-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="072f0-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="072f0-252">-WaitForBoot</span></span>
<span data-ttu-id="072f0-253">Указывает на то, что этот командлет ожидает, пока виртуальная машина не достигнет состояния ReadyRole.</span><span class="sxs-lookup"><span data-stu-id="072f0-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="072f0-254">Если виртуальная машина достигает одного из следующих состояний, командлет завершает работу со сбоем: FailedStartingVM, ProvisioningFailed или ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="072f0-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="072f0-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="072f0-255">-Windows</span></span>
<span data-ttu-id="072f0-256">Указывает на то, что этот командлет создает виртуальную машину Windows.</span><span class="sxs-lookup"><span data-stu-id="072f0-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="072f0-257">-WinRMCertificate</span></span>
<span data-ttu-id="072f0-258">Указывает сертификат, который этот командлет свяжет с конечной точкой WinRM.</span><span class="sxs-lookup"><span data-stu-id="072f0-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="072f0-259">-X509Certificates</span></span>
<span data-ttu-id="072f0-260">Указывает массив сертификатов X509, развернутых в размещенной службе.</span><span class="sxs-lookup"><span data-stu-id="072f0-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="072f0-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="072f0-261">CommonParameters</span></span>
<span data-ttu-id="072f0-262">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="072f0-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="072f0-263">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="072f0-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="072f0-264">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="072f0-264">INPUTS</span></span>

## <span data-ttu-id="072f0-265">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="072f0-265">OUTPUTS</span></span>

## <span data-ttu-id="072f0-266">Пуск</span><span class="sxs-lookup"><span data-stu-id="072f0-266">NOTES</span></span>

## <span data-ttu-id="072f0-267">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="072f0-267">RELATED LINKS</span></span>

[<span data-ttu-id="072f0-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="072f0-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="072f0-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="072f0-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="072f0-270">New-AzureDns</span><span class="sxs-lookup"><span data-stu-id="072f0-270">New-AzureDns</span></span>](./New-AzureDns.md)


