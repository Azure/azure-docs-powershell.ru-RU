---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076382"
---
# <span data-ttu-id="5b245-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="5b245-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="5b245-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b245-102">SYNOPSIS</span></span>
<span data-ttu-id="5b245-103">Добавляет конфигурацию подготовки для виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5b245-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="5b245-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b245-104">SYNTAX</span></span>

### <span data-ttu-id="5b245-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b245-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b245-106">Linux</span><span class="sxs-lookup"><span data-stu-id="5b245-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5b245-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="5b245-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5b245-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b245-108">DESCRIPTION</span></span>
<span data-ttu-id="5b245-109">Командлет **Add-AzureProvisioningConfig** добавляет сведения о конфигурации для подготовки к конфигурации виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="5b245-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="5b245-110">Вы можете использовать объект Configuration для создания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b245-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="5b245-111">Этот командлет поддерживает различные конфигурации подготовки, включая изолированные серверы Windows, серверы Windows, Объединенные с доменом Active Directory и серверами на базе Linux.</span><span class="sxs-lookup"><span data-stu-id="5b245-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="5b245-112">Чтобы создать сервер доменных имен Active Directory, укажите полное доменное имя домена Active Directory и учетные данные пользователя, имеющего разрешение на присоединение виртуальной машины к домену.</span><span class="sxs-lookup"><span data-stu-id="5b245-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="5b245-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b245-113">EXAMPLES</span></span>

### <span data-ttu-id="5b245-114">Пример 1: создание автономной виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="5b245-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5b245-115">Эта команда создает объект конфигурации виртуальной машины с помощью командлета **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="5b245-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="5b245-116">Команда передает этот объект в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="5b245-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5b245-117">Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, работающей под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="5b245-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="5b245-118">Конфигурация включает имя пользователя и пароль администратора.</span><span class="sxs-lookup"><span data-stu-id="5b245-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="5b245-119">Команда передает конфигурацию в командлет **New-AzureVM** , который создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="5b245-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="5b245-120">Пример 2: создание виртуальной машины, присоединенной к домену</span><span class="sxs-lookup"><span data-stu-id="5b245-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5b245-121">Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-122">Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, присоединенной к домену contoso.</span><span class="sxs-lookup"><span data-stu-id="5b245-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="5b245-123">Команда содержит имя пользователя и пароль, необходимые для присоединения виртуальной машины к домену.</span><span class="sxs-lookup"><span data-stu-id="5b245-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="5b245-124">Для настройки требуется, чтобы пользователь изменил пароль пользователя при первом входе.</span><span class="sxs-lookup"><span data-stu-id="5b245-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="5b245-125">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5b245-126">Пример 3: создание виртуальной машины на базе Linux</span><span class="sxs-lookup"><span data-stu-id="5b245-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="5b245-127">Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-128">Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, работающей под управлением операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="5b245-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="5b245-129">Конфигурация включает корневое имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="5b245-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="5b245-130">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5b245-131">Пример 4: создание виртуальной машины, включающей сертификаты для WinRM</span><span class="sxs-lookup"><span data-stu-id="5b245-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5b245-132">Первая команда получает сертификаты из хранилища сертификатов, а затем сохраняет их в переменной массива $certs.</span><span class="sxs-lookup"><span data-stu-id="5b245-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="5b245-133">Вторая команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-134">Текущий командлет добавляет конфигурацию подготовки, включающую сертификаты для WinRM.</span><span class="sxs-lookup"><span data-stu-id="5b245-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="5b245-135">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5b245-136">Пример 5: создание виртуальной машины с поддержкой WinRM по протоколу HTTP</span><span class="sxs-lookup"><span data-stu-id="5b245-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5b245-137">Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-138">Текущий командлет добавляет конфигурацию подготовки с поддержкой WinRM через HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b245-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="5b245-139">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5b245-140">Пример 6: создание виртуальной машины с отключенной WinRM по протоколу HTTPS</span><span class="sxs-lookup"><span data-stu-id="5b245-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5b245-141">Эта команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-142">Текущий командлет добавляет конфигурацию подготовки, которая отключает WinRM через HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b245-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="5b245-143">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="5b245-144">Пример 7: создание виртуальной машины без экспорта ключа</span><span class="sxs-lookup"><span data-stu-id="5b245-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="5b245-145">Первая команда получает сертификаты из хранилища сертификатов, а затем сохраняет их в переменной массива $certs.</span><span class="sxs-lookup"><span data-stu-id="5b245-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="5b245-146">Вторая команда создает объект конфигурации виртуальной машины и передает его в текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5b245-147">Текущий командлет добавляет конфигурацию подготовки для виртуальной машины, включающей сертификаты, и не экспортирует закрытые ключи.</span><span class="sxs-lookup"><span data-stu-id="5b245-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="5b245-148">Команда создает виртуальную машину на основе объекта подготовки.</span><span class="sxs-lookup"><span data-stu-id="5b245-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="5b245-149">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b245-149">PARAMETERS</span></span>

