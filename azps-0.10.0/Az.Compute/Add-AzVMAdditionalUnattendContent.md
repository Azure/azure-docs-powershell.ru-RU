---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: e4359629da6f4df4c8da26e5ade2b2652c0762e4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909317"
---
# <span data-ttu-id="d95fa-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="d95fa-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="d95fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d95fa-102">SYNOPSIS</span></span>
<span data-ttu-id="d95fa-103">Добавляет сведения в файл ответов для автоматической настройки Windows.</span><span class="sxs-lookup"><span data-stu-id="d95fa-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="d95fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d95fa-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d95fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d95fa-105">DESCRIPTION</span></span>
<span data-ttu-id="d95fa-106">Командлет **Add-AzVMAdditionalUnattendContent** добавляет данные в файл ответов для автоматической установки Windows.</span><span class="sxs-lookup"><span data-stu-id="d95fa-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="d95fa-107">Укажите дополнительные данные в формате Base 64 Encoded. XML, которые этот командлет добавляет в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="d95fa-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="d95fa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d95fa-108">EXAMPLES</span></span>

### <span data-ttu-id="d95fa-109">Пример 1: Добавление содержимого в unattend.xml</span><span class="sxs-lookup"><span data-stu-id="d95fa-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="d95fa-110">Первая команда получает группу доступности с именем AvailablitySet03 в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d95fa-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="d95fa-111">Вторая команда создает объект виртуальной машины и сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d95fa-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d95fa-112">Команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d95fa-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="d95fa-113">Виртуальная машина принадлежит к группе доступности, хранящейся в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="d95fa-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="d95fa-114">Третья команда создает объект учетных данных с помощью командлета Get-Credential и сохраняет результат в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="d95fa-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="d95fa-115">В командной строке будет предложено ввести имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="d95fa-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="d95fa-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="d95fa-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="d95fa-117">Четвертая команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, хранящейся в $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="d95fa-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="d95fa-118">Пятая команда назначает содержимое переменной $AucContent.</span><span class="sxs-lookup"><span data-stu-id="d95fa-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="d95fa-119">Содержимое включает пароль.</span><span class="sxs-lookup"><span data-stu-id="d95fa-119">The content includes a password.</span></span>

<span data-ttu-id="d95fa-120">Последняя команда добавляет содержимое, хранящееся в $AucContent, в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="d95fa-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="d95fa-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d95fa-121">PARAMETERS</span></span>

### <span data-ttu-id="d95fa-122">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="d95fa-122">-Content</span></span>
<span data-ttu-id="d95fa-123">Задает базовое содержимое в формате XML в кодировке 64.</span><span class="sxs-lookup"><span data-stu-id="d95fa-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="d95fa-124">Этот командлет добавляет содержимое в файл unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="d95fa-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="d95fa-125">Содержимое XML должно быть меньше 4 КБ и должно включать корневой элемент для параметра или функции, вставляемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d95fa-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

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

### <span data-ttu-id="d95fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d95fa-126">-DefaultProfile</span></span>
<span data-ttu-id="d95fa-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d95fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d95fa-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="d95fa-128">-SettingName</span></span>
<span data-ttu-id="d95fa-129">Указывает имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="d95fa-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="d95fa-130">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d95fa-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d95fa-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="d95fa-131">FirstLogonCommands</span></span>
- <span data-ttu-id="d95fa-132">Автоматический вход</span><span class="sxs-lookup"><span data-stu-id="d95fa-132">AutoLogon</span></span>

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

### <span data-ttu-id="d95fa-133">-VM</span><span class="sxs-lookup"><span data-stu-id="d95fa-133">-VM</span></span>
<span data-ttu-id="d95fa-134">Указывает объект виртуальной машины, измененный этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="d95fa-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d95fa-135">Чтобы получить объект виртуальной машины, используйте командлет [Get-AzVM](./Get-AzVM.md) .</span><span class="sxs-lookup"><span data-stu-id="d95fa-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d95fa-136">Создайте объект виртуальной машины с помощью командлета [New-AzVMConfig](./New-AzVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="d95fa-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

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

### <span data-ttu-id="d95fa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d95fa-137">CommonParameters</span></span>
<span data-ttu-id="d95fa-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d95fa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d95fa-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d95fa-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d95fa-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d95fa-140">INPUTS</span></span>

### <span data-ttu-id="d95fa-141">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d95fa-141">PSVirtualMachine</span></span>
<span data-ttu-id="d95fa-142">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d95fa-142">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="d95fa-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d95fa-143">OUTPUTS</span></span>

### <span data-ttu-id="d95fa-144">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d95fa-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d95fa-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d95fa-145">NOTES</span></span>

## <span data-ttu-id="d95fa-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d95fa-146">RELATED LINKS</span></span>

[<span data-ttu-id="d95fa-147">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d95fa-147">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="d95fa-148">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="d95fa-148">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="d95fa-149">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d95fa-149">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
