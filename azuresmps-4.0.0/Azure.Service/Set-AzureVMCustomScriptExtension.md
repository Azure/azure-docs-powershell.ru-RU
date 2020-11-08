---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076037"
---
# <span data-ttu-id="9b85a-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9b85a-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="9b85a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9b85a-102">SYNOPSIS</span></span>
<span data-ttu-id="9b85a-103">Задает данные для расширения настраиваемого сценария виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85a-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="9b85a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9b85a-104">SYNTAX</span></span>

### <span data-ttu-id="9b85a-105">SetCustomScriptExtensionByContainerAndFileNames (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9b85a-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b85a-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9b85a-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b85a-107">UninstalleCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9b85a-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9b85a-108">SetCustomScriptExtensionByUriLinks</span><span class="sxs-lookup"><span data-stu-id="9b85a-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9b85a-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b85a-109">DESCRIPTION</span></span>
<span data-ttu-id="9b85a-110">Командлет **Set-AzureVMCustomScriptExtension** задает данные для расширения настраиваемого сценария виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="9b85a-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="9b85a-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9b85a-111">EXAMPLES</span></span>

### <span data-ttu-id="9b85a-112">Пример 1: Настройка сведений о расширении настраиваемого сценария для виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9b85a-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="9b85a-113">Эта команда задает данные для расширения настраиваемого сценария виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9b85a-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="9b85a-114">Пример 2: Настройка сведений для расширения настраиваемого сценария виртуальной машины с помощью пути к файлу</span><span class="sxs-lookup"><span data-stu-id="9b85a-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="9b85a-115">Эта команда задает данные для расширения настраиваемого сценария виртуальной машины с помощью нескольких URL-адресов файла.</span><span class="sxs-lookup"><span data-stu-id="9b85a-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="9b85a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9b85a-116">PARAMETERS</span></span>

### <span data-ttu-id="9b85a-117">-Аргумент</span><span class="sxs-lookup"><span data-stu-id="9b85a-117">-Argument</span></span>
<span data-ttu-id="9b85a-118">Указывает строку, которая предоставляет аргумент, который запускается на виртуальной машине с помощью этого командлета.</span><span class="sxs-lookup"><span data-stu-id="9b85a-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-119">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="9b85a-119">-ContainerName</span></span>
<span data-ttu-id="9b85a-120">Указывает имя контейнера в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="9b85a-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-121">-Отключение</span><span class="sxs-lookup"><span data-stu-id="9b85a-121">-Disable</span></span>
<span data-ttu-id="9b85a-122">Указывает на то, что этот командлет отключает состояние расширения.</span><span class="sxs-lookup"><span data-stu-id="9b85a-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-123">-FileName</span><span class="sxs-lookup"><span data-stu-id="9b85a-123">-FileName</span></span>
<span data-ttu-id="9b85a-124">Задает массив строк, который содержит имена больших двоичных файлов в указанном контейнере.</span><span class="sxs-lookup"><span data-stu-id="9b85a-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="9b85a-125">-FileUri</span></span>
<span data-ttu-id="9b85a-126">Задает массив строк, который содержит URL-адреса файлов большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="9b85a-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="9b85a-127">-ForceUpdate</span></span>
<span data-ttu-id="9b85a-128">Указывает на то, что этот командлет повторно применяет конфигурацию к расширению, когда конфигурация не была обновлена.</span><span class="sxs-lookup"><span data-stu-id="9b85a-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9b85a-129">-InformationAction</span></span>
<span data-ttu-id="9b85a-130">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="9b85a-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9b85a-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9b85a-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b85a-132">Продолжал</span><span class="sxs-lookup"><span data-stu-id="9b85a-132">Continue</span></span>
- <span data-ttu-id="9b85a-133">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="9b85a-133">Ignore</span></span>
- <span data-ttu-id="9b85a-134">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="9b85a-134">Inquire</span></span>
- <span data-ttu-id="9b85a-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9b85a-135">SilentlyContinue</span></span>
- <span data-ttu-id="9b85a-136">Остановить</span><span class="sxs-lookup"><span data-stu-id="9b85a-136">Stop</span></span>
- <span data-ttu-id="9b85a-137">Рвать</span><span class="sxs-lookup"><span data-stu-id="9b85a-137">Suspend</span></span>

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

### <span data-ttu-id="9b85a-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9b85a-138">-InformationVariable</span></span>
<span data-ttu-id="9b85a-139">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="9b85a-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9b85a-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="9b85a-140">-Profile</span></span>
<span data-ttu-id="9b85a-141">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9b85a-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9b85a-142">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b85a-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9b85a-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="9b85a-143">-ReferenceName</span></span>
<span data-ttu-id="9b85a-144">Указывает имя ссылки для расширения.</span><span class="sxs-lookup"><span data-stu-id="9b85a-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="9b85a-145">Этот параметр является пользовательской строкой, которую можно использовать для ссылки на расширение.</span><span class="sxs-lookup"><span data-stu-id="9b85a-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="9b85a-146">Оно указывается при первом добавлении расширения на виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="9b85a-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="9b85a-147">При последующих обновлениях необходимо указать ранее использованный эталонный код при обновлении расширения.</span><span class="sxs-lookup"><span data-stu-id="9b85a-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="9b85a-148">*ReferenceName* , назначенный расширению, возвращается с помощью командлета **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="9b85a-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-149">-Run</span><span class="sxs-lookup"><span data-stu-id="9b85a-149">-Run</span></span>
<span data-ttu-id="9b85a-150">Задает команду, которую этот командлет запускает с помощью расширения на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="9b85a-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="9b85a-151">Поддерживается только "powershell.exe".</span><span class="sxs-lookup"><span data-stu-id="9b85a-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9b85a-152">-StorageAccountKey</span></span>
<span data-ttu-id="9b85a-153">Указывает ключ учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="9b85a-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9b85a-154">-StorageAccountName</span></span>
<span data-ttu-id="9b85a-155">Указывает имя учетной записи хранения в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="9b85a-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="9b85a-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="9b85a-157">Указывает конечную точку службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="9b85a-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-158">-Удаление</span><span class="sxs-lookup"><span data-stu-id="9b85a-158">-Uninstall</span></span>
<span data-ttu-id="9b85a-159">Указывает, что этот командлет удаляет настраиваемое расширение сценария из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9b85a-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b85a-160">-Version</span><span class="sxs-lookup"><span data-stu-id="9b85a-160">-Version</span></span>
<span data-ttu-id="9b85a-161">Указывает версию настраиваемого расширения сценария.</span><span class="sxs-lookup"><span data-stu-id="9b85a-161">Specifies the version of the custom script extension.</span></span>

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

### <span data-ttu-id="9b85a-162">-VM</span><span class="sxs-lookup"><span data-stu-id="9b85a-162">-VM</span></span>
<span data-ttu-id="9b85a-163">Указывает Сохраняемый объект виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="9b85a-163">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="9b85a-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b85a-164">CommonParameters</span></span>
<span data-ttu-id="9b85a-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9b85a-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b85a-166">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b85a-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b85a-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9b85a-167">INPUTS</span></span>

## <span data-ttu-id="9b85a-168">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b85a-168">OUTPUTS</span></span>

## <span data-ttu-id="9b85a-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="9b85a-169">NOTES</span></span>

## <span data-ttu-id="9b85a-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b85a-170">RELATED LINKS</span></span>

[<span data-ttu-id="9b85a-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9b85a-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="9b85a-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9b85a-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="9b85a-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="9b85a-173">Get-AzureVM</span></span>](./Get-AzureVM.md)


