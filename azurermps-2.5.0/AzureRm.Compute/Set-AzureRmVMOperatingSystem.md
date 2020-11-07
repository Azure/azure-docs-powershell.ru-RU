---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmoperatingsystem
schema: 2.0.0
ms.openlocfilehash: 0eea5d3a4f379b61e5d66e04b66e7812abaf75f0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914881"
---
# <span data-ttu-id="ecf72-101">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="ecf72-101">Set-AzureRmVMOperatingSystem</span></span>

## <span data-ttu-id="ecf72-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ecf72-102">SYNOPSIS</span></span>
<span data-ttu-id="ecf72-103">Настройка свойств операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecf72-103">Sets operating system properties for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ecf72-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ecf72-104">SYNTAX</span></span>

### <span data-ttu-id="ecf72-105">Windows (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ecf72-105">Windows (Default)</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf72-106">WindowsWinRmHttps</span><span class="sxs-lookup"><span data-stu-id="ecf72-106">WindowsWinRmHttps</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ecf72-107">Linux</span><span class="sxs-lookup"><span data-stu-id="ecf72-107">Linux</span></span>
```
Set-AzureRmVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ecf72-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf72-108">DESCRIPTION</span></span>
<span data-ttu-id="ecf72-109">Командлет **Set-AzureRmVMOperatingSystem** задает свойства операционной системы для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecf72-109">The **Set-AzureRmVMOperatingSystem** cmdlet sets operating system properties for a virtual machine.</span></span>
<span data-ttu-id="ecf72-110">Вы можете задать учетные данные для входа, имя компьютера и тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ecf72-110">You can specify logon credentials, computer name, and operating system type.</span></span>

## <span data-ttu-id="ecf72-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ecf72-111">EXAMPLES</span></span>

### <span data-ttu-id="ecf72-112">Пример 1: Настройка свойств операционной системы для новых виртуальных машин</span><span class="sxs-lookup"><span data-stu-id="ecf72-112">Example 1: Set operating system properties for a new virtual machines</span></span>
```
PS C:\> $SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $ComputerName = "ContosoVM122"
PS C:\> $WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
PS C:\> $TimeZone = "Pacific Standard Time"
PS C:\> $CustomData = "echo 'Hello World'"
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone
```

<span data-ttu-id="ecf72-113">Первая команда преобразует пароль в защищенную строку, а затем сохраняет его в переменной $SecurePassword.</span><span class="sxs-lookup"><span data-stu-id="ecf72-113">The first command converts a password to a secure string, and then stores it in the $SecurePassword variable.</span></span>
<span data-ttu-id="ecf72-114">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="ecf72-114">For more information, type `Get-Help ConvertTo-SecureString`.</span></span>

<span data-ttu-id="ecf72-115">Вторая команда создает учетные данные пользователя FullerP и пароль, хранящийся в $SecurePassword, а затем сохраняет учетные данные в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="ecf72-115">The second command creates a credential for the user FullerP and the password stored in $SecurePassword, and then stores the credential in the $Credential variable.</span></span>
<span data-ttu-id="ecf72-116">Для получения дополнительных сведений введите `Get-Help New-Object` .</span><span class="sxs-lookup"><span data-stu-id="ecf72-116">For more information, type `Get-Help New-Object`.</span></span>

<span data-ttu-id="ecf72-117">Третья команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ecf72-117">The third command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="ecf72-118">Четвертая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ecf72-118">The fourth command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="ecf72-119">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ecf72-119">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="ecf72-120">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="ecf72-120">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="ecf72-121">Следующие четыре команды назначают значения переменных для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="ecf72-121">The next four commands assign values to variables to use in the following command.</span></span>
<span data-ttu-id="ecf72-122">Так как вы можете указать эти строки непосредственно в команде **Set-AzureRmVMOperatingSystem** , этот подход используется только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ecf72-122">Because you could specify these strings directly in the **Set-AzureRmVMOperatingSystem** command, this approach is used only for readability.</span></span>
<span data-ttu-id="ecf72-123">Однако вы можете использовать такой подход в сценариях.</span><span class="sxs-lookup"><span data-stu-id="ecf72-123">However, you might use an approach such as this in scripts.</span></span>

<span data-ttu-id="ecf72-124">Последняя команда задает свойства операционной системы для виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="ecf72-124">The final command sets operating system properties for the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="ecf72-125">В команде используются учетные данные, хранящиеся в $Credential.</span><span class="sxs-lookup"><span data-stu-id="ecf72-125">The command uses the credentials stored in $Credential.</span></span>
<span data-ttu-id="ecf72-126">Команда использует переменные, назначенные в предыдущих командах, для некоторых параметров.</span><span class="sxs-lookup"><span data-stu-id="ecf72-126">The command uses variables assigned in previous commands for some parameters.</span></span>

## <span data-ttu-id="ecf72-127">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ecf72-127">PARAMETERS</span></span>

### <span data-ttu-id="ecf72-128">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="ecf72-128">-ComputerName</span></span>
<span data-ttu-id="ecf72-129">Указывает имя компьютера.</span><span class="sxs-lookup"><span data-stu-id="ecf72-129">Specifies the name of the computer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-130">-Credential</span><span class="sxs-lookup"><span data-stu-id="ecf72-130">-Credential</span></span>
<span data-ttu-id="ecf72-131">Указывает имя пользователя и пароль для виртуальной машины в качестве объекта **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="ecf72-131">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="ecf72-132">Чтобы получить учетные данные, используйте командлет Get-Credential.</span><span class="sxs-lookup"><span data-stu-id="ecf72-132">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="ecf72-133">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="ecf72-133">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-134">-CustomData</span><span class="sxs-lookup"><span data-stu-id="ecf72-134">-CustomData</span></span>
<span data-ttu-id="ecf72-135">Задает строку настраиваемых данных, закодированную в формате 64.</span><span class="sxs-lookup"><span data-stu-id="ecf72-135">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="ecf72-136">Этот код декодирован на двоичный массив, сохраненный в виде файла на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ecf72-136">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="ecf72-137">Максимальная длина двоичного массива составляет 65535 байт.</span><span class="sxs-lookup"><span data-stu-id="ecf72-137">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecf72-138">-DefaultProfile</span></span>
<span data-ttu-id="ecf72-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ecf72-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-140">-DisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="ecf72-140">-DisablePasswordAuthentication</span></span>
<span data-ttu-id="ecf72-141">Указывает на то, что этот командлет отключает проверку подлинности пароля.</span><span class="sxs-lookup"><span data-stu-id="ecf72-141">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-142">-EnableAutoUpdate</span><span class="sxs-lookup"><span data-stu-id="ecf72-142">-EnableAutoUpdate</span></span>
<span data-ttu-id="ecf72-143">Указывает на то, что этот командлет включает функцию автоматического обновления.</span><span class="sxs-lookup"><span data-stu-id="ecf72-143">Indicates that this cmdlet enables auto update.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-144">-Linux</span><span class="sxs-lookup"><span data-stu-id="ecf72-144">-Linux</span></span>
<span data-ttu-id="ecf72-145">Указывает, что тип операционной системы — Linux.</span><span class="sxs-lookup"><span data-stu-id="ecf72-145">Indicates that the type of operating system is Linux.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-146">-ProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="ecf72-146">-ProvisionVMAgent</span></span>
<span data-ttu-id="ecf72-147">Указывает на то, что для параметров требуется установка агента виртуальной машины на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ecf72-147">Indicates that the settings require that the virtual machine agent be installed on the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-148">-Часовой пояс</span><span class="sxs-lookup"><span data-stu-id="ecf72-148">-TimeZone</span></span>
<span data-ttu-id="ecf72-149">Указывает часовой пояс для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ecf72-149">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ecf72-150">-VM</span></span>
<span data-ttu-id="ecf72-151">Указывает локальный объект виртуальной машины, на котором нужно задать свойства операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ecf72-151">Specifies the local virtual machine object on which to set operating system properties.</span></span>
<span data-ttu-id="ecf72-152">Чтобы получить объект виртуальной машины, используйте командлет Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="ecf72-152">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="ecf72-153">Создайте объект виртуальной машины с помощью командлета New-AzureRmVMConfig.</span><span class="sxs-lookup"><span data-stu-id="ecf72-153">Create a virtual machine object by using the New-AzureRmVMConfig cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-154">-Windows</span><span class="sxs-lookup"><span data-stu-id="ecf72-154">-Windows</span></span>
<span data-ttu-id="ecf72-155">Указывает на то, что тип операционной системы — Windows.</span><span class="sxs-lookup"><span data-stu-id="ecf72-155">Indicates that the type of operating system is Windows.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-156">-WinRMCertificateUrl</span><span class="sxs-lookup"><span data-stu-id="ecf72-156">-WinRMCertificateUrl</span></span>
<span data-ttu-id="ecf72-157">Задает универсальный код ресурса (URI) для сертификата WinRM.</span><span class="sxs-lookup"><span data-stu-id="ecf72-157">Specifies the URI of a WinRM certificate.</span></span>
<span data-ttu-id="ecf72-158">Это необходимо для хранения в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ecf72-158">This needs to be stored in a Key Vault.</span></span>

```yaml
Type: Uri
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-159">-WinRMHttp</span><span class="sxs-lookup"><span data-stu-id="ecf72-159">-WinRMHttp</span></span>
<span data-ttu-id="ecf72-160">Указывает, что эта операционная система использует HTTP WinRM.</span><span class="sxs-lookup"><span data-stu-id="ecf72-160">Indicates that this operating system uses HTTP WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-161">-WinRMHttps</span><span class="sxs-lookup"><span data-stu-id="ecf72-161">-WinRMHttps</span></span>
<span data-ttu-id="ecf72-162">Указывает, что эта операционная система использует HTTPS WinRM.</span><span class="sxs-lookup"><span data-stu-id="ecf72-162">Indicates that this operating system uses HTTPS WinRM.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsWinRmHttps
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ecf72-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecf72-163">CommonParameters</span></span>
<span data-ttu-id="ecf72-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ecf72-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecf72-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecf72-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecf72-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ecf72-166">INPUTS</span></span>

### <span data-ttu-id="ecf72-167">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ecf72-167">PSVirtualMachine</span></span>
<span data-ttu-id="ecf72-168">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ecf72-168">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ecf72-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ecf72-169">OUTPUTS</span></span>

### <span data-ttu-id="ecf72-170">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ecf72-170">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ecf72-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="ecf72-171">NOTES</span></span>

## <span data-ttu-id="ecf72-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ecf72-172">RELATED LINKS</span></span>

[<span data-ttu-id="ecf72-173">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ecf72-173">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ecf72-174">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ecf72-174">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)


