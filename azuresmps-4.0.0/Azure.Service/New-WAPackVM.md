---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077398"
---
# <span data-ttu-id="a487f-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-101">New-WAPackVM</span></span>

## <span data-ttu-id="a487f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a487f-102">SYNOPSIS</span></span>
<span data-ttu-id="a487f-103">Создание виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a487f-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="a487f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a487f-104">SYNTAX</span></span>

### <span data-ttu-id="a487f-105">CreateVMFromTemplate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a487f-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a487f-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="a487f-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="a487f-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="a487f-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a487f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a487f-108">DESCRIPTION</span></span>
<span data-ttu-id="a487f-109">Эти разделы устарели и будут исключены в будущем.</span><span class="sxs-lookup"><span data-stu-id="a487f-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="a487f-110">В этом разделе описан командлет в версии 0.8.1 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="a487f-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="a487f-111">Чтобы узнать версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="a487f-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="a487f-112">Командлет **New-WAPackVM** создает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a487f-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="a487f-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a487f-113">EXAMPLES</span></span>

### <span data-ttu-id="a487f-114">Пример 1: создание виртуальной машины для операционной системы Windows с помощью шаблона</span><span class="sxs-lookup"><span data-stu-id="a487f-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="a487f-115">Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.</span><span class="sxs-lookup"><span data-stu-id="a487f-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="a487f-116">Командлет запрашивает учетные записи и пароль.</span><span class="sxs-lookup"><span data-stu-id="a487f-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="a487f-117">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a487f-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="a487f-118">Вторая команда получает шаблон виртуальной машины с именем ContosoTemplate04 с помощью командлета **Get-WAPackVMTemplate** и сохраняет его в переменной $Template.</span><span class="sxs-lookup"><span data-stu-id="a487f-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="a487f-119">Последняя команда создает виртуальную машину с именем ContosoV023 в соответствии с шаблоном, хранящимся в переменной $Template.</span><span class="sxs-lookup"><span data-stu-id="a487f-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="a487f-120">В команде указан параметр *Windows* , поэтому виртуальная машина должна запустить версию операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="a487f-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="a487f-121">Пример 2: создание виртуальной машины для операционной системы Linux с помощью шаблона</span><span class="sxs-lookup"><span data-stu-id="a487f-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="a487f-122">Для первой команды создается объект **PSCredential** , который затем сохраняется в переменной $Credentials.</span><span class="sxs-lookup"><span data-stu-id="a487f-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="a487f-123">Вторая команда получает шаблон виртуальной машины с именем ContosoTemplate19 с помощью командлета **Get-WAPackVMTemplate** и сохраняет его в переменной $Template.</span><span class="sxs-lookup"><span data-stu-id="a487f-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="a487f-124">Последняя команда создает виртуальную машину с именем ContosoV028 в соответствии с шаблоном, хранящимся в переменной $Template.</span><span class="sxs-lookup"><span data-stu-id="a487f-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="a487f-125">В команде указан параметр *Linux* , поэтому виртуальная машина должна использовать версию операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="a487f-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="a487f-126">Пример 3: создание виртуальной машины на диске и в профиле размера операционной системы</span><span class="sxs-lookup"><span data-stu-id="a487f-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="a487f-127">Первая команда получает диск операционной системы с именем ContosoDiskOS с помощью командлета **Get-WAPackVMOSDisk** и сохраняет его в переменной $OSDisk.</span><span class="sxs-lookup"><span data-stu-id="a487f-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="a487f-128">Вторая команда получает профиль размера с именем MediumSizeVM с помощью командлета **Get-WAPackVMSizeProfile** , а затем сохраняет его в переменной $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="a487f-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="a487f-129">Последняя команда создает виртуальную машину с именем ContosoV073 с диска операционной системы, хранящейся в $OSDisk, и профиль размера, хранящийся в $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="a487f-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="a487f-130">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a487f-130">PARAMETERS</span></span>

