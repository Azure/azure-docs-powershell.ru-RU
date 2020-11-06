---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563724"
---
# <span data-ttu-id="04220-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="04220-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="04220-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04220-102">SYNOPSIS</span></span>
<span data-ttu-id="04220-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="04220-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04220-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04220-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="04220-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04220-105">DESCRIPTION</span></span>
<span data-ttu-id="04220-106">Командлет **Add-AzureRmVMAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="04220-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="04220-107">Укажите дополнительные данные в формате Base 64 Encoded. XML, которые этот командлет добавляет в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="04220-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="04220-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04220-108">EXAMPLES</span></span>

### <span data-ttu-id="04220-109">Пример 1: Добавление содержимого в unattend.xml</span><span class="sxs-lookup"><span data-stu-id="04220-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="04220-110">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="04220-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="04220-111">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="04220-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="04220-112">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="04220-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="04220-113">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="04220-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="04220-114">Третья команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="04220-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="04220-115">В командной строке будет предложено ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="04220-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="04220-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="04220-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="04220-117">Четвертая команда использует командлет **Set-AzureRmVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="04220-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="04220-118">Пятая команда назначает содержимое переменной $AucContent.</span><span class="sxs-lookup"><span data-stu-id="04220-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="04220-119">Содержимое включает пароль.</span><span class="sxs-lookup"><span data-stu-id="04220-119">The content includes a password.</span></span>

<span data-ttu-id="04220-120">Последняя команда добавляет содержимое, хранящееся в $AucContent, в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="04220-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="04220-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04220-121">PARAMETERS</span></span>

### <span data-ttu-id="04220-122">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="04220-122">-Content</span></span>
<span data-ttu-id="04220-123">Задает базовое содержимое в формате XML в кодировке 64.</span><span class="sxs-lookup"><span data-stu-id="04220-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="04220-124">Этот командлет добавляет содержимое в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="04220-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="04220-125">Содержимое XML должно быть меньше 4 КБ и должно включать корневой элемент для параметра или функции, вставляемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="04220-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04220-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="04220-126">-SettingName</span></span>
<span data-ttu-id="04220-127">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="04220-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="04220-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="04220-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04220-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="04220-129">FirstLogonCommands</span></span>
- <span data-ttu-id="04220-130">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="04220-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04220-131">-VM</span><span class="sxs-lookup"><span data-stu-id="04220-131">-VM</span></span>
<span data-ttu-id="04220-132">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="04220-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="04220-133">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="04220-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="04220-134">Создайте объект виртуальной машины с помощью командлета [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="04220-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="04220-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04220-135">CommonParameters</span></span>
<span data-ttu-id="04220-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04220-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04220-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04220-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04220-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04220-138">INPUTS</span></span>

### <span data-ttu-id="04220-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="04220-139">None</span></span>
<span data-ttu-id="04220-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="04220-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04220-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04220-141">OUTPUTS</span></span>

## <span data-ttu-id="04220-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="04220-142">NOTES</span></span>

## <span data-ttu-id="04220-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04220-143">RELATED LINKS</span></span>

[<span data-ttu-id="04220-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="04220-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="04220-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="04220-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="04220-146">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="04220-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
