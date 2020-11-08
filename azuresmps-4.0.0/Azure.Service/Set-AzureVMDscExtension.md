---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077351"
---
# <span data-ttu-id="a87a1-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a87a1-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="a87a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a87a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a87a1-103">Настраивает расширение DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a87a1-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="a87a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a87a1-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a87a1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a87a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a87a1-106">Командлет **Set-AzureVMDscExtension** настраивает расширение конфигурации нужного состояния (DSC) на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a87a1-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="a87a1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a87a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a87a1-108">Пример 1: Настройка расширения DSC на виртуальной машине</span><span class="sxs-lookup"><span data-stu-id="a87a1-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="a87a1-109">Эта команда настраивает расширение DSC на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a87a1-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="a87a1-110">Пакет MyConfiguration.ps1.zip должен быть предварительно загружен в хранилище Azure с помощью команды **Publish-AzureVMDscConfiguration** и включает сценарий MyConfiguration.ps1 и модули, от которых он зависит.</span><span class="sxs-lookup"><span data-stu-id="a87a1-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="a87a1-111">Аргумент MyConfiguration указывает определенную конфигурацию DSC в сценарии для выполнения.</span><span class="sxs-lookup"><span data-stu-id="a87a1-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="a87a1-112">Параметр- *ConfigurationArgument* указывает Hashtable с аргументами, которые передаются в функцию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a87a1-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="a87a1-113">Пример 2: Настройка расширения DSC на виртуальной машине с помощью пути к данным конфигурации</span><span class="sxs-lookup"><span data-stu-id="a87a1-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="a87a1-114">Эта команда настраивает расширение DSC на виртуальной машине, используя путь к данным конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a87a1-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="a87a1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a87a1-115">PARAMETERS</span></span>

### <span data-ttu-id="a87a1-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="a87a1-116">-ConfigurationArchive</span></span>
<span data-ttu-id="a87a1-117">Указывает имя пакета конфигурации (ZIP-файла), который ранее был передан командой Publish — AzureVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a87a1-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="a87a1-118">Этот параметр должен указывать только имя файла без пути.</span><span class="sxs-lookup"><span data-stu-id="a87a1-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="a87a1-119">-ConfigurationArgument</span></span>
<span data-ttu-id="a87a1-120">Указывает хэш-таблицу, указывающую аргументы для функции конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a87a1-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="a87a1-121">Ключи соответствуют именам параметров и значениям для значений параметров.</span><span class="sxs-lookup"><span data-stu-id="a87a1-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="a87a1-122">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a87a1-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a87a1-123">примитивные типы</span><span class="sxs-lookup"><span data-stu-id="a87a1-123">primitive types</span></span>
- <span data-ttu-id="a87a1-124">подстрок</span><span class="sxs-lookup"><span data-stu-id="a87a1-124">string</span></span>
- <span data-ttu-id="a87a1-125">IsArray</span><span class="sxs-lookup"><span data-stu-id="a87a1-125">array</span></span>
- <span data-ttu-id="a87a1-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="a87a1-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="a87a1-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="a87a1-128">Указывает путь к PSD1-файлу, который определяет данные для функции конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a87a1-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="a87a1-129">Этот файл должен содержать Hashtable, как описано в разделе разделение конфигурации и данных среды https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="a87a1-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

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

### <span data-ttu-id="a87a1-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a87a1-130">-ConfigurationName</span></span>
<span data-ttu-id="a87a1-131">Указывает имя сценария конфигурации или модуля, вызываемого расширением DSC.</span><span class="sxs-lookup"><span data-stu-id="a87a1-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="a87a1-132">Значение этого параметра должно быть именем одной из функций конфигурации, которые содержатся в сценариях или модулях, упакованных в *ConfigurationArchive*.</span><span class="sxs-lookup"><span data-stu-id="a87a1-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="a87a1-133">Этот командлет по умолчанию имеет имя файла, заданного параметром *ConfigurationArchive* , если опустить этот параметр, исключая все расширения.</span><span class="sxs-lookup"><span data-stu-id="a87a1-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="a87a1-134">Например, если *ConfigurationArchive* "SalesWebSite.ps1.zip", для *configurationName* используется значение по умолчанию "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="a87a1-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

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

### <span data-ttu-id="a87a1-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="a87a1-135">-ContainerName</span></span>
<span data-ttu-id="a87a1-136">Указывает имя контейнера хранилища Azure, где расположен *ConfigurationArchive* .</span><span class="sxs-lookup"><span data-stu-id="a87a1-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

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

### <span data-ttu-id="a87a1-137">-Коллекция</span><span class="sxs-lookup"><span data-stu-id="a87a1-137">-DataCollection</span></span>
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

### <span data-ttu-id="a87a1-138">-Force</span><span class="sxs-lookup"><span data-stu-id="a87a1-138">-Force</span></span>
<span data-ttu-id="a87a1-139">Указывает на то, что этот командлет перезапишет существующие большие двоичные объекты.</span><span class="sxs-lookup"><span data-stu-id="a87a1-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

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