### <span data-ttu-id="a487f-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="a487f-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="a487f-132">Задает ключ безопасной оболочки (SSH) для учетной записи администратора.</span><span class="sxs-lookup"><span data-stu-id="a487f-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="a487f-133">-Linux</span></span>
<span data-ttu-id="a487f-134">Указывает на то, что командлет создает виртуальную машину для запуска операционной системы Linux.</span><span class="sxs-lookup"><span data-stu-id="a487f-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a487f-135">-Name</span></span>
<span data-ttu-id="a487f-136">Указывает имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a487f-136">Specifies a name for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="a487f-137">-OSDisk</span></span>
<span data-ttu-id="a487f-138">Указывает диск операционной системы как объект **VirtualHardDisk** .</span><span class="sxs-lookup"><span data-stu-id="a487f-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="a487f-139">Чтобы получить диск операционной системы, используйте командлет **Get-WAPackVMOSDisk** .</span><span class="sxs-lookup"><span data-stu-id="a487f-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="a487f-140">-ProductKey</span></span>
<span data-ttu-id="a487f-141">Задает ключ продукта.</span><span class="sxs-lookup"><span data-stu-id="a487f-141">Specifies a product key.</span></span>
<span data-ttu-id="a487f-142">Ключ продукта — это 25-значный номер, обозначающий лицензию на продукт.</span><span class="sxs-lookup"><span data-stu-id="a487f-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="a487f-143">Используйте ключ продукта для операционной системы, которую вы планируете установить на виртуальной машине или узле.</span><span class="sxs-lookup"><span data-stu-id="a487f-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="a487f-144">-Profile</span></span>
<span data-ttu-id="a487f-145">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a487f-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a487f-146">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a487f-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a487f-147">-Template</span><span class="sxs-lookup"><span data-stu-id="a487f-147">-Template</span></span>
<span data-ttu-id="a487f-148">Задает шаблон.</span><span class="sxs-lookup"><span data-stu-id="a487f-148">Specifies a template.</span></span>
<span data-ttu-id="a487f-149">Командлет создает виртуальную машину на основе указанного шаблона.</span><span class="sxs-lookup"><span data-stu-id="a487f-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="a487f-150">Чтобы получить объект шаблона, используйте командлет Get-WAPackVMTemplate.</span><span class="sxs-lookup"><span data-stu-id="a487f-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="a487f-151">-VMCredential</span></span>
<span data-ttu-id="a487f-152">Задает учетные данные для учетной записи локального администратора.</span><span class="sxs-lookup"><span data-stu-id="a487f-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="a487f-153">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="a487f-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="a487f-154">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="a487f-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="a487f-155">-VMSizeProfile</span></span>
<span data-ttu-id="a487f-156">Задает в качестве объекта **HardwareProfile** профиль размера для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a487f-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="a487f-157">Чтобы получить профиль размера, используйте командлет **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="a487f-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="a487f-158">-VNet</span></span>
<span data-ttu-id="a487f-159">Указывает виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a487f-159">Specifies a virtual network.</span></span>
<span data-ttu-id="a487f-160">Командлет подключается к виртуальной машине в указанную вами виртуальную сеть.</span><span class="sxs-lookup"><span data-stu-id="a487f-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="a487f-161">Чтобы получить виртуальную сеть, используйте командлет **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="a487f-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="a487f-162">-Windows</span></span>
<span data-ttu-id="a487f-163">Указывает на то, что командлет создает виртуальную машину для запуска операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="a487f-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a487f-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a487f-164">CommonParameters</span></span>
<span data-ttu-id="a487f-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a487f-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a487f-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a487f-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a487f-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a487f-167">INPUTS</span></span>

## <span data-ttu-id="a487f-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a487f-168">OUTPUTS</span></span>

## <span data-ttu-id="a487f-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="a487f-169">NOTES</span></span>

## <span data-ttu-id="a487f-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a487f-170">RELATED LINKS</span></span>

[<span data-ttu-id="a487f-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="a487f-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="a487f-173">Restarting-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="a487f-174">Возобновить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="a487f-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="a487f-176">Start-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="a487f-177">Остановить-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="a487f-178">Приостановить — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="a487f-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="a487f-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="a487f-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="a487f-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="a487f-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="a487f-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="a487f-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