### <span data-ttu-id="5b245-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="5b245-150">-AdminUsername</span></span>
<span data-ttu-id="5b245-151">Указывает имя пользователя учетной записи администратора, которую эта конфигурация создает на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5b245-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-152">-Сертификаты</span><span class="sxs-lookup"><span data-stu-id="5b245-152">-Certificates</span></span>
<span data-ttu-id="5b245-153">Указывает набор сертификатов, устанавливаемый этой конфигурацией на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5b245-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="5b245-154">-CustomDataFile</span></span>
<span data-ttu-id="5b245-155">Указывает файл данных для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b245-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="5b245-156">Этот командлет кодирует содержимое файла в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="5b245-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="5b245-157">Файл должен быть менее 64 КБ.</span><span class="sxs-lookup"><span data-stu-id="5b245-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="5b245-158">Если гостевая операционная система — операционная система Windows, эта конфигурация сохранит эти данные как двоичный файл с именем%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="5b245-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="5b245-159">Если гостевая операционная система — Linux, эти данные передаются с помощью файла ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="5b245-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="5b245-160">Configuration копирует файл в каталог/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="5b245-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="5b245-161">Агент также сохраняет данные в кодировке Base64 в/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="5b245-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="5b245-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="5b245-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="5b245-163">Указывает на то, что эта конфигурация отключает автоматические обновления.</span><span class="sxs-lookup"><span data-stu-id="5b245-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="5b245-164">-DisableGuestAgent</span></span>
<span data-ttu-id="5b245-165">Указывает на то, что эта конфигурация отключает инфраструктуру как гостевой агент службы (IaaS).</span><span class="sxs-lookup"><span data-stu-id="5b245-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="5b245-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="5b245-166">-DisableSSH</span></span>
<span data-ttu-id="5b245-167">Указывает на то, что эта конфигурация отключает SSH.</span><span class="sxs-lookup"><span data-stu-id="5b245-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="5b245-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="5b245-169">Указывает на то, что эта конфигурация отключает удаленное управление Windows (WinRM) на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b245-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="5b245-170">По умолчанию служба WinRM включена по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b245-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-171">-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="5b245-171">-Domain</span></span>
<span data-ttu-id="5b245-172">Указывает имя домена учетной записи, которая имеет разрешение на добавление компьютера в домен.</span><span class="sxs-lookup"><span data-stu-id="5b245-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="5b245-173">-DomainPassword</span></span>
<span data-ttu-id="5b245-174">Указывает пароль учетной записи пользователя, у которого есть разрешение на добавление компьютера в домен.</span><span class="sxs-lookup"><span data-stu-id="5b245-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="5b245-175">-DomainUserName</span></span>
<span data-ttu-id="5b245-176">Указывает имя учетной записи пользователя, у которой есть разрешение на добавление компьютера в домен.</span><span class="sxs-lookup"><span data-stu-id="5b245-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="5b245-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="5b245-178">Указывает на то, что эта конфигурация включает WinRM через HTTP.</span><span class="sxs-lookup"><span data-stu-id="5b245-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="5b245-179">-InformationAction</span></span>
<span data-ttu-id="5b245-180">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="5b245-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5b245-181">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5b245-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5b245-182">Продолжал</span><span class="sxs-lookup"><span data-stu-id="5b245-182">Continue</span></span>
- <span data-ttu-id="5b245-183">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="5b245-183">Ignore</span></span>
- <span data-ttu-id="5b245-184">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="5b245-184">Inquire</span></span>
- <span data-ttu-id="5b245-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="5b245-185">SilentlyContinue</span></span>
- <span data-ttu-id="5b245-186">Остановить</span><span class="sxs-lookup"><span data-stu-id="5b245-186">Stop</span></span>
- <span data-ttu-id="5b245-187">Рвать</span><span class="sxs-lookup"><span data-stu-id="5b245-187">Suspend</span></span>

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