### <span data-ttu-id="a87a1-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a87a1-140">-InformationAction</span></span>
<span data-ttu-id="a87a1-141">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="a87a1-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a87a1-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a87a1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a87a1-143">Продолжал</span><span class="sxs-lookup"><span data-stu-id="a87a1-143">Continue</span></span>
- <span data-ttu-id="a87a1-144">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="a87a1-144">Ignore</span></span>
- <span data-ttu-id="a87a1-145">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="a87a1-145">Inquire</span></span>
- <span data-ttu-id="a87a1-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a87a1-146">SilentlyContinue</span></span>
- <span data-ttu-id="a87a1-147">Остановить</span><span class="sxs-lookup"><span data-stu-id="a87a1-147">Stop</span></span>
- <span data-ttu-id="a87a1-148">Рвать</span><span class="sxs-lookup"><span data-stu-id="a87a1-148">Suspend</span></span>

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

### <span data-ttu-id="a87a1-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a87a1-149">-InformationVariable</span></span>
<span data-ttu-id="a87a1-150">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="a87a1-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a87a1-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="a87a1-151">-Profile</span></span>
<span data-ttu-id="a87a1-152">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a87a1-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a87a1-153">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a87a1-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a87a1-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="a87a1-154">-ReferenceName</span></span>
<span data-ttu-id="a87a1-155">Задает пользовательскую строку, которую можно использовать для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="a87a1-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="a87a1-156">Этот параметр задается, когда расширение добавляется на виртуальную машину в первый раз.</span><span class="sxs-lookup"><span data-stu-id="a87a1-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="a87a1-157">При последующих обновлениях необходимо указать ранее использованное Справочное имя, когда вы обновите расширение.</span><span class="sxs-lookup"><span data-stu-id="a87a1-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="a87a1-158">*ReferenceName* , назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="a87a1-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="a87a1-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="a87a1-159">-StorageContext</span></span>
<span data-ttu-id="a87a1-160">Указывает контекст хранилища Azure, предоставляющий параметры безопасности, используемые для доступа к сценарию конфигурации.</span><span class="sxs-lookup"><span data-stu-id="a87a1-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="a87a1-161">Этот контекст предоставляет доступ на чтение к контейнеру, указанному в параметре *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="a87a1-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a87a1-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="a87a1-163">Задает суффикс DNS Endpoint для всех служб хранилища (например, "core.contoso.net").</span><span class="sxs-lookup"><span data-stu-id="a87a1-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

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

### <span data-ttu-id="a87a1-164">-Version</span><span class="sxs-lookup"><span data-stu-id="a87a1-164">-Version</span></span>
<span data-ttu-id="a87a1-165">Указывает определенную версию расширения DSC, которую вы хотите использовать.</span><span class="sxs-lookup"><span data-stu-id="a87a1-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="a87a1-166">По умолчанию задано значение "1. \*", если этот параметр не указан.</span><span class="sxs-lookup"><span data-stu-id="a87a1-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

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

### <span data-ttu-id="a87a1-167">-VM</span><span class="sxs-lookup"><span data-stu-id="a87a1-167">-VM</span></span>
<span data-ttu-id="a87a1-168">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a87a1-168">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="a87a1-169">-WmfVersion</span></span>
<span data-ttu-id="a87a1-170">Указывает версию платформы управления Windows (WMF) для установки на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a87a1-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="a87a1-171">Расширение DSC зависит от функций DSC, которые доступны только в обновлениях WMF.</span><span class="sxs-lookup"><span data-stu-id="a87a1-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="a87a1-172">Этот параметр указывает версию обновления для установки на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="a87a1-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="a87a1-173">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a87a1-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a87a1-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="a87a1-174">4.0.</span></span>
<span data-ttu-id="a87a1-175">Устанавливает WMF 4,0, если уже не установлена более новая версия.</span><span class="sxs-lookup"><span data-stu-id="a87a1-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="a87a1-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="a87a1-176">5.0.</span></span>
<span data-ttu-id="a87a1-177">Установка последней версии WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="a87a1-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="a87a1-178">последнюю.</span><span class="sxs-lookup"><span data-stu-id="a87a1-178">latest.</span></span>
<span data-ttu-id="a87a1-179">Установка последней версии WMF, в настоящее время WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="a87a1-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="a87a1-180">Значение по умолчанию — новейшее.</span><span class="sxs-lookup"><span data-stu-id="a87a1-180">The default value is latest.</span></span>

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

### <span data-ttu-id="a87a1-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a87a1-181">-Confirm</span></span>
<span data-ttu-id="a87a1-182">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a87a1-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a87a1-183">-WhatIf</span></span>
<span data-ttu-id="a87a1-184">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a87a1-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a87a1-185">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a87a1-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a87a1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a87a1-186">CommonParameters</span></span>
<span data-ttu-id="a87a1-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a87a1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a87a1-188">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a87a1-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a87a1-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a87a1-189">INPUTS</span></span>

## <span data-ttu-id="a87a1-190">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a87a1-190">OUTPUTS</span></span>

## <span data-ttu-id="a87a1-191">Пуск</span><span class="sxs-lookup"><span data-stu-id="a87a1-191">NOTES</span></span>

## <span data-ttu-id="a87a1-192">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a87a1-192">RELATED LINKS</span></span>

[<span data-ttu-id="a87a1-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a87a1-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="a87a1-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a87a1-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="a87a1-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="a87a1-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="a87a1-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a87a1-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="a87a1-197">Publish-AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a87a1-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


