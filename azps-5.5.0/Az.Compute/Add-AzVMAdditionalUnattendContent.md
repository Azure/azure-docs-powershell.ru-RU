---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 05f100e730cb808bf40bbec60386901eb39020ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238993"
---
# <span data-ttu-id="b77ef-101">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="b77ef-101">Add-AzVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="b77ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b77ef-102">SYNOPSIS</span></span>
<span data-ttu-id="b77ef-103">Добавляет сведения в неотвеченный файл ответа на установку Windows.</span><span class="sxs-lookup"><span data-stu-id="b77ef-103">Adds information to the unattended Windows Setup answer file.</span></span>

## <span data-ttu-id="b77ef-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b77ef-104">SYNTAX</span></span>

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77ef-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b77ef-105">DESCRIPTION</span></span>
<span data-ttu-id="b77ef-106">Для получения сведений в файле ответа на сведения о настройке Windows добавляется **cmdlet Add-AzVMAdditionalUnattendContent.**</span><span class="sxs-lookup"><span data-stu-id="b77ef-106">The **Add-AzVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="b77ef-107">Укажите дополнительные сведения в формате XML с unattend.xml 64.</span><span class="sxs-lookup"><span data-stu-id="b77ef-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="b77ef-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b77ef-108">EXAMPLES</span></span>

### <span data-ttu-id="b77ef-109">Пример 1. Добавление содержимого в unattend.xml</span><span class="sxs-lookup"><span data-stu-id="b77ef-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="b77ef-110">Первая команда получает набор доступности с именем AvailabilitySet03 в группе ресурсов ResourceGroup11, а затем сохраняет этот объект в переменной $AvailabilitySet ресурса.</span><span class="sxs-lookup"><span data-stu-id="b77ef-110">The first command gets the availability set named AvailabilitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>
<span data-ttu-id="b77ef-111">Вторая команда создает объект виртуальной машины, а затем сохраняет его в $VirtualMachine переменной.</span><span class="sxs-lookup"><span data-stu-id="b77ef-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="b77ef-112">Эта команда назначает имя и размер виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="b77ef-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="b77ef-113">Виртуальная машину входит в набор доступности, который хранится в $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="b77ef-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>
<span data-ttu-id="b77ef-114">Третья команда создает объект учетных данных с Get-Credential командлетом, а затем сохраняет результат в переменной $Credential данных.</span><span class="sxs-lookup"><span data-stu-id="b77ef-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="b77ef-115">В результате будет предложено вводить имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="b77ef-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="b77ef-116">Для получения дополнительных сведений введите `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="b77ef-116">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="b77ef-117">Четвертая команда использует командлет **Set-AzVMOperatingSystem** для настройки виртуальной машины, $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="b77ef-117">The fourth command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="b77ef-118">Пятая команда назначает содержимое переменной $AucContent.</span><span class="sxs-lookup"><span data-stu-id="b77ef-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="b77ef-119">Содержимое содержит пароль.</span><span class="sxs-lookup"><span data-stu-id="b77ef-119">The content includes a password.</span></span>
<span data-ttu-id="b77ef-120">Конечная команда добавит содержимое из $AucContent в unattend.xml файл.</span><span class="sxs-lookup"><span data-stu-id="b77ef-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="b77ef-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b77ef-121">PARAMETERS</span></span>

### <span data-ttu-id="b77ef-122">-Содержимое</span><span class="sxs-lookup"><span data-stu-id="b77ef-122">-Content</span></span>
<span data-ttu-id="b77ef-123">Определяет содержимое в кодированном XML-формате с базой 64.</span><span class="sxs-lookup"><span data-stu-id="b77ef-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="b77ef-124">Этот cmdlet добавит содержимое в unattend.xml файл.</span><span class="sxs-lookup"><span data-stu-id="b77ef-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="b77ef-125">Содержимое XML должно быть меньше 4 КБ и должно включать корневой элемент для параметра или функции, вставляемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77ef-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77ef-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77ef-126">-DefaultProfile</span></span>
<span data-ttu-id="b77ef-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b77ef-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77ef-128">-SettingName</span><span class="sxs-lookup"><span data-stu-id="b77ef-128">-SettingName</span></span>
<span data-ttu-id="b77ef-129">Определяет имя параметра, к которому применяется содержимое.</span><span class="sxs-lookup"><span data-stu-id="b77ef-129">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="b77ef-130">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b77ef-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b77ef-131">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="b77ef-131">FirstLogonCommands</span></span>
- <span data-ttu-id="b77ef-132">AutoLogon</span><span class="sxs-lookup"><span data-stu-id="b77ef-132">AutoLogon</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b77ef-133">-VM</span><span class="sxs-lookup"><span data-stu-id="b77ef-133">-VM</span></span>
<span data-ttu-id="b77ef-134">Определяет объект виртуальной машины, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77ef-134">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="b77ef-135">Чтобы получить объект виртуальной машины, используйте [cmdlet Get-AzVM.](./Get-AzVM.md)</span><span class="sxs-lookup"><span data-stu-id="b77ef-135">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="b77ef-136">Создайте объект виртуальной машины с помощью [cmdlet New-AzVMConfig.](./New-AzVMConfig.md)</span><span class="sxs-lookup"><span data-stu-id="b77ef-136">Create a virtual machine object by using the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b77ef-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77ef-137">CommonParameters</span></span>
<span data-ttu-id="b77ef-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77ef-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77ef-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b77ef-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77ef-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b77ef-140">INPUTS</span></span>

### <span data-ttu-id="b77ef-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="b77ef-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="b77ef-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b77ef-142">System.String</span></span>

### <span data-ttu-id="b77ef-143">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="b77ef-143">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="b77ef-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b77ef-144">OUTPUTS</span></span>

### <span data-ttu-id="b77ef-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="b77ef-145">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="b77ef-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b77ef-146">NOTES</span></span>

## <span data-ttu-id="b77ef-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b77ef-147">RELATED LINKS</span></span>

[<span data-ttu-id="b77ef-148">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="b77ef-148">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="b77ef-149">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="b77ef-149">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)

[<span data-ttu-id="b77ef-150">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="b77ef-150">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