### <span data-ttu-id="5b245-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="5b245-188">-InformationVariable</span></span>
<span data-ttu-id="5b245-189">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="5b245-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5b245-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="5b245-190">-JoinDomain</span></span>
<span data-ttu-id="5b245-191">Указывает полное доменное имя (FQDN) домена, к которому нужно присоединиться.</span><span class="sxs-lookup"><span data-stu-id="5b245-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="5b245-192">-Linux</span></span>
<span data-ttu-id="5b245-193">Указывает на то, что эта конфигурация создает конфигурацию Linux.</span><span class="sxs-lookup"><span data-stu-id="5b245-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="5b245-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="5b245-194">-LinuxUser</span></span>
<span data-ttu-id="5b245-195">Указывает имя пользователя административной учетной записи Linux, которую эта конфигурация создает на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="5b245-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="5b245-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="5b245-196">-MachineObjectOU</span></span>
<span data-ttu-id="5b245-197">Полное имя подразделения (OU), в котором конфигурация создает учетную запись компьютера.</span><span class="sxs-lookup"><span data-stu-id="5b245-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="5b245-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="5b245-199">Указывает на то, что эта конфигурация не отправляет закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="5b245-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b245-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="5b245-201">Эта конфигурация указывает на то, что виртуальная машина создается без конечной точки удаленного рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="5b245-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b245-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="5b245-203">Указывает на то, что эта конфигурация создает виртуальную машину без конечной точки SSH.</span><span class="sxs-lookup"><span data-stu-id="5b245-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="5b245-204">-NoSSHPassword</span></span>
<span data-ttu-id="5b245-205">Эта конфигурация указывает на то, что виртуальная машина создается без пароля SSH.</span><span class="sxs-lookup"><span data-stu-id="5b245-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="5b245-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="5b245-207">Указывает на то, что эта конфигурация не добавляет конечную точку WinRM для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b245-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-208">-Password (пароль)</span><span class="sxs-lookup"><span data-stu-id="5b245-208">-Password</span></span>
<span data-ttu-id="5b245-209">Указывает пароль учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="5b245-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="5b245-210">-Profile</span><span class="sxs-lookup"><span data-stu-id="5b245-210">-Profile</span></span>
<span data-ttu-id="5b245-211">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="5b245-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5b245-212">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b245-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5b245-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="5b245-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="5b245-214">Указывает, что виртуальной машине требуется, чтобы пользователь изменил пароль при первом входе.</span><span class="sxs-lookup"><span data-stu-id="5b245-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="5b245-215">-SSHKeyPairs</span></span>
<span data-ttu-id="5b245-216">Задает пары ключей SSH.</span><span class="sxs-lookup"><span data-stu-id="5b245-216">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="5b245-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="5b245-217">-SSHPublicKeys</span></span>
<span data-ttu-id="5b245-218">Указывает открытые ключи SSH.</span><span class="sxs-lookup"><span data-stu-id="5b245-218">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="5b245-219">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="5b245-219">-TimeZone</span></span>
<span data-ttu-id="5b245-220">Указывает часовой пояс для виртуальной машины, например тихоокеанское стандартное время или центральное стандартное время Канады.</span><span class="sxs-lookup"><span data-stu-id="5b245-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-221">-VM</span><span class="sxs-lookup"><span data-stu-id="5b245-221">-VM</span></span>
<span data-ttu-id="5b245-222">Указывает объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5b245-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="5b245-223">-Windows</span></span>
<span data-ttu-id="5b245-224">Указывает на то, что эта конфигурация создает автономную виртуальную машину под управлением операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="5b245-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="5b245-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="5b245-225">-WindowsDomain</span></span>
<span data-ttu-id="5b245-226">Указывает на то, что эта конфигурация создает сервер Windows, который присоединен к домену Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5b245-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="5b245-227">-WinRMCertificate</span></span>
<span data-ttu-id="5b245-228">Указывает сертификат, который эта конфигурация связывает с конечной точкой WinRM.</span><span class="sxs-lookup"><span data-stu-id="5b245-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-229">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="5b245-229">-X509Certificates</span></span>
<span data-ttu-id="5b245-230">Указывает массив сертификатов X509, развернутых в размещенной службе.</span><span class="sxs-lookup"><span data-stu-id="5b245-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b245-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b245-231">CommonParameters</span></span>
<span data-ttu-id="5b245-232">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b245-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b245-233">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b245-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b245-234">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b245-234">INPUTS</span></span>

## <span data-ttu-id="5b245-235">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b245-235">OUTPUTS</span></span>

## <span data-ttu-id="5b245-236">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b245-236">NOTES</span></span>

## <span data-ttu-id="5b245-237">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b245-237">RELATED LINKS</span></span>

[<span data-ttu-id="5b245-238">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="5b245-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="5b245-239">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="5b245-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


